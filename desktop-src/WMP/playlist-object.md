---
title: Wiedergabelistenobjekt
description: Das Playlist-Objekt bietet eine Möglichkeit zum Organisieren von Medienelementen in einer Liste zur einfachen Bearbeitung mithilfe der folgenden Eigenschaften und Methoden.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Wiedergabelistenobjekt-Windows Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0709b24779d3aac90d496b38b4654596479ad7a9122660158b53b4b2e75ba622
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336718"
---
# <a name="playlist-object"></a>Wiedergabelistenobjekt

Das **Playlist-Objekt** bietet eine Möglichkeit zum Organisieren von Medienelementen in einer Liste zur einfachen Bearbeitung mithilfe der folgenden Eigenschaften und Methoden.

Das **Playlist-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                      | Beschreibung                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | Ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind. |
| [Attributename](playlist-attributename.md)   | Ruft den Namen eines Attributs ab, das von einem Index angegeben wird.        |
| [count](playlist-count.md)                   | Ruft die Anzahl der Elemente in der Wiedergabeliste ab.                   |
| [name](playlist-name.md)                     | Gibt den Namen der Wiedergabeliste an oder ruft sie ab.                 |



 

Das **Playlist-Objekt** unterstützt die folgenden Methoden.



| Methode                                  | Beschreibung                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Fügt am Ende der Wiedergabeliste ein Medienelement hinzu.                                                          |
| **Löschen**                               | Für die zukünftige Verwendung reserviert.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Ruft den Wert eines Wiedergabelistenattributs ab.                                                           |
| [insertItem](playlist-insertitem.md)   | Fügt ein Medienelement an der angegebenen Position in die Wiedergabeliste ein.                                      |
| [isIdentical](playlist-isidentical.md) | Ruft einen Wert ab, der angibt, ob das **angegebene Playlist-Objekt** mit dem aktuellen identisch ist. |
| [item](playlist-item.md)               | Ruft das Medienelement am angegebenen Index ab.                                                       |
| [moveItem](playlist-moveitem.md)       | Ändert den Speicherort eines Elements in der Wiedergabeliste.                                                       |
| [removeItem](playlist-removeitem.md)   | Entfernt das angegebene Element aus der Wiedergabeliste.                                                          |
| [setItemInfo](playlist-setiteminfo.md) | Gibt den Wert eines Wiedergabelistenattributs an.                                                           |



 

Der Zugriff auf das **Playlist-Objekt** erfolgt über die folgenden Eigenschaften und Methoden.



| Object                                              | Eigenschaft oder Methode                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cdrom](cdrom-object.md)                           | [Playlist](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [MediaCollection](mediacollection-object.md)       | [getAll](mediacollection-getall.md), [getByAuth](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md) |
| [Player](player-object.md)                         | [currentPlaylist,](player-currentplaylist.md) [newPlaylist](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [PlaylistCollection](playlistcollection-object.md) | [newPlaylist](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Da es sich um die gängigste Zugriffsberechtigung handelt, *player*. **currentPlaylist** wird zur Veranschaulichung in den Abschnitten zur Referenzsyntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




