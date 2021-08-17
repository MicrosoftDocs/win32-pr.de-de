---
title: IWMPMetadataPicture-Schnittstelle (VB und C) (Wmp.h)
description: Stellt Eigenschaften zum Abrufen von Informationen über das Bild bereit, das in einer digitalen Mediendatei enthalten ist, die durch ein WM/Picturemetadata-Attribut dargestellt wird.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture-Schnittstelle (VB und C) Windows Media Player
- IWMPMetadataPicture-Schnittstelle (VB und C) Windows Media Player beschrieben
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
ms.openlocfilehash: 1b73a48b2ea93d696f2b8780edec90dfcf0522e2353c508e31d96dd7a404d0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996490"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>IWMPMetadataPicture-Schnittstelle (VB und C#)

Stellt Eigenschaften zum Abrufen von Informationen über das Bild bereit, das in einer digitalen Mediendatei enthalten ist, die durch ein [**WM/Picture-Metadatenattribut**](/windows/desktop/wmformat/wmpicture)dargestellt wird. Dieses Attribut entspricht Albumartbildern, die in einer digitalen Mediendatei enthalten sind, nicht der Über das Internet heruntergeladenen Albumart.

Die **IWMPMetadataPicture-Schnittstelle** macht die folgenden Eigenschaften verfügbar.



| Eigenschaft                                                                                   | Beschreibung                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Beschreibung**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Ruft die Beschreibung des Bilds ab, das durch das Metadatenattribut dargestellt wird.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Ruft den MIME-Typ des durch das Metadatenattribut dargestellten Bilds ab.    |
| [**pictureType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Ruft den Bildtyp des Bilds ab, das durch das Metadatenattribut dargestellt wird. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | Nur interne Verwendung.                                                        |



 

Sie erhalten eine **IWMPMetadataPicture-Schnittstelle,** indem Sie den Attributnamen [**WM/Picture**](/windows/desktop/wmformat/wmpicture) an die folgende Methode übergeben und das zurückgegebene Objekt umwandeln.



| Schnittstelle                                  | Eigenschaft                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Member

Die **IWMPMetadataPicture-Schnittstelle (VB und C#)** definiert keine Member.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

