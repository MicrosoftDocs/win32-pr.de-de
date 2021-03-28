---
title: ps_3_0
description: Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5aca251b1e8a462b4f2204241680922d76c45ba0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315579"
---
# <a name="ps_3_0"></a>PS \_ 3 \_ 0

Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.

-   [die \_ Anweisungen für PS 3 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) enthalten eine Liste der verfügbaren Anweisungen.
-   [PS \_ 3 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) listet die verschiedenen Register Typen auf, die von PixelShader Alu verwendet werden.
-   [Modifiziererer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Wird verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   Die [Ziel Register-Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.
-   [Pixel-Shader-Quell Registrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.
-   Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Fügen Sie ein Gesichts Register hinzu. Fügen Sie ein Positions Register hinzu. Farbregister (v \# ) sind nun vollständig Gleit Komma und die Texturkoordinaten Register (t \# ) wurden konsolidiert. Eingabe Deklarationen übernehmen die Verwendungs Namen, und für Komponenten eines bestimmten Registers sind mehrere Verwendungen zulässig.

## <a name="dynamic-flow-control"></a>Dynamische Fluss Steuerung

Das Gerät unterstützt die dynamische Fluss Steuerung ([Wenn bool-PS](if-bool---ps.md), [break-PS](break---ps.md)und die unter [Brechung von \_ Comp-PS](break-comp---ps.md)). Die Tiefe der Schachtelung liegt zwischen 0 und 24.

## <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

Die Anzahl der unterstützten temporären Register beträgt 32.

## <a name="static-flow-control-nesting-depth"></a>Schachtelungs Tiefe der statischen Fluss Steuerung

Der Aufruf der pred für den [Aufruf des Aufruf-PS](call---ps.md) / [callnz](callnz-bool---ps.md)  / [ \_ ](callnz-pred---ps.md) kann in eine maximale Tiefe von 4 schachtelt werden. Unabhängig davon können [Schleifen-PS-](loop---ps.md) / [Rep-PS](rep---ps.md) -Anweisungen in eine maximale Tiefe von 4 schachtelt werden.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Beliebiges Swizzle wird unterstützt. Weitere Informationen finden Sie unter [Quellen Register: schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Farbverlaufs Anweisungen

Farbverlaufs Anweisungen werden unterstützt. Siehe [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)und [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Prädikation

Das Anweisungs Prädikat wird unterstützt. Siehe [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Abhängiges Lese Limit

Es sind keine abhängigen Lese Limits vorhanden.

## <a name="texture-instruction-limit"></a>Grenzwert für Textur Anweisung

Es gibt keine Begrenzung der Textur Anweisungen.

## <a name="instruction-count"></a>Anweisungs Anzahl

Jeder Pixel-Shader ist von 512 bis zur Anzahl der Slots in MaxPixelShader30InstructionSlots zulässig (nicht mehr als 32768). Die Anzahl der ausgelaufenden Anweisungen kann aufgrund der Schleifen Unterstützung erheblich höher sein. Maxpshaderinstructionsexecuted muss mindestens 2 ^ 16 sein.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Textur-Samplern ist 16.

## <a name="device-caps"></a>Geräte Obergrenzen

Wenn PS \_ 3 \_ 0 unterstützt wird, werden die folgenden Obergrenzen (minimal) in der Hardware unterstützt:



| Decke                                                                                                          | Wert                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | jeweils 4K                                                                                                                                                                                                                                                                                               |
| Maxtextureretorf                                                                                             | 8 KB                                                                                                                                                                                                                                                                                                    |
| Maxanisotropie                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Die folgenden primitiven Obergrenzen werden festgelegt:                                                                        | D3DPMISCCAPS \_ blendop, D3DPMISCCAPS \_ clipplanescaledpoints, D3DPMISCCAPS \_ cliptlverts, D3DPMISCCAPS \_ cullccw, D3DPMISCCAPS \_ cullcw, D3DPMISCCAPS \_ cullnone, D3DPMISCCAPS \_ foginfvf, D3DPMISCCAPS \_ maskz                                                                                               |
| Die folgenden Raster Caps sind festgelegt:                                                                           | D3DPRASTERCAPS \_ mipmaplodbias, D3DPRASTERCAPS \_ Anisotropy, D3DPRASTERCAPS \_ colorperspective, D3DPRASTERCAPS \_ scissortest in D3DCAPS9                                                                                                                                                                  |
| Vollständige Unterstützung für tiefe Voreingenommenheit, einschließlich:                                                                       | D3DPRASTERCAPS \_ slopescaledepthbias, D3DPRASTERCAPS \_ depthbias                                                                                                                                                                                                                                        |
| Vollständiger Satz von vergleichen für Tiefe und Alpha Test einschließlich:                                                  | Alle D3DPCMPCAPS in D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Quellmischungs Modi                                                                                        | Alle Mischungs Modi werden als Quelle unterstützt (außer D3DPBLENDCAPS \_ srcalphasat, D3DPBLENDCAPS \_ bothsrcalpha und D3DPBLENDCAPS \_ bothinvsrcalpha).                                                                                                                                                    |
| Die folgenden Textur Obergrenzen werden unterstützt:                                                                    | D3DPTEXTURECAPS \_ cubemap, D3DPTEXTURECAPS \_ mipcubemap, D3DPTEXTURECAPS \_ MipMap, D3DPTEXTURECAPS \_ mipvolumemap, D3DPTEXTURECAPS \_ Perspective, D3DPTEXTURECAPS \_ projizierte, D3DPTEXTURECAPS \_ texrepeatnotscaledbysize, D3DPTEXTURECAPS \_ volumemap                                                        |
| Folgendes wird für Textur Filter Caps, volumetextur-Filter Caps und cubetexturfiltercaps unterstützt: | D3DPTFILTERCAPS \_ minfpoint, D3DPTFILTERCAPS \_ minflinear, D3DPTFILTERCAPS \_ minfanisotropic (Dies ist für volumetexturefiltercaps und cubetexturefiltercaps nicht erforderlich), D3DPTFILTERCAPS \_ mipfpoint, D3DPTFILTERCAPS \_ mipflinear, D3DPTFILTERCAPS \_ magfpoint, D3DPTFILTERCAPS \_ magflinear             |
| Die folgenden Textur Adress Modi werden in Scheitelpunkt-und Pixel Stufen unterstützt:                                | D3DPTADDRESSCAPS \_ Wrap, D3DPTADDRESSCAPS \_ Mirror, D3DPTADDRESSCAPS \_ Clamp, D3DPTADDRESSCAPS \_ Border, D3DPTADDRESSCAPS \_ independentuv, D3DPTADDRESSCAPS \_ mirroronce                                                                                                                                    |
| Alle Pixel-Shader-Caps werden unterstützt.                                                                     | Dynamicflowcontroltiefe = 24, numTemps = 32, staticflowcontroltiefe = 4, numinstructionslots = 512. Die folgenden Funktionen werden unterstützt: prädikations-, willkürlich-und Farbverlaufs Anweisungen. Es gibt keine abhängige Lese Beschränkung und keine Beschränkung für die Mischung aus Textur-und mathematischen Anweisungen. |
| Alle Schablone-Vorgänge werden unterstützt. Dies schließt zweiseitige Schablonen ein.                                   | Siehe [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Geräte Unterstützungs Punkt-Größe pro Scheitelpunkt                                                                         | D3DFVFCAPS \_ Psize in D3DCAPS9                                                                                                                                                                                                                                                                         |
| Keine Potenz von 2 Textur Unterstützung.                                                                              | Vollständige Unterstützung oder bedingte nicht-Pow-2-Unterstützung; das Gerät darf nicht die Einschränkung der quadratischen Textur aufweisen, wie in D3DPTEXTURECAPS \_ squareonly.                                                                                                                                                    |
| Wenn das Gerät mehrere Rendertargets unterstützt, werden die folgenden Obergrenzen unterstützt:                             | D3DPMISCCAPS \_ independentwrite temasks, D3DPMISCCAPS \_ mrtpostpixelshaderblending                                                                                                                                                                                                                         |
| Wenn vs \_ 3 \_ 0 unterstützt wird                                                                                     | Maxuserclipplane in D3DCAPS9 ist 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 