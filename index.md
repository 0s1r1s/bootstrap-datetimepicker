---
title: Bootstrap Date/Time Picker
layout: default
author: Thiago de Arruda
authorUrl: https://github.com/tarruda
projectName: bootstrap-datetimepicker
projectDescription: Date/Time Picker for Twitter Boostrap 
zipDownloadUrl: assets/dist/bootstrap-datetimepicker-0.0.2.zip
githubUrl: https://github.com/tarruda/bootstrap-datetimepicker
css:
  - assets/css/bootstrap-datetimepicker.min.css
js:
  - assets/js/bootstrap-datetimepicker.min.js
  - assets/js/index.js
---
### Introduction
Simple date/time picker component based on the work of [Stefan Petre](http://www.eyecon.ro/bootstrap-datepicker/),
with contributions taken from [Andrew Rowls](https://github.com/eternicode) and
[jdewit](https://github.com/jdewit).

### Demo
{% include demo.html %}

### Usage
Copy and paste the following code in a file(eg: test.html) and it should
produce a widget similar to the one above:

{% highlight html %}
<!DOCTYPE HTML>
<html>
  <head>
    <link href="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.2.2/css/bootstrap-combined.min.css" rel="stylesheet">
    <link rel="stylesheet" type="text/css" media="screen"
     href="http://tarruda.github.com/bootstrap-datetimepicker/assets/css/bootstrap-datetimepicker.min.css">
  </head>
  <body>
    <div id="datetimepicker" class="input-append date">
      <input type="text"></input>
      <span class="add-on">
        <i data-time-icon="icon-time" data-date-icon="icon-calendar"></i>
      </span>
    </div>
    <script type="text/javascript"
     src="http://cdnjs.cloudflare.com/ajax/libs/jquery/1.8.3/jquery.min.js">
    </script> 
    <script type="text/javascript"
     src="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.2.2/js/bootstrap.min.js">
    </script>
    <script type="text/javascript"
     src="http://tarruda.github.com/bootstrap-datetimepicker/assets/js/bootstrap-datetimepicker.min.js">
    </script>
    <script type="text/javascript">
      $('#datetimepicker').datetimepicker({
        format: 'MM/dd/yyyy hh:mm',
        language: 'en',
        pickDate: true,
        pickTime: true,
        hourStep: 1,
        minuteStep: 15,
        secondStep: 30,
        inputMask: true
      });
    </script>
  </body>
<html>
{% endhighlight %}

The element also has the bootstrap-datepicker 'changeDate' event and 'setValue' method.

### Compilation
To compile/minify you need to have make, node.js and npm on your $PATH

{% highlight sh %}
$ git clone git://github.com/tarruda/bootstrap-datetimepicker.git
$ cd bootstrap-datetimepicker
$ make deps
$ make build
{% endhighlight %}
