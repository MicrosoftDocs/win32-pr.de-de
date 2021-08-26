---
title: ps_2_0-Anweisungen
description: Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shaderversion 2 \_ 0.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 292263ed6331c8cc878d6dbd9cfa3e4d766c193d2242b841afb926b296675ccf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067990"
---
# <a name="ps_2_0-instructions"></a>ps \_ 2 \_ 0 Instructions

Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shaderversion 2 \_ 0.

Es gibt verschiedene Arten von Shaderanweisungen für Pixel, wie in der Tabelle gezeigt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungsslots: Anzahl von Anweisungsslots, die von jeder Anweisung verwendet werden.
-   Setup: Ein Pixel-Shader muss über eine Versionsanweisung verfügen, und er muss die erste Anweisung sein.
-   Arithmetisch: Diese Anweisungen stellen die mathematischen Operationen in einem Shader zur Verfügung.
-   Textur: Diese Anweisungen werden zum Laden und Abtasten von Texturdaten und zum Ändern von Texturkoordinaten verwendet.
-   Neu: Diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                             | BESCHREIBUNG                                                                                      | Anweisungsslots | Einrichten | Arithmetik | Struktur | Neu |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [abs - ps](abs---ps.md)                                         | Absoluter Wert                                                                                   | 1                 |       | x          |         | x   |
| [add - ps](add---ps.md)                                         | Hinzufügen von zwei Vektoren                                                                                  | 1                 |       | x          |         |     |
| [cmp - ps](cmp---ps.md)                                         | Vergleichen der Quelle mit 0                                                                              | 1                 |       | x          |         |     |
| [crs - ps](crs---ps.md)                                         | Produktübergreifend                                                                                    | 2                 |       | x          |         | x   |
| [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) | Deklarieren der Texturdimension für einen Sampler                                                      | 0                 | x     |            |         | x   |
| [dcl - (sm2, sm3 - ps asm)](dcl---ps.md)                        | Deklarieren Sie die Zuordnung zwischen Vertex-Shader-Ausgaberegistern und Pixel-Shader-Eingaberegistern. | 0                 | x     |            |         | x   |
| [def – ps](def---ps.md)                                         | Definieren von Konstanten                                                                                 | 0                 | x     |            |         |     |
| [dp2add – ps](dp2add---ps.md)                                   | 2D-Punktprodukt und Hinzufügen                                                                           | 2                 |       | x          |         | x   |
| [dp3 – ps](dp3---ps.md)                                         | 3D-Punktprodukt                                                                                   | 1                 |       | x          |         |     |
| [dp4 – ps](dp4---ps.md)                                         | 4D-Punktprodukt                                                                                   | 1                 |       | x          |         |     |
| [exp – ps](exp---ps.md)                                         | Vollständige Genauigkeit 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [frc - ps](frc---ps.md)                                         | Bruchkomponente                                                                             | 1                 |       | x          |         | x   |
| [log – ps](log---ps.md)                                         | Protokoll mit vollständiger genauigkeit₂(x)                                                                           | 1                 |       | x          |         | x   |
| [lrp – ps](lrp---ps.md)                                         | Lineare Interpolation                                                                               | 2                 |       | x          |         |     |
| [m3x2 – ps](m3x2---ps.md)                                       | 3x2 multiplizieren                                                                                     | 2                 |       | x          |         | x   |
| [m3x3 – ps](m3x3---ps.md)                                       | 3x3 Multiplikation                                                                                     | 3                 |       | x          |         | x   |
| [m3x4 – ps](m3x4---ps.md)                                       | 3x4 Multiplikation                                                                                     | 4                 |       | x          |         | x   |
| [m4x3 – ps](m4x3---ps.md)                                       | 4x3 multiplizieren                                                                                     | 3                 |       | x          |         | x   |
| [m4x4 – ps](m4x4---ps.md)                                       | 4x4 multiplizieren                                                                                     | 4                 |       | x          |         | x   |
| [mad - ps](mad---ps.md)                                         | Multiplizieren und Hinzufügen                                                                                 | 1                 |       | x          |         |     |
| [max – ps](max---ps.md)                                         | Maximum                                                                                          | 1                 |       | x          |         | x   |
| [min – ps](min---ps.md)                                         | Minimum                                                                                          | 1                 |       | x          |         | x   |
| [mov – ps](mov---ps.md)                                         | Move                                                                                             | 1                 |       | x          |         |     |
| [mul - ps](mul---ps.md)                                         | Multiplizieren                                                                                         | 1                 |       | x          |         |     |
| [nop - ps](nop---ps.md)                                         | Keine Operation                                                                                     | 1                 |       | x          |         |     |
| [nrm - ps](nrm---ps.md)                                         | Normalize                                                                                        | 3                 |       | x          |         | x   |
| [pow – ps](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [ps](ps---ps.md)                                                | Version                                                                                          | 0                 | x     |            |         |     |
| [rcp – ps](rcp---ps.md)                                         | Gegenseitige                                                                                       | 1                 |       | x          |         | x   |
| [rsq - ps](rsq---ps.md)                                         | Reziproke Quadratwurzel                                                                           | 1                 |       | x          |         | x   |
| [sincos – ps](sincos---ps.md)                                   | Sinus und Kosinus                                                                                  | 8                 |       | x          |         | x   |
| [sub – ps](sub---ps.md)                                         | Subtrahieren                                                                                         | 1                 |       | x          |         |     |
| [texkill - ps](texkill---ps.md)                                 | Rendern des Kill-Pixels                                                                                | 1                 |       |            | x       |     |
| [texld – ps \_ 2 \_ 0 und mehr](texld---ps-2-0.md)                    | Beispiel für eine Textur                                                                                 | 1                 |       |            | x       | x   |
| [texldb – ps](texldb---ps.md)                                   | Textursampling mit Detailgenauigkeitsvoreingenommenheit von w-component                                      | 1                 |       |            | x       | x   |
| [texldp – ps](texldp---ps.md)                                   | Textursampling mit projektiver Division durch w-Komponente                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




