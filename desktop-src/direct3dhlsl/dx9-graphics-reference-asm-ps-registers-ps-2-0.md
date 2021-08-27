---
title: ps_2_0 Register
description: Dieser Artikel enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Der Pixel-Shader Version 2_0 implementiert wurden.
ms.assetid: 8002e3eb-b9d4-4ecb-a9e5-ae58a9e20ace
keywords:
- Register – ps_2_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b8e4300765f340b99da5d06b7651c4daaae4c97b043c6ceb5017aa43b2e2dcb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024150"
---
# <a name="ps_2_0-registers"></a>ps \_ 2 \_ 0 Register

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

1.  Max. 12 Min./32: Die Anzahl der \# r-Register wird durch D3DPSHADERCAPS2 \_ 0.NumTemps (zwischen 12 und 32) bestimmt.
2.  Kann nur von einer Flusssteuerungsanweisung verwendet werden.
3.  Kann nur von einer Textursamplinganweisung verwendet werden.
4.  partial(x, y, z, w): Wenn nur eine Teilmenge der Kanäle im Register aktualisiert wird, werden für die verbleibenden Kanäle standardmäßig die angegebenen Werte (x, y, z, w) verwendet.
5.  Die Standardwerte für Samplersuche sind vorhanden, werte hängen jedoch vom Texturformat ab.

Die Anzahl der Leseports ist die Anzahl der verschiedenen Register (für jeden Registertyp), die in einer einzelnen Anweisung gelesen werden können.

## <a name="output-register-types"></a>Ausgaberegistertypen



| Registrieren | Name                                                                              | Anzahl                                                                             | R/W | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Ausgabefarbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) | Siehe Texturen mit [mehreren Elementen (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Keine     | N            |
| oDepth   | [Ausgabetieferegister](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Keine     | N            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 