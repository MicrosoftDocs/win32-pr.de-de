---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4 Anweisungen
description: Dieser Abschnitt enthält Referenzinformationen für Anweisungen zur Pixels shader-Version 1 \_ X.
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc624c3f3b64d41f428f68fcf2643f4600dcdec1
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129898"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4 Instructions

Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shaderversion 1 \_ X.

Es gibt verschiedene Arten von Shaderanweisungen für Pixel, wie in der folgenden Tabelle gezeigt.

## <a name="instruction-set"></a>Instruktionssatz



| Version                                    | Beschreibung                                                                   | Anweisungsslots | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [Ps](ps---ps.md)                          | Versionsnummer                                                                | 0                 | x    | x    | x    | x    |
| Anweisungen für Konstanten                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def – ps](def---ps.md)                   | Definieren von Konstanten                                                              | 0                 | x    | x    | x    | x    |
| Anweisungen zu Phasen                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [phase – ps](phase---ps.md)               | Übergang zwischen Phase 1 und Phase 2                                        | 0                 |      |      |      | x    |
| Arithmetische Anweisungen                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [add - ps](add---ps.md)                   | Hinzufügen von zwei Vektoren                                                               | 1                 | x    | x    | x    | x    |
| [bem - ps](bem---ps.md)                   | Anwenden einer Fake-Bump-Umgebungszuordnungstransformation                                   | 2                 |      |      |      | x    |
| [cmp - ps](cmp---ps.md)                   | Vergleichen der Quelle mit 0                                                           | 1.                |      | x    | x    | x    |
| [cnd - ps](cnd---ps.md)                   | Vergleichen der Quelle mit 0.5                                                         | 1                 | x    | x    | x    | x    |
| [dp3 – ps](dp3---ps.md)                   | Punktprodukt mit drei Komponenten                                                   | 1                 | x    | x    | x    | x    |
| [dp4 – ps](dp4---ps.md)                   | Vier-Komponenten-Punktprodukt                                                    | 1.                |      | x    | x    | x    |
| [lrp – ps](lrp---ps.md)                   | Lineare Interpolation                                                            | 1                 | x    | x    | x    | x    |
| [mad – ps](mad---ps.md)                   | Multiplizieren und Hinzufügen                                                              | 1                 | x    | x    | x    | x    |
| [mov – ps](mov---ps.md)                   | Move                                                                          | 1                 | x    | x    | x    | x    |
| [mul - ps](mul---ps.md)                   | Multiplizieren                                                                      | 1                 | x    | x    | x    | x    |
| [nop - ps](nop---ps.md)                   | Keine Operation                                                                  | 0                 | x    | x    | x    | x    |
| [sub – ps](sub---ps.md)                   | Subtrahieren                                                                      | 1                 | x    | x    | x    | x    |
| Texturanweisungen                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [tex - ps](tex---ps.md)                   | Beispiel für eine Textur                                                              | 1                 | x    | x    | x    |      |
| [texbem – ps](texbem---ps.md)             | Anwenden einer fake bump-Umgebungszuordnungstransformation                                   | 1                 | x    | x    | x    |      |
| [texbeml – ps](texbeml---ps.md)           | Anwenden einer gefälschten Umgebungszuordnungstransformation mit Leuchtdichtekorrektur         | 1+1²              | x    | x    | x    |      |
| [texcoord – ps](texcoord---ps.md)         | Interpretieren von Texturkoordinatendaten als Farbdaten                               | 1                 | x    | x    | x    |      |
| [texcrd – ps](texcrd---ps.md)             | Kopieren von Texturkoordinatendaten als Farbdaten                                    | 1                 |      |      |      | x    |
| [texdepth - ps](texdepth---ps.md)         | Berechnen von Tiefenwerten                                                        | 1                 |      |      |      | x    |
| [texdp3 – ps](texdp3---ps.md)             | Punktprodukt mit drei Komponenten zwischen Texturdaten und Texturkoordinaten  | 1                 |      | x    | x    |      |
| [texdp3tex – ps](texdp3tex---ps.md)       | Punktprodukt mit drei Komponenten und 1D-Textursuche                             | 1                 |      | x    | x    |      |
| [texkill - ps](texkill---ps.md)           | Bricht das Rendering von Pixeln basierend auf einem Vergleich ab.                             | 1                 | x    | x    | x    | x    |
| [texld - ps \_ 1 \_ 4](texld---ps-1-4.md)     | Beispiel für eine Textur                                                              | 1                 |      |      |      | x    |
| [texm3x2depth – ps](texm3x2depth---ps.md) | Berechnen von Tiefenwerten pro Pixel                                              | 1                 |      |      | x    |      |
| [texm3x2pad – ps](texm3x2pad---ps.md)     | Multiplikation der ersten Zeilenmatrix einer Multiplikation einer zweizzeilenbasierten Matrix                        | 1                 | x    | x    | x    |      |
| [texm3x2tex – ps](texm3x2tex---ps.md)     | Multiplikation der letzten Zeilenmatrix einer Multiplikation einer zweizzeilenbasierten Matrix                        | 1                 | x    | x    | x    |      |
| [texm3x3 – ps](texm3x3---ps.md)           | Multiplikation der 3x3-Matrix                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad – ps](texm3x3pad---ps.md)     | Multiplikation der ersten oder zweiten Zeile einer Drei-Zeilen-Matrix multiplizieren                   | 1                 | x    | x    | x    |      |
| [texm3x3spec – ps](texm3x3spec---ps.md)   | Letzte Zeilenmultiplikation einer Multiplikation einer Drei-Zeilen-Matrix                             | 1                 | x    | x    | x    |      |
| [texm3x3tex – ps](texm3x3tex---ps.md)     | Textursuche mit einer Multiplikation der 3x3-Matrix                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec – ps](texm3x3vspec---ps.md) | Textursuche mit einer 3x3-Matrixmultiplikation mit einem nicht konstanten Augenstrahlvektor | 1                 | x    | x    | x    |      |
| [texreg2ar – ps](texreg2ar---ps.md)       | Probieren Sie eine Textur mithilfe der Alpha- und rot-Komponenten aus.                           | 1                 | x    | x    | x    |      |
| [texreg2gb - ps](texreg2gb---ps.md)       | Sampling einer Textur mithilfe der grünen und blauen Komponenten                          | 1                 | x    | x    | x    |      |
| [texreg2rgb – ps](texreg2rgb---ps.md)     | Probieren Sie eine Textur mithilfe der roten, grünen und blauen Komponenten aus.                     | 1                 |      | x    | x    |      |



 

1.  1 Slot in PS \_ 1 \_ 4; 2 Slots in ps \_ 1 \_ 2 und ps \_ 1 \_ 3
2.  1 + 1 = 1 arithmetische Anweisung + 1 Texturanweisung

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




