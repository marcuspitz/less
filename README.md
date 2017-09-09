# Less
Less solutions and prototypes

## Getting started
### Install using NPM
npm install -g less
### Compile your file
<b>lessc styles.less styles.css</b>
### The less file has two variables (@base and @boxlength) and one function (.box)
```css
@base: #f9aaab;
@boxlength: 200px;

.box {
	border: solid;
	.box(@base)
}

.box(@color, @alphalength: @boxlength)  {
	background-color: @color;	
	width: @alphalength;
	height: @alphalength;
}

.shadow {	
	.box( lighten(@base, 10%), @boxlength * 2 )
}
```