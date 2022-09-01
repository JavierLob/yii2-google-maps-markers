<p align="center">
    <a href="https://github.com/yiisoft" target="_blank">
        <img src="https://avatars0.githubusercontent.com/u/993323" height="100px">
    </a>
    <h1 align="center">Google Maps Markers Widget for Yii2</h1>
    <br>
</p>
This is a fork from "yii2mod/yii2-google-maps-markers" that fix or add the widget capacity of build a marker with lat and lng directly,
and not take it like an adress, becasuse of that the marker don't point where it has to be.
GoogleMaps Widget displays a set of user addresses as markers on the map.


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require javierlob/yii2-google-maps-markers "*"
```

or add

```
"javierlob/yii2-google-maps-markers": "*"
```

to the require section of your composer.json.

Usage
-----

To use GoogleMaps, you need to configure its [[userLocations]] property. For example:

```php
echo yii2mod\google\maps\markers\GoogleMaps::widget([
    'userLocations' => [
        [
            'location' => [
                'address' => 'Kharkiv',
                'country' => 'Ukraine',
            ],
            'htmlContent' => '<h1>Kharkiv</h1>',
        ],
        [
            'location' => [
                'lat' => '-33.44403850076919',
                'lng' => '-70.65367723654894',
            ],
            'htmlContent' => '<h1>Palacio de la moneda</h1>',
        ],
        [
            'location' => [
                'city' => 'New York',
                'country' => 'United States',
            ],
            'htmlContent' => '<h1>New York</h1>',
        ],
    ],
]);
```

Configuration
-------------

To configure the Google Maps key or other options like language, version, library, or map options:

```php
echo yii2mod\google\maps\markers\GoogleMaps::widget([
    'userLocations' => [...],
    'googleMapsUrlOptions' => [
        'key' => 'this_is_my_key',
        'language' => 'es',
        'version' => 'weekly',
    ],
    'googleMapsOptions' => [
        'mapTypeId' => 'roadmap',
        'tilt' => 45,
        'zoom' => 5,
    ],
]);
```

OR via yii params configuration. For example:

```php
'params' => [
    'googleMapsUrlOptions' => [
        'key' => 'this_is_my_key',
        'language' => 'es',
        'version' => 'weekly',
     ],
    'googleMapsOptions' => [
        'mapTypeId' => 'roadmap',
        'tilt' => 45,
        'zoom' => 10,
    ],
],
```

To get key, please visit [page](https://developers.google.com/maps/documentation/javascript/get-api-key)

Google Maps Options
-------------------

You can find them on the [options page](https://developers.google.com/maps/documentation/javascript/reference)

#### Example
------------

![Alt text](http://res.cloudinary.com/zfort/image/upload/v1441115988/Map_preview_hcwb1x.png "Example")
