# html-copy
html页面复制


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
