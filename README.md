## ![](logo.png) Xamarin.Forms.GoogleMaps 

![](https://img.shields.io/nuget/v/Xamarin.Forms.GoogleMaps.svg) ![](https://img.shields.io/nuget/dt/Xamarin.Forms.GoogleMaps.svg) [![Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/Xamarin-Forms-GoogleMaps/public) [![donate/gumload](https://img.shields.io/badge/donate-gumload-orange.svg)](#donation)

[日本語の README はこちら！](README-ja.md)

Yet another maps library for Xamarin.Forms that optimized for Google maps.

Usage is almost the same as [Xamarin.Forms.Maps](https://www.nuget.org/packages/Xamarin.Forms.Maps), Because this is forked from [Xamarin.Forms.Maps - github](https://github.com/xamarin/Xamarin.Forms) 

## DEMO Apps

You can try DEMO Apps for Android/iOS that includes all this library features.
[DEMO Apps source code is here](https://github.com/amay077/Xamarin.Forms.GoogleMaps/tree/master/XFGoogleMapSample).

* [Android DEMO Apps](https://install.mobile.azure.com/users/okuokuoku/apps/xfgooglemapsample/distribution_groups/trial) - Open this link in your Android browser
* iOS DEMO Apps - Please request in [Gitter](https://gitter.im/Xamarin-Forms-GoogleMaps/public)

![screenshot](screenshot01.png)

## Motivation

The official [Xamarin.Forms.Map](https://developer.xamarin.com/guides/xamarin-forms/user-interface/map/)  has minumn functions only.

Especially, Bing Maps SDK is very old-fashioned because it has not vector-tile, marker's infowindow.

Android and iOS monopolize most the mobile apps market. Thus I think no need Bing maps support.

Furthermore, I am using Google Maps instead of MapKit because it is easy for define common API for Android and iOS.

**Xamarin.Forms.GoogleMaps provides maximum Google maps features for Xamarin.Forms!!**

## Comparison with Xamarin.Forms.Maps

|Feature|X.F.Maps|X.F.GoogleMaps|
| ------------------- | :-----------: | :-----------: |
|Map types|Yes|Yes|
|Traffic map|-|Yes|
|Map events|-|Yes|
|Panning with animation|Yes|Yes|
|Panning directly|-|Yes|
|Pins|Yes|Yes|
|Custom Pins|-|Yes|
|Pin drag & drop|-|Yes|
|Polygons|-|Yes|
|Lines|-|Yes|
|Circles|-|Yes|
|Custom map tiles|-|Yes|

For more information, see [Comparison with Xamarin.Forms.Maps](https://github.com/amay077/Xamarin.Forms.GoogleMaps/wiki/Comparison-with-Xamarin.Forms.Maps).

## Setup

* Available on NuGet: https://www.nuget.org/packages/Xamarin.Forms.GoogleMaps/ [![NuGet](https://img.shields.io/nuget/v/Xam.Plugin.Geolocator.svg?label=NuGet)](https://www.nuget.org/packages/Xamarin.Forms.GoogleMaps/)
* Install into your PCL project and Client projects.

## Platform Support

|Platform|Supported|
| ------------------- | :-----------: |
|iOS Unified|Yes|
|Android|Yes|
|Windows 10 UWP|No|
|Others|No|

## Usage

Same as this

* [Map Control - Xamarin](https://developer.xamarin.com/guides/xamarin-forms/user-interface/map/)

In iOS, get the API Key from [Google Maps API for iOS](https://developers.google.com/maps/documentation/ios-sdk/) then insert ``Init`` of ``AppDelegate.cs``.  

```csharp
// AppDelegate.cs
[Register("AppDelegate")]
public partial class AppDelegate : global::Xamarin.Forms.Platform.iOS.FormsApplicationDelegate
{
    public override bool FinishedLaunching(UIApplication app, NSDictionary options)
    {
        global::Xamarin.Forms.Forms.Init();
        Xamarin.FormsGoogleMaps.Init("your_google_maps_ios_api_key");
        LoadApplication(new App());

        return base.FinishedLaunching(app, options);
    }
}
``` 

Namespace is ``Xamarin.Forms.GoogleMaps`` instead of ``Xamarin.Forms.Maps``. 

Sample application is here.

* [XFGoogleMapSample](https://github.com/amay077/Xamarin.Forms.GoogleMaps/tree/master/XFGoogleMapSample)

## Who uses it?

This is just a short list of apps and projects that use Xamarin.Forms.GoogleMaps. If you've used Xamarin.Forms.GoogleMaps in a apps and would like it listed on this page, [**Please report it**](https://github.com/amay077/Xamarin.Forms.GoogleMaps/issues/512). 

<table>
  <tr>
    <td align="center">
      <h3><a target="_blank" href="https://www.herenow.city/">HereNow</a></h3>
      <img src="showcase_herenow.jpg" width="200" width="200" style="max-width:100%;">
      <p>by <a target="_blank" href="https://www.cinra.co.jp/">CINRA, Inc.</a></p>
    </td>
    <td align="center">
      <h3><a target="_new" href="https://www.citybee.lt/">CityBee</a></h3>
      <img src="showcase_citybee.png" width="200" width="200" style="max-width:100%;">
      <p>&nbsp;</p>
    </td>
    <td align="center">
      <h3><a target="_new" href="https://itunes.apple.com/tr/app/rentacarss-ara%C3%A7-takip/id1276280125">Rentacarss Araç Takip</a></h3>
      <img src="showcase_rentacarss.jpg" width="200" width="200" style="max-width:100%;">
      <p>&nbsp;</p>
    </td>
    <td align="center">
      <h3>yakala.co</h3>
      <a target="_blank" href="https://apps.apple.com/tr/app/yakala-co/id834961121?l=tr">iOS</a>
      &nbsp;/&nbsp;<a target="_blank" href="https://play.google.com/store/apps/details?id=com.mobven.yakalaco">Android</a>
      <img src="showcase_yakala.png" width="200" width="200" style="max-width:100%;">
      <p>by <a target="_blank" href="http://www.dakicksoft.com/">Dakicksoft</a></p>
    </td>
  </tr>
  <tr>
    <td align="center">
      <h3><a target="_blank" href="https://itunes.apple.com/us/app/transantiagomaster/id541341697?mt=8">TransantiagoMaster</a></h3>
      <img src="https://user-images.githubusercontent.com/1848210/47026824-b3d31c00-d13c-11e8-926a-d7e68403e856.png" width="200" width="200" style="max-width:100%;">
    </td>
    <td align="center">
    </td>
    <td align="center">
      <h3>CmsApp</h3>
      <a target="_blank" href="https://itunes.apple.com/us/app/cmsmobileapp/id1151248489?ls=1&mt=8">iOS</a>
      &nbsp;/&nbsp;<a target="_blank" href="https://play.google.com/store/apps/details?id=net.winsir.cms.CmsMobile">Android</a>
      <img src="https://user-images.githubusercontent.com/20931876/64476046-8540a400-d147-11e9-9b62-22894d5e2ffd.png" width="200" width="200" style="max-width:100%;">
      <p>by <a target="_blank" href="http://cms.winsir.net/">Ruben Carreon</a></p>
    </td>
    <td align="center">
      <h3>UsynligO</h3>
      <a target="_blank" href="https://apps.apple.com/us/app/usynligo/id1306699569">iOS</a>
      &nbsp;/&nbsp;<a target="_blank" href="https://play.google.com/store/apps/details?id=com.Benum.UsynligO">Android</a>
      <img src="https://lh3.googleusercontent.com/fqVdiOUQTz7oBwCccvmgq8z8tmV0Ip6tLBI6SCEDVHiKcVGGZWwUrEufJ-iOmUZhxu8=s180-rw" width="200" width="200" style="max-width:100%;">
      <p>by <a target="_blank" href="https://play.google.com/store/apps/developer?id=Trond+Benum">Trond Benum</a></p>
    </td>
  </tr>
  <tr>
    <td align="center">
      <h3>Taiwan-AskFaceMask (問口罩)</h3>
      <a target="_blank" href="https://apps.apple.com/tw/app/id1498868646">iOS</a>
      &nbsp;/&nbsp;<a target="_blank" href="https://play.google.com/store/apps/details?id=tw.goodjob.askfacemaskapp">Android</a>
      <img src="showcase_taiwan_askfacemask.gif" width="200" width="200" style="max-width:100%;">
      <p>by <a target="_blank" href="https://github.com/JamestsaiTW">JamestsaiTW</a></p>
    </td>
    <td align="center">
      <h3>Bipbip Navigation GPS</h3>
      <a target="_blank" href="https://apps.apple.com/app/id1588690430">iOS</a>
      &nbsp;/&nbsp;<a target="_blank" href="https://play.google.com/store/apps/details?id=com.Beepbip">Android</a>
      <img src="showcase_bipbip.png" width="200" width="200" style="max-width:100%;">
      <p>by <a target="_blank" href="https://bipbip.tv/">Bipbip</a></p>
    </td>
    <td align="center">
      <h3>eLandFly</h3>
      <a target="_blank" href="https://apps.apple.com/app/id1527799439">iOS</a>
      &nbsp;/&nbsp;<a target="_blank" href="https://play.google.com/store/apps/details?id=com.elandfly.elandfly">Android</a>
      <img src="showcase_elandfly.png" width="200" width="200" style="max-width:100%;">
      <p>by <a target="_blank" href="https://www.elandfly.com/">elandfly.com</a></p>    
    </td>
    <td align="center">
    </td>
  </tr>  
</table>

## Releases

See [Releases](https://github.com/amay077/Xamarin.Forms.GoogleMaps/releases) or [RELEASE_NOTES](RELEASE_NOTES.md).

## Future plans

I will follow Xamarin.Forms.Maps API as possible. I will add new API only when I implement Google maps original feature.

If you have proposals then send to [@amay077](https://twitter.com/amay077) or submit ISSUE or Pull-request!

Latest scheduled features as follows:

* ~~Pin.ShowInfoWindow/HideInfoWindow method(or IsVisibleInfoWindow property)~~ add in v1.0.0
* ~~Moving pin by tap and hold~~ add in v1.5.0
* ~~Adding Polygon, Polyline, Circle~~ add in v1.1.0
* and more [enhancements](https://github.com/amay077/Xamarin.Forms.GoogleMaps/labels/enhancement)!

Windows 10 UWP is no longer supported from v5.0.0.

## Contribution

We really appreciate your contribution.

Please read the [contribution guideline](CONTRIBUTING.md).

## Commmunity Chat

You can join to out [gitter room](https://gitter.im/Xamarin-Forms-GoogleMaps/public)!

## Donation

I will continue to work hard with your support!

Donate through [Gumroad](https://amay077.gumroad.com/).

If this project help you reduce time to develop, you can give me a :sushi: :)

## License

See [LICENSE](LICENSE.txt) .

* logo.png by [alecive](http://www.iconarchive.com/show/flatwoken-icons-by-alecive.html) - [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed)
* Android Icon made by [Hanan](http://www.flaticon.com/free-icon/android_109464) from www.flaticon.com
* Apple Icon made by [Dave Gandy](http://www.flaticon.com/free-icon/apple-logo_25345) from www.flaticon.com


http://xamaringuyshow.com/2023/06/28/dotnet-maui-google-maps-with-custom-pins/
