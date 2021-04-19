---
title: Iwmpmedia (VB und C)-Schnittstelle (WMP. h)
description: Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medien Elements. Die iwmpmedia-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- Iwmpmedia (VB und C) Interface Windows Media Player
- Iwmpmedia (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367749"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>Iwmpmedia (VB und c#)-Schnittstelle

Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medien Elements.

Die **iwmpmedia** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmpmedia-Schnittstelle (VB und c#)** verfügt über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmpmedia-Schnittstelle (VB und c#)** verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**GetAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Gibt den Wert des angegebenen Attributs für das Medien Element zurück.<br/>                                   |
| [**getiteminfobyatom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.<br/>                                |
| [**getmarkername**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Gibt den Namen des Markers am angegebenen Index zurück.<br/>                                             |
| [**getmarkertime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Gibt die Zeit des Markers am angegebenen Index zurück.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Gibt einen Wert zurück, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.<br/> |
| [**isread onlyitem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Gibt einen Wert zurück, der angibt, ob die Attribute des angegebenen Medien Elements bearbeitet werden können.<br/>       |
| [**"Einstellungs Element"**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Legt den Wert des angegebenen Attributs für das Medien Element fest.<br/>                                      |



 

### <a name="properties"></a>Eigenschaften

Die **iwmpmedia-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp          | BESCHREIBUNG                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.<br/>                                                          |
| [**auf**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Schreibgeschützt<br/> | Ruft die Dauer des aktuellen Medien Elements in Sekunden ab.<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Wert ab, der die Dauer des aktuellen Medien Elements im Format "hh: mm: SS" angibt.<br/>                                                        |
| [**imagesourceheight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft die Höhe des aktuellen Medien Elements in Pixel ab.<br/>                                                                                      |
| [**imagesourcewidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Schreibgeschützt<br/> | Ruft die Breite des aktuellen Medien Elements in Pixel ab.<br/>                                                                                       |
| [**isidentical**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob das angegebene Medien Element mit dem aktuellen Medien Element identisch ist. In c# ist dies die **get \_ isidentical** -Methode.<br/> |
| [**markercount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Schreibgeschützt<br/> | Ruft die Anzahl der Marker im Medien Element ab.<br/>                                                                                             |
| [**Benennen**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Schreibgeschützt<br/> | Ruft den Namen des Medien Elements ab oder legt ihn fest.<br/>                                                                                                  |
| [**SourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Schreibgeschützt<br/> | Ruft die URL des Medien Elements ab.<br/>                                                                                                           |



 

Abrufen einer **iwmpmedia** -Schnittstelle mithilfe der folgenden Eigenschaften oder Methoden, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird.



| Objekt oder Schnittstelle                                               | Eigenschaft oder Methode                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmpcontrols**](iwmpcontrols--vb-and-c.md)                    | [**CurrentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newmedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**Iwmpwiedergabe**](iwmpplaylist--vb-and-c.md)                    | [**Item**](iwmpplaylist-item--vb-and-c.md) ( \_ Element in c# Get)                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMedia2-Schnittstelle (VB und c#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3-Schnittstelle (VB und c#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





