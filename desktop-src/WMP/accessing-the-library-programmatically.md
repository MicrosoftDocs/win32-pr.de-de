---
title: Programm gesteuerter Zugriff auf die Bibliothek
description: Programm gesteuerter Zugriff auf die Bibliothek
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player-Bibliothek, zugreifen auf Programm gesteuert
- Bibliothek, zugreifen
- Programm gesteuerter Zugriff auf die Windows Media Player-Bibliothek
- Windows Media Player-Bibliothek, Hinzufügen von Medien Elementen
- Bibliothek, Hinzufügen von Medien Elementen
- Windows Media Player-Bibliothek, Abrufen von Medien Elementen
- Bibliothek, Abrufen von Medien Elementen
- Windows Media Player-Bibliothek, Entfernen von Medien Elementen
- Bibliothek, Entfernen von Medien Elementen
- Hinzufügen von Medien Elementen zur Windows-Media Player Bibliothek
- Abrufen von Medien Elementen aus der Windows Media Player-Bibliothek
- Entfernen von Medien Elementen aus der Windows Media Player-Bibliothek
- Abrufen von Metadaten
- Windows Media Player-Bibliothek, Abrufen von Metadaten von Medien Elementen
- Bibliothek, Abrufen von Metadaten von Medien Elementen
- Metadaten, Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388513"
---
# <a name="accessing-the-library-programmatically"></a>Programm gesteuerter Zugriff auf die Bibliothek

Im Code wird die Bibliothek durch das **mediacollection** -Objekt (oder die **iwmpmediacollection** -Schnittstelle) dargestellt. Medienelemente werden als **Medien** Objekte (oder von der **iwmpmedia** -Schnittstelle) dargestellt. Wiedergabelisten Elemente werden als **Wiedergabe** Listen Objekte dargestellt (oder von der **iwmpwiedergabe** -Schnittstelle). Der Einfachheit halber wird in diesem Abschnitt nach Möglichkeit nur auf Objektnamen verwiesen.

Mithilfe des **mediacollection** -Objekts können Sie mit Medien Elementen und-Wiedergabelisten arbeiten. Die Bibliothek macht auch das **playlistcollection** -Objekt (oder die **iwmpplaylistcollection** -Schnittstelle) verfügbar, das einige Funktionen bereitstellt, die für die Arbeit mit Wiedergabelisten spezifisch sind. In den meisten Fällen stellt das **mediacollection** -Objekt Ihnen die erforderliche Funktionalität zur Verfügung, auch wenn Sie mit Wiedergabelisten arbeiten. Weitere Informationen zum Arbeiten mit Medien Elementen finden Sie unter [Verwalten von Medien Elementen](managing-media-items.md). Weitere Informationen zum Arbeiten mit Wiedergabelisten finden Sie unter [Verwalten von Wiedergabe](managing-playlists.md)Listen.

## <a name="adding-media-items-to-the-library"></a>Hinzufügen von Medien Elementen zur Bibliothek

Das Hinzufügen digitaler Medieninhalte zur Bibliothek ist einfach. Nennen Sie einfach die [mediacollection. Add](mediacollection-add.md) -Methode, und geben Sie den Pfad zur Mediendatei als Argument an.

## <a name="retrieving-media-items-from-the-library"></a>Abrufen von Medien Elementen aus der Bibliothek

Wenn Sie Medienelemente aus der Bibliothek abrufen, ist das, was Sie wirklich abrufen, eine Wiedergabeliste. Auch wenn Sie davon ausgehen, dass nur ein Medien Element abgerufen wird, erhalten Sie ein **Wiedergabe** Listen Objekt, das ein einzelnes Element enthält, das mit dem Index 0 (null) verknüpft wird. Wenn Sie z. b. ein **Medien** Objekt mit dem Namen "Jeanne" abrufen möchten, können Sie den folgenden JScript-Code verwenden:


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



Der vorangehende Code Ruft eine Wiedergabeliste ab, die alle Medienelemente mit dem Namen "Jeanne" als Titel enthält. Nehmen Sie für dieses Beispiel an, dass Sie wissen, dass es in der Bibliothek nur einen Song mit diesem Namen gibt (Beachten Sie, dass die Bibliothek mehrere Lieder mit dem gleichen Namen unterstützt). Dies bedeutet, dass Sie erwarten können, dass die Anzahl der Elemente in der Wiedergabeliste, die Sie abgerufen haben, gleich 1 ist, und dass das Medien Element durch Index NULL dargestellt wird. Im folgenden Beispielcode wird das vorherige Beispiel fortgesetzt, um zu veranschaulichen, wie Sie das Medien Element mithilfe der [Wiedergabe. Item](playlist-item.md) -Methode aus der Wiedergabeliste abrufen.


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Weitere Informationen zum Abrufen von Medien Elementen aus Wiedergabelisten finden Sie unter [Wiedergabelisten und Medienelemente](playlists-and-media-items.md) im [Player-Steuerelement Handbuch](player-control-guide.md).

## <a name="retrieving-metadata-from-a-media-item"></a>Abrufen von Metadaten aus einem Medien Element

Nachdem Sie ein **Medien** Objekt abgerufen haben, können Sie die dem Inhalt zugeordneten Attributwerte lesen. Im einfachsten Fall möchten Sie vielleicht nur einen einzelnen Wert kennen, z. b. den Namen des Künstlers, der einen Musiktitel durchgeführt hat. Im folgenden JScript-Beispiel wird gezeigt, wie die [Media. getiteminfo](media-getiteminfo.md) -Methode verwendet wird, um den Namen des Künstlers aus den im vorherigen Beispiel abgerufenen Medien abzurufen:


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Ein Medien Element kann über viele verschiedene Attribute verfügen, und die Arbeit mit Metadaten ist nicht immer so einfach wie die im vorherigen Beispiel gezeigte einfache groß-und Kleinschreibung. Beispielsweise können einige Attribute mehrere Werte enthalten oder Werte in mehr als einer Sprache aufweisen. Weitere Informationen zum Arbeiten mit Metadaten finden Sie unter [Medien Element Attribute](media-item-attributes.md). Weitere Informationen zu den verschiedenen Attributen, deren Bedeutungen und Dateityp Unterstützung finden Sie in der [Attribut Referenz](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Entfernen von Medien Elementen aus der Bibliothek

Das Entfernen digitaler Medieninhalte aus der Bibliothek ist ebenfalls unkompliziert. Nennen Sie einfach " **mediacollection. Remove**", und stellen Sie das **Medien** Objekt, das das Element darstellt, als erstes Argument und den Wert " **true** " als zweiten dar. Im folgenden JScript-Beispiel wird die Datei mit dem Namen "Jeanne (im vorherigen Beispiel abgerufen)" aus der Bibliothek entfernt:


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Bibliothek**](about-the-library.md)
</dt> <dt>

[**Informationen zu mediacollection und Media Objects**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 




