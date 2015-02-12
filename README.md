thesechars
=============

A faster way to restrict characters in inputs

[View the demo](https://guimadaleno.github.io/demos/thesechars/demo.html)

### Allow numbers only

```js
$(".numbers-only").on('keydown', function(e)
{
	if 
	(
		e.keyCode == 46 || e.keyCode == 8 || e.keyCode == 9 || e.keyCode == 27 || e.keyCode == 13 || 
		(e.keyCode == 65 && e.ctrlKey === true) || 
		(e.keyCode == 67 && e.ctrlKey === true) || 
		(e.keyCode == 88 && e.ctrlKey === true) || 
		(e.keyCode == 86 && e.ctrlKey === true) || 
		(e.keyCode == 65 && e.metaKey === true) || 
		(e.keyCode == 67 && e.metaKey === true) || 
		(e.keyCode == 88 && e.metaKey === true) || 
		(e.keyCode == 86 && e.metaKey === true) || 
		(e.keyCode >= 35 && e.keyCode <= 39)
	) 
	{
		return;
	}
	else
 	{
		if (e.shiftKey || (e.keyCode < 48 || e.keyCode > 57) && (e.keyCode < 96 || e.keyCode > 105 )) 
		{
			e.preventDefault(); 
		}   	
	}
});
```

```html
<input type="text" class="numbers-only">
```

### Allow float numbers only

```js
$(".float-numbers-only").on('keydown', function(e)
{
	if 
	(
		e.keyCode == 46 || e.keyCode == 8 || e.keyCode == 9 || e.keyCode == 27 || e.keyCode == 13 || 
		(e.keyCode == 65 && e.ctrlKey === true) || 
		(e.keyCode == 67 && e.ctrlKey === true) || 
		(e.keyCode == 88 && e.ctrlKey === true) || 
		(e.keyCode == 86 && e.ctrlKey === true) || 
		(e.keyCode == 65 && e.metaKey === true) || 
		(e.keyCode == 67 && e.metaKey === true) || 
		(e.keyCode == 88 && e.metaKey === true) || 
		(e.keyCode == 86 && e.metaKey === true) || 
		(e.keyCode >= 35 && e.keyCode <= 39)
	) 
	{
		return;
	}
	else
 	{
		if (e.shiftKey || (e.keyCode < 48 || e.keyCode > 57) && (e.keyCode < 96 || e.keyCode > 105 ) && (e.keyCode != 190)) 
		{
			e.preventDefault(); 
		}   	
	}
});
```

```html
<input type="text" class="float-numbers-only">
```

### Allow letters only

```js
$('.letters-only').on('keydown', function (e) 
{ 
    if (e.keyCode >= 48 && e.keyCode <= 57)
    {
    	e.preventDefault();
    }
    else if 
    (
    	(
    		e.keyCode == 46 || e.keyCode == 8 || e.keyCode == 9 || e.keyCode == 27 || e.keyCode == 13 || 
	    	(e.keyCode == 65 && e.ctrlKey === true) || 
	    	(e.keyCode == 67 && e.ctrlKey === true) || 
	    	(e.keyCode == 88 && e.ctrlKey === true) || 
	    	(e.keyCode == 86 && e.ctrlKey === true) || 
	    	(e.keyCode == 65 && e.metaKey === true) || 
	    	(e.keyCode == 67 && e.metaKey === true) || 
	    	(e.keyCode == 88 && e.metaKey === true) || 
	    	(e.keyCode == 86 && e.metaKey === true) || 
	    	(e.keyCode >= 35 && e.keyCode <= 39)
	    ) || (e.keyCode >= 65 && e.keyCode <= 90)
    )
    {
    	return;
    }
    else
    {
    	e.preventDefault();
    }
});
```

```html
<input type="text" class="latters-only">
```
