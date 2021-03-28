---
title: PS_2_0 Anweisungen
description: Dieser Abschnitt enthält Referenzinformationen für die Anweisungen für die Pixel-Shader, Version 2 \_ 0.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bac2a70ed0147885174c2290d5e58c92ae3347e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992879"
---
# <a name="ps_2_0-instructions"></a>PS \_ 2 \_ 0-Anweisungen

Dieser Abschnitt enthält Referenzinformationen für die Anweisungen für die Pixel-Shader, Version 2 \_ 0.

Es gibt mehrere Arten von pixelshaderanweisungen, wie in der Tabelle dargestellt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungs Slots: Anzahl der Anweisungs Slots, die von jeder Anweisung verwendet werden.
-   Setup: ein Pixelshader muss über eine Versions Anweisung verfügen, und es muss sich um die erste Anweisung handeln.
-   Arithmetik: diese Anweisungen bieten die mathematischen Vorgänge in einem Shader.
-   Textur: diese Anweisungen werden verwendet, um Textur Daten zu laden und zu untersuchen und um Texturkoordinaten zu ändern.
-   Neu: diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                             | BESCHREIBUNG                                                                                      | Anweisungs Slots | Einrichten | Arithmetik | Struktur | Neu |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [ABS-PS](abs---ps.md)                                         | Absoluter Wert                                                                                   | 1                 |       | x          |         | x   |
| [Add-PS](add---ps.md)                                         | Hinzufügen von zwei Vektoren                                                                                  | 1                 |       | x          |         |     |
| [CMP-PS](cmp---ps.md)                                         | Quelle mit 0 vergleichen                                                                              | 1                 |       | x          |         |     |
| [CRS-PS](crs---ps.md)                                         | Kreuz Produkt                                                                                    | 2                 |       | x          |         | x   |
| [DCL- \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Die Textur Dimension für einen Sampler deklarieren                                                      | 0                 | x     |            |         | x   |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Deklarieren Sie die Zuordnung zwischen Scheitelpunkt-Shader-Ausgabe Registern und Pixel-Shader-Eingabe Registern. | 0                 | x     |            |         | x   |
| [DEF-PS](def---ps.md)                                         | Definieren von Konstanten                                                                                 | 0                 | x     |            |         |     |
| [dp2add-PS](dp2add---ps.md)                                   | 2D-Punktprodukt und hinzufügen                                                                           | 2                 |       | x          |         | x   |
| [DP3-PS](dp3---ps.md)                                         | 3D-Punktprodukt                                                                                   | 1                 |       | x          |         |     |
| [DP4-PS](dp4---ps.md)                                         | 4D-Punktprodukt                                                                                   | 1                 |       | x          |         |     |
| [Exp-PS](exp---ps.md)                                         | Vollständige Genauigkeit 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [FRC-PS](frc---ps.md)                                         | Bruchteile                                                                             | 1                 |       | x          |         | x   |
| [Log-PS](log---ps.md)                                         | Protokoll der vollständigen Genauigkeit (x)                                                                           | 1                 |       | x          |         | x   |
| [LRP-PS](lrp---ps.md)                                         | Lineare interpolieren                                                                               | 2                 |       | x          |         |     |
| [m3x2-PS](m3x2---ps.md)                                       | 3 x 2 multiplizieren                                                                                     | 2                 |       | x          |         | x   |
| [M3x3-PS](m3x3---ps.md)                                       | 3X3 multiplizieren                                                                                     | 3                 |       | x          |         | x   |
| [M3x4-PS](m3x4---ps.md)                                       | rund m3 multiplizieren                                                                                     | 4                 |       | x          |         | x   |
| [m4x3-PS](m4x3---ps.md)                                       | 4 x 3 multiplizieren                                                                                     | 3                 |       | x          |         | x   |
| [M4x4-PS](m4x4---ps.md)                                       | 4 x 4 multiplizieren                                                                                     | 4                 |       | x          |         | x   |
| [Mad-PS](mad---ps.md)                                         | Multiplizieren und hinzufügen                                                                                 | 1                 |       | x          |         |     |
| [Max-PS](max---ps.md)                                         | Maximum                                                                                          | 1                 |       | x          |         | x   |
| [min-PS](min---ps.md)                                         | Minimum                                                                                          | 1                 |       | x          |         | x   |
| [MOV-PS](mov---ps.md)                                         | Move                                                                                             | 1                 |       | x          |         |     |
| [Mul-PS](mul---ps.md)                                         | Multiplizieren                                                                                         | 1                 |       | x          |         |     |
| [NOP-PS](nop---ps.md)                                         | Keine Operation                                                                                     | 1                 |       | x          |         |     |
| [NRM-PS](nrm---ps.md)                                         | Normalize                                                                                        | 3                 |       | x          |         | x   |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [Psel](ps---ps.md)                                                | Version                                                                                          | 0                 | x     |            |         |     |
| [RCP-PS](rcp---ps.md)                                         | Reziproke                                                                                       | 1                 |       | x          |         | x   |
| [RSQ-PS](rsq---ps.md)                                         | Gegenseitige Quadratwurzel                                                                           | 1                 |       | x          |         | x   |
| [SinCos-PS](sincos---ps.md)                                   | Sinus und Kosinus                                                                                  | 8                 |       | x          |         | x   |
| [Sub-PS](sub---ps.md)                                         | Subtrahieren                                                                                         | 1                 |       | x          |         |     |
| [texkill-PS](texkill---ps.md)                                 | Pixel Rendering beenden                                                                                | 1                 |       |            | x       |     |
| [texld-PS \_ 2 \_ 0 und aufwärts](texld---ps-2-0.md)                    | Beispiel für eine Textur                                                                                 | 1                 |       |            | x       | x   |
| [texldb-PS](texldb---ps.md)                                   | Textur Stichproben mit einer Detailebene von w-Component                                      | 1                 |       |            | x       | x   |
| [texldp-PS](texldp---ps.md)                                   | Textur Sampling mit Projective Division durch w-Component                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




