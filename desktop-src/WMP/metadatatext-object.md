---
title: MetadataText-Objekt
description: Das MetadataText-Objekt bietet eine Möglichkeit, Metadaten für komplexe Textmetadatenattribute abzurufen.
ms.assetid: cf8e4524-6fc5-4534-9542-6bdc7d34bca4
keywords:
- MetadataText-Windows Media Player
topic_type:
- apiref
api_name:
- MetadataText Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f79c4f4bb80855cf84d576c126e30dc5301c45ca6f1a7c34c5d54e57844abfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135023"
---
# <a name="metadatatext-object"></a>MetadataText-Objekt

Das **MetadataText-Objekt** bietet eine Möglichkeit, Metadaten für komplexe Textmetadatenattribute abzurufen.

Das **MetadataText-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                    | Beschreibung                                   |
|---------------------------------------------|-----------------------------------------------|
| [description](metadatatext-description.md) | Ruft eine Beschreibung des Metadatentexts ab. |
| [text](metadatatext-text.md)               | Ruft den Metadatentext ab.                  |



 

Der **Zugriff auf das MetadataText-Objekt** erfolgt über die folgende Methode.



| Object                    | Methode                                           |
|---------------------------|--------------------------------------------------|
| [Medien](media-object.md) | [getItemInfoByType](media-getiteminfobytype.md) |



 

Zur Veranschaulichung: *Player*. *currentMedia*. **getItemInfoByType**(*name*, *language*, *index*) wird in den Referenzsyntaxabschnitten verwendet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




