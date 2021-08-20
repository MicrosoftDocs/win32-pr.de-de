---
title: WM/ProviderRating-Attribut
description: Das WM/ProviderRating-Attribut ist die Bewertung des Elements, das vom Anbieter der Attributwerte zugewiesen wird.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- WM/ProviderRating-Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcff262f21b4f31daff6f704dba1cb096f54bb295a21a3ae9a7c90f574af34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116606"
---
# <a name="wmproviderrating-attribute"></a>WM/ProviderRating-Attribut

Das **WM/ProviderRating-Attribut** ist die Bewertung des Elements, das vom Anbieter der Attributwerte zugewiesen wird.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Wiedergabelisten](cd-playlist-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

**Rating** ist ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMProviderRating.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





