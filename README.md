loadMore.js
=======

loadMore.js is a jQuery plugin for easily adding an AJAX-based "more"-link pagination to an element on ones site.

## Usage

Simple:

    $('.list').loadmore('/path/to/more/html');

Advanced:

    $('.list').loadmore('/path/to/more/html', {
      'className' : '',
      text : 'More',
      loadingText : 'Loading',
      page : 0,
      pageSize : false,
      'pageParam' : 'page',
      loaded : false
    });

## Advanced options

* **id** - a string identifier for this particular pager to make it easier for the History API integration to restore the correct pager.
* **className** - extra classes to add to the more-link container
* **text** - text to use in the more-link - should be either a string or a function
* **loadingText** - text to use in the more-link when it is loading - should be either a string or a function
* **page** - the current page in the list
* **rowsPerPage** - how many elements should be expected on a new page? If less than this amount is received we've reached the end and will remove the pager
* **maxPageCount** - the maximum numbers of pages to fetch at once - used by the History API integration
* **pageParam** - the query parameter used to specify which page to fetch
* **pageStartParam** - when more than one page is fetched at once this is the query parameter used to specify the page to start from
* **complete** - a function to execute once a new page has been loaded, return false if the pager should be removed
* **useHistoryAPI** - whether to use the History API in supported browsers or not

### Events

* **loadmore:last** - triggered on the pager when the last page has been fetched

## In action on

* **Flattr.com**, eg. https://flattr.com/profile/voxpelli

## Support

[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=voxpelli&url=https://github.com/voxpelli/jquery-loadmore&title=loadmore.js&language=en_GB&tags=github&category=software)
