---
title: Author-Attribut
description: Das Author-Attribut ist der Name eines Medienkünstlers oder Akteurs, der dem Inhalt zugeordnet ist.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Author-Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361339"
---
# <a name="author-attribute"></a>Author-Attribut

Das **Author** -Attribut ist der Name eines Medienkünstlers oder Akteurs, der dem Inhalt zugeordnet ist.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Wiedergabelisten](cd-playlist-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Media-Dateien](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Media. getItemInfoByType](media-getiteminfobytype.md)
-   [Foto Elemente](photo-item-attributes.md)
-   [Wiedergabelisten](playlist-attributes-ref.md)
-   [Options Felder](radio-item-attributes.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die *Medien* verwenden. **getItemInfoByType** -Methode, nicht das *Medium*. **getiteminfo** -Methode.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmauthor.

**Actor** und **Künstlerin** sind Aliase für dieses Attribut.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





