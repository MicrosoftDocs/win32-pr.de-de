---
title: MetadataPicture-Objekt
description: Das MetadataPicture-Objekt bietet eine Möglichkeit zum Abrufen der Werte des WM/Bild-metadatenattributs. Dieses Attribut entspricht der in einer digitalen Mediendatei enthaltenen Albumkunst, nicht der über das Internet heruntergeladenen Albumkunst.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- MetadataPicture-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473933"
---
# <a name="metadatapicture-object"></a>MetadataPicture-Objekt

Das **MetadataPicture** -Objekt bietet eine Möglichkeit zum Abrufen der Werte des [**WM/Bild-**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadatenattributs. Dieses Attribut entspricht der in einer digitalen Mediendatei enthaltenen Albumkunst, nicht der über das Internet heruntergeladenen Albumkunst.

Das **MetadataPicture** -Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**Beschreibung**](metadatapicture-description.md) | Ruft eine Beschreibung des metadatenbilds ab.    |
| [**mimeType**](metadatapicture-mimetype.md)       | Ruft den MIME-Typ des metadatenbilds ab.    |
| [**PictureType**](metadatapicture-picturetype.md) | Ruft den Bildtyp des metadatenbilds ab. |
| [**URL**](metadatapicture-url.md)                 | Nur interne Verwendung.                                |



 

Der Zugriff auf das **MetadataPicture** -Objekt erfolgt über die folgende Methode.



| Object                        | Methode                                               |
|-------------------------------|------------------------------------------------------|
| [**Medien**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

Zur Veranschaulichung `player.currentMedia.getItemInfoByType(name, language, index)` wird in den Abschnitten der Verweis Syntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 