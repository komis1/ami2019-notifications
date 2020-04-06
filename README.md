# ami2019-notifications
Notification dataset for our AmI2019 paper "Discovering User Location Semantics using Mobile Notification Handling Behaviour". The dataset is free to use for any purpose, but if using for academic purposes, please cite our work as follows:

Komninos, A., Simou I., Frengkou E., & Garofalakis J. (2019).  Discovering User Location Semantics using Mobile Notification Handling Behaviour. 15th European Conference on Ambient Intelligence (AmI'19). Rome, Italy, Springer. DOI:10.1007/978-3-030-34255-5_15

Bibtex for convenience:

@conference {143,
	title = {Discovering User Location Semantics using Mobile Notification Handling Behaviour},
	booktitle = {15th European Conference on Ambient Intelligence (AmI{\textquoteright}19)},
	year = {2019},
	note = {Best paper nomination},
	month = {11/2019},
	publisher = {Springer},
	organization = {Springer},
	address = {Rome, Italy},
	abstract = {We analyse data from a longitudinal study of 44participants, including notification handling, device state and location information. We demonstrate that it is possible to semantically label a user{\textquoteright}s location based on their notification handling behaviour, even when location coordinates are obfuscated so as not to precisely match known venue lo- cations. Privacy-preserving semantic labelling of a user{\textquoteright}s location can be useful for the contextually-relevant handling of interruptions and service delivery on mobile device},
	keywords = {Interruption management, Mobile notifications, Semantic location labelling},
	doi = {10.1007/978-3-030-34255-5_15},
	author = {Andreas Komninos and Ioulia Simou and Elton Frengkou and John Garofalakis}
}


DATA DESCRIPTION
----------------

This dataset contains details of 229,792 logged notifications received on the Android devices of 44 users, in the period between 2018-12-19 and 2019-05-03.

In this dataset, we logged the users' notifications and the details of the venue where the user was when receiving the notification, as obtained by the Google Places API. Only the most likely venue candidate was logged (Places API returns a number of candidates).

The following fields are found in the "notifications" table:


primid - autoincremented row identifier


user_id - user's unique id


id - the user's autoincremented row identifier


nid - the notification id (set by the issuing application)


priority - the notification priority (set by the issuing application)


packageName - the application generating the notification


timePosted - unix timestamp of notification issue


timeRemoved - unix timestamp of notification dismissal


sound - whether the notification was programmed to have a custom sound


default_Sound - whether the notificaiton was programmed to use the device default sound


LED - whether the notification was programmed to have a custom LED blinking pattern


default_LED - whether the notification was programmed to use the device default LED blinking pattern


vibrationPattern - whether the notification was programmed to have a custom vibration pattern


default_Vibration - whether the notification was programmed to use the device default vibration pattern


ringerMode - the current ringer mode of the device


PlaceName - the current user's venue name, retrieved from the Google Places API.


PlaceId - the current user's venue ID, retrieved from the Google Places API.


place_confidence - the current user's venue confidence, retrieved from the Google Places API.


PlaceCategories - the current user's venue categories, retrieved from the Google Places API (see also locationtypes table).


lat - the current user's venue latitude, retrieved from the Google Places API.


lng - the current user's venue longitude, retrieved from the Google Places API.


idle - whether the user's device was in "idle" state


interactive - whether the user's device was in "interactive" state


screen_state - the current state of the user's device screen


lock_scr_notifs - whether the user's device is set to allow notifications on the lock screen


flags - various flags associated with notification state


primarycat - extracted primary category of the user's current venue (from placeCategories field)


secondarycat - extracted secondary category of the user's current venue (from placeCategories field)


finalcat - primarycat with some manual amendments for certain venues
