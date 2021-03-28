---
title: Register-VS_2_0
description: Dieser Abschnitt enthält Referenzinformationen zu den von Vertex Shader Version 2 0 implementierten Eingabe-und Ausgabe Registern \_ .
ms.assetid: e5ef015e-1e4d-41b3-95da-3b44ef0bd73e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 156367ec08a5f1ecd94181be56558f4ba07005b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036809"
---
# <a name="registers---vs_2_0"></a>Register-vs \_ 2 \_ 0

Dieser Abschnitt enthält Referenzinformationen zu den von Vertex Shader Version 2 0 implementierten Eingabe-und Ausgabe Registern \_ .

## <a name="input-registers"></a>Eingabe Register



| Register | Name                                                                                      | Anzahl      | R/W | \# Leseports | \# Lese-/inst- | Dimension | Reladdr | der Arbeitszeittabelle     | Erfordert DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| Ramelow\#      | [Eingabe Register](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Unbegrenzt       | 4         | Nein      | Siehe Hinweis 1   | Ja          |
| r\#      | [Temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | R/W | 3             | Unbegrenzt       | 4         | Nein      | Keine         | Nein           |
| c\#      | [Konstantes float-Register](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Siehe Hinweis 2 | R   | 1             | 2               | 4         | a0/Al | (0, 0, 0, 0) | Nein           |
| a0       | [Adress Register](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | 2               | 4         | Nein      | Keine         | Nein           |
| b\#      | [Konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Nein      | FALSE        | Nein           |
| Ich\#      | [Konstanter ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Nein      | (0, 0, 0, 0) | Nein           |
| irdische       | [Schleifen-Counter-Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | Nein      | Keine         | Nein           |



 

Hinweise:

1.  Partiell (0, 0, 0, 1): Wenn nur eine Teilmenge von Kanälen aktualisiert wird, werden die restlichen Kanäle standardmäßig auf (0, 0, 0, 1) festgelegt.
2.  Gleich D3DCAPS9. Maxvertexshaderconst (mindestens 256 für vs \_ 2 \_ 0).

## <a name="output-registers"></a>Ausgabe Register



| Register | Name                                                                                          | Anzahl | R/W | Dimension | Reladdr | der Arbeitszeittabelle | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| OPOS     | [Positions Register](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | Nein      | Keine     | Nein           |
| onebel     | [Nebelregister](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | Nein      | Keine     | Nein           |
| oPts     | [Punktgröße registrieren](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | Nein      | Keine     | Nein           |
| gen\#     | [Farb Register](dx9-graphics-reference-asm-vs-registers-color.md); Siehe Hinweis 1               | 2     | W   | 4         | Nein      | Keine     | Nein           |
| TS\#     | [Texturkoordinaten Register](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | Nein      | Keine     | Nein           |



 

Hinweise:

-   oD0 ist die Ausgabe der diffusen Farbe. oD1 ist die Glanz Farben Ausgabe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




