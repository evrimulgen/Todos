# Pre-work - *WonderTodo*

**WonderTodo** is an android app that allows building a todo list and basic todo items management functionality including adding new items, editing and deleting an existing item.

Submitted by: **Changching Chi**

Time spent: **120** hours spent in total

## User Stories

The following **required** functionality is completed:

* [X] User can **successfully add and remove items** from the todo list
* [X] User can **tap a todo item in the list and bring up an edit screen for the todo item** and then have any changes to the text reflected in the todo list.
* [X] User can **persist todo items** and retrieve them properly on app restart -- The app uses firebase as service and enable offline data handling.

The following **optional** features are implemented:

* [X] Persist the todo items [into SQLite](http://guides.codepath.com/android/Persisting-Data-to-the-Device#sqlite) instead of a text file -- The app uses firebase as service at the backend, its essentially same concept.
* [X] Improve style of the todo items in the list [using a custom adapter](http://guides.codepath.com/android/Using-an-ArrayAdapter-with-ListView) -- using custom **FireBaseAdaptor**
* [X] Add support for completion due dates for todo items (and display within listview item)
* [X] Use a [DialogFragment](http://guides.codepath.com/android/Using-DialogFragment) instead of new Activity for editing items
* [X] Add support for selecting the priority of each todo item (and display in listview item)
* [X] Tweak the style improving the UI / UX, play with colors, images or backgrounds -- match Material Design theme as much as possible.

The following **additional** features are implemented:

* [X] Support multiple devices synchronization
* [X] Update layout to cardview for better UI.
* [X] Leverage Google Login into Sing-In page.
* [X] Add custom animation between Sign-In and Sign-up page.
* [X] Support Sign-In Page using Google account or email.
* [X] Support Sign-Up Page using traditional email.
* [X] Client input validation.
* [X] Add **swipe-to-delete** functionality.
* [X] Add **UNDO** option for deleted item.
* [X] Create alarm for reminder, and enable cross out done item when user finished it.
* [ ] Add photo note feature -- future action item. (integrate with firebase storage)

## Video Walkthrough

Here's a walkthrough of implemented user stories:

<img src='walkthru.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

1. Migrate Activity to Fragment for listview item.
2. Pass item back and forth between acitivty and fragment. Fragment to its parent fragment.
3. Migrate simple listview to viewhold and recyclerview in order to recycle the view to avoid heavy load.
4. Switch to google firebase and enable realtime database from traditional SQLite database/ internal storage.

 When I decided move away from traditional android database to remote database using google firebase, it was a big challenge to me since this is a new stuff to me. I had to re-structure the style I had before in the project in order to fit the requirement of realtime database data model pattern. It was a fun story to me. During the implementation, I leveraged the authentication in to the application and also set up the database rule for the request in order to provide the security to users data on remote server. I had encountered singleton issue from the library as well as concurrency issue for accessing the database. that was a long non-sleep night for me as a firebase first timer to sort out the tricks. I have learnt alot from this project although it is just a todo list. I think It has met the every requirement to get on Google Play store. I am trying to make it function-wise as close as possible to EVERNOTES or GOOGLE KEEP. I had photo note functionality before in the project, however, due to the lack of time working on the project, I have not yet figured out how to make firebase storage in to my project, but i am close to it.

## License

    Copyright [2017] [Changching Chi]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.