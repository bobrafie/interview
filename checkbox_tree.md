Checkbox Tree
===========

### Task 

Write a custom checkbox-tree component by hand, using this data: https://rawgit.com/bobrafie/interview/master/checkbox_tree.json

__The purpose of this test is to determine your ability to create custom components on top of existing, base-functionality JavaScript libraries (e.g. jQuery). You CANNOT use exisiting UI component libraries, plugins or extensions that render a tree with checkbox capabilities.__

### UI Mockup

    + [x] Arizona
      * [x] Phoenix
      * [x] Tucson
    + [-] California
      * [ ] Fresno
      * [x] Los Angeles
      * [ ] Sacramento
      * [ ] San Diego
      * [ ] San Francisco
      * [ ] San Jose
    - [ ] Oregon
    - [ ] Nevada
    - [ ] New Mexico

### Component requirements

1.  If any node or any of its children is initially selected, open it by default at render time. 
2.  Only nodes with children can be opened or closed using a plus/minus or right triangle/down triangle (triangle with CSS preferred).
3.  Each node has a checkbox which does not impact closed/open state (checkboxes indicate selection state e.g. for a filter).

### Code requirements

1.  You can use base JavaScript libraries such as jQuery, underscore.js, React, Backbone.js, etc.
2.  HTML markup should be written through JavaScript either as templates or by creating DOM nodes.
3.  CSS should be contained in its own file which could be included in any application page.
4.  Component constructor takes in JSON data as demonstrated below.
5.  Provide a public API that retrieves the selection state of the component in JSON format (semi-checked is false). API result format is up to you.

### Data Load and Transformation

1. Perform an ajax call like below.
2. You will need to parse it and transform it to look like the structure above as _input for the component_.

#### Starter Code
    
    $.ajax({
        url: "https://rawgit.com/bobrafie/interview/master/checkbox_tree.json"
    }).done(function (result) {
        $(document.body).append(JSON.stringify(result));
    });

### Usage

    var checkboxTree = new CheckboxTree({
        el: "#cities",
        data: jsonData
    });
    checkboxTree.render();

### Evaluation

Your implementation will be evaluated on the style and architecture of your code as well as the extent to which it meets the specifications above.



