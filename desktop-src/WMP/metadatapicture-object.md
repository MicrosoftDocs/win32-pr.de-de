---
title: MetadataPicture-Objekt
description: Das MetadataPicture-Objekt bietet eine Möglichkeit, die Werte des WM/Picture-Metadatenattributs abzurufen. Dieses Attribut entspricht der Albumart, die in einer digitalen Mediendatei enthalten ist, nicht der Über das Internet heruntergeladenen Albumart.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- MetadataPicture-Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 261ed17a156e1b5563b52744490e2ed014803eb9f1e75c182f44d5bd228b11c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996210"
---
# <a name="metadatapicture-object"></a>MetadataPicture-Objekt

Das **MetadataPicture-Objekt** bietet eine Möglichkeit, die Werte des [**WM/Picture-Metadatenattributs**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) abzurufen. Dieses Attribut entspricht der Albumart, die in einer digitalen Mediendatei enthalten ist, nicht der Über das Internet heruntergeladenen Albumart.

Das **MetadataPicture-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**Beschreibung**](metadatapicture-description.md) | Ruft eine Beschreibung des Metadatenbilds ab.    |
| [**mimeType**](metadatapicture-mimetype.md)       | Ruft den MIME-Typ des Metadatenbilds ab.    |
| [**pictureType**](metadatapicture-picturetype.md) | Ruft den Bildtyp des Metadatenbilds ab. |
| [**URL**](metadatapicture-url.md)                 | Nur interne Verwendung.                                |



 

Der **Zugriff auf das MetadataPicture-Objekt** erfolgt über die folgende Methode.



| Object                        | Methode                                               |
|-------------------------------|------------------------------------------------------|
| [**Medien**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

Zur Veranschaulichung `player.currentMedia.getItemInfoByType(name, language, index)` wird in den Abschnitten zur Referenzsyntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 