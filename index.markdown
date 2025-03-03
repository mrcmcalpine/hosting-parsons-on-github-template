---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: IGCSE Parson Puzzles
---
# Parsons Practice

# Calculation of Average
Calculate, store and output the average grade from a 1D array (Scores) of length NumStudents
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


# Input Validation in an 1D Array
Input and validate the scores for a 1D array, Scores, of size NumStudents
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

# Reset Values -
Reset any values in the array which are below the threshold
<div id="ResetThreshold-sortableTrash" class="sortable-code"></div> 
<div id="ResetThreshold-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="ResetThreshold-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="ResetThreshold-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "CONSTANT Threshold &lt;- 50\n" +
    "for i in range(0, NumStudents):#loop to reset\n" +
    "    if Scores[i] &lt; Threshold:\n" +
    "        Scores[i] = -1";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "ResetThreshold-sortable",
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
  $("#ResetThreshold-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#ResetThreshold-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

#Count the number of students above average
<div id="CountAboveAverage-sortableTrash" class="sortable-code"></div> 
<div id="CountAboveAverage-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="CountAboveAverage-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="CountAboveAverage-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "DECLARE countAboveAvg: INTEGER\n" +
    "countAboveAvg &lt;- 0\n" +
    "for i in range(0, NumStudents):#loop to count above average\n" +
    "    if Scores[i] &gt; classAverage:\n" +
    "        countAboveAvg = countAboveAvg + 1\n" +
    "print (&#039;Students above average:&#039;, countAboveAvg)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "CountAboveAverage-sortable",
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
  $("#CountAboveAverage-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#CountAboveAverage-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

# Use a pre-condition loop to output a message based on the grade
<div id="Pre-conditionLoop-sortableTrash" class="sortable-code"></div> 
<div id="Pre-conditionLoop-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Pre-conditionLoop-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Pre-conditionLoop-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "index = 0\n" +
    "while index &lt; NumStudents:\n" +
    "    if Scores[i] &gt; 80:\n" +
    "        print (&quot;Excellent score&quot;)\n" +
    "    else:\n" +
    "        if Scores[i] &lt; threshold:\n" +
    "            print (&quot;Resit Required&quot;)\n" +
    "        else:\n" +
    "            print (&quot;Try harder&quot;)\n" +
    "    index = index + 1";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Pre-conditionLoop-sortable",
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
  $("#Pre-conditionLoop-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Pre-conditionLoop-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

# Post condtion loop to output names and scores
<div id="Post-conditionLoop-sortableTrash" class="sortable-code"></div> 
<div id="Post-conditionLoop-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Post-conditionLoop-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Post-conditionLoop-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "Index &lt;-- 1\n" +
    "DO\n" +
    "   OUTPUT StudentNames[Index]\n" +
    "   OUTPUT Scores[Index]\n" +
    "   Index &lt;-- Index + 1\n" +
    "LOOP UNTIL Index = NumStudents + 1";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Post-conditionLoop-sortable",
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
  $("#Post-conditionLoop-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Post-conditionLoop-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
