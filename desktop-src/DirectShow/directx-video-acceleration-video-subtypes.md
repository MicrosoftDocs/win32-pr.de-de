---
description: Die folgenden Untertypen werden von Decodern verwendet, die DirectX Video Acceleration (DXVA) verwenden.
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: DirectX Video Acceleration Video Subtypes (Dshow.h) (DirectX Video Acceleration Video-Untertypen (Dshow.h))
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a2197d504929e001e07fb1ac107dbd7b13b1f443e43ec8ed90232372b08f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016148"
---
# <a name="directx-video-acceleration-video-subtypes"></a>DirectX-Videobeschleunigung – Videountertypen

Die folgenden Untertypen werden von Decodern verwendet, die DirectX Video Acceleration (DXVA) verwenden. AI44 und IA44 sind Oberflächen mit einem Bits-pro-Pixel-Wert von 8. Es gibt 4 Bits von I und 4 Bits von *A*. *Ich* stelle einen Index in einer YUV-Palette mit 16 Einträgen dar. *Ein* stellt 4 Bits von Transparenzinformationen dar (auch als pro Pixel-Alpha bezeichnet). Daher ermöglichen AI44- und IA44-Oberflächen 16 verschiedene Farben bei 16 verschiedenen Transparenzwerten oder 256 verschiedene Pixeldarstellungen. Bei AI44 wird das Alpha im Hi-Nibble gespeichert, in IA44 wird das Alpha im Lo-Nibble gespeichert. Beide Formate sind sehr nützlich für DVD-Unterbildbilder und Line21- und Teletext-Bilder. Microsoft bevorzugt die AI44-Version, da es etwas einfacher ist, Text mit diesem Format zu generieren.

| Subtype            | Beschreibung                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | Für Unterbild- und Textüberlagerungen. Siehe vorherige Beschreibung. |
| MEDIASUBTYPE \_ IA44 | Für Unterbild- und Textüberlagerungen. Siehe vorherige Beschreibung. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videountertypen](video-subtypes.md)
</dt> </dl>

 

 




