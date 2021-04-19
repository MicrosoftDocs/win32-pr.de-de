---
title: IWMPMediaCollection2-Schnittstelle (VB und C) (WMP. h)
description: Stellt Methoden bereit, die die iwmpmediacollection-Schnittstelle ergänzen.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB und C) Interface Windows Media Player
- IWMPMediaCollection2 (VB und C) Interface Windows Media Player, beschrieben
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
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355937"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>IWMPMediaCollection2-Schnittstelle (VB und c#)

Stellt Methoden bereit, die die **iwmpmediacollection** -Schnittstelle ergänzen.

## <a name="members"></a>Member

Die IWMPMediaCollection2-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die IWMPMediaCollection2-Schnittstelle **(VB und c#)** verfügt über diese Methoden.



| Methode                                                                                                                     | BESCHREIBUNG                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**createQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | Gibt eine **iwmpquery** -Schnittstelle zurück, die eine neue Abfrage darstellt.<br/>                                                                                               |
| [**getbyattributeandmediatype**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp ermöglicht.<br/>                                     |
| [**getplaylistbyquery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die Zugriff auf Medienelemente bietet, die den Abfragebedingungen entsprechen.<br/>                                                    |
| [**getstringcollectionbyquery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | Gibt eine **iwmpstringcollection** -Schnittstelle zurück, die Zugriff auf den Satz aller Zeichen folgen Werte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.<br/> |



 

Sie erhalten eine **IWMPMediaCollection2** -Schnittstelle, indem Sie den Wert umwandeln, der von der [**AxWindowsMediaPlayer. mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) -Eigenschaft zurückgegeben wird, oder den von der [**iwmplibrary. mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) -Eigenschaft zurückgegebenen Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





