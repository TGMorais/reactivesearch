# Changelog

## Unreleased

<details>
    <summary>The following changes have been included in the <code>dev</code> branch and will be out in the next release. <b>Click to expand</b></summary>
    - Add support for `histogramQuery` prop in RangeSlider component - [#459](https://github.com/appbaseio/reactivesearch/pull/459)
    - Add support for aggs with query size 0 for hits removal - [#459](https://github.com/appbaseio/reactivesearch/pull/459) and [here](https://github.com/appbaseio/reactivesearch/commit/5d88dbd0b0f1d3291f3de3571f5a85a9f2a4f2d5)
    - Adds typings to npm package [#466](https://github.com/appbaseio/reactivesearch/issues/466)
    - Extend `SelectedFilters` support for range slider components i.e. `RangeInput`, `RangeSlider` and `DynamicRangeSlider`. The usage is similar to other components, with the `showFilter` prop. [#442](https://github.com/appbaseio/reactivesearch/issues/442)
    - Update `defaultQuery` prop append logic for search components [here](https://github.com/appbaseio/reactivesearch/commit/46177528d5ed0b00a4a0cc5d7e8d5dec0adfaa69). `defaultQuery` is now always appended regardless of the `customQuery`
    - Adds pagination support in SSR [#441](https://github.com/appbaseio/reactivesearch/issues/441) - This is a `Breaking Change`. Your app will be affected if you have `pagination` and `URLParams` enabled on the result component.
    - Addresses [#460](https://github.com/appbaseio/reactivesearch/issues/460) - Instead of adding a new prop to customise the url params, we have removed `-page` string from the result component. Hence, you can now set `p` or `page` as the componentId and expected results can be achieved.
</details>

## v2.6.12
- Upgrade reactivecore and appbase-js

## v2.6.11
- Upgrade reactivecore and fix an import with maps

## v2.6.10
- Upgraded reactivecore to improve reactive-maps behavior and experience 

## v2.6.9
- Fix an issue with `ReactiveList` rendering 'undefined' as class [#416](https://github.com/appbaseio/reactivesearch/issues/416)
- Fix an issue with `DateRange` field to accept both string and array [#421](https://github.com/appbaseio/reactivesearch/issues/421)
- Fix some edge cases in `DateRange` and add hover effect when selecting a date range [PR #428](https://github.com/appbaseio/reactivesearch/pull/428)
- Fix `react` prop update in `ReactiveComponent` [PR #451](https://github.com/appbaseio/reactivesearch/pull/451)
-  Add onFilterCleared prop to SelectedFilters [#401](https://github.com/appbaseio/reactivesearch/issues/401)

## v2.6.8
- Update core dependencies to fix streaming issues

## v2.6.7
- Add `defaultQuery` in search components [#353](https://github.com/appbaseio/reactivesearch/issues/353) (Support will be added in other components in coming releases)
- Add `onPageClick` in result components [#396](https://github.com/appbaseio/reactivesearch/issues/396)
- Add `containerProps` in `ResultCard` and `ResultList` [#376](https://github.com/appbaseio/reactivesearch/issues/376)

## v2.6.6
- Fix issue with `onValueSelected` getting called twice [here](https://github.com/appbaseio/reactivesearch/commit/dc60b2e46a8b6d923224e4fd6f017f535a35f79f)
- Support dyanmic props on ReactiveBase component [#373](https://github.com/appbaseio/reactivesearch/issues/373)
- Handle pagination updates on defaultQuery change in result components - [here](https://github.com/appbaseio/reactivesearch/commit/b7543e2f73828fc4bd846bc00ac1d2aa2b35e2ca)

## v2.6.5
- core: Fix an edge case with generating suggestions with numeric splits [#8](https://github.com/appbaseio/reactivecore/issues/8)
- core: Add `_index` key to hits - to help segregate the hits handling based incase of multiple indexes [#9](https://github.com/appbaseio/reactivecore/pull/9/)
- core: Fix onQueryChange behavior [#335](https://github.com/appbaseio/reactivesearch/issues/335) [#362](https://github.com/appbaseio/reactivesearch/issues/362)

## v2.6.4
- Architectural fixes to persist the watchman state in case of component unmount - This helps in keeping the component subscription active incase the component gets remounted.

## v2.6.3
- Add `onValueSelected` in search components [#254](https://github.com/appbaseio/reactivesearch/issues/254)
- Fix issue #371 resetting page number on sort change [#372](https://github.com/appbaseio/reactivesearch/pull/372)
- Cleanup stale url-params on component unmount [#368](https://github.com/appbaseio/reactivesearch/issues/368)

## v2.6.2

- Fixed query timestamp logic in core - should prevent stale results from getting rendered

## v2.6.1

- Fixed (multiple) partial queries firing issues with result component [here](https://github.com/appbaseio/reactivesearch/commit/254598be037c44a31a5aeed941176007bd1ca722)
- Fixed MultiDataList missing queryListener handlers [here](https://github.com/appbaseio/reactivesearch/commit/89d3ffb278e20233b84abd1f2df89441d9a17664)

## v2.6.0

- Fix `onSuggestion` rendering logic in search components [here](https://github.com/appbaseio/reactivesearch/commit/a2fa590710a77c9298b88a501074d08e326eb76e)
- Add `onError` support in result components [here](https://github.com/appbaseio/reactivesearch/commit/6c01c872e9211339ad972b69296f2b1da1e4fa12)
- Support toggling on integer based dropdown lists [#337](https://github.com/appbaseio/reactivesearch/commit/c10b5f222cd21e01b0208351f8d64c56e6eda148)
- Fix and cleanup infinte loading logic in Result components [#336](https://github.com/appbaseio/reactivesearch/commit/b4835ea2d623667852fdd466690cf0d66ecba5cd)
- Fix queryOptions generation logic in search components [here](https://github.com/appbaseio/reactivesearch/commit/88c850a8cc90060373a520ed73f01afc8ef05dce)
- Better query generation support in core.
- Fix complex react prop based query generation logic in core.


## v2.5.1

- Fix defaultQuery behavior in ReactiveComponent
- fix [#329](https://github.com/appbaseio/reactivesearch/issues/329) - highlightQuery issue with SSR
- update query logic for SSR
- update URLParams prop type to bool

## v2.5.0

- Add dynamic defaultQuery support in ReactiveComponent [#313](https://github.com/appbaseio/reactivesearch/issues/313)
- Fix an edge case with SingleDropdownList which threw React into an infinite update loop [#317](https://github.com/appbaseio/reactivesearch/issues/317)
- Add support for `showClear` and `clearIcon` props in `TextField`, `DataSearch` and `CategorySearch` [#255](https://github.com/appbaseio/reactivesearch/issues/255)
- Add support for combined queries via `msearch`
- Add support for SSR
- Fix onValueChange behavior

## v2.3.3

- Use commonjs module for `rheostat` [#289](https://github.com/appbaseio/reactivesearch/issues/289)
- Adds support for aggregations on missing values for list components via `showMissing` and `missingLabel` prop [#291](https://github.com/appbaseio/reactivesearch/issues/291)
- Adds `onDrag` support for RangeSlider components [#284](https://github.com/appbaseio/reactivesearch/issues/284)
- Fixes dynamic size and pagination updates [#298](https://github.com/appbaseio/reactivesearch/issues/298)
- Refactor Result Components [#303](https://github.com/appbaseio/reactivesearch/issues/303)

## v2.3.2

- Add `customHighlight` prop support in `DataSearch` and `CategorySearch` [#285](https://github.com/appbaseio/reactivesearch/issues/285)
- Add `renderListItem` prop support in `Single/Multi/DropdownList` components [#282](https://github.com/appbaseio/reactivesearch/issues/282)

## v2.3.1

- Add 🌳 tree shaking capabilities with ES modules support [here](https://github.com/appbaseio/reactivesearch/commit/62a2ace6148fbbe6795ea69fc85a0ea260501a72)
