---
title: IWMPMediaCollection-Schnittstelle (VB und C) (Wmp.h)
description: Stellt Methoden bereit, die verwendet werden können, um eine große Sammlung von Medienelementen zu organisieren.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- IWMPMediaCollection-Schnittstelle (VB und C) Windows Media Player
- IWMPMediaCollection-Schnittstelle (VB und C) Windows Media Player beschrieben
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
ms.openlocfilehash: ce15616b2059802610360b52d5af9bfa8d56b56b7ed06129bb849de567e22e26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468450"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>IWMPMediaCollection-Schnittstelle (VB und C#)

Stellt Methoden bereit, die verwendet werden können, um eine große Sammlung von Medienelementen zu organisieren.

## <a name="members"></a>Member

Die **IWMPMediaCollection-Schnittstelle (VB und C#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMPMediaCollection-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                                                                       | Beschreibung                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | Fügt der Bibliothek ein neues Medienelement oder eine neue Wiedergabeliste hinzu.<br/>                                                                                  |
| [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die der Wiedergabeliste entspricht, die alle Medienelemente in der Bibliothek enthält.<br/>               |
| [**getAttributeStringCollection**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | Gibt eine **IWMPStringCollection-Schnittstelle** zurück, die den Satz aller Werte für ein angegebenes Attribut innerhalb eines Medientyps darstellt.<br/> |
| [**getBy Einmal**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente aus dem angegebenen Album bietet.<br/>                                |
| [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.<br/>                      |
| [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die zugriff auf die Medienelemente durch den angegebenen Autor bereitstellt.<br/>                             |
| [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente des angegebenen Genre bereitstellt.<br/>                                  |
| [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente mit dem angegebenen Namen bietet.<br/>                                 |
| [**getMediaAtom**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | Gibt den Index eines angegebenen Attributs zurück.<br/>                                                                                        |
| **isDeleted**                                                                                                                | Wird nicht mehr unterstützt.<br/>                                                                                                               |
| [**Entfernen**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | Entfernt das angegebene Medienelement aus der Medienauflistung.<br/>                                                                        |
| [**setDeleted**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | Verschiebt das angegebene Medienelement in den Ordner für gelöschte Elemente.<br/>                                                                        |



 

Abrufen einer **IWMPMediaCollection-Schnittstelle** mithilfe der folgenden Eigenschaften, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird.



| Objekt oder Schnittstelle                                               | Eigenschaft                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**IWMPLibrary**](iwmplibrary--vb-and-c.md)                      | [**mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2-Schnittstelle**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection-Schnittstelle (VB und C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





