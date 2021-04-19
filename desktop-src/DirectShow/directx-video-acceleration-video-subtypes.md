---
description: Die folgenden Untertypen werden von Decodern verwendet, die DirectX Video Acceleration (DXVA) verwenden.
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Video-Untertypen der DirectX-Videobeschleunigung (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361935"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Video-Untertypen der DirectX-Videobeschleunigung

Die folgenden Untertypen werden von Decodern verwendet, die DirectX Video Acceleration (DXVA) verwenden. AI44 und IA44 sind Flächen mit einem Bits-pro-Pixel-Wert von 8. Es gibt vier *Bits von I* und 4 Bits von. *Ich Stelle* einen Index in einer 16-Eintrag-YUV-Palette dar. *Ein* stellt vier Bits von Transparenz Informationen dar (auch als pro Pixel-Alpha bezeichnet). Daher ermöglichen AI44-und IA44-Oberflächen 16 verschiedene Farben bei 16 verschiedenen Transparenz Werten oder 256 verschiedene Pixel Darstellungen. Mit AI44 wird das Alpha in "Hi-Nibble" gespeichert, in IA44 wird das Alpha in "Lo-Nibble" gespeichert. Beide Formate sind für DVD-unter Bild Bilder und Line21-und Teletext-Bilder sehr nützlich. Microsoft bevorzugt die AI44-Version, da es etwas einfacher ist, Text mit diesem Format zu generieren.

| Subtype            | BESCHREIBUNG                                                 |
|--------------------|-------------------------------------------------------------|
| Mediasubtype \_ AI44 | Für untergeordnete Bild-und Text Überlagerungen. Siehe vorherige Beschreibung. |
| Mediasubtype \_ IA44 | Für untergeordnete Bild-und Text Überlagerungen. Siehe vorherige Beschreibung. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Untertypen](video-subtypes.md)
</dt> </dl>

 

 




