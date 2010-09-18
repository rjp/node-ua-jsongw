Experimental UA-JSON gateway mapper.

Rather than trying to make a full UA-HTTP from scratch, this is a simple
gateway between JSON and (essentially) EDF (with helper functions).

Announcements and events are queued until they are requested.

GET

    /events         get pending events/announcements
    /folders        get a list of all folders (with unread counts?)
    /folder/f       get details for folder f
    /unread         get a list of our unread folders
    /who            get a who list
    /users          get a list of all users
    /user/xyz       get details for user xyz
    /post/12345     get a specific post

POST

    /login          start a ua session
    /logout         terminate our session
    /post/new       post a message
    /post/12345/del delete post 12345
    /page/xyz       page user xyz
    /folder/f/add   subscribe to folder f
    /folder/f/del   unsubscribe to folder f
