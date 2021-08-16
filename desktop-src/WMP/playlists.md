---
title: Wiedergabelisten
description: Wiedergabelisten
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobil, Wiedergabelisten
- Wiedergabelisten, Migration
- Windows Medienmetadatei-Wiedergabelisten, Migration
- Metafile-Wiedergabelisten, Migration
- Migrationshandbuch, Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccdd98789de6c8d4faa06882376967298646febabd790067710dc4f460ba65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334473"
---
# <a name="playlists"></a>Wiedergabelisten

Das Windows Media Player 6.4 ActiveX-Steuerelementobjektmodell enthält vier Methoden und eine Eigenschaft für die Arbeit mit Windows Media-Metadateiwiedergabelisten:

-   *Player6*. **GetCurrentEntry**
-   *Player6*. **SetCurrentEntry**
-   *Player6*. **GetMediaParameter**
-   *Player6*. **GetMediaParameterName**
-   *Player6*. **EntryCount**.

Zusammen bieten diese eingeschränkte Funktionalität zum Navigieren in einer Wiedergabelisten-Metadatei mit der Dateinamenerweiterung ASX und zum Abrufen von Informationen zu den in der Wiedergabeliste enthaltenen Einträgen.

Windows Media Player 7 wurde "Media Library" eingeführt. Mit der Bibliothek können Benutzer ihre digitalen Medieninhalte organisieren und benutzerdefinierte Wiedergabelisten erstellen, die über die grafische Benutzeroberfläche des Players verwaltet werden können. Das Windows Media Player 7 oder höher ActiveX Steuerelementobjektmodells bietet Unterstützung für die Arbeit mit Bibliothekswiedergabelisten sowie wiedergabelisten, die in Windows Media-Metadateien mit einer ASX-Dateinamenerweiterung enthalten sind.

> [!Note]  
> Aus Sicherheitsgründen muss der Benutzer Zugriffsrechte für die Bibliothek gewähren, bevor das Programm seinen Inhalt bearbeiten kann. Zugriffsrechte können nur über das Objektmodell der Windows Media Player 9er Serie oder höher angefordert und gewährt werden. Weitere Informationen zu Zugriffsrechten finden Sie unter [Bibliothekszugriff.](library-access.md)

 

Das Windows Media Player 7 oder höher-Objektmodell enthält drei Objekte für die Verarbeitung von Wiedergabelisten. Das **PlaylistCollection-Objekt** stellt Funktionen zum Organisieren von Wiedergabelisten bereit. sie stellt die gesamte Sammlung von Wiedergabelisten in der Bibliothek des Benutzers dar. Das **PlaylistArray-Objekt** bietet eine Möglichkeit, eine bestimmte Wiedergabeliste mithilfe einer Indexnummer aus dem **PlaylistCollection-Objekt** abzurufen. zwei der **PlaylistCollection-Objektmethoden** rufen ein **PlaylistArray-Objekt** ab. Das **Playlist-Objekt** stellt die Eigenschaften und Methoden bereit, die zum Bearbeiten von Medienelementen in einer einzigen Wiedergabeliste erforderlich sind.

Da beispielsweise jede Wiedergabeliste in der Bibliothek einen eindeutigen Namen hat, können Sie mithilfe der *PlaylistCollection* eine Wiedergabeliste aus der Bibliothek abrufen. **getByName-Methode:**


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



Sie möchten am häufigsten mit der aktuellen Wiedergabeliste arbeiten. Es ist zwar möglich, mehrere Wiedergabelistenobjekte zu verwenden, aber nur eines kann vom *Player* abgerufen werden. **currentPlaylist-Eigenschaft** zu einem beliebigen Zeitpunkt: die eigenschaft, die Windows Media Player gerade verarbeitet.

Wenn Windows Media Player 7 oder höher eine Windows Medienmetadatei mit der Dateinamenerweiterung ASX wiederherstellt, wird zunächst ein **Wiedergabelistenobjekt** erstellt. Als Nächstes füllt es das Objekt mit den Informationen aus der ASX-Wiedergabeliste auf und macht dieses **Wiedergabelistenobjekt** dann zur aktuellen Wiedergabeliste. Dies bedeutet, dass Sie die Eigenschaften und Methoden, die dem **Playlist-Objekt** zugeordnet sind, verwenden können, um ASX-Wiedergabelisten genau so zu bearbeiten, wie Sie Wiedergabelisten in der Bibliothek behandeln würden. Um beispielsweise die Anzahl der Einträge in einer ASX-Wiedergabeliste mit dem Objektmodell der Version 6.4 abzurufen, verwenden Sie *Player6.* **EntryCount-Eigenschaft:**


```C++
var entrycount = WMP64.EntryCount;

```



Wenn Sie das objektmodell Windows Media Player 7 oder höher verwenden, verwenden Sie die *Wiedergabeliste*. **count-Eigenschaft:**


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Wenn Sie das -Steuerelement der Version 6.4 verwenden, können Sie *Player6* verwenden. **GetCurrentEntry-Methode** zum Abrufen des Indexes des aktuellen Eintrags in einer ASX-Wiedergabeliste:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



Sie können das gleiche Ergebnis erzielen, indem Sie das Windows Media Player 7 oder höher im Skript verwenden. Im folgenden JScript Beispiel wird das aktuelle Medienobjekt mit jedem Element in der Wiedergabeliste verglichen. Wenn *Medien*. **isIdentical** gibt TRUE zurück. In einem Meldungsfeld wird der Index des aktuellen Medienelements angezeigt.


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



Um den Index des aktuellen Eintrags in einer ASX-Wiedergabeliste anzugeben, verwenden Sie *Player6*. **SetCurrentEntry**. Wiedergabelisteneintragsindizes in Version 6.4 beginnen mit 1. Verwenden Sie daher die folgende Syntax, um den zweiten Eintrag in einer Metadatei-Wiedergabeliste zum aktuellen Eintrag zu machen:


```C++
WMP6.SetCurrentEntry(2);

```



Wiedergabelisteneintragsindizes sind in Windows Media Player 7 oder höher nullbasiert. Um den zweiten Eintrag in einer Metadateiwiedergabeliste als aktuellen Eintrag zu machen, verwenden Sie bei Verwendung des Windows Media Player 7 oder höher-Objektmodells die folgende Syntax:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



Im folgenden JScript Beispiel wird eine Funktion veranschaulicht, die eine Indexnummer als Parameter akzeptiert und dann den Wiedergabelisteneintrag, der dem Index entspricht, zum aktuellen Medienelement macht:


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



Windows Medienmetadateien können benutzerdefinierte Parameterelemente enthalten, die Sie mit dem **<PARAM>** -Tag angeben. Wenn Sie das Objektmodell der Version 6.4 verwenden, können Sie den Namen eines bestimmten Parameters mit *player6* abrufen. **GetMediaParameterName-Methode.** Im folgenden JScript Beispiel wird der Name des ersten Parameters im ersten Eintrag einer ASX-Wiedergabeliste abgerufen:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



Auf ähnliche Weise können Sie den wert abrufen, der dem Parameter zugeordnet ist, indem *Sie Player6* verwenden. **GetMediaParameter**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



Im folgenden JScript Beispiel wird das objektmodell Windows Media Player 7 oder höher verwendet, um den Parameternamen und -wert aus dem ersten Eintrag in einer ASX-Wiedergabeliste abzurufen:


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



Sie können die *PlaylistCollection* verwenden. **importPlaylist-Methode,** um der Bibliothek eine ASX-Wiedergabeliste hinzuzufügen. Nach dem Importieren wird die Metadateiwiedergabeliste zu einer Bibliothekswiedergabeliste, sodass Sie sie mit allen verfügbaren Eigenschaften und Methoden bearbeiten können. Der Benutzer muss vollzugriffsrechte für die Bibliothek gewähren, damit Ihre Anwendung die **importPlaylist-Methode** verwenden kann.

Sie können *PlaylistCollection* verwenden. **getByName,** um zu testen, ob eine Wiedergabeliste vorhanden ist. Diese Methode gibt immer ein gültiges **PlaylistArray-Objekt** zurück. Wenn das abgerufene Wiedergabelistenarray genau eine Wiedergabeliste enthält, ist eine Wiedergabeliste mit diesem Namen in der Bibliothek vorhanden. Andernfalls enthält das Wiedergabelistenarray kein Wiedergabelistenobjekt. Dies bedeutet, dass in der Bibliothek keine Wiedergabeliste mit dem Namen vorhanden ist, der als Argument an die **getByName-Methode** übergeben wird. Dies wird im folgenden JScript Beispiel veranschaulicht:


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Leitfaden zur Migration von Objektmodellen**](object-model-migration-guide.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> </dl>

 

 




