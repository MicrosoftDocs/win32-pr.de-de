---
title: ps_2_x Anweisungen
description: Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shader-Version 2 \_ x.
ms.assetid: a9b5f9dd-1139-4f80-ada6-e2fc0fb7effe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 047067d26f9b85ef981a007059d9f2e87ae28ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976760"
---
# <a name="ps_2_x-instructions"></a>PS \_ 2 \_ x-Anweisungen

Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shader-Version 2 \_ x.

Es gibt mehrere Arten von pixelshaderanweisungen, wie in der Tabelle dargestellt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungs Slots: Anzahl der Anweisungs Slots, die von jeder Anweisung verwendet werden.
-   Setup: ein Pixelshader muss über eine Versions Anweisung verfügen, und es muss sich um die erste Anweisung handeln.
-   Arithmetik: diese Anweisungen bieten die mathematischen Vorgänge in einem Shader.
-   Textur: diese Anweisungen werden verwendet, um Textur Daten zu laden und zu untersuchen und um Texturkoordinaten zu ändern.
-   Fluss Steuerung: diese Anweisungen bieten statische und dynamische Fluss Steuerung für die Ausführung von Anweisungen.
-   Neu: diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                             | BESCHREIBUNG                                                                                      | Anweisungs Slots | Einrichten | Arithmetik | Struktur | Flusssteuerung | Neu |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-PS](abs---ps.md)                                         | Absoluter Wert                                                                                   | 1                 |       | x          |         |              |     |
| [Add-PS](add---ps.md)                                         | Hinzufügen von zwei Vektoren                                                                                  | 1                 |       | x          |         |              |     |
| [Break-PS](break---ps.md)                                     | Abbrechen von Rep... ENDREP-Block                                                                | 1                 |       |            |         | x            | x   |
| [\_Comp-PS Abbrechen](break-comp---ps.md)                          | Bedingtes Abbrechen von Rep... ENDREP-Block mit einem Vergleich                               | 3                 |       |            |         | x            | x   |
| [breakp-PS](break-p---ps.md)                                  | Abbrechen von Rep... ENDREP-Block, basierend auf einem Prädikat                                          | 3                 |       |            |         | x            | x   |
| [callps](call---ps.md)                                       | Aufrufen einer Unterroutine                                                                                | 2                 |       |            |         | x            | x   |
| [callnz bool-PS](callnz-bool---ps.md)                         | Unterroutine aufrufen, wenn ein boolesches Register nicht 0 (null) ist                                              | 3                 |       |            |         | x            | x   |
| [callnz pred-PS](callnz-pred---ps.md)                         | Unterroutine aufrufen, wenn ein Prädikat Register nicht 0 (null) ist                                            | 3                 |       |            |         | x            | x   |
| [CMP-PS](cmp---ps.md)                                         | Quelle mit 0 vergleichen                                                                              | 1                 |       | x          |         |              |     |
| [CRS-PS](crs---ps.md)                                         | Kreuz Produkt                                                                                    | 2                 |       | x          |         |              |     |
| [DCL- \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Die Textur Dimension für einen Sampler deklarieren                                                      | 0                 | x     |            |         |              |     |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Deklarieren Sie die Zuordnung zwischen Scheitelpunkt-Shader-Ausgabe Registern und Pixel-Shader-Eingabe Registern. | 0                 | x     |            |         |              |     |
| [DEF-PS](def---ps.md)                                         | Definieren von Konstanten                                                                                 | 0                 | x     |            |         |              |     |
| [DEFB-PS](defb---ps.md)                                       | Definieren einer booleschen Konstante                                                                        | 0                 | x     |            |         |              | x   |
| [Defi-PS](defi---ps.md)                                       | Definieren einer ganzzahligen Konstante                                                                       | 0                 | x     |            |         |              | x   |
| [dp2add-PS](dp2add---ps.md)                                   | 2D-Punktprodukt und hinzufügen                                                                           | 2                 |       | x          |         |              |     |
| [DP3-PS](dp3---ps.md)                                         | 3D-Punktprodukt                                                                                   | 1                 |       | x          |         |              |     |
| [DP4-PS](dp4---ps.md)                                         | 4D-Punktprodukt                                                                                   | 1                 |       | x          |         |              |     |
| [DSX-PS](dsx---ps.md)                                         | Änderungs Rate in der x-Richtung                                                                | 2                 |       | x          |         |              | x   |
| [DSY-PS](dsy---ps.md)                                         | Änderungs Rate in der y-Richtung                                                                | 2                 |       | x          |         |              | x   |
| [Else-PS](else---ps.md)                                       | BEGIN an einem Else-Block                                                                              | 1                 |       |            |         | x            | x   |
| [in-PS-PS](endif---ps.md)                                     | Beenden einer if... Else-Block                                                                           | 1                 |       |            |         | x            | x   |
| [ENDREP-PS](endrep---ps.md)                                   | Ende eines Wiederholungs Blocks                                                                            | 2                 |       |            |         | x            | x   |
| [Exp-PS](exp---ps.md)                                         | Vollständige Genauigkeit 2<sup>x</sup>                                                                     | 1                 |       | x          |         |              |     |
| [FRC-PS](frc---ps.md)                                         | Bruchteile                                                                             | 1                 |       | x          |         |              |     |
| [Wenn bool-PS](if-bool---ps.md)                                 | BEGIN an einem If-Block                                                                                | 3                 |       |            |         | x            | x   |
| [Wenn \_ Comp-PS](if-comp---ps.md)                                | Startet einen If-Block mit einem Vergleich.                                                              | 3                 |       |            |         | x            | x   |
| [Wenn pred-PS](if-pred---ps.md)                                 | BEGIN an einem If-Block mit Prädikat                                                               | 3                 |       |            |         | x            | x   |
| [Bezeichnung-PS](label---ps.md)                                     | Bezeichnung                                                                                            | 0                 |       |            |         | x            | x   |
| [Log-PS](log---ps.md)                                         | Protokoll der vollständigen Genauigkeit (x)                                                                           | 1                 |       | x          |         |              |     |
| [LRP-PS](lrp---ps.md)                                         | Lineare interpolieren                                                                               | 2                 |       | x          |         |              |     |
| [m3x2-PS](m3x2---ps.md)                                       | 3 x 2 multiplizieren                                                                                     | 2                 |       | x          |         |              |     |
| [M3x3-PS](m3x3---ps.md)                                       | 3X3 multiplizieren                                                                                     | 3                 |       | x          |         |              |     |
| [M3x4-PS](m3x4---ps.md)                                       | rund m3 multiplizieren                                                                                     | 4                 |       | x          |         |              |     |
| [m4x3-PS](m4x3---ps.md)                                       | 4 x 3 multiplizieren                                                                                     | 3                 |       | x          |         |              |     |
| [M4x4-PS](m4x4---ps.md)                                       | 4 x 4 multiplizieren                                                                                     | 4                 |       | x          |         |              |     |
| [Mad-PS](mad---ps.md)                                         | Multiplizieren und hinzufügen                                                                                 | 1                 |       | x          |         |              |     |
| [Max-PS](max---ps.md)                                         | Maximum                                                                                          | 1                 |       | x          |         |              |     |
| [min-PS](min---ps.md)                                         | Minimum                                                                                          | 1                 |       | x          |         |              |     |
| [MOV-PS](mov---ps.md)                                         | Move                                                                                             | 1                 |       | x          |         |              |     |
| [Mul-PS](mul---ps.md)                                         | Multiplizieren                                                                                         | 1                 |       | x          |         |              |     |
| [NOP-PS](nop---ps.md)                                         | Keine Operation                                                                                     | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normalize                                                                                        | 3                 |       | x          |         |              |     |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         |              |     |
| [Psel](ps---ps.md)                                                | Version                                                                                          | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Reziproke                                                                                       | 1                 |       | x          |         |              |     |
| [Rep-PS](rep---ps.md)                                         | Repeat                                                                                           | 3                 |       |            |         | x            | x   |
| [Ret-PS](ret---ps.md)                                         | Ende einer Unterroutine                                                                              | 1                 |       |            |         | x            | x   |
| [RSQ-PS](rsq---ps.md)                                         | Gegenseitige Quadratwurzel                                                                           | 1                 |       | x          |         |              |     |
| [SETP \_ comp](setp-comp---ps.md)                                 | Legen Sie das Prädikat Register fest.                                                                       | 1                 |       |            |         | x            | x   |
| [SinCos-PS](sincos---ps.md)                                   | Sinus und Kosinus                                                                                  | 8                 |       | x          |         |              |     |
| [Sub-PS](sub---ps.md)                                         | Subtrahieren                                                                                         | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Pixel Rendering beenden                                                                                | Siehe Hinweis 1        |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 und aufwärts](texld---ps-2-0.md)                    | Beispiel für eine Textur                                                                                 | Siehe Hinweis 2        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Textur Stichproben mit einer Detailebene von w-Component                                      | Siehe Hinweis 3        |       |            | x       |              |     |
| [texldd-PS](texldd---ps.md)                                   | Textur Stichproben mit vom Benutzer bereitgestellten Farbverläufen                                                    | 3                 |       |            | x       |              | x   |
| [texldp-PS](texldp---ps.md)                                   | Textur Sampling mit Projective Division durch w-Component                                           | Siehe Hinweis 4        |       |            | x       |              |     |



 

Hinweise:

1.  Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, Slots = 2; andernfalls Slots = 1.
2.  Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist und die Textur eine cubemap ist, Slots = 4; andernfalls Slot = 1.
3.  Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, Slots = 6; andernfalls Slots = 1.
4.  Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) nicht festgelegt ist, Slots = 1; andernfalls:
    -   Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist und die Textur eine cubemap ist, Slots = 4.
    -   Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist und die Textur keine cubemap ist, Slots = 3.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 