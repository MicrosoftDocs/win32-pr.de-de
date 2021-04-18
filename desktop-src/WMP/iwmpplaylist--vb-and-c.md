---
title: IWMPPlaylist (VB und C )-Schnittstelle (Wmp.h)
description: Stellt Eigenschaften und Methoden bereit, um Medienelemente in einer Wiedergabeliste zu organisieren, zu verwalten und zu bearbeiten. Die iwmpwiedergabe-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- Media Player der iwmpwiedergabe-Schnittstelle (VB und C)
- Windows Media Player der iwmpwiedergabe-Schnittstelle (VB und C), beschrieben
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365669"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>Iwmpwiedergabe-Schnittstelle (VB und c#)

Stellt Eigenschaften und Methoden bereit, um Medienelemente in einer Wiedergabeliste zu organisieren, zu verwalten und zu bearbeiten.

Die **iwmpwiedergabe** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmpwiedergabe-Schnittstelle (VB und c#)** verfügt über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmpwiedergabe-Schnittstelle (VB und c#)** verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Fügt ein Medien Element am Ende der Wiedergabeliste hinzu.<br/>                |
| [**Klartext**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Für die zukünftige Verwendung reserviert.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Gibt den Wert eines durch den Namen angegebenen Wiedergabelisten Attributs zurück.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Fügt ein Medien Element an einem angegebenen Speicherort in eine Wiedergabeliste ein.<br/>  |
| [**"muveitem"**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Ändert den Speicherort eines Medien Elements in der Wiedergabeliste.<br/>        |
| [**RemoveItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Entfernt das angegebene Medien Element aus der Wiedergabeliste.<br/>          |
| [**"Einstellungs Element"**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Legt den Wert eines Wiedergabelisten Attributs fest.<br/>                      |



 

### <a name="properties"></a>Eigenschaften

Die **iwmpwiedergabe-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp           | BESCHREIBUNG                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft die Anzahl der einer Wiedergabeliste zugeordneten Attribute ab.<br/>                                                                                |
| [**AttributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Schreibgeschützt<br/>  | Ruft den Namen eines durch einen Index angegebenen Wiedergabelisten Attributs ab. In c# ist dies die get \_ attributeName-Methode.<br/>                               |
| [**Countdown**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Schreibgeschützt<br/>  | Ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.<br/>                                                                                            |
| [**isidentical**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob die angegebene Wiedergabeliste mit der aktuellen Wiedergabeliste identisch ist. In c# ist dies die get \_ isidentical-Methode.<br/> |
| [**Element**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Schreibgeschützt<br/>  | Ruft eine Schnittstelle zum Medien Element am angegebenen Index ab. In c# ist dies die get \_ Item-Methode.<br/>                                         |
| [**Benennen**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Lesen/Schreiben<br/> | Ruft den Namen der Wiedergabeliste ab oder legt ihn fest.<br/>                                                                                                   |



 

Abrufen einer **iwmpwiedergabe** -Schnittstelle mithilfe der folgenden Eigenschaften oder Methoden, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird.



| Objekt oder Schnittstelle                                                | Eigenschaft oder Methode                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmpcdrom**](iwmpcdrom--vb-and-c.md)                           | [**Abspielen**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**Iwmpmediacollection**](iwmpmediacollection--vb-and-c.md)       | [**GetAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getbyalbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getbyattribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getbyauthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getbygenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentwiedergabe**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **newwiedergabe**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**Iwmpplaylistarray**](iwmpplaylistarray--vb-and-c.md)           | [**Element**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Iwmpplaylistcollection**](iwmpplaylistcollection--vb-and-c.md) | [**neue**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





