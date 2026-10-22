# City Grid

Part of [Geomingo](https://hectorei19.github.io/geo-games/), daily geography games: the colours, fonts, Mingo and the shared header come from `../geo-games/brand/` (Geomingo's repository), so publish that first. Fonts: Fredoka and Nunito.

Geography grid game with cities: name a city that matches each row and column (505 to choose from: every national capital, the big cities of each continent and other famous ones). A sister of [Country Grid](https://hectorei19.github.io/country-grid/), same game and same look, with cities instead of countries. Every grid is checked so it can always be completed, whatever answers are given.

Live at https://hectorei19.github.io/city-grid/ · all the games: https://hectorei19.github.io/geo-games/

- Today's grid: one 4×4 Normal grid a day for everyone, new at midnight CET (Spain), one try.
- Solo: unlimited grids (Easy, Normal, Hard; 3×3 to 5×5). A shared result link (`?grid=4-KQPMT`) opens the same grid.
- With friends: shown as "coming soon".
- Results and stats are kept on the device (localStorage keys starting with `cc-`, so they never mix with Country Grid's `bl-` keys on the same website).

Files:
- `index.html` – the whole game (cities, categories, country data and flags included).

## How it was made

`index.html` is Country Grid's game with its data swapped: the city list, the categories (continent and country, capital, coast, seas, rivers, height, latitude, Olympic and World Cup hosts, the city's country: EU, NATO, languages, currency...), and their explanations. Each category's ⓘ in the game gives the exact rule and the doubtful cases.

The daily grids are fixed in advance in `index.html` (`DAILY_FIXED`, one entry per day from 2026-10-22 to 2027-10-22), so changing categories later never changes a day's grid. Days not in the list fall back to generating the grid from the date. A category never comes back within 3 days and appears at most 40 times a year.

## Credits

- Cities: [GeoNames](https://www.geonames.org) (via the `all-the-cities` package), CC BY 4.0: names, coordinates, population. A few outdated populations corrected.
- Countries: Country Grid's data, from [mledoze/countries](https://github.com/mledoze/countries) (ODbL 1.0, adapted) and hand-checked lists.
- Capitals, coasts, seas, rivers, heights, hosts: compiled by hand from Wikipedia (CC BY-SA 4.0), coasts checked against [Natural Earth](https://www.naturalearthdata.com) (public domain), October 2026.
- Megacities: UN World Urbanization Prospects 2018 (Wikipedia, "Megacity").
- Flags: [flag-icons](https://github.com/lipis/flag-icons), MIT License.
- Fonts: Big Shoulders Display, Barlow Semi Condensed, JetBrains Mono (Google Fonts, SIL Open Font License).
