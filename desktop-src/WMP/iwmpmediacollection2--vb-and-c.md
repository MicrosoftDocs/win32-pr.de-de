---
title: IWMPMediaCollection2-Schnittstelle (VB und C ) (Wmp.h)
description: Stellt Methoden bereit, die die IWMPMediaCollection-Schnittstelle ergänzen.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2-Schnittstelle (VB und C) Windows Media Player
- IWMPMediaCollection2-Schnittstelle (VB und C) Windows Media Player , beschrieben
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 725580d504d07ecc311c89b0ba3121f4f0f62990fcd1cfb6e92cdcbbd3535a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508740"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>IWMPMediaCollection2-Schnittstelle (VB und C#)

Stellt Methoden bereit, die die **IWMPMediaCollection-Schnittstelle** ergänzen.

## <a name="members"></a>Member

Die **IWMPMediaCollection2-Schnittstelle (VB und C#)** verfügt über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMPMediaCollection2-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                                                                     | Beschreibung                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Createquery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | Gibt eine **IWMPQuery-Schnittstelle** zurück, die eine neue Abfrage darstellt.<br/>                                                                                               |
| [**getByAttributeAndMediaType**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp bietet.<br/>                                     |
| [**getPlaylistByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | Gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente bietet, die den Abfragebedingungen entsprechen.<br/>                                                    |
| [**getStringCollectionByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | Gibt eine **IWMPStringCollection-Schnittstelle** zurück, die Zugriff auf den Satz aller Zeichenfolgenwerte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.<br/> |



 

Sie erhalten **eine IWMPMediaCollection2-Schnittstelle,** indem Sie den von der [**AxWindowsMediaPlayer.mediaCollection-Eigenschaft**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) zurückgegebenen Wert oder den von der [**IWMPLibrary.mediaCollection-Eigenschaft**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) zurückgegebenen Wert umschalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





