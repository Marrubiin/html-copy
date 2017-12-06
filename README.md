# html-copy
html页面复制

<div id="value">需要复制的内容</div>

<div id="copy_btn">复制按钮</div>

$('#copy_btn').click(function () {
    var uri = document.getElementById('value').innerText;
    copy(uri);
})

function copy(event) {
    var oInput = document.createElement('input');
    oInput.value = event;
    document.body.appendChild(oInput);
    oInput.select();
    document.execCommand('Copy');
    oInput.style.display = 'none';
    alert('复制成功');
}
