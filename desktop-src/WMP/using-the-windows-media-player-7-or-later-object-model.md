---
title: Verwenden des Objektmodells Windows Media Player 7 oder höher
description: Verwenden des Objektmodells Windows Media Player 7 oder höher
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player-Objektmodell, Version 7 oder höher
- Objektmodell, Version 7 oder höher
- Windows Media Player ActiveX-Steuerelement, Version 7 oder höher
- ActiveX-Steuerelement, Version 7 oder höher
- Windows Media Player Mobile ActiveX-Steuerelement, Version 7 oder höher
- Windows Media Player Mobile, Objektmodell
- Migrations Handbuch, Version 7 oder höher
- Versionen von Windows Media Player, Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310395"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Verwenden des Objektmodells Windows Media Player 7 oder höher

Die meisten Aufgaben, die Sie möglicherweise mit dem Windows Media Player 6,4-ActiveX-Steuerelement Objektmodell durchgeführt haben, erfordern einen neuen Ansatz. In vielen Fällen haben sich die Namen der Eigenschaften, Methoden und Ereignisse im Objektmodell Windows Media Player 7 oder höher geändert. Um beispielsweise den Dateipfad im Objektmodell der Version 6,4 anzugeben, legen Sie die **Player6. filename** -Eigenschaft fest:


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden, müssen Sie die Eigenschaft **Player. URL** festlegen:


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



Alternativ können Sie das 10-Objektmodell verwenden, indem Sie ein **Medien** Objekt aus der Bibliothek abrufen und dann die Eigenschaft **Player. currentMedia** festlegen:


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Der Zugriff auf einen Großteil der Funktionen des Objektmodells Windows Media Player 7 oder höher erfolgt über die Objekthierarchie. Wie im vorherigen Beispiel gezeigt, können Sie ein **Wiedergabe** Listen Objekt mithilfe der **GetAll** -Methode des **mediacollection** -Objekts abrufen, auf das über das root **Player** -Objekt zugegriffen wird. Sie können dann mithilfe der **Item** -Methode des **Wiedergabe** Listen Objekts ein bestimmtes **Medien** Objekt aus dem **Wiedergabe** Listen Objekt abrufen. Es gibt fünf zusätzliche Methoden, auf die über das **mediacollection** -Objekt zugegriffen werden kann, die ein **Wiedergabe** Listen Objekt zurückgeben mit jeder Methode können Sie das Objekt auf der Grundlage spezifischer Kriterien abrufen, z. b. Genre oder Album.

Die hierarchische Struktur des ActiveX-Steuerelement Objektmodells Windows Media Player 7 oder höher bietet einen logischeren Ansatz zum Organisieren der Eigenschaften, Methoden und Ereignisse, die für ihre Verwendung verfügbar sind. Alle Funktionen für die Player-Steuerelemente sind im Steuer **Element Objekt enthalten** , die gesamte Funktionalität für die Player-Netzwerkverbindung ist im **Netzwerk** Objekt enthalten usw. Um beispielsweise die Wiedergabe von Inhalten mit dem Objektmodell der Version 6,4 zu starten, verwenden Sie die **Player6. Play** -Methode:


```C++
WMP64.Play();

```



Wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden, müssen Sie über das Steuerelement **-Objekt auf** die **Play** -Methode zugreifen:


```C++
WMP9.controls.play();

```



Die Tiefe des Objektmodells kann jedoch zu sehr langen Skript Anweisungen führen:


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Anweisungen wie die vorherige können viel einfacher und lesbarer werden, indem Sie mit einzelnen benannten Objekten arbeiten. Im folgenden Beispiel wird die vorherige Code Anweisung durch Syntax unter Verwendung separater Objektvariablen ersetzt:


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



Dieser Codierungsstil erfordert mehr Skript Zeilen, ist jedoch viel leichter zu befolgen, insbesondere mit den hinzugefügten Kommentaren. Es gibt einen weiteren Vorteil: das **currentwiedergabe** -Objekt ist leicht wiederzuverwenden, da es in der Variablen "pl" gespeichert ist.

Viele der Eigenschaften, Methoden und Ereignisse im Objektmodell Windows Media Player 7 oder höher legen unterschiedliche Werte fest oder rufen Werte eines anderen Typs oder einer anderen Zahl ab, und zwar im Vergleich zu den entsprechenden Funktionen im Objektmodell der Version 6,4. Wenn **Player6. openstate** beispielsweise 2 abruft, entspricht dieser Wert der Visual Basic Konstante **nsloadingnsc**. Dies bedeutet, dass der Spieler eine Stations Datei mit der Dateinamenerweiterung ". NSC" lädt. Wenn jedoch die Eigenschaften **Player. openstate** von Windows Media Player 7 oder höher den objektmodelltyp 2 abruft, entspricht dieser Wert dem Status playlistlocate, d. h., Windows Media Player versucht, eine Wiedergabeliste zu finden. Darüber hinaus können mit der **Player6. openstate** -Eigenschaft sieben verschiedene Werte abgerufen werden, während die Windows Media Player 7-oder spätere **Player. openstate** -Eigenschaft 22 verschiedene Werte abrufen kann. Achten Sie darauf, dass Sie im Abschnitt "Objektmodell Referenz für Skripterstellung" des Windows Media Player SDK nach dem Überarbeiten von Code für die Verwendung einer anderen Objektmodell Version darauf verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Handbuch für die Migration des Objektmodells**](object-model-migration-guide.md)
</dt> </dl>

 

 




