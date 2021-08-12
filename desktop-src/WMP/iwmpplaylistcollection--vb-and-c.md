---
title: IWMPPlaylistCollection-Schnittstelle (VB und C) (Wmp.h)
description: Stellt Methoden zum Bearbeiten von IWMPPlaylist- und IWMPPlaylistArray-Schnittstellen in einer Auflistung bereit.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- IWMPPlaylistCollection-Schnittstelle (VB und C) Windows Media Player
- IWMPPlaylistCollection-Schnittstelle (VB und C) Windows Media Player beschrieben
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae130b9134d9ad6e19fa062946a591cdf7749b428201750fda8ff55252c3212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575216"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a>IWMPPlaylistCollection-Schnittstelle (VB und C#)

Stellt Methoden zum Bearbeiten von **IWMPPlaylist-** und **IWMPPlaylistArray-Schnittstellen** in einer Auflistung bereit.

## <a name="members"></a>Member

Die **IWMPPlaylistCollection-Schnittstelle (VB und C#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMPPlaylistCollection-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                                                 | Beschreibung                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**getAll**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | Gibt eine **IWMPPlaylistArray-Schnittstelle** zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.<br/>             |
| [**getByName**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | Gibt eine **IWMPPlaylistArray-Schnittstelle** zurück, die den Zugriff auf Wiedergabelisten mit dem angegebenen Namen ermöglicht, sofern vorhanden.<br/> |
| [**importPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | Fügt der Bibliothek eine statische Wiedergabeliste hinzu.<br/>                                                                              |
| [**isDeleted**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | Gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner für gelöschte Elemente befindet.<br/>                           |
| [**newPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | Gibt eine **IWMPPlaylist-Schnittstelle** für eine neue, leere Wiedergabeliste in der Bibliothek zurück.<br/>                                     |
| [**Entfernen**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | Entfernt eine Wiedergabeliste aus der Bibliothek.<br/>                                                                                |
| **setDeleted**                                                                                         | Wird nicht mehr unterstützt.<br/>                                                                                                |



 

Abrufen einer **IWMPPlaylistCollection-Schnittstelle** mithilfe der folgenden Eigenschaft.



| Object                                                                   | Eigenschaft                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**playlistCollection**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray-Schnittstelle (VB und C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





