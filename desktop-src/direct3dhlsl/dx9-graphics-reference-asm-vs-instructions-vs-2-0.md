---
title: Anweisungen-VS_2_0
description: Dieser Abschnitt enthält Referenzinformationen für die Anweisungen der Vertex-Shader-Version 2 \_ 0.
ms.assetid: f5ca3e44-3c71-4221-9381-cea521d984e0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8ea2dbe5d70cc4be8d3867cafc6127138f833a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388532"
---
# <a name="instructions---vs_2_0"></a>Anweisungen: vs \_ 2 \_ 0

Dieser Abschnitt enthält Referenzinformationen für die Anweisungen der Vertex-Shader-Version 2 \_ 0.

Es gibt mehrere Arten von Vertex-shaderanweisungen, wie in der Tabelle dargestellt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungs Slots: Anzahl der Anweisungs Slots, die von jeder Anweisung verwendet werden.
-   Setup: nicht arithmetische Anweisungen. Jeder Shader muss über eine Versions Anweisung verfügen, und er muss die erste Anweisung sein.
-   Arithmetik: diese Anweisungen bieten die mathematischen Vorgänge in einem Shader.
-   Fluss Steuerung: diese Anweisungen fügen Fluss Steuerungsfunktionen hinzu, z. b. [Schleife](loop---vs.md)... [ENDLOOP](endloop---vs.md), [if](if-bool---vs.md)... [else](else---vs.md)... ein [-oder-](endif---vs.md)Unterroutine Aufruf.
-   Neu: diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                                           | BESCHREIBUNG                                                                                                     | Anweisungs Slots | Einrichten | Arithmetik | Flusssteuerung | Neu |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [ABS-vs](abs---vs.md)                                                       | Absoluter Wert                                                                                                  | 1                 |       | x          |              | x   |
| [Add-vs](add---vs.md)                                                       | Hinzufügen von zwei Vektoren                                                                                                 | 1                 |       | x          |              |     |
| [callvs](call---vs.md)                                                     | Aufrufen einer Unterroutine                                                                                               | 2                 |       |            | x            | x   |
| [callnz bool-vs](callnz-bool---vs.md)                                       | Unterroutine aufrufen, wenn ein boolesches Register nicht 0 (null) ist                                                             | 3                 |       |            | x            | x   |
| [CRS-vs](crs---vs.md)                                                       | Kreuz Produkt                                                                                                   | 2                 |       | x          |              | x   |
| [DCL- \_ Verwendungs Eingabe (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Deklarieren von Vertex-Eingabe Registern (siehe [Register-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md)) | 0                 | x     |            |              |     |
| [DEF-vs](def---vs.md)                                                       | Definieren von Konstanten                                                                                                | 0                 | x     |            |              |     |
| [DEFB-vs](defb---vs.md)                                                     | Definieren einer booleschen Konstante                                                                                       | 0                 | x     |            |              | x   |
| [Defi-vs](defi---vs.md)                                                     | Definieren einer ganzzahligen Konstante                                                                                      | 0                 | x     |            |              | x   |
| [DP3-vs](dp3---vs.md)                                                       | 3-Komponenten-Punktprodukt                                                                                     | 1                 |       | x          |              |     |
| [DP4-vs](dp4---vs.md)                                                       | Punktprodukt mit vier Komponenten                                                                                      | 1                 |       | x          |              |     |
| [DST-vs](dst---vs.md)                                                       | Berechnen des Entfernungs Vektors                                                                                   | 1                 |       | x          |              |     |
| [Else-vs](else---vs.md)                                                     | Starten eines [else-vs-](else---vs.md) Blocks                                                                       | 1                 |       |            | x            | x   |
| [umdif-vs](endif---vs.md)                                                   | Beenden eines, [Wenn bool-vs](if-bool---vs.md)... [else-vs-](else---vs.md) Block                                      | 1                 |       |            | x            | x   |
| [ENDLOOP-vs](endloop---vs.md)                                               | Ende eines [Schleifen-vs-](loop---vs.md) Blocks                                                                       | 2                 |       |            | x            | x   |
| [ENDREP-vs](endrep---vs.md)                                                 | Ende eines Wiederholungs Blocks                                                                                           | 2                 |       |            | x            | x   |
| [Exp-vs](exp---vs.md)                                                       | Vollständige Genauigkeit 2<sup>x</sup>                                                                                    | 1                 |       | x          |              |     |
| [Exp-vs](exp---vs.md)                                                       | Partielle Genauigkeit 2<sup>x</sup>                                                                                 | 1                 |       | x          |              |     |
| [FRC-vs](frc---vs.md)                                                       | Bruchteile                                                                                            | 1                 |       | x          |              |     |
| [Wenn bool-vs](if-bool---vs.md)                                               | BEGIN an einem [if bool-vs-](if-bool---vs.md) Block (unter Verwendung einer booleschen Bedingung)                                     | 3                 |       |            | x            | x   |
| [Bezeichnung (VS)](label---vs.md)                                                   | Bezeichnung                                                                                                           | 0                 |       |            | x            | x   |
| [Lit-vs](lit---vs.md)                                                       | Berechnung der partiellen Beleuchtung                                                                                    | 3                 |       | x          |              |     |
| [Log-vs](log---vs.md)                                                       | Protokoll der vollständigen Genauigkeit (x)                                                                                          | 1                 |       | x          |              |     |
| [LogP-vs](logp---vs.md)                                                     | Protokoll der partiellen Genauigkeit (x)                                                                                       | 1                 |       | x          |              |     |
| [Schleifen-vs](loop---vs.md)                                                     | Loop                                                                                                            | 3                 |       |            | x            | x   |
| [LRP-vs](lrp---vs.md)                                                       | Lineare interpolung                                                                                            | 2                 |       | x          |              | x   |
| [m3x2-vs](m3x2---vs.md)                                                     | 3 x 2 multiplizieren                                                                                                    | 2                 |       | x          |              |     |
| [M3x3-vs](m3x3---vs.md)                                                     | 3X3 multiplizieren                                                                                                    | 3                 |       | x          |              |     |
| [M3x4-vs](m3x4---vs.md)                                                     | rund m3 multiplizieren                                                                                                    | 4                 |       | x          |              |     |
| [m4x3-vs](m4x3---vs.md)                                                     | 4 x 3 multiplizieren                                                                                                    | 3                 |       | x          |              |     |
| [M4x4-vs](m4x4---vs.md)                                                     | 4 x 4 multiplizieren                                                                                                    | 4                 |       | x          |              |     |
| [Mad-vs](mad---vs.md)                                                       | Multiplizieren und hinzufügen                                                                                                | 1                 |       | x          |              |     |
| [Max-vs](max---vs.md)                                                       | Maximum                                                                                                         | 1                 |       | x          |              |     |
| [min-vs](min---vs.md)                                                       | Minimum                                                                                                         | 1                 |       | x          |              |     |
| [MOV (VS)](mov---vs.md)                                                       | Move                                                                                                            | 1                 |       | x          |              |     |
| [vs](mova---vs.md)                                                     | Verschieben von Daten aus einem Gleit Komma Register in das Adressregister (a0)                                           | 1                 |       | x          |              | x   |
| [Mul-vs](mul---vs.md)                                                       | Multiplizieren                                                                                                        | 1                 |       | x          |              |     |
| [NOP-vs](nop---vs.md)                                                       | Keine Operation                                                                                                    | 1                 |       | x          |              |     |
| [NRM-vs](nrm---vs.md)                                                       | Normalisieren eines 4D-Vektors                                                                                           | 3                 |       | x          |              | x   |
| [Pow-vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                   | 3                 |       | x          |              | x   |
| [RCP-vs](rcp---vs.md)                                                       | Reziproke                                                                                                      | 1                 |       | x          |              |     |
| [Rep-vs](rep---vs.md)                                                       | Repeat                                                                                                          | 3                 |       |            | x            | x   |
| [Ret-vs](ret---vs.md)                                                       | Ende einer Unterroutine oder einer Haupt Routine                                                                              | 1                 |       |            | x            | x   |
| [RSQ-vs](rsq---vs.md)                                                       | Gegenseitige Quadratwurzel                                                                                          | 1                 |       | x          |              |     |
| [SGE-vs](sge---vs.md)                                                       | Vergleich größer als oder gleich                                                                                   | 1                 |       | x          |              |     |
| [SGN-vs](sgn---vs.md)                                                       | Signieren                                                                                                            | 3                 |       | x          |              | x   |
| [SinCos-vs](sincos---vs.md)                                                 | Sinus und Kosinus                                                                                                 | 8                 |       | x          |              | x   |
| [SLT-vs](slt---vs.md)                                                       | Kleiner als Vergleich                                                                                               | 1                 |       | x          |              |     |
| [Sub-vs](sub---vs.md)                                                       | Subtrahieren                                                                                                        | 1                 |       | x          |              |     |
| [Jews](vs---vs.md)                                                              | Version                                                                                                         | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




