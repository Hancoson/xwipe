html���ֽṹ
xwipe�ṹ
<div id='xwipe' class='xwipe'>
    <div class='xwipe-wrap'>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        ..
    </div>
</div>

tab�ṹ
<ul id="tab" class="tab clearfix">
    <li>0</li>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    ...
</ul>

css��ʽ
.xwipe {
    overflow: hidden;
    visibility: hidden;
}
.xwipe-wrap {
    overflow: hidden;
}
.xwipe-wrap > div {
    float:left;
    position: relative;
}

js����
1.����xwipe.js
2.ʵ��������
function xwipeCallback(index){

}
var myXwipe = document.getElementById("xwipe"),
    tab = document.getElementById("tab"),
    options = {
        callback : xwipeCallback,
        auto : 3000,
        curIndex : 0,
        speed : 300
    }

var xwipe = new Xwipe(myXwipe,options,tab);


����optionsΪXwipe���ò���,��ѡ��
    callbackΪ��������֮��ص�������
    ����auto����,xwipe����Ϊ�Զ���������λΪms
    curIndexΪ��ʼ��ʼ���û���slide����ֵ��Ĭ��Ϊ0
    speedΪ��������ʱ����̳���duration

tabΪtab�л���������ѡ
    �ṹΪ
        <ul>
            <li>tab1</li>
            <li>tab2</li>
            <li>tab3</li>
            ...
        </ul>

Xwipe API:
    prev() ��������һ��slide
    next() ��������һ��slide
    goTo(index) ������ָ��index����
    option.curIndex ��ȡ��ǰ����

