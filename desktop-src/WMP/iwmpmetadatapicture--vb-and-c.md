---
title: IWMPMetadataPicture-Schnittstelle (VB und C) (WMP. h)
description: Stellt Eigenschaften bereit, mit denen Informationen zu dem Bild, das in einer digitalen Mediendatei enthalten ist, die durch ein WM/picturemetadata-Attribut dargestellt wird, erhalten.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB und C) Interface Windows Media Player
- IWMPMetadataPicture (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352067"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>IWMPMetadataPicture-Schnittstelle (VB und c#)

Stellt Eigenschaften bereit, mit denen Informationen zu dem Bild, das in einer digitalen Mediendatei enthalten ist, die durch ein [**WM/Bild-**](/windows/desktop/wmformat/wmpicture)Metadatenattribut dargestellt wird, erhalten Dieses Attribut entspricht Albumkunst Bildern, die in einer digitalen Mediendatei enthalten sind, und nicht in albumgrafiken, die über das Internet heruntergeladen wurden.

Die **IWMPMetadataPicture** -Schnittstelle macht die folgenden Eigenschaften verfügbar.



| Eigenschaft                                                                                   | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Beschreibung**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Ruft die Beschreibung des Bilds ab, das durch das Metadatenattribut dargestellt wird.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Ruft den MIME-Typ des Bilds ab, das durch das Metadatenattribut dargestellt wird.    |
| [**PictureType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Ruft den Bildtyp des Bilds ab, das durch das Metadatenattribut dargestellt wird. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Nur interne Verwendung.                                                        |



 

Sie erhalten eine **IWMPMetadataPicture** -Schnittstelle, indem Sie den Attributnamen [**WM/Bild**](/windows/desktop/wmformat/wmpicture) an die folgende Methode übergeben und das zurückgegebene Objekt umwandeln.



| Schnittstelle                                  | Eigenschaft                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Member

Die **IWMPMetadataPicture-Schnittstelle (VB und c#)** definiert keine Member.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

