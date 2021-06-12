---
title: ps_3_0
description: Erfahren Sie ps_3_0, einem programmierbaren Pixel-Shader, der aus einer Reihe von Anweisungen besteht, die mit Pixeldaten arbeiten.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19587cbaa79e2b89633560a7b7889219172d0c25
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010863"
---
# <a name="ps_3_0"></a>ps \_ 3 \_ 0

Ein programmierbarer Pixel-Shader besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten. Registriert Übertragungsdaten in und aus der ALU. Zusätzliche Steuerung kann angewendet werden, um die Anweisung, die Ergebnisse oder die ausgeschriebenen Daten zu ändern.

-   [ps \_ 3 \_ 0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [ps \_ 3 \_ 0 Register listet](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) die verschiedenen Registertypen auf, die vom Pixel-Shader ALU verwendet werden.
-   [Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Werden verwendet, um die Art und Weise zu ändern, wie eine Anweisung funktioniert.
-   [Die Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.
-   [Registermodifizierer für Pixel-Shaderquellen](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Source Register Swizzling bietet](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Fügen Sie ein Gesichtsregister hinzu. Fügen Sie ein Positionsregister hinzu. Farbregister (v) sind jetzt vollständig Gleitkomma, \# und die Texturkoordinatenregister (t \# ) wurden konsolidiert. Eingabedeklarationen übernehmen die Verwendungsnamen, und mehrere Verwendungen sind für Komponenten eines bestimmten Registers zulässig.

## <a name="dynamic-flow-control"></a>Dynamische Flusssteuerung

Das Gerät unterstützt die dynamische Flusssteuerung ([wenn bool - ps](if-bool---ps.md), break - [ps](break---ps.md)und break comp [- \_ ps](break-comp---ps.md)). Die Schachtelungstiefe liegt zwischen 0 und 24.

## <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

Die Anzahl der unterstützten temporären Register beträgt 32.

## <a name="static-flow-control-nesting-depth"></a>Schachtelungstiefe der statischen Flusssteuerung

Der [Aufruf - ps](call---ps.md)callnz call pred kann bis zu einer maximalen Tiefe von / [](callnz-bool---ps.md)  / 4 geschachtelt[ \_ ](callnz-pred---ps.md) werden. Unabhängig davon [können Anweisungen für "loop - ps](loop---ps.md)rep - ps" bis zu einer maximalen Tiefe von / [](rep---ps.md) 4 geschachtelt werden.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Beliebiges Swizzle wird unterstützt. Siehe [Quellregister Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Anweisungen zum Farbverlauf

Anweisungen zum Farbverlauf werden unterstützt. Siehe [dsx – ps](dsx---ps.md), [dsy – ps](dsy---ps.md)und [texldd – ps](texldd---ps.md).

## <a name="predication"></a>Prädikation

Anweisungsvordication wird unterstützt. Weitere Informationen [finden Sie unter Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)

## <a name="dependent-read-limit"></a>Abhängiger Lesegrenzwert

Es gibt keine abhängigen Lesegrenzwerte.

## <a name="texture-instruction-limit"></a>Texturanweisungslimit

Es gibt keine Beschränkung für Texturanweisungen.

## <a name="instruction-count"></a>Anweisungsanzahl

Jeder Pixelshader ist zwischen 512 und der Anzahl von Slots in MaxPixelShader30InstructionSlots (nicht mehr als 32768) zulässig. Die Anzahl der ausgeführten Anweisungen kann aufgrund der Schleifenunterstützung deutlich höher sein. MaxPShaderInstructionsExecuted sollte mindestens 2^16 sein.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Texturs sampler beträgt 16.

## <a name="device-caps"></a>Geräteobergrenze

Wenn ps \_ 3 \_ 0 unterstützt wird, werden die folgenden Obergrenzen in der Hardware unterstützt (mindestens):



| Cap                                                                                                          | Wert                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 4.000                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 KB                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropie                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Die folgenden primitiven Obergrenzen sind festgelegt:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, D3DPMISCCAPS \_ CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ NAPINFVF, D3DPMISCCAPS \_ MASKZ                                                                                               |
| Die folgenden Rasteroberungen sind festgelegt:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ ANISOTROPY, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ SCISSORTEST in D3DCAPS9                                                                                                                                                                  |
| Vollständige Unterstützung für Tiefenvoreingenommenheit, einschließlich:                                                                       | D3DPRASTERCAPS \_ VERSKALIERTEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Vollständiger Satz von Vergleichen für Tiefen- und Alphatests, einschließlich:                                                  | Alle D3DPCMPCAPS in D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Quellmischungsmodi                                                                                        | Alle Blendingmodi werden als Quelle unterstützt (außer D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA und D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Die folgenden Texturoberungen werden unterstützt:                                                                    | D3DPTEXTURECAPS \_ CUBEMAP, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ PERSPECTIVE, D3DPTEXTURECAPS \_ PROJECTED, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| Folgendes wird für Texturfilteroberungen, Volumentexturfilter-Obergrenzen und Cubetexturfilter-Obergrenzen unterstützt: | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS \_ MINFANISOTROPIC (dies ist für VolumeTextureFilterCaps und CubeTextureFilterCaps nicht erforderlich), D3DPTFILTERCAPS \_ MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, D3DPTFILTERCAPS \_ MAGFPOINT, D3DPTFILTERCAPS \_ MAGFLINEAR             |
| Die folgenden Texturadressenmodi werden in Scheitelpunkt- und Pixelphasen unterstützt:                                | D3DPTADDRESSCAPS \_ WRAP, D3DPTADDRESSCAPS \_ MIRROR, D3DPTADDRESSCAPS \_ CLAMP, D3DPTADDRESSCAPS \_ BORDER, D3DPTADDRESSCAPS \_ INDEPENDENTUV, D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Alle Pixel-Shader-Caps werden unterstützt.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Die folgenden Features werden unterstützt: Prädication, beliebige Swizzles und Gradient-Anweisungen. Es gibt kein abhängiges Leselimit und keine Beschränkung für die Mischung aus Textur- und mathematischen Anweisungen. |
| Alle Schablonenvorgänge werden unterstützt. Dies schließt zwei seitenseitige Schablonen ein.                                   | Siehe [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Größe des Geräteunterstützungspunkts pro Scheitelpunkt                                                                         | D3DFVFCAPS \_ PSIZE in D3DCAPS9                                                                                                                                                                                                                                                                         |
| Nicht-Leistung von 2 Texturunterstützung.                                                                              | Entweder vollständige Unterstützung oder bedingte Nicht-pow-2-Unterstützung; Das Gerät sollte nicht die ausschließliche Einschränkung der Quadrattextur aufweisen, wie in D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Wenn das Gerät mehrere Rendertargets unterstützt, werden die folgenden Obergrenzen unterstützt:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Wenn vs \_ 3 \_ 0 unterstützt wird                                                                                     | MaxUserClipPlanes in D3DCAPS9 ist 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 