---
title: ps_2_x Register
description: Dieser Artikel enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von der Pixelshaderversion 2_x implementiert werden.
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
ms.openlocfilehash: be0e7f282978ada28c2dd71dc7c16dd317ddce42
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406703"
---
# <a name="ps_2_x-registers"></a>ps \_ 2 \_ x Register

Pixel-Shader sind von Registern abhängig, um Scheitelpunktdaten abzurufen, Pixeldaten auszugeben, temporäre Ergebnisse bei Berechnungen zu speichern und Textursamplingstufen zu identifizieren. Es gibt mehrere Arten von Registern, die jeweils eine eindeutige Funktionalität aufweisen. Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 2 x des Pixelshader implementiert \_ werden.

## <a name="input-register-types"></a>Eingaberegistertypen



| Registrieren | Name                                                                                          | Anzahl      | R/W        | \# Leseports | \# Lese-/Inst-Lesefunktionen | Dimension | RelAddr | Standardeinstellungen                  | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| V\#      | [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Unbegrenzt     | 4         | N       | Partial(0001). Siehe Hinweis 4 | „Y“ zugeordnet ist            |
| R\#      | [Temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Siehe Hinweis 1 | R/W        | 3             | Unbegrenzt     | 4         | N       | Keine                      | N            |
| c\#      | [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| Ich\#      | [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Siehe Hinweis 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Siehe Hinweis 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| p0       | [Prädikatregister](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Siehe Hinweis 2 | 1             | 1             | 1         | N       | Keine                      | „Y“ zugeordnet ist            |
| s\#      | [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Siehe Hinweis 3. | 1             | 1             | 4         | N       | Siehe Hinweis 5                | „Y“ zugeordnet ist            |
| T\#      | [Texturkoordinatenregister](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Keine                      | „Y“ zugeordnet ist            |



 

Hinweise:

1.  Maximal 12 Min./32: Die Anzahl der r-Register wird durch \# D3DPSHADERCAPS2 \_ 0.NumTemps (zwischen 12 und 32) bestimmt.
2.  Nur von einer Flusssteuerungsanweisung nutzbar.
3.  Kann nur von einer Textur-Samplinganweisung verwendet werden.
4.  partial(x, y, z, w): Wenn nur eine Teilmenge der Kanäle im Register aktualisiert wird, werden die verbleibenden Kanäle standardmäßig auf die angegebenen Werte (x, y, z, w) festgelegt.
5.  Es sind Standardwerte für Samplersuchen vorhanden, die Werte hängen jedoch vom Texturformat ab.

Die Anzahl der Readports ist die Anzahl verschiedener Register (für jeden Registertyp), die in einer einzelnen Anweisung gelesen werden können.

## <a name="output-register-types"></a>Ausgaberegistertypen



| Registrieren | Name                                                                              | Anzahl                                                                             | R/W | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Ausgabefarbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) | Weitere [Informationen finden Sie unter Texturen mit mehreren Element (Direct3D 9).](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Keine     | N            |
| oDepth   | [Ausgabetiefenregister](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Keine     | N            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 