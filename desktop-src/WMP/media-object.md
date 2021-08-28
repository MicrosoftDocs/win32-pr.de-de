---
title: Medienobjekt
description: Das Medienobjekt bietet eine Möglichkeit zum Angeben oder Abrufen von Eigenschaften eines Medienelements mithilfe der folgenden Eigenschaften und Methoden.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Medienobjekt-Windows Media Player
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c1dbcb3dc662a431f279e03697620b80c242c99eb32e3bbcdc26d71796f7e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123310"
---
# <a name="media-object"></a>Medienobjekt

Das **Medienobjekt** bietet eine Möglichkeit zum Angeben oder Abrufen von Eigenschaften eines Medienelements mithilfe der folgenden Eigenschaften und Methoden.

Das **Media-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                         | Beschreibung                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [attributeCount](media-attributecount.md)       | Ruft die Anzahl der Attribute ab, die für das Medienelement abgefragt und/oder festgelegt werden können.              |
| [duration](media-duration.md)                   | Ruft die Dauer des aktuellen Medienelements in Sekunden ab.                                       |
| [durationString](media-durationstring.md)       | Ruft einen **Zeichenfolgenwert** ab, der die Dauer des aktuellen Medienelements im HH:MM:SS-Format angibt. |
| [error](media-error.md)                         | Ruft ein [ErrorItem-Objekt](erroritem-object.md) ab, wenn das Medienelement eine Fehlerbedingung aufweist.    |
| [imageSourceHeight](media-imagesourceheight.md) | Ruft die Höhe des aktuellen Medienelements in Pixel ab.                                          |
| [imageSourceWidth](media-imagesourcewidth.md)   | Ruft die Breite des aktuellen Medienelements in Pixel ab.                                           |
| [markerCount](media-markercount.md)             | Ruft die Anzahl der Marker im Medienelement ab.                                                 |
| [name](media-name.md)                           | Gibt den Namen des Medienelements an oder ruft diesen ab.                                                 |
| [sourceURL](media-sourceurl.md)                 | Ruft die URL des Medienelements ab.                                                               |



 

Das **Media-Objekt** unterstützt die folgenden Methoden.



| Methode                                                       | Beschreibung                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](media-getattributecountbytype.md) | Ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.            |
| [getAttributeName](media-getattributename.md)               | Ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.                                |
| [getItemInfo](media-getiteminfo.md)                         | Ruft den Wert des angegebenen Attributs für das Medienelement ab.                                       |
| [getItemInfoByAtom](media-getiteminfobyatom.md)             | Ruft den Wert des Attributs mit der angegebenen Indexnummer ab.                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | Ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht. |
| [getMarkerName](media-getmarkername.md)                     | Ruft den Namen des Markers am angegebenen Index ab.                                                 |
| [getMarkerTime](media-getmarkertime.md)                     | Ruft die Zeit des Markers am angegebenen Index ab.                                                 |
| [isIdentical](media-isidentical.md)                         | Ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.                 |
| [isMemberOf](media-ismemberof.md)                           | Ruft einen Wert ab, der angibt, ob das angegebene Medienelement ein Member der angegebenen Wiedergabeliste ist.     |
| [isReadOnlyItem](media-isreadonlyitem.md)                   | Ruft einen Wert ab, der angibt, ob die Attribute des angegebenen Medienelements bearbeitet werden können.           |
| [setItemInfo](media-setiteminfo.md)                         | Legt den Wert des angegebenen Attributs für das Medienelement fest.                                            |



 

Der Zugriff auf das **Medienobjekt** erfolgt über die folgenden Eigenschaften und Methoden.



| Object                          | Eigenschaft oder Methode                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [Steuerelemente](controls-object.md) | [Currentitem](controls-currentitem.md)                                  |
| [Player](player-object.md)     | [currentMedia,](player-currentmedia.md) [newMedia](player-newmedia.md) |
| [Wiedergabeliste](playlist-object.md) | [item](playlist-item.md)                                                |



 

Da dies die gängigste Zugriffshilfe ist, *player*. **currentMedia** wird zur Veranschaulichung in den Abschnitten zur Referenzsyntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodellreferenz für Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




