html���ֽṹ
<div id='xwipe' class='xwipe'>
    <div class='xwipe-wrap'>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        ..
    </div>
</div>

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

var xwipe = new Xwipe(options,myXwipe,tab);

����optionsΪ�����ò�����
    callbackΪ��������֮��ص�������
    ����auto����,xwipe����Ϊ�Զ���������λΪms
    curIndexΪ��ʼ��ʼ���û���slide����ֵ��Ĭ��Ϊ0
    speedΪ��������ʱ����̳���duration
