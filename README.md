# Dora

[![Build Status](https://travis-ci.org/gajus/dora.png?branch=master)](https://travis-ci.org/gajus/dora)
[![Coverage Status](https://coveralls.io/repos/gajus/dora/badge.png)](https://coveralls.io/r/gajus/dora)

Input generation/handling library.

Dora has evolved from a [single function](https://gist.github.com/gajus/8392582). Generating input does not require much more than a single function. However, procedural implementation encouraged bad practises, e.g. relying on the state of `$GLOBALS`. Dora embodies the simplicity of the original implementation with a light touch of OO to properly handle environment variables.

## Using Dora

```php
<?php
$form = new \gajus\thorax\Form(['foo' => 1]);

echo $form->input('foo', ['data-custom-attribute' => 'test'], ['options' => ['Knock, knock...', 'Come in.']]);
```

The above will produce:

```html
<select data-custom-attribute="test" name="foo" type="select">
	<option value="0">Knock, knock...</option>
	<option value="1" selected="selected">Come in.</option>
</select>
```

## Documentation & Examples

[Interactive documentation](https://dev.anuary.com/2f46cbc3-5bba-590c-bb08-66aca81710a1/demo/) covers all of the Dora functionality.