---
title: StringCollection-Objekt
description: Das StringCollection-Objekt bietet eine Möglichkeit, eine Auflistung von Zeichen folgen zu bearbeiten.
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- StringCollection-Objekt, Windows Media Player
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313248"
---
# <a name="stringcollection-object"></a>StringCollection-Objekt

Das **StringCollection** -Objekt bietet eine Möglichkeit, eine Auflistung von Zeichen folgen zu bearbeiten.

Das **StringCollection** -Objekt unterstützt die folgende Eigenschaft.



| Eigenschaft                            | BESCHREIBUNG                                             |
|-------------------------------------|---------------------------------------------------------|
| [count](stringcollection-count.md) | Ruft die Anzahl der Elemente in der Zeichen folgen Auflistung ab. |



 

Das **StringCollection** -Objekt unterstützt die folgenden Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [getattributecountrytbytype](stringcollection-getattributecountbytype.md) | Ruft die Anzahl der Attribute ab, die dem angegebenen **StringCollection** -Element Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind. |
| [getItemInfo](stringcollection-getiteminfo.md)                         | Ruft die Zeichenfolge ab, die dem angegebenen **StringCollection** -Element Index und dem angegebenen Namen entspricht.                                   |
| [getItemInfoByType](stringcollection-getiteminfobytype.md)             | Ruft die Zeichenfolge ab, die dem angegebenen Index der **StringCollection** -Elemente, dem Namen, der Sprache und dem Attribut Index entspricht.       |
| [isidentical](stringcollection-isidentical.md)                         | Ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.                                        |
| [item](stringcollection-item.md)                                       | Ruft die Zeichenfolge am angegebenen Index ab.                                                                                    |



 

Der Zugriff auf das **StringCollection** -Objekt erfolgt über die folgende Methode.



| Object                                        | Methode                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [Mediacollection](mediacollection-object.md) | [getAttributeStringCollection](mediacollection-getattributestringcollection.md) |



 

Dient zur Veranschaulichung des *Players*. *mediacollection*. **getAttributeStringCollection**(*Attribut*, *mediaType*) wird in den Abschnitten der Verweis Syntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




