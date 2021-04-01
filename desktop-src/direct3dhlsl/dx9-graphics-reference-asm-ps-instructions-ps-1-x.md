---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4 Anweisungen
description: Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shader-Version 1 \_ X.
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c3fa8e76e1075da321a60d05504dff074dbfcfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207450"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, Anweisungen

Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shader-Version 1 \_ X.

Es gibt mehrere Arten von pixelshaderanweisungen, wie in der folgenden Tabelle dargestellt.

## <a name="instruction-set"></a>Instruktionssatz



| Version                                    |                                                                               | Anweisungs Slots | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [Psel](ps---ps.md)                          | Versionsnummer                                                                | 0                 | x    | x    | x    | x    |
| Konstantenanweisungen                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [DEF-PS](def---ps.md)                   | Definieren von Konstanten                                                              | 0                 | x    | x    | x    | x    |
| Phasen Anweisungen                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Phase-PS](phase---ps.md)               | Übergang Zwischenphase 1 und Phase 2                                        | 0                 |      |      |      | x    |
| Arithmetische Anweisungen                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Add-PS](add---ps.md)                   | Hinzufügen von zwei Vektoren                                                               | 1                 | x    | x    | x    | x    |
| [Bem-PS](bem---ps.md)                   | Anwenden einer gefälschten Bump Environment-Map-Transformation                                   | 2                 |      |      |      | x    |
| [CMP-PS](cmp---ps.md)                   | Quelle mit 0 vergleichen                                                           | 1 ¹                |      | x    | x    | x    |
| [CND-PS](cnd---ps.md)                   | Quelle mit 0,5 vergleichen                                                         | 1                 | x    | x    | x    | x    |
| [DP3-PS](dp3---ps.md)                   | 3-Komponenten-Punktprodukt                                                   | 1                 | x    | x    | x    | x    |
| [DP4-PS](dp4---ps.md)                   | Punktprodukt mit vier Komponenten                                                    | 1 ¹                |      | x    | x    | x    |
| [LRP-PS](lrp---ps.md)                   | Lineare interpolieren                                                            | 1                 | x    | x    | x    | x    |
| [Mad-PS](mad---ps.md)                   | Multiplizieren und hinzufügen                                                              | 1                 | x    | x    | x    | x    |
| [MOV-PS](mov---ps.md)                   | Move                                                                          | 1                 | x    | x    | x    | x    |
| [Mul-PS](mul---ps.md)                   | Multiplizieren                                                                      | 1                 | x    | x    | x    | x    |
| [NOP-PS](nop---ps.md)                   | Keine Operation                                                                  | 0                 | x    | x    | x    | x    |
| [Sub-PS](sub---ps.md)                   | Subtrahieren                                                                      | 1                 | x    | x    | x    | x    |
| Textur Anweisungen                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [tex-PS](tex---ps.md)                   | Beispiel für eine Textur                                                              | 1                 | x    | x    | x    |      |
| [texbem-PS](texbem---ps.md)             | Anwenden einer gefälschten Bump Environment-Map-Transformation                                   | 1                 | x    | x    | x    |      |
| [texbeml-PS](texbeml---ps.md)           | Anwenden einer gefälschten Bump-Umgebung-Map-Transformation mit Beleuchtungs Korrektur         | 1 +1 ²              | x    | x    | x    |      |
| [texcoord-PS](texcoord---ps.md)         | Interpretieren von Texturkoordinaten Daten als Farbdaten                               | 1                 | x    | x    | x    |      |
| [texcrd-PS](texcrd---ps.md)             | Texturkoordinaten Daten als Farbdaten kopieren                                    | 1                 |      |      |      | x    |
| [textiefe-PS](texdepth---ps.md)         | Berechnen von tiefen Werten                                                        | 1                 |      |      |      | x    |
| [texdp3-PS](texdp3---ps.md)             | 3-Komponenten-Punktprodukt zwischen Textur Daten und den Texturkoordinaten  | 1                 |      | x    | x    |      |
| [texdp3tex-PS](texdp3tex---ps.md)       | 3-Komponenten-Punktprodukt und 1D-Textur Suche                             | 1                 |      | x    | x    |      |
| [texkill-PS](texkill---ps.md)           | Bricht das Rendering von Pixeln auf der Grundlage eines Vergleichs ab                             | 1                 | x    | x    | x    | x    |
| [texld-PS \_ 1 \_ 4](texld---ps-1-4.md)     | Beispiel für eine Textur                                                              | 1                 |      |      |      | x    |
| [texm3x2depth-PS](texm3x2depth---ps.md) | Berechnen von pro-Pixel-tiefen Werten                                              | 1                 |      |      | x    |      |
| [texm3x2pad-PS](texm3x2pad---ps.md)     | Erste Zeilen Matrix multiplizieren einer zweizeiligen Matrix multiplizieren                        | 1                 | x    | x    | x    |      |
| [texm3x2tex-PS](texm3x2tex---ps.md)     | Endgültige Zeilen Matrix multiplizieren einer 2-Zeilen-Matrix multiplizieren                        | 1                 | x    | x    | x    |      |
| [texm3x3-PS](texm3x3---ps.md)           | 3X3-Matrix multiplizieren                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad-PS](texm3x3pad---ps.md)     | Multiplizieren der ersten oder zweiten Zeile einer Matrix mit drei Zeilen                   | 1                 | x    | x    | x    |      |
| [texm3x3spec-PS](texm3x3spec---ps.md)   | Endgültige Zeilen Multiplikation einer Matrix mit drei Zeilen multiplizieren                             | 1                 | x    | x    | x    |      |
| [texm3x3tex-PS](texm3x3tex---ps.md)     | Textur Suche mithilfe einer 3X3-Matrix multiplizieren                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec-PS](texm3x3vspec---ps.md) | Textur Suche mithilfe einer 3X3-Matrix multiplizieren mit einem nicht konstanten Augen Strahl Vektor | 1                 | x    | x    | x    |      |
| [texreg2ar-PS](texreg2ar---ps.md)       | Beispiel für eine Textur mithilfe der Alpha-und Red-Komponenten                           | 1                 | x    | x    | x    |      |
| [texreg2gb-PS](texreg2gb---ps.md)       | Beispiel für eine Textur mit den grünen und blauen Komponenten                          | 1                 | x    | x    | x    |      |
| [texreg2rgb-PS](texreg2rgb---ps.md)     | Beispiel für eine Textur mithilfe der roten, grünen und blauen Komponenten                     | 1                 |      | x    | x    |      |



 

1.  1 Slot in PS \_ 1 \_ 4; 2 Slots in PS \_ 1 \_ 2 und PS \_ 1 \_ 3
2.  1 + 1 = 1 Arithmetische Anweisung + 1 Textur Anweisung

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




