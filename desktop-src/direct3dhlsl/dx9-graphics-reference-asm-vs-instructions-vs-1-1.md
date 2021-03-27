---
title: Anweisungen-vs_1_1
description: Dieser Abschnitt enthält Referenzinformationen für die Anweisungen der Vertex-Shader-Version 1 \_ 1.
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b4def55dfaca19608599d9c79e20d3e0690832c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104975929"
---
# <a name="instructions---vs_1_1"></a>Anweisungen-vs \_ 1 \_ 1

Dieser Abschnitt enthält Referenzinformationen für die Anweisungen der Vertex-Shader-Version 1 \_ 1.

Es gibt mehrere Arten von Vertex-shaderanweisungen, wie in der Tabelle dargestellt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungs Slots: Anzahl der Anweisungs Slots, die von jeder Anweisung verwendet werden.
-   Setup: nicht arithmetische Anweisungen. Jeder Shader muss über eine Versions Anweisung verfügen, und er muss die erste Anweisung sein.
-   Arithmetik: diese Anweisungen bieten die mathematischen Vorgänge in einem Shader.
-   Neu: diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                                           | BESCHREIBUNG                                                                                                     | Anweisungs Slots | Einrichten | Arithmetik | Neu |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [Add-vs](add---vs.md)                                                       | Hinzufügen von zwei Vektoren                                                                                                 | 1                 |       | x          | x   |
| [DCL- \_ Verwendungs Eingabe (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Deklarieren von Vertex-Eingabe Registern (siehe [Register-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [DEF-vs](def---vs.md)                                                       | Definieren von Konstanten                                                                                                | 0                 | x     |            | x   |
| [DP3-vs](dp3---vs.md)                                                       | 3-Komponenten-Punktprodukt                                                                                     | 1                 |       | x          | x   |
| [DP4-vs](dp4---vs.md)                                                       | Punktprodukt mit vier Komponenten                                                                                      | 1                 |       | x          | x   |
| [DST-vs](dst---vs.md)                                                       | Berechnen des Entfernungs Vektors                                                                                   | 1                 |       | x          | x   |
| [Exp-vs](exp---vs.md)                                                       | Vollständige Genauigkeit 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [Exp-vs](exp---vs.md)                                                       | Partielle Genauigkeit 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [FRC-vs](frc---vs.md)                                                       | Bruchteile                                                                                            | 3                 |       | x          | x   |
| [Lit-vs](lit---vs.md)                                                       | Berechnung der partiellen Beleuchtung                                                                                    | 1                 |       | x          | x   |
| [Log-vs](log---vs.md)                                                       | Protokoll der vollständigen Genauigkeit (x)                                                                                          | 10                |       | x          | x   |
| [LogP-vs](logp---vs.md)                                                     | Protokoll der partiellen Genauigkeit (x)                                                                                       | 1                 |       | x          | x   |
| [m3x2-vs](m3x2---vs.md)                                                     | 3 x 2 multiplizieren                                                                                                    | 2                 |       | x          | x   |
| [M3x3-vs](m3x3---vs.md)                                                     | 3X3 multiplizieren                                                                                                    | 3                 |       | x          | x   |
| [M3x4-vs](m3x4---vs.md)                                                     | rund m3 multiplizieren                                                                                                    | 4                 |       | x          | x   |
| [m4x3-vs](m4x3---vs.md)                                                     | 4 x 3 multiplizieren                                                                                                    | 3                 |       | x          | x   |
| [M4x4-vs](m4x4---vs.md)                                                     | 4 x 4 multiplizieren                                                                                                    | 4                 |       | x          | x   |
| [Mad-vs](mad---vs.md)                                                       | Multiplizieren und hinzufügen                                                                                                | 1                 |       | x          | x   |
| [Max-vs](max---vs.md)                                                       | Maximum                                                                                                         | 1                 |       | x          | x   |
| [min-vs](min---vs.md)                                                       | Minimum                                                                                                         | 1                 |       | x          | x   |
| [MOV (VS)](mov---vs.md)                                                       | Move                                                                                                            | 1                 |       | x          | x   |
| [Mul-vs](mul---vs.md)                                                       | Multiplizieren                                                                                                        | 1                 |       | x          | x   |
| [NOP-vs](nop---vs.md)                                                       | Keine Operation                                                                                                    | 1                 |       | x          | x   |
| [RCP-vs](rcp---vs.md)                                                       | Reziproke                                                                                                      | 1                 |       | x          | x   |
| [RSQ-vs](rsq---vs.md)                                                       | Gegenseitige Quadratwurzel                                                                                          | 1                 |       | x          | x   |
| [SGE-vs](sge---vs.md)                                                       | Vergleich größer als oder gleich                                                                                   | 1                 |       | x          | x   |
| [SLT-vs](slt---vs.md)                                                       | Kleiner als Vergleich                                                                                               | 1                 |       | x          | x   |
| [Sub-vs](sub---vs.md)                                                       | Subtrahieren                                                                                                        | 1                 |       | x          | x   |
| [Jews](vs---vs.md)                                                              | Version                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




