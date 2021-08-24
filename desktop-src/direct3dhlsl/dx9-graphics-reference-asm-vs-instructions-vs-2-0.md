---
title: Anweisungen – vs_2_0
description: Dieser Abschnitt enthält Referenzinformationen für die Vertex-Shader-Anweisungen in Version 2 \_ 0.
ms.assetid: f5ca3e44-3c71-4221-9381-cea521d984e0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0baaa0fb9523e59e3dafdb0a7dd1dd7856325c518f06995da4d768929982b6f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744470"
---
# <a name="instructions---vs_2_0"></a>Anweisungen im Vergleich zu \_ 2 \_ 0

Dieser Abschnitt enthält Referenzinformationen für die Vertex-Shader-Anweisungen in Version 2 \_ 0.

Es gibt mehrere Arten von Vertex-Shaderanweisungen, wie in der Tabelle gezeigt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungsslots: Anzahl von Anweisungsslots, die von jeder Anweisung verwendet werden.
-   Setup: Nicht arithmetische Anweisungen. Jeder Shader muss über eine Versionsanweisung verfügen und muss die erste Anweisung sein.
-   Arithmetisch: Diese Anweisungen stellen die mathematischen Operationen in einem Shader bereit.
-   Flow-Steuerelement: Diese Anweisungen fügen Flusssteuerungsfunktionen hinzu, z. B. [Schleife](loop---vs.md)... [endloop](endloop---vs.md), [wenn](if-bool---vs.md)... [else](else---vs.md)... [endif – im Vergleich zu](endif---vs.md)- und -Unterroutinenaufrufen.
-   Neu: Diese Anweisungen sind für diese Version neu.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                                           | Beschreibung                                                                                                     | Anweisungsslots | Einrichten | Arithmetik | Flusssteuerung | Neu |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [abs – im Vergleich zu](abs---vs.md)                                                       | Absoluter Wert                                                                                                  | 1                 |       | x          |              | x   |
| [add – im Vergleich zu](add---vs.md)                                                       | Hinzufügen von zwei Vektoren                                                                                                 | 1                 |       | x          |              |     |
| [call – vs](call---vs.md)                                                     | Aufrufen einer Unterroutine                                                                                               | 2                 |       |            | x            | x   |
| [callnz bool – vs](callnz-bool---vs.md)                                       | Aufrufen einer Unterroutine, wenn ein boolescher Register nicht 0 (null) ist                                                             | 3                 |       |            | x            | x   |
| [crs – vs](crs---vs.md)                                                       | Produktübergreifend                                                                                                   | 2                 |       | x          |              | x   |
| [dcl \_ usage input (sm1, sm2, sm3 - vs asm) (dcl usage input (sm1, sm2, sm3 – vs asm))](dcl-usage-input-register---vs.md) | Deklarieren von Eingabevertexregistern (siehe [Register – vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md)) | 0                 | x     |            |              |     |
| [def – vs](def---vs.md)                                                       | Definieren von Konstanten                                                                                                | 0                 | x     |            |              |     |
| [defb – vs](defb---vs.md)                                                     | Definieren einer booleschen Konstante                                                                                       | 0                 | x     |            |              | x   |
| [defi – vs](defi---vs.md)                                                     | Definieren einer ganzzahligen Konstante                                                                                      | 0                 | x     |            |              | x   |
| [dp3 – im Vergleich zu](dp3---vs.md)                                                       | Punktprodukt mit drei Komponenten                                                                                     | 1                 |       | x          |              |     |
| [dp4 – im Vergleich zu](dp4---vs.md)                                                       | Punktprodukt mit vier Komponenten                                                                                      | 1                 |       | x          |              |     |
| [dst – vs](dst---vs.md)                                                       | Berechnen des Entfernungsvektors                                                                                   | 1                 |       | x          |              |     |
| [else – im Vergleich zu](else---vs.md)                                                     | Starten einer [anderen - vs](else---vs.md) block                                                                       | 1                 |       |            | x            | x   |
| [endif – im Vergleich zu](endif---vs.md)                                                   | Beenden sie eine [if bool - vs](if-bool---vs.md)... [else – vs](else---vs.md) block                                      | 1                 |       |            | x            | x   |
| [endloop – vergleicht](endloop---vs.md)                                               | Ende einer [Schleife – vs](loop---vs.md) Block                                                                       | 2                 |       |            | x            | x   |
| [endrep – vs](endrep---vs.md)                                                 | Ende eines Wiederholungsblocks                                                                                           | 2                 |       |            | x            | x   |
| [exp – im Vergleich zu](exp---vs.md)                                                       | Vollständige Genauigkeit 2<sup>x</sup>                                                                                    | 1                 |       | x          |              |     |
| [exp – im Vergleich zu](exp---vs.md)                                                       | Teilgenauigkeit 2<sup>x</sup>                                                                                 | 1                 |       | x          |              |     |
| [frc – vs](frc---vs.md)                                                       | Bruchkomponente                                                                                            | 1                 |       | x          |              |     |
| [if bool – vs](if-bool---vs.md)                                               | Begin an [if bool - vs](if-bool---vs.md) block (using a Boolean condition)                                     | 3                 |       |            | x            | x   |
| [label – im Vergleich zu](label---vs.md)                                                   | Bezeichnung                                                                                                           | 0                 |       |            | x            | x   |
| [lit – vs](lit---vs.md)                                                       | Berechnung der Teilbeleuchtung                                                                                    | 3                 |       | x          |              |     |
| [log – im Vergleich zu](log---vs.md)                                                       | Protokoll mit vollständiger genauigkeit₂(x)                                                                                          | 1                 |       | x          |              |     |
| [logp – vs](logp---vs.md)                                                     | Log log₂(x) mit partieller Genauigkeit                                                                                       | 1                 |       | x          |              |     |
| [-Schleife im Vergleich zu](loop---vs.md)                                                     | Loop                                                                                                            | 3                 |       |            | x            | x   |
| [lrp – vs](lrp---vs.md)                                                       | Lineare Interpolation                                                                                            | 2                 |       | x          |              | x   |
| [m3x2 – vs](m3x2---vs.md)                                                     | 3x2 multiplizieren                                                                                                    | 2                 |       | x          |              |     |
| [m3x3 – vs](m3x3---vs.md)                                                     | 3x3 Multiplikation                                                                                                    | 3                 |       | x          |              |     |
| [m3x4 – vs](m3x4---vs.md)                                                     | 3x4 Multiplikation                                                                                                    | 4                 |       | x          |              |     |
| [m4x3 – vs](m4x3---vs.md)                                                     | 4x3 multiplizieren                                                                                                    | 3                 |       | x          |              |     |
| [m4x4 – vs](m4x4---vs.md)                                                     | 4x4-Multiplikation                                                                                                    | 4                 |       | x          |              |     |
| [mad – vs](mad---vs.md)                                                       | Multiplizieren und Hinzufügen                                                                                                | 1                 |       | x          |              |     |
| [max – vs](max---vs.md)                                                       | Maximum                                                                                                         | 1                 |       | x          |              |     |
| [min – vs](min---vs.md)                                                       | Minimum                                                                                                         | 1                 |       | x          |              |     |
| [mov – vs](mov---vs.md)                                                       | Move                                                                                                            | 1                 |       | x          |              |     |
| [mova – im Vergleich zu](mova---vs.md)                                                     | Verschieben von Daten aus einem Gleitkommaregister in das Adressregister (a0)                                           | 1                 |       | x          |              | x   |
| [mul – vs](mul---vs.md)                                                       | Multiplizieren                                                                                                        | 1                 |       | x          |              |     |
| [nop – vs](nop---vs.md)                                                       | Keine Operation                                                                                                    | 1                 |       | x          |              |     |
| [nrm – vs](nrm---vs.md)                                                       | Normalisieren eines 4D-Vektors                                                                                           | 3                 |       | x          |              | x   |
| [pow – vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                   | 3                 |       | x          |              | x   |
| [rcp – vs](rcp---vs.md)                                                       | Gegenseitige                                                                                                      | 1                 |       | x          |              |     |
| [rep – im Vergleich zu](rep---vs.md)                                                       | Repeat                                                                                                          | 3                 |       |            | x            | x   |
| [ret – vs](ret---vs.md)                                                       | Ende einer Unterroutine oder eines Main-Paars                                                                              | 1                 |       |            | x            | x   |
| [rsq – vs](rsq---vs.md)                                                       | Reziproke Quadratwurzel                                                                                          | 1                 |       | x          |              |     |
| [sge – vs](sge---vs.md)                                                       | Größer als oder gleich im Vergleich                                                                                   | 1                 |       | x          |              |     |
| [sgn – vs](sgn---vs.md)                                                       | Signieren                                                                                                            | 3                 |       | x          |              | x   |
| [sincos – vs](sincos---vs.md)                                                 | Sinus und Kosinus                                                                                                 | 8                 |       | x          |              | x   |
| [slt – vs](slt---vs.md)                                                       | Kleiner als vergleichen                                                                                               | 1                 |       | x          |              |     |
| [sub – im Vergleich zu](sub---vs.md)                                                       | Subtrahieren                                                                                                        | 1                 |       | x          |              |     |
| [Vs](vs---vs.md)                                                              | Version                                                                                                         | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




