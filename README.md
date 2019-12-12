# Nomato Restaurant Searcher
## Overview
This project was assigned to me by General Assembly during Software Engineering Immersive course. This was done in pair with [Lloyd Noone](https://github.com/lloydnoone), with the aim to use public api. We chose to use [zomato api](https://developers.zomato.com/api).

It was designed to be a mock up page after [Zomato](https://www.zomato.com/). It can search for restaurants with filter for city, area, cuisine, and search keyword.

Clicking on a result will show detailed information about the restaurant.

The project is currently deployed at https://nomato-api.herokuapp.com/.

## Timeframe
1 day

## Technologies
* React
* SCSS
* Webpack
* Zomato API

# Instructions
![Imgur](https://i.imgur.com/u0tZJXF.jpg)
Start by writing the name of the city you want to search restaurants in, in this example I will use 'london'.

![Imgur](https://i.imgur.com/secPl8m.jpg)
This will show your all the Londons in the world. In this case we want London, UK, and that's the first one. Click on it.

![Imgur](https://i.imgur.com/nu1rz61.jpg)
This will list the cuisine choices in London. This part is optional, but you can click on the cuisines to select them as filters.

![Imgur](https://i.imgur.com/SivH1fz.png)
In this example we clicked on 'fish and chips' and then click the search button on the right. The search term is optional, but you can filter it with areas or restaurant name you would like to find.

![Imgur](https://i.imgur.com/ZbUXhGP.png)
You can click on the restaurant link to go to the show page to see a more detailed information.
# Process
We began by choosing a 3rd party API to use, since Lloyd was a chef and with my interest in food, we chose Zomato API.

Once the API was decided, we studied the API in detail before we started any coding, to understand what we could do with it. Then we went on to plan overall how our website should look like.

We decided on having the search bar be on the home page, with a search for the city, and then the search for keywords.

Since the main aim of the project was learning. We tried to divide our workload evenly, with each of us having a chance to do React code, API usage, documentation reading, and styling.

One of us would work on React code, getting the data we need from the API without thinking much about the design and layout. The other person would then work on styling, arranging the elements in their proper places, giving it the styling we wanted.

After that we would swap role, so each of use will have the chance to work with both React and SCSS.

```javascript
  <header>
    <Link to='/' className='logo'>Nomato</Link>
    <div className='search-bar'>
      <SearchForm className='searchCities' name='searchCities' onChange={this.onChange} onSubmit={this.submitCities} />
      <SearchForm name='searchTerm' onChange={this.onChange} onSubmit={this.submitSearch} />

      <div className='flex-wrapper city-list'>
        {citySuggestions && citySuggestions.map(loc => (
          <Item className={`item ${selectedCity === loc.id ? 'active' : ''}`} key={loc.id} {...loc} onClick={this.selectCity} />
        ))}
      </div>
    </div>
  </header>
```
Above: the code for the search bars in the header. With the `SearchForm` components, one for city search and one for keyword search.

# Challenges
The first challenge was choosing the API, since both of us did not have much experience working with 3rd party API, first time for Lloyd and second time for me, with the previous API being Screeps (a game played by writing JavaScript code). Reading documentations was a challenge in itself, but it was a good learning experience. We tried to find an API that has enough content to work with while not being too complicated, along with giving us enough API call for the free trial.

Working in a pair without using Git was complicated. We were adviced to use one notebook and code in pair to practice, however we ended up using Live Share on VS Code and code on the same codebase at the same time together. With each of us working on different part.

Also with the time constraint, the code base is messier than what we would have liked. With SCSS code not as reusable as it could have been.

# Wins
* I learnt how to use a 3rd party API, and practice reading documentation.
* Working in a team, learning to communicate my ideas and agreeing on a compromise.
* Learning to cut extra unnecessary contents and focusing on the main feature and finish it in time for the deadline.

# Further Features
* Improvement on the search UI, currently it requires too many clicks and not intuitive to use.
* Refactor the code, make it more readable.
