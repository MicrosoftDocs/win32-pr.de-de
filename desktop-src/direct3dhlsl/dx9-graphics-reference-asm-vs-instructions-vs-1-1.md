---
title: Anweisungen – vs_1_1
description: Dieser Abschnitt enthält Referenzinformationen für die Anweisungen zum Vertex-Shader Version \_ 1 1.
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f980640009158c6c4dc684158836d1514ca47755fea700ac7cc619f6e7574409
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789090"
---
# <a name="instructions---vs_1_1"></a>Anweisungen im Vergleich \_ zu 1 \_ 1

Dieser Abschnitt enthält Referenzinformationen für die Anweisungen zum Vertex-Shader Version \_ 1 1.

Es gibt verschiedene Typen von Vertex-Shaderanweisungen, wie in der Tabelle gezeigt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungsslots: Anzahl von Anweisungsslots, die von jeder Anweisung verwendet werden.
-   Setup: Nicht arithmetische Anweisungen. Jeder Shader muss über eine Versionsanweisung verfügen und die erste Anweisung sein.
-   Arithmetisch: Diese Anweisungen stellen die mathematischen Operationen in einem Shader zur Verfügung.
-   Neu: Diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                                           | Beschreibung                                                                                                     | Anweisungsslots | Setup | Arithmetik | Neu |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [hinzufügen – im Vergleich zu](add---vs.md)                                                       | Hinzufügen von zwei Vektoren                                                                                                 | 1                 |       | x          | x   |
| [dcl \_ usage input (sm1, sm2, sm3 – vs asm)](dcl-usage-input-register---vs.md) | Deklarieren von Eingabevertexregistern (siehe [Register – im Vergleich zu \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [def – vs](def---vs.md)                                                       | Definieren von Konstanten                                                                                                | 0                 | x     |            | x   |
| [dp3 – vs](dp3---vs.md)                                                       | Punktprodukt mit drei Komponenten                                                                                     | 1                 |       | x          | x   |
| [dp4 – vs](dp4---vs.md)                                                       | Punktprodukt mit vier Komponenten                                                                                      | 1                 |       | x          | x   |
| [dst – vs](dst---vs.md)                                                       | Berechnen des Entfernungsvektors                                                                                   | 1                 |       | x          | x   |
| [exp – vs](exp---vs.md)                                                       | Vollständige Genauigkeit 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp – vs](exp---vs.md)                                                       | Teilweise Genauigkeit 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [frc – vs](frc---vs.md)                                                       | Bruchkomponente                                                                                            | 3                 |       | x          | x   |
| [lit – vs](lit---vs.md)                                                       | Berechnung der Teilbeleuchtung                                                                                    | 1                 |       | x          | x   |
| [log – im Vergleich zu](log---vs.md)                                                       | Protokoll mit vollständiger genauigkeit₂(x)                                                                                          | 10                |       | x          | x   |
| [logp – vs](logp---vs.md)                                                     | Protokoll mit partieller Genauigkeit₂(x)                                                                                       | 1                 |       | x          | x   |
| [m3x2 – vs](m3x2---vs.md)                                                     | 3x2 multiplizieren                                                                                                    | 2                 |       | x          | x   |
| [m3x3 – vs](m3x3---vs.md)                                                     | 3x3 Multiplikation                                                                                                    | 3                 |       | x          | x   |
| [m3x4 – vs](m3x4---vs.md)                                                     | 3x4 Multiplikation                                                                                                    | 4                 |       | x          | x   |
| [m4x3 – vs](m4x3---vs.md)                                                     | 4x3 multiplizieren                                                                                                    | 3                 |       | x          | x   |
| [m4x4 – vs](m4x4---vs.md)                                                     | 4x4-Multiplikation                                                                                                    | 4                 |       | x          | x   |
| [mad – vs](mad---vs.md)                                                       | Multiplizieren und Hinzufügen                                                                                                | 1                 |       | x          | x   |
| [max – vs](max---vs.md)                                                       | Maximum                                                                                                         | 1                 |       | x          | x   |
| [min – vs](min---vs.md)                                                       | Minimum                                                                                                         | 1                 |       | x          | x   |
| [mov – vs](mov---vs.md)                                                       | Move                                                                                                            | 1                 |       | x          | x   |
| [mul – vs](mul---vs.md)                                                       | Multiplizieren                                                                                                        | 1                 |       | x          | x   |
| [nop – vs](nop---vs.md)                                                       | Keine Operation                                                                                                    | 1                 |       | x          | x   |
| [rcp – vs](rcp---vs.md)                                                       | Gegenseitige                                                                                                      | 1                 |       | x          | x   |
| [rsq – vs](rsq---vs.md)                                                       | Reziproke Quadratwurzel                                                                                          | 1                 |       | x          | x   |
| [sge – vs](sge---vs.md)                                                       | Größer als oder gleich im Vergleich                                                                                   | 1                 |       | x          | x   |
| [slt – vs](slt---vs.md)                                                       | Kleiner als vergleichen                                                                                               | 1                 |       | x          | x   |
| [sub – im Vergleich zu](sub---vs.md)                                                       | Subtrahieren                                                                                                        | 1                 |       | x          | x   |
| [Vs](vs---vs.md)                                                              | Version                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




