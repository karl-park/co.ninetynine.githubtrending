# Android Assignment
The goal of this assignment is to build a simple single screen app which shows the current trending Github repositories fetched from a public API. The design and business specifications have been provided which we expect you to follow as closely as possible.
We have deliberately kept the app simple enough for everyone to attempt it, but we are keen to see the approach you take to solve it. You have the freedom to give your best into it and demonstrate your skills for us to evaluate you better.

## Requirements
- The app should support a minimum SDK version of 21
- The app should fetch the trending repositories from the provided public API and display it to
the users.
- While the data is being fetched, the app should show a loading state. Shimmer
animation is optional
- If the app is not able to fetch the data, then it should show an error state to the user with an
option to retry again.
- All the items in the list should be in their collapsed state by default and can be expanded on
being tapped.
- Tapping any item will expand it to show more details and collapse any already expanded item.
Tapping the same item in expanded state should collapse it
- The app should be able to handle configuration changes (like rotation)
- The app should have 100% offline support. Once the data is fetched successfully from remote,
it should be stored locally and served from cache thereafter till the cache is not expired
- The cached data should only be valid for a duration of 2 hour after that the app should attempt
to refresh the data from remote and purge the cache if successful
- The app should give a pull-to-refresh option to the user to force fetch data from remote (refer
fig. 5)

## API Details
The complete API docs are available [here](https://githubtrendingapi.docs.apiary.io/). 
You need to fetch the data from [/repositories](https://githubtrendingapi.docs.apiary.io/%23reference/0/repositories/list-trending-repositories) endpoint. The “language” and “since” are optional parameters and are not needed in this case.
You will get a list of the trending repositories as a response from this API. If interested, you can have a look at the backend source code [here](https://github.com/huchenme/github-trending-api).

