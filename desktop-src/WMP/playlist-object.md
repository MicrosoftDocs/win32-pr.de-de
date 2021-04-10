---
title: Wiedergabelisten Objekt
description: Das Wiedergabelisten Objekt bietet eine Möglichkeit, Medienelemente in einer Liste zu organisieren, um eine einfache Bearbeitung mithilfe der folgenden Eigenschaften und Methoden zu ermöglichen.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Wiedergabelisten Objekt-Fenster Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037762"
---
# <a name="playlist-object"></a>Wiedergabelisten Objekt

Das **Wiedergabe** Listen Objekt bietet eine Möglichkeit, Medienelemente in einer Liste zu organisieren, um eine einfache Bearbeitung mithilfe der folgenden Eigenschaften und Methoden zu ermöglichen.

Das **Wiedergabe** Listen Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                      | BESCHREIBUNG                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [AttributeCount](playlist-attributecount.md) | Ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind. |
| [AttributeName](playlist-attributename.md)   | Ruft den Namen eines durch einen Index angegebenen Attributs ab.        |
| [count](playlist-count.md)                   | Ruft die Anzahl der Elemente in der Wiedergabeliste ab.                   |
| [name](playlist-name.md)                     | Gibt den Namen der Wiedergabeliste an oder ruft ihn ab.                 |



 

Das **Wiedergabe** Listen Objekt unterstützt die folgenden Methoden.



| Methode                                  | BESCHREIBUNG                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Fügt ein Medien Element am Ende der Wiedergabeliste hinzu.                                                          |
| **Löschen**                               | Für die zukünftige Verwendung reserviert.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Ruft den Wert eines Wiedergabelisten Attributs ab.                                                           |
| [insertItem](playlist-insertitem.md)   | Fügt ein Medien Element an der angegebenen Position in die Wiedergabeliste ein.                                      |
| [isidentical](playlist-isidentical.md) | Ruft einen Wert ab, der angibt, ob das angegebene **Wiedergabe** Listen Objekt mit dem aktuellen-Objekt identisch ist. |
| [item](playlist-item.md)               | Ruft das Medien Element am angegebenen Index ab.                                                       |
| ["muveitem"](playlist-moveitem.md)       | Ändert die Position eines Elements in der Wiedergabeliste.                                                       |
| [RemoveItem](playlist-removeitem.md)   | Entfernt das angegebene Element aus der Wiedergabeliste.                                                          |
| ["Einstellungs Element"](playlist-setiteminfo.md) | Gibt den Wert eines Wiedergabelisten Attributs an.                                                           |



 

Der Zugriff auf das **Wiedergabe** Listen Objekt erfolgt über die folgenden Eigenschaften und Methoden.



| Object                                              | Eigenschaft oder Methode                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rom](cdrom-object.md)                           | [Abspielen](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [Mediacollection](mediacollection-object.md)       | [GetAll](mediacollection-getall.md), [getbyalbum](mediacollection-getbyalbum.md), [getbyattribute](mediacollection-getbyattribute.md), [getbyauthor](mediacollection-getbyauthor.md), [getbygenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md) |
| [Player](player-object.md)                         | [currentwiedergabe](player-currentplaylist.md), [newwiedergabe](player-newplaylist.md)                                                                                                                                                                                               |
| [Playlistarray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [Playlistcollection](playlistcollection-object.md) | [neue](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Da es sich um die gängigste Zugriffsmethode handelt, ist der *Player*. **currentwiedergabe** wird zur Veranschaulichung in den Abschnitten der Referenz Syntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




