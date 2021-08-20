---
title: Verwenden des Windows Media Player 7 oder höher
description: Verwenden des Windows Media Player 7 oder höher
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player,Objektmodell
- Windows Media Player Objektmodell, Version 7 oder höher
- Objektmodell, Version 7 oder höher
- Windows Media Player ActiveX,Version 7 oder höher
- ActiveX,Version 7 oder höher
- Windows Media Player Mobile ActiveX-Steuerelement, Version 7 oder höher
- Windows Media Player Mobil, Objektmodell
- Migrationshandbuch, Version 7 oder höher
- Versionen von Windows Media Player,Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa40dea2718c602bfae305703913b418d0f8a48b90278683aba099dfe0d703bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117028"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Verwenden des Windows Media Player 7 oder höher

Die meisten Aufgaben, die Sie möglicherweise mit dem Windows Media Player 6.4-Steuerelementobjektmodell ActiveX einen neuen Ansatz erfordern. In vielen Fällen haben sich die Namen der Eigenschaften, Methoden und Ereignisse im Objektmodell Windows Media Player 7 oder höher geändert. Um beispielsweise den Dateipfad im Objektmodell der Version 6.4 anzugeben, legen Sie die **Player6.FileName-Eigenschaft** fest:


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Wenn Sie das Windows Media Player 7 oder höher verwenden, müssen Sie die **Player.URL-Eigenschaft** festlegen:


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



Alternativ können Sie mit dem 10-Objektmodell ein **Media-Objekt** aus der Bibliothek abrufen und dann die **Player.currentMedia-Eigenschaft** festlegen:


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Auf einen großen Teil der Funktionalität im Windows Media Player 7 oder höher wird über die Objekthierarchie zugegriffen. Wie im vorherigen Beispiel gezeigt, können Sie ein **Playlist-Objekt** abrufen, indem Sie die **getAll-Methode** des **mediaCollection-Objekts** verwenden, auf das über das Player-Stammobjekt **zugegriffen** wird. Anschließend können Sie ein bestimmtes **Medienobjekt** aus dem **Playlist-Objekt** abrufen, indem Sie die **Elementmethode** des **Playlist-Objekts** verwenden. Es gibt fünf zusätzliche Methoden, auf die über das **mediaCollection-Objekt** zugegriffen werden kann, die ein **Playlist-Objekt** zurückgeben. Mit jeder Methode können Sie das Objekt basierend auf bestimmten Kriterien wie Genre oder Album abrufen.

Die hierarchische Struktur des Windows Media Player 7 oder höher ActiveX-Steuerelementobjektmodells bietet einen logischeren Ansatz zum Organisieren der Eigenschaften, Methoden und Ereignisse, die für Ihre Verwendung verfügbar sind. Alle Funktionen für die Player-Steuerelemente sind im **Controls-Objekt** enthalten, alle Funktionen für die Player-Netzwerkverbindung sind im **Network-Objekt** enthalten usw. Um beispielsweise mit dem Objektmodell der Version 6.4 mit der Wiedergabe von Inhalten zu beginnen, verwenden Sie die **Player6.Play-Methode:**


```C++
WMP64.Play();

```



Wenn Sie das Windows Media Player 7 oder höher verwenden, müssen Sie mithilfe des **Controls-Objekts** auf die **Play-Methode** zugreifen:


```C++
WMP9.controls.play();

```



Die Tiefe des Objektmodells kann jedoch zu sehr langen Skript-Anweisungen führen:


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Anweisungen wie die vorherige können durch die Arbeit mit einzelnen benannten Objekten wesentlich einfacher und besser lesbar gemacht werden. Im folgenden Beispiel wird die vorangehende Code-Anweisung durch Syntax ersetzt, indem separate Objektvariablen verwendet werden:


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



Dieser Codierungsstil erfordert mehr Skriptzeilen, ist aber viel einfacher zu befolgen, insbesondere mit den hinzugefügten Kommentaren. Es gibt einen weiteren Vorteil: Das **currentPlaylist-Objekt** ist einfach wiederzuverwenden, da es in der Variablen pl gespeichert ist.

Viele der Eigenschaften, Methoden und Ereignisse im Windows Media Player 7- oder höher-Objektmodell legen im Vergleich zur entsprechenden Funktionalität im Objektmodell der Version 6.4 unterschiedliche Werte fest oder rufen unterschiedliche Werte ab oder geben Werte eines anderen Typs oder einer anderen Zahl zurück. Wenn **Player6.openState** beispielsweise 2 abruft, entspricht dieser Wert der Visual Basic-Konstante **nsLoadingNSC,** was bedeutet, dass der Player eine Stationsdatei mit der Dateierweiterung NSC lädt. Wenn die Windows Media Player 7- oder höher-Objektmodelleigenschaft **Player.openState** jedoch 2 abruft, entspricht dieser Wert dem Status PlaylistLocating, was bedeutet, dass Windows Media Player versucht, eine Wiedergabeliste zu finden. Darüber hinaus kann die **Player6.openState-Eigenschaft** sieben verschiedene Werte abrufen, während die Windows Media Player 7 oder höher **Player.openState** 22 verschiedene Werte abrufen kann. Lesen Sie unbedingt den Abschnitt Objektmodellreferenz für Die Skripterstellung des Windows Media Player SDK, wenn Sie Code für die Verwendung einer anderen Objektmodellversion über überarbeitet haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Leitfaden zur Objektmodellmigration**](object-model-migration-guide.md)
</dt> </dl>

 

 




