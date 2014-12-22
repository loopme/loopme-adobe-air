# LoopMe-Adobe-Air #

## Overview ##

LoopMe is the largest mobile video DSP and Ad Network, reaching over 1 billion consumers world-wide. LoopMe’s full-screen video and rich media ad formats deliver more engaging mobile advertising experiences to consumers on smartphones and tablets.

The `loopme-adobe-air` is an extension for `Adobe Air`, allowing app developers to monetize apps via the LoopMe ad network.

<p align="center">
<img align="center" src="images/ad_overview.jpg" alt="LoopMe Interstitial Ad">
</p>

If you have questions please contact us at support@loopmemedia.com. 

## Features ##

* Full-screen image interstitials
* Full-screen rich media interstitials
* Banner ads
* Preloaded video ads
* In-app ad reward notifications, including video view completed

## Requirements ##

An appKey is required to use the `loopme-adobe-air`. The appKey uniquely identifies your app to the LoopMe ad network. (Example appKey: 7643ba4d53.) To get an appKey visit the **[LoopMe Dashboard](http://loopme.me/)**. 

`loopme-adobe-air` extension connects to native LoopMe `iOS` & `Android` libraries which control the interstitial ads, requires `Flash Proffessioanl` or `Flash Builder`, supports a minimum of `Android 4.0 (API Level 14)` and `iOS 6.0` and above.

## Usage ##

Integrating the `loopme-adobe-air` extension is very simple and should take less than 10 minutes. 

* Download `loopme-adobe-air`
* Import the `loopme-adobe-air.ane` to your project
* Use `loopme-adobe-air` extension's main **LoopMeInterstitial** class static methods to create and display interstitial ads:
   * `createInstance`: this method creates interstitial with specified appKey.
   * `load`: retrieves ads for previously specified appKey
   * `show`: makes ads visible on the screen
   * `isReady`: checks if ad is ready to be displayed
   * `destroy`: use this if interstitial is no longer needed
* Subscribe to `LoopMeInterstitial` in order to receive interstitial ad events:
   * `onLoopMeInterstitialLoadSuccess`: triggered when interstitial has been loaded the ad content
   * `onLoopMeInterstitialLoadFail`: triggered when interstitial failed to load the ad content
   * `onLoopMeInterstitialShow`: triggered when interstitial ad appeared on the screen
   * `onLoopMeInterstitialHide`: triggered when interstitial ad disappeared from the screen
   * `onLoopMeInterstitialVideoReachedEnd`: triggered when interstitial video ad has been completely watched
   * `onLoopMeInterstitialClicked`: triggered when interstitial ad was clicked
   * `onLoopMeInterstitialExpired`: triggered when interstitial ad is expired, it is recommended to re-load
* Update Application Descriptor File
   * Set AIR SDK to 13.0 or highe<br/>
   `<application xmlns="http://ns.adobe.com/air/application/13.0">`
   * Include the LoopMe extension in your application descriptor XML<br/>
    `<extensions>`<br/>
        `<extensionID>com.loopme.air</extensionID>`<br/>
    `</extensions>`   
    * Update `Android` manifest additions (Android only)<br/>
    `<activity android:name="com.loopme.AdActivity" android:configChanges="orientation|keyboardHidden|screenSize"
       android:hardwareAccelerated="true"/>`<br>
    `<activity android:name="com.loopme.AdBrowserActivity" />`<br>
    `<activity android:name="com.loopme.PlayerActivity" android:configChanges="orientation|keyboardHidden|screenSize"
       android:hardwareAccelerated="true"/>`<br>
    `<uses-permission android:name="android.permission.INTERNET" />`<br>
    `<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />`<br>
    `<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />`<br>
    `<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />`<br>
    `<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />`<br>
    `<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />`<br>
    `<uses-permission android:name="android.permission.VIBRATE" />`

## Sample project ##

Check out our `loopme-adobe-air-sample` as an example of `loopme-adobe-air` extension integration.

## License ##
LICENSED UNDER THE TERMS OF THE BSD LICENSE, AS SPECIFIED BELOW.

DISCLAIMER: IMPORTANT: THIS LOOPME SOFTWARE IS SUPPLIED TO YOU BY LOOPME LTD. ("LOOPME") IN CONSIDERATION OF YOUR AGREEMENT TO THE TERMS FOUND ON OUR **[WEBSITE](http://www.loopmemedia.com/privacy/)**, 
AND YOUR USE, INSTALLATION, MODIFICATION OR REDISTRIBUTION OF THIS LOOPME SOFTWARE CONSTITUTES ACCEPTANCE OF THESE TERMS. 
IF YOU DO NOT AGREE WITH THESE TERMS, PLEASE DO NOT USE, INSTALL, MODIFY OR REDISTRIBUTE THIS LOOPME SOFTWARE.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, 
INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. 
IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, 
OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) 
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

COPYRIGHT © 2012, LOOPME LTD, ALL RIGHTS RESERVED