---
title: ps_2_x Register
description: Pixel-Shader sind von Registern abhängig, um Vertex-Daten zu erhalten, Pixeldaten auszugeben, temporäre Ergebnisse während der Berechnungen zu speichern und Textur-Samplings zu identifizieren.
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- Register-ps_2_x
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 880c897aa3d812d1e94e5dc408e97ec18b5de106
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976681"
---
# <a name="ps_2_x-registers"></a>PS \_ 2 \_ x-Register

Pixel-Shader sind von Registern abhängig, um Vertex-Daten zu erhalten, Pixeldaten auszugeben, temporäre Ergebnisse während der Berechnungen zu speichern und Textur-Samplings zu identifizieren. Es gibt mehrere Arten von Registern, von denen jede über eine eindeutige Funktionalität verfügt. Dieser Abschnitt enthält Referenzinformationen zu den von Pixel Shader Version 2 x implementierten Eingabe-und Ausgabe Registern \_ .

## <a name="input-register-types"></a>Eingabe Register Typen



| Register | Name                                                                                          | Anzahl      | R/W        | \# Leseports | \# Lese-/inst- | Dimension | Reladdr | der Arbeitszeittabelle                  | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| Ramelow\#      | [Eingabe Farb Register](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Unbegrenzt     | 4         | N       | Partiell (0001). Siehe Hinweis 4 | J            |
| r\#      | [Temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Siehe Hinweis 1 | R/W        | 3             | Unbegrenzt     | 4         | N       | Keine                      | N            |
| c\#      | [Konstantes float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| Ich\#      | [Konstanter ganzzahliges Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Siehe Hinweis 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Konstantes boolesches Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Siehe Hinweis 2 | 1             | 1             | 1         | N       | false                     | N            |
| P0       | [Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Siehe Hinweis 2 | 1             | 1             | 1         | N       | Keine                      | J            |
| s\#      | [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Siehe Hinweis 3 | 1             | 1             | 4         | N       | Siehe Hinweis 5                | J            |
| t\#      | [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Keine                      | J            |



 

Hinweise:

1.  12 min/32 Max: die Anzahl der r- \# Register wird von D3DPSHADERCAPS2 \_ 0. numTemps (der zwischen 12 und 32 liegen) bestimmt.
2.  Nur von einer Fluss Steuerungs Anweisung verwendbar.
3.  Nur für eine Textur-Samplings-Anweisung verwendbar.
4.  partiell (x, y, z, w): Wenn nur eine Teilmenge von Kanälen im Register aktualisiert wird, werden die restlichen Kanäle standardmäßig festgelegte Werte (x, y, z, w).
5.  Standardwerte für samplerlookups sind vorhanden, aber die Werte hängen vom Textur Format ab.

Die Anzahl der Schreibvorgänge ist die Anzahl der verschiedenen Register (für jeden Registrierungstyp), die in einer einzelnen Anweisung gelesen werden können.

## <a name="output-register-types"></a>Ausgabe Register Typen



| Register | Name                                                                              | Anzahl                                                                             | R/W | Dimension | Reladdr | der Arbeitszeittabelle | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| d #     | [Ausgabe Farb Register](dx9-graphics-reference-asm-ps-registers-output-color.md) | Siehe [Texturen mit mehreren Elementen (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Keine     | N            |
| otiefe   | [Ausgabe tiefen Register](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Keine     | N            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 