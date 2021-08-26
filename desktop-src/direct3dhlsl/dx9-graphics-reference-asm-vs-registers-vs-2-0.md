---
title: Register – vs_2_0
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 2 0 des Vertex-Shaders implementiert \_ werden.
ms.assetid: e5ef015e-1e4d-41b3-95da-3b44ef0bd73e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd31f4ce5cac538624fe736642b30cbee9ba54579ee50da9a2ccd027847e9ecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067970"
---
# <a name="registers---vs_2_0"></a>Registrierungen im Vergleich \_ zu 2 \_ 0

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 2 0 des Vertex-Shaders implementiert \_ werden.

## <a name="input-registers"></a>Eingaberegister



| Registrieren | Name                                                                                      | Anzahl      | R/W | \# Leseports | \# Reads/inst | Dimension | RelAddr | Standardeinstellungen     | Erfordert DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| V\#      | [Eingaberegister](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Unbegrenzt       | 4         | Nein      | Siehe Hinweis 1   | Ja          |
| R\#      | [Temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | R/W | 3             | Unbegrenzt       | 4         | Nein      | Keine         | Nein           |
| c\#      | [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Siehe Hinweis 2 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | Nein           |
| a0       | [Adressregister](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | 2               | 4         | Nein      | Keine         | Nein           |
| b\#      | [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Nein      | FALSE        | Nein           |
| Ich\#      | [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Nein      | (0, 0, 0, 0) | Nein           |
| Al       | [Schleifenzählerregister](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | Nein      | Keine         | Nein           |



 

Hinweise:

1.  Teilweise (0, 0, 0, 1): Wenn nur eine Teilmenge der Kanäle aktualisiert wird, werden die verbleibenden Kanäle standardmäßig auf (0, 0, 0, 1) eingestellt.
2.  Entspricht D3DCAPS9. MaxVertexShaderConst (mindestens 256 im Vergleich \_ zu 2 \_ 0).

## <a name="output-registers"></a>Ausgaberegister



| Registrieren | Name                                                                                          | Anzahl | R/W | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| Opos     | [Positionsregister](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | Nein      | Keine     | Nein           |
| oFog     | [Register "Register"](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | Nein      | Keine     | Nein           |
| Setzt     | [Punktgrößenregister](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | Nein      | Keine     | Nein           |
| Od\#     | [Farbregister](dx9-graphics-reference-asm-vs-registers-color.md); Siehe Hinweis 1               | 2     | W   | 4         | Nein      | Keine     | Nein           |
| Ot\#     | [Texturkoordinatenregister](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | Nein      | Keine     | Nein           |



 

Hinweise:

-   oD0 ist die Ausgabe der diffusen Farbe. oD1 ist die Ausgabe der Glanzfarbe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




