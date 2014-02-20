*This repository is a mirror of the [component](http://component.io) module [component/url](http://github.com/component/url). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-url`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# url

  url parser.

## Installation

    $ component install component/url

## Example

```js
var url = require('url');
url.parse('http://example.com:3000/store/shoes?sort=desc');
```

yields:

```js
{
  hash: ""
  host: "example.com:3000"
  port: 3000,
  hostname: "example.com"
  href: "http://example.com:3000/store/shoes?sort=desc"
  pathname: "/store/shoes"
  protocol: "http:"
  query: "sort=desc"
  search: "?sort=desc"
}
```

## API

### url.parse(string)

  Parse the given url `string`.

### url.isAbsolute(string)

  Check if the given url `string` is absolute (has a scheme specified).

### url.isRelative(string)

  Check if the given url `string` is relative.

### url.isCrossDomain(string)

  Check if the given url `string` is cross-domain.

## Note

  This url "parser" uses an `<a>` tag, this means that when
  a relative url is given, such as "/foo", it becomes relative
  to the current domain / path, because the browser resolves it
  as it normally would.

## License

  MIT
