---
title: Medienobjekt
description: Das Medienobjekt bietet eine Möglichkeit zum angeben oder Abrufen von Eigenschaften eines Medien Elements mithilfe der folgenden Eigenschaften und Methoden.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Windows-Media Player für Medienobjekte
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341277"
---
# <a name="media-object"></a>Medienobjekt

Das **Medien** Objekt bietet eine Möglichkeit zum angeben oder Abrufen von Eigenschaften eines Medien Elements mithilfe der folgenden Eigenschaften und Methoden.

Das **Medien** Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                         | BESCHREIBUNG                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [AttributeCount](media-attributecount.md)       | Ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.              |
| [duration](media-duration.md)                   | Ruft die Dauer des aktuellen Medien Elements in Sekunden ab.                                       |
| [durationString](media-durationstring.md)       | Ruft einen **Zeichen** folgen Wert ab, der die Dauer des aktuellen Medien Elements im Format "hh: mm: SS" angibt. |
| [error](media-error.md)                         | Ruft ein [ErrorItem](erroritem-object.md) -Objekt ab, wenn das Medien Element einen Fehlerzustand aufweist.    |
| [imagesourceheight](media-imagesourceheight.md) | Ruft die Höhe des aktuellen Medien Elements in Pixel ab.                                          |
| [imagesourcewidth](media-imagesourcewidth.md)   | Ruft die Breite des aktuellen Medien Elements in Pixel ab.                                           |
| [markercount](media-markercount.md)             | Ruft die Anzahl der Marker im Medien Element ab.                                                 |
| [name](media-name.md)                           | Gibt den Namen des Medien Elements an oder ruft ihn ab.                                                 |
| [SourceURL](media-sourceurl.md)                 | Ruft die URL des Medien Elements ab.                                                               |



 

Das **Medien** Objekt unterstützt die folgenden Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getattributecountrytbytype](media-getattributecountbytype.md) | Ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der Sprache zugeordnet sind.            |
| [GetAttributeName](media-getattributename.md)               | Ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.                                |
| [getItemInfo](media-getiteminfo.md)                         | Ruft den Wert des angegebenen Attributs für das Medien Element ab.                                       |
| [getiteminfobyatom](media-getiteminfobyatom.md)             | Ruft den Wert des Attributs mit der angegebenen Indexnummer ab.                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | Ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht. |
| [getmarkername](media-getmarkername.md)                     | Ruft den Namen des Markers am angegebenen Index ab.                                                 |
| [getmarkertime](media-getmarkertime.md)                     | Ruft die Zeit des Markers am angegebenen Index ab.                                                 |
| [isidentical](media-isidentical.md)                         | Ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.                 |
| [isMemberOf](media-ismemberof.md)                           | Ruft einen Wert ab, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.     |
| [isread onlyitem](media-isreadonlyitem.md)                   | Ruft einen Wert ab, der angibt, ob die Attribute des angegebenen Medien Elements bearbeitet werden können.           |
| ["Einstellungs Element"](media-setiteminfo.md)                         | Legt den Wert des angegebenen Attributs für das Medien Element fest.                                            |



 

Der Zugriff auf das **Medien** Objekt erfolgt über die folgenden Eigenschaften und Methoden.



| Object                          | Eigenschaft oder Methode                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [Steuerelemente](controls-object.md) | [currentItem](controls-currentitem.md)                                  |
| [Player](player-object.md)     | [currentMedia](player-currentmedia.md), [newmedia](player-newmedia.md) |
| [Abspielen](playlist-object.md) | [item](playlist-item.md)                                                |



 

Da es sich um die gängigste Zugriffsmethode handelt, ist der *Player*. **currentMedia** wird zur Veranschaulichung in den Abschnitten der Referenz Syntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




