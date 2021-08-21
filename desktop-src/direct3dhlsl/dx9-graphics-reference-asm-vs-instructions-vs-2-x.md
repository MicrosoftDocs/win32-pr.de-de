---
title: Anweisungen – vs_2_x
description: Dieser Abschnitt enthält Referenzinformationen für die Vertex-Shaderversion 2 \_ x-Anweisungen.
ms.assetid: fac85f96-0f4b-49a8-9c00-9e68000d1c76
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 579e52349031545fd540a98c7ea12876ae0700f725ea81ee05ac0fed65b09a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512276"
---
# <a name="instructions---vs_2_x"></a>Anweisungen im Vergleich \_ zu 2 \_ x

Dieser Abschnitt enthält Referenzinformationen für die Vertex-Shaderversion 2 \_ x-Anweisungen.

Es gibt verschiedene Typen von Vertex-Shaderanweisungen, wie in der Tabelle gezeigt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungsslots: Anzahl von Anweisungsslots, die von jeder Anweisung verwendet werden.
-   Setup: Nicht arithmetische Anweisungen. Jeder Shader muss über eine Versionsanweisung verfügen und die erste Anweisung sein.
-   Arithmetisch: Diese Anweisungen stellen die mathematischen Operationen in einem Shader zur Verfügung.
-   Flow-Steuerelement: Mit diesen Anweisungen werden Flusssteuerungsfunktionen hinzugefügt, z. B. ["loop" oder "...](loop---vs.md) [endloop - vs](endloop---vs.md), [if bool - vs](if-bool---vs.md)... [else](else---vs.md)... [endif-](endif---vs.md)und Unterroutinenaufrufe.
-   Neu: Diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                                           | Beschreibung                                                                                                                                                            | Anweisungsslots | Setup | Arithmetik | Flusssteuerung | Neu |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [abs – vs](abs---vs.md)                                                       | Absoluter Wert                                                                                                                                                         | 1                 |       | x          |              |     |
| [hinzufügen – im Vergleich zu](add---vs.md)                                                       | Hinzufügen von zwei Vektoren                                                                                                                                                        | 1                 |       | x          |              |     |
| [Break - vs](break---vs.md)                                                   | Break out of a [loop - vs](loop---vs.md)... [endloop – vs](endloop---vs.md) oder [rep](rep---vs.md)... [endrep-Block](endrep---vs.md)                                  | 1                 |       |            | x            | x   |
| [break \_ comp – vs](break-comp---vs.md)                                        | Bedingtes Ausbrechen einer [Schleife im Vergleich zu](loop---vs.md)... [endloop – vs](endloop---vs.md) oder [rep](rep---vs.md)... [endrep-Block](endrep---vs.md) mit einem Vergleich | 3                 |       |            | x            | x   |
| [Breakp im Vergleich zu](breakp---vs.md)                                                 | Break out of a [loop - vs](loop---vs.md)... [endloop – vs](endloop---vs.md) oder [rep](rep---vs.md)... [endrep-Block](endrep---vs.md) basierend auf einem Prädikat            | 3                 |       |            | x            | x   |
| [call – vs](call---vs.md)                                                     | Aufrufen einer Unterroutine                                                                                                                                                      | 2                 |       |            | x            |     |
| [callnz bool – vs](callnz-bool---vs.md)                                       | Aufrufen einer Unterroutine, wenn ein boolescher Register nicht 0 (null) ist                                                                                                                    | 3                 |       |            | x            |     |
| [callnz pred – vs](callnz-pred---vs.md)                                       | Aufrufen einer Unterroutine, wenn ein Prädikatregister nicht 0 (null) ist                                                                                                                  | 3                 |       |            | x            | x   |
| [crs – im Vergleich zu](crs---vs.md)                                                       | Produktübergreifend                                                                                                                                                          | 2                 |       | x          |              |     |
| [dcl \_ usage input (sm1, sm2, sm3 – vs asm)](dcl-usage-input-register---vs.md) | Deklarieren von Eingabevertexregistern (siehe [Register – im Vergleich zu \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md))                                                        | 0                 | x     |            |              |     |
| [def – vs](def---vs.md)                                                       | Definieren von Konstanten                                                                                                                                                       | 0                 | x     |            |              |     |
| [defb – vs](defb---vs.md)                                                     | Definieren einer booleschen Konstante                                                                                                                                              | 0                 | x     |            |              |     |
| [defi – vs](defi---vs.md)                                                     | Definieren einer ganzzahligen Konstante                                                                                                                                             | 0                 | x     |            |              |     |
| [dp3 – vs](dp3---vs.md)                                                       | Punktprodukt mit drei Komponenten                                                                                                                                            | 1                 |       | x          |              |     |
| [dp4 – vs](dp4---vs.md)                                                       | Punktprodukt mit vier Komponenten                                                                                                                                             | 1                 |       | x          |              |     |
| [dst – vs](dst---vs.md)                                                       | Berechnen des Entfernungsvektors                                                                                                                                          | 1                 |       | x          |              |     |
| [else – vs](else---vs.md)                                                     | Begin an [else - vs](else---vs.md) block                                                                                                                              | 1                 |       |            | x            |     |
| [endif – vs](endif---vs.md)                                                   | Beenden eines [if bool - vs](if-bool---vs.md)... [else – vs](else---vs.md) block                                                                                             | 1                 |       |            | x            |     |
| [endloop – vs](endloop---vs.md)                                               | Ende einer [Schleife – vs.](loop---vs.md) Block                                                                                                                              | 2                 |       |            | x            |     |
| [endrep – vs](endrep---vs.md)                                                 | Ende eines Wiederholungsblocks                                                                                                                                                  | 2                 |       |            | x            |     |
| [exp – im Vergleich zu](exp---vs.md)                                                       | Vollständige Genauigkeit 2<sup>x</sup>                                                                                                                                           | 1                 |       | x          |              |     |
| [exp – im Vergleich zu](exp---vs.md)                                                       | Teilgenauigkeit 2<sup>x</sup>                                                                                                                                        | 1                 |       | x          |              |     |
| [frc – vs](frc---vs.md)                                                       | Fractional-Komponente                                                                                                                                                   | 1                 |       | x          |              |     |
| [if bool – vs](if-bool---vs.md)                                               | Begin an [if bool - vs](if-bool---vs.md) block (using a Boolean condition)                                                                                            | 3                 |       |            | x            |     |
| [if \_ comp - vs](if-comp---vs.md)                                              | Beginnen sie mit einem Vergleich, [wenn bool – vs](if-bool---vs.md) block                                                                                                     | 3                 |       |            | x            | x   |
| [if pred – vs](if-pred---vs.md)                                               | Begin an [if bool - vs](if-bool---vs.md) block with a predicate condition                                                                                             | 3                 |       |            | x            | x   |
| [label – im Vergleich zu](label---vs.md)                                                   | Bezeichnung                                                                                                                                                                  | 0                 |       |            | x            |     |
| [lit – vs](lit---vs.md)                                                       | Berechnung der partiellen Beleuchtung                                                                                                                                           | 3                 |       | x          |              |     |
| [log – im Vergleich zu](log---vs.md)                                                       | Protokoll mit vollständiger Genauigkeit₂(x)                                                                                                                                                 | 1                 |       | x          |              |     |
| [logp – im Vergleich zu](logp---vs.md)                                                     | Protokoll mit teilweiser Genauigkeit₂(x)                                                                                                                                              | 1                 |       | x          |              |     |
| [loop – im Vergleich zu](loop---vs.md)                                                     | Loop                                                                                                                                                                   | 3                 |       |            | x            |     |
| [lrp – vergleicht](lrp---vs.md)                                                       | Lineare Interpolation                                                                                                                                                   | 2                 |       | x          |              |     |
| [m3x2 – im Vergleich](m3x2---vs.md)                                                     | 3x2 Multiplikation                                                                                                                                                           | 2                 |       | x          |              |     |
| [m3x3 – im Vergleich](m3x3---vs.md)                                                     | 3x3 multiplizieren                                                                                                                                                           | 3                 |       | x          |              |     |
| [m3x4 – im Vergleich](m3x4---vs.md)                                                     | 3x4 Multiplikation                                                                                                                                                           | 4                 |       | x          |              |     |
| [m4x3 – im Vergleich](m4x3---vs.md)                                                     | 4x3 multiplizieren                                                                                                                                                           | 3                 |       | x          |              |     |
| [m4x4 – im Vergleich zu](m4x4---vs.md)                                                     | 4x4 multiplizieren                                                                                                                                                           | 4                 |       | x          |              |     |
| [mad – vs](mad---vs.md)                                                       | Multiplizieren und Hinzufügen                                                                                                                                                       | 1                 |       | x          |              |     |
| [max – im Vergleich zu](max---vs.md)                                                       | Maximum                                                                                                                                                                | 1                 |       | x          |              |     |
| [min – vs](min---vs.md)                                                       | Minimum                                                                                                                                                                | 1                 |       | x          |              |     |
| [mov – im Vergleich zu](mov---vs.md)                                                       | Move                                                                                                                                                                   | 1                 |       | x          |              |     |
| [mova - vs](mova---vs.md)                                                     | Verschieben von Daten aus einem Gleitkommaregister in das Adressregister (a0)                                                                                                  | 1                 |       | x          |              |     |
| [mul – im Vergleich zu](mul---vs.md)                                                       | Multiplizieren                                                                                                                                                               | 1                 |       | x          |              |     |
| [nop – vs](nop---vs.md)                                                       | Keine Operation                                                                                                                                                           | 1                 |       | x          |              |     |
| [nrm – vs](nrm---vs.md)                                                       | Normalisieren eines 4D-Vektors                                                                                                                                                  | 3                 |       | x          |              |     |
| [pow – vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                                                                          | 3                 |       | x          |              |     |
| [rcp – vergleicht](rcp---vs.md)                                                       | Gegenseitige                                                                                                                                                             | 1                 |       | x          |              |     |
| [rep – im Vergleich zu](rep---vs.md)                                                       | Repeat                                                                                                                                                                 | 3                 |       |            | x            |     |
| [ret – im Vergleich zu](ret---vs.md)                                                       | Ende einer Unterroutine oder main                                                                                                                                     | 1                 |       |            | x            |     |
| [rsq – vs](rsq---vs.md)                                                       | Reziproke Quadratwurzel                                                                                                                                                 | 1                 |       | x          |              |     |
| [setp \_ comp – vs](setp-comp---vs.md)                                          | Festlegen des Prädikatregisters                                                                                                                                             | 1                 |       |            | x            | x   |
| [sge – im Vergleich zu](sge---vs.md)                                                       | Größer als oder gleich vergleicht                                                                                                                                          | 1                 |       | x          |              |     |
| [sgn – vs](sgn---vs.md)                                                       | Signieren                                                                                                                                                                   | 3                 |       | x          |              |     |
| [sincos – vs](sincos---vs.md)                                                 | Sinus und Kosinus                                                                                                                                                        | 8                 |       | x          |              |     |
| [slt – vs](slt---vs.md)                                                       | Kleiner als vergleich                                                                                                                                                      | 1                 |       | x          |              |     |
| [sub – vs](sub---vs.md)                                                       | Subtrahieren                                                                                                                                                               | 1                 |       | x          |              |     |
| [Vs](vs---vs.md)                                                              | Version                                                                                                                                                                | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




