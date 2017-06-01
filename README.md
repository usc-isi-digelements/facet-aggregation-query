# facet-aggregation-query

A Polymer Element that performs an ajax query or elasticsearch aggregation query and returns results in a format ready to use as a set of facets (for an example, see `<facet-list>`).

### Example that runs an elasticsearch aggregation query
```html
  <facet-aggregation-query
    name="facetAgg"
    query-builder-config="[[queryBuilderConfig]]"
    search-parameters="[[searchParameters]]"
    client="[[esclient]]"
    index="mockads"
    index-types='["ad"]'
    error="{{error}}"
    loading="{{loading}}"
    process-request="[[processRequest]]"
    field="city"
    count="10"
    result-function="[[resultFunction]]"
    result-list="{{resultList}}">
  </facet-aggregation-query>
```

### Example that runs an ajax query
```html
  <facet-aggregation-query
    query-url="[[url]]"
    process-request="[[processRequest]]"
    result-function="[[resultFunction]]"
    search-function="[[searchFunction]]"
    search-parameters="[[searchParameters]]"
    error="{{error}}"
    loading="{{loading}}"
    result-list="{{resultList}}">
  </facet-aggregation-query>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve

The demo will require a local instance of elasticsearch with the `mockads` index created by running `data/import_test_data.sh`.
