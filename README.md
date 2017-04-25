# facet-aggregation-query

A Polymer Element that performs an elasticsearch aggregation query, with the results in a format ready to use as a set of facets (for an example, see `<facet-list>`).

### Example
```html
    <facet-aggregation-query
      name="facetAgg"
      query-builder-config="[[queryBuilderConfig]]"
      search-parameters="[[searchParameters]]"
      client="[[esclient]]"
      index="mockads"
      index-types='["ad"]'
      last-error="{{error}}"
      loading="{{loading}}"
      process-request="{{processRequest}}"
      field="city"
      count="10"
      combine-function="[[combineFunction]]"
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
