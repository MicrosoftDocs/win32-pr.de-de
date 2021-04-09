---
title: Wiedergabelisten
description: Wiedergabelisten
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Wiedergabelisten, Migration
- Windows Media Metadatei-Wiedergabelisten, Migration
- Metadatei-Wiedergabelisten, Migration
- Migrations Handbuch, Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036695"
---
# <a name="playlists"></a>Wiedergabelisten

Das Windows Media Player 6,4-ActiveX-Steuerelement-Objektmodell enthält vier Methoden und eine Eigenschaft zum Arbeiten mit Windows Media Metadatei-Wiedergabelisten:

-   *Player6*. **Getcurrententry**
-   *Player6*. **Setcurrententry**
-   *Player6*. **Getmediaparameter**
-   *Player6*. **Getmediaparametername**
-   *Player6*. **Entrycount**.

Diese bieten eine begrenzte Funktionalität zum Navigieren in einer Wiedergabelisten-Metadatei mit der Dateinamenerweiterung. ASX und zum Abrufen von Informationen zu den Einträgen, die in der Wiedergabeliste enthalten sind.

In Windows Media Player 7 wurde "Medienbibliothek" eingeführt. Die Bibliothek ermöglicht es Benutzern, Ihre digitalen Medieninhalte zu organisieren und benutzerdefinierte Wiedergabelisten zu erstellen, die von der grafischen Benutzeroberfläche des Players verwaltet werden können. Das ActiveX-Steuerelement Objektmodell von Windows Media Player 7 oder höher bietet Unterstützung für die Arbeit mit Bibliotheks Wiedergabelisten sowie die in Windows Media-Metadateien mit der Dateinamenerweiterung ". asx" enthaltenen Wiedergabelisten.

> [!Note]  
> Aus Sicherheitsgründen muss der Benutzer die Zugriffsrechte für die Bibliothek erteilen, bevor das Programm seinen Inhalt bearbeiten kann. Zugriffsrechte können nur über das Windows Media Player 9-oder spätere Objektmodell angefordert und erteilt werden. Weitere Informationen zu Zugriffsrechten finden Sie unter [Bibliotheks Zugriff](library-access.md).

 

Das Objektmodell Windows Media Player 7 oder höher enthält drei Objekte zum Verarbeiten von Wiedergabelisten. Das **playlistcollection** -Objekt stellt Funktionen zum Organisieren von Wiedergabelisten bereit. Er stellt die gesamte Auflistung von Wiedergabelisten in der Bibliothek des Benutzers dar. Das **playlistarray** -Objekt bietet eine Möglichkeit zum Abrufen einer bestimmten Wiedergabeliste aus dem **playlistcollection** -Objekt mithilfe einer Indexnummer. zwei der **playlistcollection** -Objektmethoden rufen ein **playlistarray** -Objekt ab. Das **Wiedergabe** Listen Objekt stellt die Eigenschaften und Methoden bereit, die zum Bearbeiten von in einer einzelnen Wiedergabeliste enthaltenen Medien Elementen erforderlich sind.

Da jede Wiedergabeliste in der Bibliothek z. b. einen eindeutigen Namen hat, können Sie mithilfe von *playlistcollection* eine Wiedergabeliste aus der Bibliothek abrufen. **getByName** -Methode:


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



Am häufigsten möchten Sie mit der aktuellen Wiedergabeliste arbeiten. Obwohl es möglich ist, mehrere Wiedergabelisten Objekte zu verwenden, kann nur eine vom *Player* abgerufen werden. **currentwiedergabe** -Eigenschaft zu einem beliebigen Zeitpunkt: der, den Windows Media Player zu diesem Zeitpunkt verarbeitet.

Wenn Windows Media Player 7 oder höher eine Windows Media-Metadatei mit der Dateinamenerweiterung ". asx" wieder gibt, erstellt Sie zuerst ein **Wiedergabe** Listen Objekt. Anschließend wird das Objekt mit den Informationen aus der. ASX-Wiedergabeliste gefüllt, und dieses **Wiedergabe** Listen Objekt wird zur aktuellen Wiedergabeliste. Dies bedeutet, dass Sie die dem **Wiedergabe** Listen Objekt zugeordneten Eigenschaften und Methoden verwenden können, um. ASX-Wiedergabelisten genau so zu bearbeiten, wie Sie die Wiedergabelisten in der Bibliothek verarbeiten würden. Um beispielsweise die Anzahl der Einträge in einer. ASX-Wiedergabeliste mit dem Objektmodell der Version 6,4 abzurufen, verwenden Sie *Player6*. **Entrycount** -Eigenschaft:


```C++
var entrycount = WMP64.EntryCount;

```



Wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden, verwenden Sie die *Wiedergabeliste*. **count** -Eigenschaft:


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Wenn Sie das-Steuerelement der Version 6,4 verwenden, können Sie *Player6* verwenden. **Getcurrententry** -Methode zum Abrufen des Index des aktuellen Eintrags in einer. ASX-Wiedergabeliste:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



Sie können das gleiche Ergebnis erzielen, indem Sie das Objektmodell Windows Media Player 7 oder höher im Skript verwenden. Im folgenden JScript-Beispiel wird das aktuelle Medienobjekt mit jedem Element in der Wiedergabeliste verglichen. Wenn *Medien*. **isidentical** gibt true zurück, ein Meldungs Feld zeigt den Index des aktuellen Medien Elements an.


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



Um den Index des aktuellen Eintrags in einer. ASX-Wiedergabeliste anzugeben, verwenden Sie *Player6*. **Setcurrententry**. Wiedergabe Indizes der Wiedergabeliste in Version 6,4 beginnen mit 1. Wenn Sie also den zweiten Eintrag in einer Metadatei Wiedergabeliste des aktuellen Eintrags vornehmen möchten, verwenden Sie die folgende Syntax:


```C++
WMP6.SetCurrentEntry(2);

```



Wiedergabe Indizes für Wiedergabelisten sind in Windows Media Player 7 oder höher Null basiert; Verwenden Sie die folgende Syntax, um den zweiten Eintrag in einer Metadatei-Wiedergabeliste für die aktuelle zu verwenden, wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



Im folgenden JScript-Beispiel wird eine Funktion veranschaulicht, die eine Indexnummer als Parameter akzeptiert, und dann den Wiedergabelisten Eintrag, der dem Index das aktuelle Medien Element entspricht, erstellt:


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



Windows Media-Metadateien können benutzerdefinierte Parameter Elemente enthalten, die Sie mit dem- **<PARAM>** Tag angeben. Wenn Sie das Objektmodell der Version 6,4 verwenden, können Sie den Namen eines bestimmten Parameters mit *Player6* abrufen. **Getmediaparametername** -Methode. Im folgenden JScript-Beispiel wird der Name des ersten Parameters im ersten Eintrag einer. ASX-Wiedergabeliste abgerufen:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



Auf ähnliche Weise können Sie den Wert, der dem Parameter zugeordnet ist, mithilfe von *Player6* abrufen. **Getmediaparameter**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



Im folgenden JScript-Beispiel wird das Objektmodell Windows Media Player 7 oder höher verwendet, um den Parameternamen und den Wert aus dem ersten Eintrag in einer. ASX-Wiedergabeliste abzurufen:


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



Sie können den *playlistcollection*-Befehl verwenden. **importwiedergabe** -Methode, um der Bibliothek eine. ASX-Wiedergabeliste hinzuzufügen. Nach dem Importieren wird die Metadatei-Wiedergabeliste zu einer Bibliotheks Wiedergabeliste, sodass Sie Sie mit allen Eigenschaften und Methoden, die Sie zur Verfügung stellen, bearbeiten können. Der Benutzer muss Vollzugriff auf die Bibliothek gewähren, damit Ihre Anwendung die **importwiedergabe** -Methode verwenden kann.

Sie können *playlistcollection* verwenden. **getByName** , um zu testen, ob eine Wiedergabeliste vorhanden ist. Diese Methode gibt immer ein gültiges **playlistarray** -Objekt zurück. Wenn das abgerufene Wiedergabelisten Array genau eine Wiedergabeliste enthält, ist eine Wiedergabeliste mit diesem Namen in der Bibliothek vorhanden. Andernfalls enthält das Wiedergabelisten Array kein Wiedergabelisten Objekt. Dies bedeutet, dass keine Wiedergabeliste in der Bibliothek vorhanden ist, in der der Name als Argument an die **getByName** -Methode übermittelt wird. Dies wird im folgenden JScript-Beispiel veranschaulicht:


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

[**Handbuch für die Migration des Objektmodells**](object-model-migration-guide.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> </dl>

 

 




