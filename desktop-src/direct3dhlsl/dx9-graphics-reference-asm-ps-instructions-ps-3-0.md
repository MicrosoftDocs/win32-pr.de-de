---
title: ps_3_0 Anweisungen
description: Dieser Abschnitt enthält Referenzinformationen für die Anweisungen für die Pixel-Shader, Version 3 \_ 0.
ms.assetid: 36972b9b-a4e7-45b4-83f5-959e75d270de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d43f17ef765feb5899c7dd4537a1770155b4aa59
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856980"
---
# <a name="ps_3_0-instructions"></a>PS \_ 3 \_ 0-Anweisungen

Dieser Abschnitt enthält Referenzinformationen für die Anweisungen für die Pixel-Shader, Version 3 \_ 0.

Es gibt mehrere Arten von pixelshaderanweisungen, wie in der Tabelle dargestellt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungs Slots: Anzahl der Anweisungs Slots, die von jeder Anweisung verwendet werden.
-   Setup: ein Pixelshader muss über eine Versions Anweisung verfügen, und es muss sich um die erste Anweisung handeln.
-   Arithmetik: diese Anweisungen bieten die mathematischen Vorgänge in einem Shader.
-   Textur: diese Anweisungen werden verwendet, um Textur Daten zu laden und zu untersuchen und um Texturkoordinaten zu ändern.
-   Fluss Steuerung: diese Anweisungen bieten statische und dynamische Fluss Steuerung für die Ausführung von Anweisungen.
-   Neu: diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                             | BESCHREIBUNG                                                                          | Anweisungs Slots | Einrichten | Arithmetik | Struktur | Flusssteuerung | Neu |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-PS](abs---ps.md)                                         | Absoluter Wert                                                                       | 1                 |       | x          |         |              |     |
| [Add-PS](add---ps.md)                                         | Hinzufügen von zwei Vektoren                                                                      | 1                 |       | x          |         |              |     |
| [Break-PS](break---ps.md)                                     | Abbrechen einer Schleife... ENDLOOP oder Rep... ENDREP-Block                                  | 1                 |       |            |         | x            |     |
| [\_Comp-PS Abbrechen](break-comp---ps.md)                          | Bedingt aus einer Schleife abbrechen... ENDLOOP oder Rep... ENDREP-Block mit einem Vergleich | 3                 |       |            |         | x            |     |
| [breakp-PS](break-p---ps.md)                                  | Abbrechen einer Schleife... ENDLOOP oder Rep... ENDREP-Block, basierend auf einem Prädikat            | 3                 |       |            |         | x            |     |
| [callps](call---ps.md)                                       | Aufrufen einer Unterroutine                                                                    | 2                 |       |            |         | x            |     |
| [callnz bool-PS](callnz-bool---ps.md)                         | Unterroutine aufrufen, wenn ein boolesches Register nicht 0 (null) ist                                  | 3                 |       |            |         | x            |     |
| [callnz pred-PS](callnz-pred---ps.md)                         | Unterroutine aufrufen, wenn ein Prädikat Register nicht 0 (null) ist                                | 3                 |       |            |         | x            |     |
| [CMP-PS](cmp---ps.md)                                         | Quelle mit 0 vergleichen                                                                  | 1                 |       | x          |         |              |     |
| [CRS-PS](crs---ps.md)                                         | Kreuz Produkt                                                                        | 2                 |       | x          |         |              |     |
| [DCL- \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Die Textur Dimension für einen Sampler deklarieren                                          | 0                 | x     |            |         |              |     |
| [DCL \_ -Semantik (SM3-PS ASM)](dcl-usage---ps.md)              | Deklarieren von Eingabe-und Ausgabe Registern                                                   | 0                 | x     |            |         |              | x   |
| [DEF-PS](def---ps.md)                                         | Definieren von Konstanten                                                                     | 0                 | x     |            |         |              |     |
| [DEFB-PS](defb---ps.md)                                       | Definieren einer booleschen Konstante                                                            | 0                 | x     |            |         |              |     |
| [Defi-PS](defi---ps.md)                                       | Definieren einer ganzzahligen Konstante                                                           | 0                 | x     |            |         |              |     |
| [dp2add-PS](dp2add---ps.md)                                   | 2D-Punktprodukt und hinzufügen                                                               | 2                 |       | x          |         |              |     |
| [DP3-PS](dp3---ps.md)                                         | 3D-Punktprodukt                                                                       | 1                 |       | x          |         |              |     |
| [DP4-PS](dp4---ps.md)                                         | 4D-Punktprodukt                                                                       | 1                 |       | x          |         |              |     |
| [DSX-PS](dsx---ps.md)                                         | Änderungs Rate in der x-Richtung                                                    | 2                 |       | x          |         |              |     |
| [DSY-PS](dsy---ps.md)                                         | Änderungs Rate in der y-Richtung                                                    | 2                 |       | x          |         |              |     |
| [Else-PS](else---ps.md)                                       | BEGIN an einem Else-Block                                                                  | 1                 |       |            |         | x            |     |
| [in-PS-PS](endif---ps.md)                                     | Beenden einer if... Else-Block                                                               | 1                 |       |            |         | x            |     |
| [ENDLOOP-PS](endloop---ps.md)                                 | Beenden einer Schleife                                                                           | 2                 |       |            |         | x            | x   |
| [ENDREP-PS](endrep---ps.md)                                   | Ende eines Wiederholungs Blocks                                                                | 2                 |       |            |         | x            |     |
| [Exp-PS](exp---ps.md)                                         | Vollständige Genauigkeit 2<sup>x</sup>                                                         | 1                 |       | x          |         |              |     |
| [FRC-PS](frc---ps.md)                                         | Bruchteile                                                                 | 1                 |       | x          |         |              |     |
| [Wenn bool-PS](if-bool---ps.md)                                 | BEGIN an einem If-Block                                                                    | 3                 |       |            |         | x            |     |
| [Wenn \_ Comp-PS](if-comp---ps.md)                                | Startet einen If-Block mit einem Vergleich.                                                  | 3                 |       |            |         | x            |     |
| [Wenn pred-PS](if-pred---ps.md)                                 | BEGIN an einem If-Block mit Prädikat                                                   | 3                 |       |            |         | x            |     |
| [Bezeichnung-PS](label---ps.md)                                     | Bezeichnung                                                                                | 0                 |       |            |         | x            |     |
| [Log-PS](log---ps.md)                                         | Protokoll der vollständigen Genauigkeit (x)                                                               | 1                 |       | x          |         |              |     |
| [Schleife-PS](loop---ps.md)                                       | Loop                                                                                 | 3                 |       |            |         | x            | x   |
| [LRP-PS](lrp---ps.md)                                         | Lineare interpolieren                                                                   | 2                 |       | x          |         |              |     |
| [m3x2-PS](m3x2---ps.md)                                       | 3 x 2 multiplizieren                                                                         | 2                 |       | x          |         |              |     |
| [M3x3-PS](m3x3---ps.md)                                       | 3X3 multiplizieren                                                                         | 3                 |       | x          |         |              |     |
| [M3x4-PS](m3x4---ps.md)                                       | rund m3 multiplizieren                                                                         | 4                 |       | x          |         |              |     |
| [m4x3-PS](m4x3---ps.md)                                       | 4 x 3 multiplizieren                                                                         | 3                 |       | x          |         |              |     |
| [M4x4-PS](m4x4---ps.md)                                       | 4 x 4 multiplizieren                                                                         | 4                 |       | x          |         |              |     |
| [Mad-PS](mad---ps.md)                                         | Multiplizieren und hinzufügen                                                                     | 1                 |       | x          |         |              |     |
| [Max-PS](max---ps.md)                                         | Maximum                                                                              | 1                 |       | x          |         |              |     |
| [min-PS](min---ps.md)                                         | Minimum                                                                              | 1                 |       | x          |         |              |     |
| [MOV-PS](mov---ps.md)                                         | Move                                                                                 | 1                 |       | x          |         |              |     |
| [Mul-PS](mul---ps.md)                                         | Multiplizieren                                                                             | 1                 |       | x          |         |              |     |
| [NOP-PS](nop---ps.md)                                         | Keine Operation                                                                         | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normalize                                                                            | 3                 |       | x          |         |              |     |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                        | 3                 |       | x          |         |              |     |
| [Psel](ps---ps.md)                                                | Version                                                                              | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Reziproke                                                                           | 1                 |       | x          |         |              |     |
| [Rep-PS](rep---ps.md)                                         | Repeat                                                                               | 3                 |       |            |         | x            |     |
| [Ret-PS](ret---ps.md)                                         | Ende einer Unterroutine                                                                  | 1                 |       |            |         | x            |     |
| [RSQ-PS](rsq---ps.md)                                         | Gegenseitige Quadratwurzel                                                               | 1                 |       | x          |         |              |     |
| [SETP \_ comp](setp-comp---ps.md)                                 | Legen Sie das Prädikat Register fest.                                                           | 1                 |       |            |         | x            |     |
| [SinCos-PS](sincos---ps.md)                                   | Sinus und Kosinus                                                                      | 8                 |       | x          |         |              |     |
| [Sub-PS](sub---ps.md)                                         | Subtrahieren                                                                             | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Pixel Rendering beenden                                                                    | 2                 |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 und aufwärts](texld---ps-2-0.md)                    | Beispiel für eine Textur                                                                     | Siehe Hinweis 1        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Textur Stichproben mit einer Detailebene von w-Component                          | 6                 |       |            | x       |              |     |
| [texldl-PS](texldl---ps.md)                                   | Textur Stichproben mit Detailstufe von w-Component                               | Siehe Hinweis 2        |       |            | x       |              | x   |
| [texldd-PS](texldd---ps.md)                                   | Textur Stichproben mit vom Benutzer bereitgestellten Farbverläufen                                        | 3                 |       |            | x       |              |     |
| [texldp-PS](texldp---ps.md)                                   | Textur Sampling mit Projective Division durch w-Component                               | Siehe Hinweis 3        |       |            | x       |              |     |



 

Hinweise:

1.  Wenn die Textur eine cubemap ist, Slots = 4; Andernfalls Slots = 1.
2.  Wenn die Textur eine cubemap ist, Slots = 5; Andernfalls Slots = 2.
3.  Wenn die Textur eine cubemap ist, Slots = 4; Andernfalls Slots = 3.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




