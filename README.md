# jquery.fileuplad
Plugin for upload files via AJAX compatible with ASPX and PHP and other...(Testing)

#Usage:
```javascript
$("#form").fileupload("niceurl/myupload.[php/ashx]",{
    //testing.... if any file fail then the upload is cancelled.
    cancelable: true,
    //Comming Soon
    //trigger : {
    //      target: "#btnUpload",
    //      event: "click"
    //}
    //Called every time that a file is upload to server and no return error
    success : function(filename,responseText,percent){
        alert("The" + filename + " was upload correctly");
        updateMyCustomProgressBar("#uploadPG",percent);
    },
    //Called every time that a file not upload 
    error : function(filename,responseText,percent){
        alert("The" + filename + " was not upload correctly");
        updateMyCustomProgressBar("#errorPG",percent);
    },
    //all files are sent to the server.
    complete : function(responseText){
        alert("All Done");
        alert(responseText);
    }
    
})
```
