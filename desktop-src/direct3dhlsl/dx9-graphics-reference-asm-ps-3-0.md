---
title: ps_3_0
description: Erfahren Sie mehr über ps_3_0, einen programmierbaren Pixelshader, der aus einer Reihe von Anweisungen besteht, die mit Pixeldaten arbeiten.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79145936709e43fab9b87602233225567a0067528a31036aacc11c5b425c0dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512892"
---
# <a name="ps_3_0"></a>ps \_ 3 \_ 0

Ein programmierbarer Pixel-Shader besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten. Registriert Datenübertragungen in und aus der ALU. Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.

-   [ps \_ 3 \_ 0 Anweisungen](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [ps \_ 3 \_ 0 Register listet](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) die verschiedenen Registertypen auf, die von der Pixel-Shader-ALU verwendet werden.
-   [Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.
-   [Die Quellregistermodifizierer des Pixelshader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Das Quellenregister swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Fügen Sie ein Gesichtsregister hinzu. Fügen Sie ein Positionsregister hinzu. Farbregister (v \# ) sind jetzt vollständig Gleitkomma, und die Texturkoordinatenregister (t ) wurden \# konsolidiert. Eingabedeklarationen übernehmen die Verwendungsnamen, und mehrere Verwendungen sind für Komponenten eines bestimmten Registers zulässig.

## <a name="dynamic-flow-control"></a>Dynamisches Flow-Steuerelement

Das Gerät unterstützt die dynamische Flusssteuerung ([bei bool - ps](if-bool---ps.md), break - [ps](break---ps.md)und break comp [- \_ ps](break-comp---ps.md)). Die Tiefe der Schachtelung liegt zwischen 0 und 24.

## <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

Die Anzahl der unterstützten temporären Register beträgt 32.

## <a name="static-flow-control-nesting-depth"></a>Statische Flow Schachtelungstiefe von Steuerelementen

Der [Aufruf – ps](call---ps.md) / [callnz](callnz-bool---ps.md)call  / [ \_ pred](callnz-pred---ps.md) kann auf eine maximale Tiefe von 4 geschachtelt werden. Unabhängig voneinander können [schleifenbasierte](loop---ps.md) / [PS-Anweisungen](rep---ps.md) bis zu einer maximalen Tiefe von 4 geschachtelt werden.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Beliebige Swizzle wird unterstützt. Weitere Informationen finden Sie [unter Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Farbverlaufsanweisungen

Farbverlaufsanweisungen werden unterstützt. Siehe [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)und [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Prädikation

Anweisungsprädikation wird unterstützt. Weitere Informationen finden Sie unter [Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)

## <a name="dependent-read-limit"></a>Abhängiger Lesegrenzwert

Es gibt keine abhängigen Leselimits.

## <a name="texture-instruction-limit"></a>Grenzwert für Texturanweisung

Texturanweisungen sind nicht begrenzt.

## <a name="instruction-count"></a>Anweisungsanzahl

Jeder Pixelshader ist überall von 512 bis zur Anzahl der Slots in MaxPixelShader30InstructionSlots zulässig (nicht mehr als 32768). Die Anzahl der ausgeführten Anweisungen kann aufgrund der Schleifenunterstützung deutlich höher sein. MaxPShaderInstructionsExecuted sollte mindestens 2^16 sein.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Textur-Sampler beträgt 16.

## <a name="device-caps"></a>Geräteobergrenzen

Wenn PS \_ 3 \_ 0 unterstützt wird, werden die folgenden Obergrenzen (mindestens) in der Hardware unterstützt:



| Cap                                                                                                          | Wert                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | jeweils 4 KB                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 KB                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropie                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Die folgenden primitiven Obergrenzen werden festgelegt:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, D3DPMISCCAPS \_ CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ COGINFVF, D3DPMISCCAPS \_ MASKZ                                                                                               |
| Die folgenden Rasterobergrenzen sind festgelegt:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ ANISOTROPY, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ SCISSORTEST in D3DCAPS9                                                                                                                                                                  |
| Vollständige Unterstützung für Tiefenvoreingenommenheit, einschließlich:                                                                       | D3DPRASTERCAPS- \_ UND D3DPRASTERCAPS-DEPTHBIAS \_                                                                                                                                                                                                                                        |
| Vollständige Vergleiche für Tiefen- und Alphatests, einschließlich:                                                  | Alle D3DPCMPCAPS in D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Quellmischungsmodi                                                                                        | Alle Mischungsmodi werden als Quelle unterstützt (mit Ausnahme von D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA und D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Die folgenden Texturkapseln werden unterstützt:                                                                    | D3DPTEXTURECAPS \_ CUBEMAP, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ PERSPECTIVE, D3DPTEXTURECAPS \_ PROJECTED, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| Folgendes wird für Texturfilter-Kapselungen, Volumentexturfilter-Kapselungen und Cubetexturfilter-Kapselungen unterstützt: | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS \_ MINFANISOTROP (dies ist für VolumeTextureFilterCaps und CubeTextureFilterCaps nicht erforderlich), D3DPTFILTERCAPS \_ MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, D3DPTFILTERCAPS \_ MAGFPOINT, D3DPTFILTERCAPS \_ MAGFLINEAR             |
| Die folgenden Texturadressmodi werden in Scheitelpunkt- und Pixelstufen unterstützt:                                | D3DPTADDRESSCAPS \_ WRAP, D3DPTADDRESSCAPS \_ MIRROR, D3DPTADDRESSCAPS \_ CLAMP, D3DPTADDRESSCAPS \_ BORDER, D3DPTADDRESSCAPS \_ INDEPENDENTUV, D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Alle Pixel-Shader-Kapselungen werden unterstützt.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Die folgenden Features werden unterstützt: Prädikation, beliebige Swizzles und Farbverlaufsanweisungen. Es gibt kein Limit für abhängige Lese- und Mathematische Anweisungen sowie keine Beschränkung für die Mischung aus Textur und mathematischen Anweisungen. |
| Alle Schablonenvorgänge werden unterstützt. Dies schließt zwei seitenseitige Schablone ein.                                   | Siehe [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Geräteunterstützungspunktgröße pro Scheitelpunkt                                                                         | D3DFVFCAPS \_ PSIZE in D3DCAPS9                                                                                                                                                                                                                                                                         |
| Nichtleistung von 2 Texturunterstützung.                                                                              | Vollständige Unterstützung oder bedingte Nicht-Pow-2-Unterstützung; Das Gerät sollte nicht die einschränkung der quadratischen Textur aufweisen, wie in D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Wenn das Gerät mehrere Renderziele unterstützt, werden die folgenden Obergrenzen unterstützt:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Wenn \_ vs 3 \_ 0 unterstützt wird                                                                                     | MaxUserClipPlanes in D3DCAPS9 ist 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 