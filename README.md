select2OptionPicker
===================

Jquery plugin convert standard html select into list ui to picker

## About

select2OptionPicker is a jQuery plugin that provides an alternative to the standard html select. The plugin converts selects into a series of li like elements, 
and if used correctly can provide a better visual representation of the options available to a user.

### Features

* Converts normal HTML selects into button like elements (a tags)
* Supports JS change callbacks
* Supports image and color options
* Supports disabled options
* Supports disabled selects
* Supports OptGroups
* Allows no default selection

## Howto

Add a standard select to the page and then make 1 jQuery call to convert it into buttons:

    <select name="simple-select">
      <option>One</option>
      <option>Two</option>
      <option>Three</option>
    </select>

    <script>
       $('select[name=simple-select]').select2OptionPicker();
    </script>

When the user clicks on one of the buttons (their really links), the plugin sets that value in your select so server side your code should be exactly the same.

### Image & color

	<select name="adv-select" class="standard-demo">
          <option data-img-src="http://i.imgur.com/fBJ88eD.png">One</option>
          <option data-color="#C978D7">Two</option>
          <option>Three</option>
        </select>

    <script>
       $('select[name=adv-select]').select2OptionPicker();
    </script>

### Javascript Callbacks
Any change events registered against the original select will also fire when the select buttons are clicked. e.g.

      $('select[name=simple-select]').change(function() {
        alert('Changed to ' + $(this).val());
      });

### No Default Selection
By default the option selected in your select will be marked as selected
in the buttons.  However, the plugin also supports the threadless style,
no default selection.

       $('select[name=simple-select]').select2OptionPicker({noDefault: true});

### OptGroups
The plugin understands and honors option groups.  Each option group will
be placed in a seperate UL and the optgroups label will be added to the
page as a strong tag.

### Disabling
The plugin supports disabled options and disabled selects.

### Styling
The select2OptionPicker.css is provided as a guide, it's mostly copied from
threadless.com.  I suggest restyling if your going to use the plugin on a
commercial site.

## Licencing

MIT

## Contact

TienNH - nguyentien8x(at)gmail.com
