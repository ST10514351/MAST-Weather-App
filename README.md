**ReadMe document**

*Below are the changes made to the weather application*

| # | Error | Fix | Explanation |
|---:|---|---|---|
| 1 | Missing `ImageBackground` import | Imported `ImageBackground` from `react-native`. | Prevents an undefined component error. |
| 2 | Incorrect background image source | Used `source={{ uri: selectedWeather.backgroundImage }}`. | Loads remote images correctly. |
| 3 | City selection compared against `weather.country` | Changed the comparison to `weather.city`. | Highlights the correct city. |
| 4 | Selected country instead of city | Used `setSelectedCity(weather.city)`. | Keeps the selected state consistent with the lookup. |
| 5 | Humidity displayed the feels-like temperature | Used `selectedWeather.humidity`. | Displays the correct humidity percentage. |
| 6 | Hourly forecast was not horizontal | Changed `horizontal={false}` to `horizontal={true}`. | Enables horizontal scrolling. |
| 7 | Every hourly card showed the same temperature | Used `hour.temperature`. | Displays the temperature for each hour. |
| 8 | Daily forecast `.map()` did not return JSX | Changed `{}` to `()` around the returned JSX. | Renders all five daily forecast cards. |
| 9 | Daily high and low were reversed | Displayed `day.high` before `day.low`. | Shows temperatures in the correct order. |
| 10 | Daily forecast used a column layout | Changed `flexDirection: 'column'` to `'row'`. | Aligns forecast information horizontally. |
| 11 | Sunrise displayed the sunset value | Used `selectedWeather.sunrise`. | Shows the correct sunrise time. |
| 12 | Weather detail displayed `{label}` instead of `{value}` | Changed the rendered variable to `{value}`. | Displays the actual weather information. |
| 13 | Weather detail items occupied the full width | Changed `width: '100%'` to `width: '48%'`. | Allows two items per row. |
| 14 | Sun and moon details lacked a flexible row layout | Added `flexDirection: 'row'`, `flexWrap: 'wrap'`, and `justifyContent: 'space-between'`. |
