# Briev Less example
Briev less solution for css re-use problems.

## Getting started
### Install using NPM
npm install -g less
### Compile your file
<b>lessc styles.less styles.css</b>
#### The less file has two variables (@base and @boxlength) and one function (.box)
#### Pay attention on re-use .box function to .shadow properties!!!
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
## Please contact-me to questions or contributions: marcusviniciuspitz@ioapps.com.br