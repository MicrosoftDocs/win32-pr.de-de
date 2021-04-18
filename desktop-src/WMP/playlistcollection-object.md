---
title: Playlistcollection-Objekt
description: Das playlistcollection-Objekt bietet eine Möglichkeit zum Organisieren von Wiedergabelisten.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Playlistcollection-Objekt, Windows-Media Player
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339244"
---
# <a name="playlistcollection-object"></a>Playlistcollection-Objekt

Das **playlistcollection** -Objekt bietet eine Möglichkeit zum Organisieren von Wiedergabelisten.

Das **playlistcollection** -Objekt unterstützt die folgenden Methoden.



| Methode                                                  | BESCHREIBUNG                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ["GetAll"](playlistcollection-getall.md)                 | Ruft ein [playlistarray](playlistarray-object.md) -Objekt ab, das alle Wiedergabelisten in der Bibliothek enthält.                |
| [getByName](playlistcollection-getbyname.md)           | Ruft ein [playlistarray](playlistarray-object.md) -Objekt ab, das ggf. vorhandene Wiedergabelisten mit dem angegebenen Namen enthält. |
| [importwiedergabe Liste](playlistcollection-importplaylist.md) | Fügt der Bibliothek eine statische Wiedergabeliste hinzu.                                                                                   |
| [isDeleted](playlistcollection-isdeleted.md)           | Ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner "Gelöschte Elemente" befindet.                              |
| [neue](playlistcollection-newplaylist.md)       | Erstellt eine neue Wiedergabeliste in der Bibliothek.                                                                                   |
| [remove](playlistcollection-remove.md)                 | Entfernt eine Wiedergabeliste aus der Bibliothek.                                                                                     |
| [SetDeleted](playlistcollection-setdeleted.md)         | Verschiebt eine Wiedergabeliste in den Ordner "Gelöschte Elemente".                                                                            |



 

Der Zugriff auf das **playlistcollection** -Objekt erfolgt über die folgende Eigenschaft.



| Object                      | Eigenschaft                                            |
|-----------------------------|-----------------------------------------------------|
| [Player](player-object.md) | [playlistcollection](player-playlistcollection.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




