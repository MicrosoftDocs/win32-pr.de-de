---
title: WM/Writer-Attribut
description: Das WM/Writer-Attribut ist der Name des Autors, der die Wörter des Inhalts geschrieben hat.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- WM/Writer-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a239fd83c936a0712459307fbf08b01c4bfcc4f6fd4c6d32cddc12d8092f2b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332055"
---
# <a name="wmwriter-attribute"></a>WM/Writer-Attribut

Das **WM/Writer-Attribut** ist der Name des Autors, der die Wörter des Inhalts geschrieben hat.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Um alle Werte für ein mehrwertiges Attribut abzurufen, müssen Sie die **Media.getItemInfoByType-Methode** verwenden, nicht die **Media.getItemInfo-Methode.**

**Writer** ist ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMWriter.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





