---
title: ps_2_x Register
description: Dieser Artikel enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von der Pixel-Shaderversion implementiert 2_x.
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- Register – ps_2_x
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c9f3c71ab6308ad921b5cce27f2c078ad980da17daa7c0045228d27ef0579ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024120"
---
# <a name="ps_2_x-registers"></a>ps \_ 2 \_ x Register

Pixel-Shader sind von Registern abhängig, um Scheitelpunktdaten zu erhalten, Pixeldaten ausausgaben, temporäre Ergebnisse während Berechnungen zu enthalten und Texturstichprobenstufen zu identifizieren. Es gibt mehrere Arten von Registern, die jeweils eine eindeutige Funktionalität haben. Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Der Pixel-Shader Version 2 \_ x implementiert werden.

## <a name="input-register-types"></a>Eingaberegistertypen



| Registrieren | Name                                                                                          | Anzahl      | R/W        | \# Lesen von Ports | \# Reads/inst | Dimension | RelAddr | Standardeinstellungen                  | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| V\#      | [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Unbegrenzt     | 4         | N       | Partial(0001). Siehe Hinweis 4 | J            |
| R\#      | [Temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Siehe Hinweis 1 | R/W        | 3             | Unbegrenzt     | 4         | N       | Keine                      | N            |
| c\#      | [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| Ich\#      | [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Siehe Hinweis 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Konstantes boolesches Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Siehe Hinweis 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| p0       | [Prädikatregister](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Siehe Hinweis 2 | 1             | 1             | 1         | N       | Keine                      | J            |
| s\#      | [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Siehe Hinweis 3 | 1             | 1             | 4         | N       | Siehe Hinweis 5                | J            |
| t\#      | [Texturkoordinatenregister](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Keine                      | J            |



 

Hinweise:

1.  Maximal 12 Min./32: Die Anzahl der r-Register wird durch \# D3DPSHADERCAPS2 \_ 0.NumTemps (zwischen 12 und 32) bestimmt.
2.  Nur von einer Flusssteuerungsanweisung nutzbar.
3.  Kann nur von einer Textur-Samplinganweisung verwendet werden.
4.  partial(x, y, z, w): Wenn nur eine Teilmenge der Kanäle im Register aktualisiert wird, werden die übrigen Kanäle standardmäßig auf die angegebenen Werte (x, y, z, w) festgelegt.
5.  Es sind Standardwerte für Samplersuchen vorhanden, die Werte hängen jedoch vom Texturformat ab.

Die Anzahl der Readports ist die Anzahl der verschiedenen Register (für jeden Registertyp), die in einer einzelnen Anweisung gelesen werden können.

## <a name="output-register-types"></a>Ausgaberegistertypen



| Registrieren | Name                                                                              | Anzahl                                                                             | R/W | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Ausgabefarbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) | Weitere [Informationen finden Sie unter Texturen mit mehreren Elemente (Direct3D 9).](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Keine     | N            |
| oDepth   | [Ausgabetiefenregister](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Keine     | N            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 