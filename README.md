This is a small mixin to only include a scss object once.

I recently discovered an issue with bower components and shared dependencies.
If you have multiple bower components that depend on a shared component
when the scss is compiled these styles will be outputted twice duplicating
the amount of code.

This mixin solves this by outputting the code only once. You can import sass-require in each
bower_component, it won't care.

## Usage

Define an scss object

```
@import 'bower_components/sass-require';

@include define('test-object') {
	
	.object-code {
		display: block;
	}

}
```

See the example folder but example output code.