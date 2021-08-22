---
title: WM/Publisher-Attribut
description: Das WM/Publisher-Attribut ist der Name des Unternehmens, das den Inhalt veröffentlicht hat.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- WM/Publisher Attribute Windows Media Player
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22aa04eecb3999b3029948739eef51dab094d0ebf9b65ba01ccdcf6de59efc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053788"
---
# <a name="wmpublisher-attribute"></a>WM/Publisher-Attribut

Das **WM/Publisher-Attribut** ist der Name des Unternehmens, das den Inhalt veröffentlicht hat.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Wiedergabelisten](cd-playlist-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

**Label,** **ReleasedBy** und **Studio** sind Aliase für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMPublisher.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





