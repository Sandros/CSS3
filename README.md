CSS3
====

CSS3 Navigation - No JavaScript needed

The label element may be used to attach information to controls. 
The for attribute associates a label with another control explicitly 
that can be used for a modern web navigation as a toggle effect.

Each LABEL element is associated with exactly one form control.
The for attribute associates a label with another control explicitly: the value 
of the for attribute must be the same as the value of the id attribute of the 
associated control element. More than one LABEL may be associated with the same 
control by creating multiple references via the for attribute.

A good solution for browsers with deactivated JavaScript support 


<style>

 *{
		padding: 0;
		margin: 0;
		border: 0;
	}
	body {
		background: #eee;	
		overflow-x: hidden;		
	}

	#menu {
		position: absolute;
		height: 100%;
		width: 250px;
		left: -250px;
		background: #666;
		color: #ccc;	
		-webkit-transition: left 0.2s ease;
		-moz-transition: left 0.2s ease;
		transition: left 0.2s ease;		
	}


/* Important for css3 toggle functionalities */
	
	input[type=checkbox] {
		position: absolute;				
		top: -9999px;
		left: -9999px;	
	}
	
	#toggle-1:checked  ~ #content {
		position: relative;
		width: 100%;
		left: 250px;
		-webkit-transition: left 0.2s ease;
		-moz-transition: left 0.2s ease;
		transition: left 0.2s ease;	
	}
	#toggle-1:checked  ~ #menu {
		left: 0;
		-webkit-transition: left 0.2s ease;
		-moz-transition: left 0.2s ease;
		transition: left 0.2s ease;	
	}
	
	</style>
	
	
<body>
	
	<!-- Important to set input first -->
	<input id="toggle-1" type="checkbox">
	
	<!-- #menu -->
	<div id="menu">
			<h3>Menu 1</h3>
			<ul>
			<li><a href="#">Home</a></li>
			<li><a href="#">Products</a></li>
			<li><a href="#">About</a></li>
			</ul>		
		</div>
	
	<!-- #content -->
	<div id="content">
	
	  <label for="toggle-1">&#9776; Menu 1</label>	
	
	</div>
	
	</body>

