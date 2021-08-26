---
title: ps_3_0-Anweisungen
description: Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shaderversion 3 \_ 0.
ms.assetid: 36972b9b-a4e7-45b4-83f5-959e75d270de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e44d13bfc726830a8c3fb770b34d5563fde2684f5c8bdf3fea54dec2312af4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982860"
---
# <a name="ps_3_0-instructions"></a>ps \_ 3 \_ 0 Instructions

Dieser Abschnitt enthält Referenzinformationen zu den Anweisungen für die Pixel-Shaderversion 3 \_ 0.

Es gibt verschiedene Arten von Shaderanweisungen für Pixel, wie in der Tabelle gezeigt. Spalten auf der rechten Seite bedeuten Folgendes:

-   Anweisungsslots: Anzahl von Anweisungsslots, die von jeder Anweisung verwendet werden.
-   Setup: Ein Pixel-Shader muss über eine Versionsanweisung verfügen, und er muss die erste Anweisung sein.
-   Arithmetisch: Diese Anweisungen stellen die mathematischen Operationen in einem Shader zur Verfügung.
-   Textur: Diese Anweisungen werden zum Laden und Abtasten von Texturdaten und zum Ändern von Texturkoordinaten verwendet.
-   Flow- und Ablaufsteuerung: Diese Anweisungen bieten statische und dynamische Flusssteuerung für die Ausführung von Anweisungen.
-   Neu: Diese Anweisungen sind neu in dieser Version.

## <a name="instruction-set"></a>Instruktionssatz



| Name                                                             | BESCHREIBUNG                                                                          | Anweisungsslots | Einrichten | Arithmetik | Struktur | Flusssteuerung | Neu |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [abs - ps](abs---ps.md)                                         | Absoluter Wert                                                                       | 1                 |       | x          |         |              |     |
| [add - ps](add---ps.md)                                         | Hinzufügen von zwei Vektoren                                                                      | 1                 |       | x          |         |              |     |
| [break – ps](break---ps.md)                                     | Break out of a loop... endloop oder rep... endrep-Block                                  | 1                 |       |            |         | x            |     |
| [break \_ comp - ps](break-comp---ps.md)                          | Bedingtes Ausbrechen einer Schleife... endloop oder rep... endrep-Block mit einem Vergleich | 3                 |       |            |         | x            |     |
| [breakp – ps](break-p---ps.md)                                  | Break out of a loop... endloop oder rep... endrep-Block basierend auf einem Prädikat            | 3                 |       |            |         | x            |     |
| [call – ps](call---ps.md)                                       | Aufrufen einer Unterroutine                                                                    | 2                 |       |            |         | x            |     |
| [callnz bool – ps](callnz-bool---ps.md)                         | Aufrufen einer Unterroutine, wenn ein boolescher Register nicht 0 (null) ist                                  | 3                 |       |            |         | x            |     |
| [callnz pred - ps](callnz-pred---ps.md)                         | Aufrufen einer Unterroutine, wenn ein Prädikatregister nicht 0 (null) ist                                | 3                 |       |            |         | x            |     |
| [cmp - ps](cmp---ps.md)                                         | Vergleichen der Quelle mit 0                                                                  | 1                 |       | x          |         |              |     |
| [crs - ps](crs---ps.md)                                         | Produktübergreifend                                                                        | 2                 |       | x          |         |              |     |
| [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) | Deklarieren der Texturdimension für einen Sampler                                          | 0                 | x     |            |         |              |     |
| [dcl \_ semantics (sm3 - ps asm)](dcl-usage---ps.md)              | Deklarieren von Eingabe- und Ausgaberegistern                                                   | 0                 | x     |            |         |              | x   |
| [def – ps](def---ps.md)                                         | Definieren von Konstanten                                                                     | 0                 | x     |            |         |              |     |
| [defb – ps](defb---ps.md)                                       | Definieren einer booleschen Konstante                                                            | 0                 | x     |            |         |              |     |
| [defi – ps](defi---ps.md)                                       | Definieren einer ganzzahligen Konstante                                                           | 0                 | x     |            |         |              |     |
| [dp2add – ps](dp2add---ps.md)                                   | 2D-Punktprodukt und Hinzufügen                                                               | 2                 |       | x          |         |              |     |
| [dp3 – ps](dp3---ps.md)                                         | 3D-Punktprodukt                                                                       | 1                 |       | x          |         |              |     |
| [dp4 – ps](dp4---ps.md)                                         | 4D-Punktprodukt                                                                       | 1                 |       | x          |         |              |     |
| [dsx – ps](dsx---ps.md)                                         | Änderungsrate in x-Richtung                                                    | 2                 |       | x          |         |              |     |
| [dsy - ps](dsy---ps.md)                                         | Änderungsrate in y-Richtung                                                    | 2                 |       | x          |         |              |     |
| [else – ps](else---ps.md)                                       | Starten eines else-Blocks                                                                  | 1                 |       |            |         | x            |     |
| [endif – ps](endif---ps.md)                                     | Beenden sie eine if... else-Block                                                               | 1                 |       |            |         | x            |     |
| [endloop – ps](endloop---ps.md)                                 | Beenden einer Schleife                                                                           | 2                 |       |            |         | x            | x   |
| [endrep – ps](endrep---ps.md)                                   | Ende eines Wiederholungsblocks                                                                | 2                 |       |            |         | x            |     |
| [exp – ps](exp---ps.md)                                         | Vollständige Genauigkeit 2<sup>x</sup>                                                         | 1                 |       | x          |         |              |     |
| [frc - ps](frc---ps.md)                                         | Bruchkomponente                                                                 | 1                 |       | x          |         |              |     |
| [if bool - ps](if-bool---ps.md)                                 | Starten eines if-Blocks                                                                    | 3                 |       |            |         | x            |     |
| [if \_ comp - ps](if-comp---ps.md)                                | Beginnen eines if-Blocks mit einem Vergleich                                                  | 3                 |       |            |         | x            |     |
| [if pred - ps](if-pred---ps.md)                                 | Beginnen eines if-Blocks mit Prädication                                                   | 3                 |       |            |         | x            |     |
| [label – ps](label---ps.md)                                     | Bezeichnung                                                                                | 0                 |       |            |         | x            |     |
| [log – ps](log---ps.md)                                         | Protokoll mit vollständiger genauigkeit₂(x)                                                               | 1                 |       | x          |         |              |     |
| [loop – ps](loop---ps.md)                                       | Loop                                                                                 | 3                 |       |            |         | x            | x   |
| [lrp – ps](lrp---ps.md)                                         | Lineare Interpolation                                                                   | 2                 |       | x          |         |              |     |
| [m3x2 – ps](m3x2---ps.md)                                       | 3x2 multiplizieren                                                                         | 2                 |       | x          |         |              |     |
| [m3x3 – ps](m3x3---ps.md)                                       | 3x3 Multiplikation                                                                         | 3                 |       | x          |         |              |     |
| [m3x4 – ps](m3x4---ps.md)                                       | 3x4 Multiplikation                                                                         | 4                 |       | x          |         |              |     |
| [m4x3 – ps](m4x3---ps.md)                                       | 4x3 multiplizieren                                                                         | 3                 |       | x          |         |              |     |
| [m4x4 – ps](m4x4---ps.md)                                       | 4x4-Multiplikation                                                                         | 4                 |       | x          |         |              |     |
| [mad – ps](mad---ps.md)                                         | Multiplizieren und Hinzufügen                                                                     | 1                 |       | x          |         |              |     |
| [max – ps](max---ps.md)                                         | Maximum                                                                              | 1                 |       | x          |         |              |     |
| [min – ps](min---ps.md)                                         | Minimum                                                                              | 1                 |       | x          |         |              |     |
| [mov – ps](mov---ps.md)                                         | Move                                                                                 | 1                 |       | x          |         |              |     |
| [mul – ps](mul---ps.md)                                         | Multiplizieren                                                                             | 1                 |       | x          |         |              |     |
| [nop - ps](nop---ps.md)                                         | Keine Operation                                                                         | 1                 |       | x          |         |              |     |
| [nrm - ps](nrm---ps.md)                                         | Normalize                                                                            | 3                 |       | x          |         |              |     |
| [pow – ps](pow---ps.md)                                         | x<sup>y</sup>                                                                        | 3                 |       | x          |         |              |     |
| [ps](ps---ps.md)                                                | Version                                                                              | 0                 | x     |            |         |              |     |
| [rcp – ps](rcp---ps.md)                                         | Gegenseitige                                                                           | 1                 |       | x          |         |              |     |
| [rep - ps](rep---ps.md)                                         | Repeat                                                                               | 3                 |       |            |         | x            |     |
| [ret – ps](ret---ps.md)                                         | Ende einer Unterroutine                                                                  | 1                 |       |            |         | x            |     |
| [rsq – ps](rsq---ps.md)                                         | Reziproke Quadratwurzel                                                               | 1                 |       | x          |         |              |     |
| [setp \_ comp](setp-comp---ps.md)                                 | Festlegen des Prädikatregisters                                                           | 1                 |       |            |         | x            |     |
| [sincos – ps](sincos---ps.md)                                   | Sinus und Kosinus                                                                      | 8                 |       | x          |         |              |     |
| [sub – ps](sub---ps.md)                                         | Subtrahieren                                                                             | 1                 |       | x          |         |              |     |
| [texkill - ps](texkill---ps.md)                                 | Pixelrendering ab kill                                                                    | 2                 |       |            | x       |              |     |
| [texld – ps \_ 2 \_ 0 und up](texld---ps-2-0.md)                    | Beispiel für eine Textur                                                                     | Siehe Hinweis 1        |       |            | x       |              |     |
| [texldb – ps](texldb---ps.md)                                   | Texturs sampling with level-of-detail bias from w-component                          | 6                 |       |            | x       |              |     |
| [texldl - ps](texldl---ps.md)                                   | Texturs sampling with level-of-detail from w-component (Textursyntmuster mit Detailebene von w-component)                               | Siehe Hinweis 2        |       |            | x       |              | x   |
| [texldd – ps](texldd---ps.md)                                   | Texturstichproben mit vom Benutzer bereitgestellten Farbverläufen                                        | 3                 |       |            | x       |              |     |
| [texldp – ps](texldp---ps.md)                                   | Texturs sampling with projective divide by w-component                               | Siehe Hinweis 3        |       |            | x       |              |     |



 

Hinweise:

1.  Wenn die Textur eine Cube map ist, slots = 4; andernfalls slots = 1.
2.  Wenn es sich bei der Textur um eine Cubemap handelt, werden Slots = 5; andernfalls slots = 2.
3.  Wenn die Textur eine Cube map ist, slots = 4; andernfalls slots = 3.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




