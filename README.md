# Locompleter

**An Angular directive for Google Maps location autocompletion API.**

A modified version of: https://github.com/gvn/locompleter

## Usage

Add an `autocomplete-location` attribute to any input element.

```html
<input autocomplete-location type="text">
```

For location metadata listen for a `locationAutocompleted` event on the parent $scope.
```javascript
        $scope.$on('locationAutocompleted', function(scope,autocompleteData) {
            console.log(autocompleteData);
        });
```



```javascript
//Output
{
    address: {
        city: "Bradford"
        county: "West Yorkshire"
        postcode: "BD2 2EZ"
        street: "Robin Close"
        streetNumber: "22"
    }

    fullAddress: "22, Robin Close, Bradford, West Yorkshire, BD2 2EZ"
    latitude: 53.8185482
    longitude: -1.724217899999985
}
```
