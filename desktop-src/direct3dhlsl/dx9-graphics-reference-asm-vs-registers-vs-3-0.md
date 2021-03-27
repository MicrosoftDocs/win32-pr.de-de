---
title: Register-vs_3_0
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 3 0 implementiert werden \_ .
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47353a3f312a2abbd6f4fe5ea1dcd1ed9495a9d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712774"
---
# <a name="registers---vs_3_0"></a>Register-vs \_ 3 \_ 0

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 3 0 implementiert werden \_ .

## <a name="input-registers"></a>Eingabe Register



| Register | Name                                                                                      | Anzahl      | R/W | \# Leseports | \# Lese-/inst- | Dimension | Reladdr | der Arbeitszeittabelle     | Erfordert DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| Ramelow\#      | [Eingabe Register](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Unbegrenzt       | 4         | a0/Al   | Siehe Hinweis 1   | Ja          |
| r\#      | [Temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W | 3             | Unbegrenzt       | 4         | Nein      | Keine         | Nein           |
| c\#      | [Konstantes float-Register](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Siehe Hinweis 2 | R   | 1             | Unbegrenzt       | 4         | a0/Al   | (0, 0, 0, 0) | Nein           |
| a0       | [Adress Register](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | Unbegrenzt       | 4         | Nein      | Keine         | Nein           |
| b\#      | [Konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Nein      | FALSE        | Nein           |
| Ich\#      | [Konstanter ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Nein      | (0, 0, 0, 0) | Nein           |
| irdische       | [Schleifen-Counter-Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Unbegrenzt       | 1         | Nein      | Keine         | Nein           |
| P0       | [Prädikat Register](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W | 1             | 1               | 4         | nein      | Keine         | nein           |
| s\#      | [Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | Nein      | Siehe Hinweis 3   | Ja          |



 

Hinweise:

1.  Partiell (0, 0, 0, 1): Wenn nur eine Teilmenge von Kanälen aktualisiert wird, werden die restlichen Kanäle standardmäßig auf (0, 0, 0, 1) festgelegt.
2.  Gleich D3DCAPS9. Maxvertexshaderconst (mindestens 256 für vs \_ 3 \_ 0).
3.  Es sind Standardwerte für die Sampler-Suche vorhanden, aber die Werte sind vom Textur Format abhängig.

## <a name="output-registers"></a>Ausgabe Register

Ausgabe Register wurden in 12 o \# (Output)-Register reduziert. Diese können für alle Elemente verwendet werden, die der Benutzer für den Pixelshader interpolieren möchte: Texturkoordinaten, Farben, Nebel usw.



| Register | Name            | Anzahl | R/W | Dimension | Reladdr | der Arbeitszeittabelle | Erfordert DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| o\#      | Ausgabe Register | 12    | W   | 4         | irdische      | Keine     | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




