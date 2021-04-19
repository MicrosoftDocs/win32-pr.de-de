---
title: WM/Composer-Attribut
description: Das WM/Composer-Attribut ist der Name des Composer der Musik.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- WM/Composer-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356426"
---
# <a name="wmcomposer-attribute"></a>WM/Composer-Attribut

Das **WM/Composer-** Attribut ist der Name des Composer der Musik.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Wiedergabelisten](cd-playlist-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.

**Composer** ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmcomposer.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





