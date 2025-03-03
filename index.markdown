---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

#Calculation of Average
<div id="Year9-sortableTrash" class="sortable-code"></div> 
<div id="Year9-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Year9-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Year9-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for i in range(0, NumStudents):\n" +
    "    totalClass = totalClass + Scores[i]\n" +
    "classAverage = totalClass / NumStudents\n" +
    "print (&#039;Class average:&#039;, classAverage)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Year9-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Year9-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Year9-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


# Input Validation in an Array
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for i in range(0,NumStudents):\n" +
    "    print (&quot;Enter your score&quot;)\n" +
    "    Scores[i] =int(input())#INPUT 1\n" +
    "    while Scores[i]&lt;0 or Scores[i]&gt;100:\n" +
    "        print (&quot;Error - range 1 to 100 only&quot;)\n" +
    "        Scores[i] = int(input())#INPUT 2";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


# 2D Array 15 markers
#Calculate, store and output the student total from 3 assessments.
<div id="f1sortableTrash" class="sortable-code"></div> 
<div id="f1sortable" class="sortable-code"></div> 
<div style="clear:both;" width =400></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "DECLARE AverageGrades[1:NumStudents]: OF TYPE REAL\n" +
    "for i in range(0, NumStudents):\n" +
    "    tot = 0\n" +
    "    for j in range(0, NumAssessments):\n" +
    "        tot = tot + Grades[i][j]\n" +
    "    avgG = round(tot / NumAssessments, 2)\n" +
    "    AverageGrades[i] = avgG\n" +
    "    print (Names[i], &quot;average grade&quot;, avgG)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
