---
title: WM/Genre-Attribut
description: Das WM/Genre-Attribut ist das Genre des Inhalts.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- WM/Genre-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0ef67b0b41ff59f644b0d52376428ae7a2330d388aa62f9765cb4842eeb561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000980"
---
# <a name="wmgenre-attribute"></a>WM/Genre-Attribut

Das **WM/Genre-Attribut** ist das Genre des Inhalts.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Wiedergabelisten](cd-playlist-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Wiedergabelisten](playlist-attributes-ref.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Um alle Werte für ein mehrwertiges Attribut abzurufen, müssen Sie die **Media.getItemInfoByType-Methode** verwenden, nicht die **Media.getItemInfo-Methode.**

**Genre** ist ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut lautet g \_ wszWMGenre.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





