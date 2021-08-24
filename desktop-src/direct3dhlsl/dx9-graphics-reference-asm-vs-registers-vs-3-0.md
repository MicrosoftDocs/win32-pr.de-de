---
title: Register – vs_3_0
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 3 0 des Vertex-Shaders implementiert \_ werden.
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d658d2d14d149d5d83d673269f2a414d7feaa22f13f1b32f57c4b80500fb1398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673100"
---
# <a name="registers---vs_3_0"></a>Registrierungen im Vergleich \_ zu 3 \_ 0

Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 3 0 des Vertex-Shaders implementiert \_ werden.

## <a name="input-registers"></a>Eingaberegister



| Registrieren | Name                                                                                      | Anzahl      | R/W | \# Leseports | \# Reads/inst | Dimension | RelAddr | Standardeinstellungen     | Erfordert DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| V\#      | [Eingaberegister](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Unbegrenzt       | 4         | a0/aL   | Siehe Hinweis 1   | Ja          |
| r\#      | [Temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W | 3             | Unbegrenzt       | 4         | Nein      | Keine         | Nein           |
| c\#      | [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Siehe Hinweis 2 | R   | 1             | Unbegrenzt       | 4         | a0/aL   | (0, 0, 0, 0) | Nein           |
| a0       | [Adressregister](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | Unbegrenzt       | 4         | Nein      | Keine         | Nein           |
| b\#      | [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Nein      | FALSE        | Nein           |
| Ich\#      | [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Nein      | (0, 0, 0, 0) | Nein           |
| Al       | [Schleifenzählerregister](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Unbegrenzt       | 1         | Nein      | Keine         | Nein           |
| p0       | [Prädikatregister](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W | 1             | 1               | 4         | Nein      | Keine         | Nein           |
| s\#      | [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | Nein      | Siehe Hinweis 3   | Ja          |



 

Hinweise:

1.  Teilweise (0, 0, 0, 1): Wenn nur eine Teilmenge der Kanäle aktualisiert wird, werden die verbleibenden Kanäle standardmäßig auf (0, 0, 0, 1) eingestellt.
2.  Entspricht D3DCAPS9. MaxVertexShaderConst (mindestens 256 im Vergleich \_ zu 3 \_ 0).
3.  Die Standardwerte für die Stichprobensuche sind vorhanden, die Werte hängen jedoch vom Texturformat ab.

## <a name="output-registers"></a>Ausgaberegister

Ausgaberegister wurden in 12 \# o-Register (Ausgaberegister) reduziert. Diese können für alles verwendet werden, was der Benutzer für den Pixelshader interpolieren möchte: Texturkoordinaten, Farben, Oberflächen usw.



| Registrieren | Name            | Anzahl | R/W | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| O\#      | Ausgaberegister | 12    | W   | 4         | Al      | Keine     | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




