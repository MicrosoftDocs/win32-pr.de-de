---
title: IWMPMedia-Schnittstelle (VB und C ) (Wmp.h)
description: Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medienelements. Die IWMPMedia-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia-Schnittstelle (VB und C) Windows Media Player
- IWMPMedia-Schnittstelle (VB und C) Windows Media Player , beschrieben
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
ms.openlocfilehash: 8d36fc2a7c4f65856b68c00147e32f9b3af4cc3e649a9717e7734583d4516b44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572460"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>IWMPMedia-Schnittstelle (VB und C#)

Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medienelements.

Die **IWMPMedia-Schnittstelle** macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPMedia-Schnittstelle (VB und C#)** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPMedia-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                             | Beschreibung                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**getAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Gibt den Wert des angegebenen Attributs für das Medienelement zurück.<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.<br/>                                |
| [**getMarkerName**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Gibt den Namen des Markers am angegebenen Index zurück.<br/>                                             |
| [**getMarkerTime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Gibt die Zeit des Markers am angegebenen Index zurück.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Gibt einen Wert zurück, der angibt, ob das angegebene Medienelement ein Element der angegebenen Wiedergabeliste ist.<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Gibt einen Wert zurück, der angibt, ob die Attribute des angegebenen Medienelements bearbeitet werden können.<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Legt den Wert des angegebenen Attributs für das Medienelement fest.<br/>                                      |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPMedia-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp          | Beschreibung                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der Attribute ab, die für das Medienelement abgefragt und/oder festgelegt werden können.<br/>                                                          |
| [**Dauer**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Schreibgeschützt<br/> | Ruft die Dauer des aktuellen Medienelements in Sekunden ab.<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Wert ab, der die Dauer des aktuellen Medienelements im Format HH:MM:SS angibt.<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft die Höhe des aktuellen Medienelements in Pixel ab.<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Schreibgeschützt<br/> | Ruft die Breite des aktuellen Medienelements in Pixel ab.<br/>                                                                                       |
| [**isIdentical**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob das angegebene Medienelement mit dem aktuellen identisch ist. In C# ist dies die **get \_ isIdentical-Methode.**<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Schreibgeschützt<br/> | Ruft die Anzahl der Marker im Medienelement ab.<br/>                                                                                             |
| [**Namen**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Schreibgeschützt<br/> | Ruft den Namen des Medienelements ab oder legt diesen fest.<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Schreibgeschützt<br/> | Ruft die URL des Medienelements ab.<br/>                                                                                                           |



 

Verwenden Sie die folgenden Eigenschaften oder Methoden, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird, um eine **IWMPMedia-Schnittstelle** zu erhalten.



| Objekt oder Schnittstelle                                               | Eigenschaft oder Methode                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**Currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia,**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [**Item**](iwmpplaylist-item--vb-and-c.md) (element \_ in C#)                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMedia2-Schnittstelle (VB und C#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3-Schnittstelle (VB und C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





