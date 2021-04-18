---
title: Is_Protected-Attribut
description: Das \_ protected-Attribut gibt an, ob der Inhalt durch Digital Rights Management (DRM) geschützt ist.
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Windows-Is_Protected-Attribut Media Player
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365431"
---
# <a name="is_protected-attribute"></a>Ist \_ geschütztes Attribut

Das **\_ Protected** -Attribut gibt an, ob der Inhalt durch Digital Rights Management (DRM) geschützt ist.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateien](commonly-used-windows-media-file-attributes.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

" **Digitallysecure** " ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmprotected.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





