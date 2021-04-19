---
title: Iwmpmediacollection-Schnittstelle (VB und C) (WMP. h)
description: Stellt Methoden bereit, die verwendet werden können, um eine große Auflistung von Medien Elementen zu organisieren.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- Iwmpmediacollection (VB und C) Interface Windows Media Player
- Iwmpmediacollection (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370945"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>Iwmpmediacollection-Schnittstelle (VB und c#)

Stellt Methoden bereit, die verwendet werden können, um eine große Auflistung von Medien Elementen zu organisieren.

## <a name="members"></a>Member

Die **iwmpmediacollection-Schnittstelle (VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmpmediacollection-Schnittstelle (VB und c#)** verfügt über diese Methoden.



| Methode                                                                                                                       | BESCHREIBUNG                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | Fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.<br/>                                                                                  |
| [**"GetAll"**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die der Wiedergabeliste entspricht, die alle Medienelemente in der Bibliothek enthält.<br/>               |
| [**getAttributeStringCollection**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | Gibt eine **iwmpstringcollection** -Schnittstelle zurück, die den Satz aller Werte für ein angegebenes Attribut innerhalb eines Medientyps darstellt.<br/> |
| [**getbyalbum**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente aus dem angegebenen Album ermöglicht.<br/>                                |
| [**getbyattribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.<br/>                      |
| [**getbyauthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf die Medienelemente durch den angegebenen Autor ermöglicht.<br/>                             |
| [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente des angegebenen Genres ermöglicht.<br/>                                  |
| [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente mit dem angegebenen Namen ermöglicht.<br/>                                 |
| [**getmediaatom**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | Gibt den Index eines angegebenen Attributs zurück.<br/>                                                                                        |
| **isDeleted**                                                                                                                | Wird nicht mehr unterstützt.<br/>                                                                                                               |
| [**aufgeh**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | Entfernt das angegebene Medien Element aus der Medien Auflistung.<br/>                                                                        |
| [**SetDeleted**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | Verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".<br/>                                                                        |



 

Sie erhalten eine **iwmpmediacollection** -Schnittstelle mit den folgenden Eigenschaften, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird.



| Objekt oder Schnittstelle                                               | Eigenschaft                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**Iwmplibrary**](iwmplibrary--vb-and-c.md)                      | [**mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2-Schnittstelle**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpstringcollection-Schnittstelle (VB und c#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





