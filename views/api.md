#Documentation::API
This page refers to the Fracture.it API. Below I will describe how to interact with the application through the POST method.
 
[Back](/)

##Console

    curl -d 'url=yourdomain' http://fracture.it

**JSON Return**

`{"fractured_url":"http://fracture.it/3","errors":""}`

If your URL is more than 200 characters, or is an invalid URL:

`{"fractured_url":"","errors":["Not a valid URL format"]}`

##AJAX

    $.ajax({
      type: "POST",
      url: "http://fracture.it",
      data: { url: "yourdomain" },
      dataType: 'JSON'
    }).done(function(data) {
      $('#message').html("Fractured URL: " + data.fractured_url);
    });

##Sandbox

    curl -d 'url=yourdomain' http://fracture.it/sandbox

**JSON Return**

`{"fractured_url":"http://fracture.it/$url","errors":""}`

[Back](/)