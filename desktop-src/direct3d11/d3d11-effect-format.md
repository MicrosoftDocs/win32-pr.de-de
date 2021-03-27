---
title: Effekt Format (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Weitere Informationen zum: Effekt Format (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214134"
---
# <a name="effect-format-direct3d-11"></a>Effekt Format (Direct3D 11)

Ein Effekt (der häufig in einer Datei mit der Dateierweiterung ". FX" gespeichert ist) deklariert den Pipeline Status, der durch einen Effekt festgelegt wird. Der Effekt Zustand kann ungefähr in drei Kategorien unterteilt werden:

-   [Variablen](d3d11-effect-variable-syntax.md), die in der Regel am Anfang eines Effekts deklariert werden.
-   [Funktionen](d3d11-effect-function-syntax.md), die Shader-Code implementieren oder von anderen Funktionen als Hilfsfunktionen verwendet werden.
-   [Techniken](d3d11-effect-technique-syntax.md), die in Wirkungs Gruppen angeordnet werden können, und Implementieren von renderingsequenzen mithilfe mindestens eines Effekts. Jeder Durchlauf legt eine oder mehrere [Zustands Gruppen fest](d3d11-effect-states.md) und ruft Shaderfunktionen auf.

![Diagramm der Kategorien von Deklarationen für Effekte, einschließlich Variablen oben, Funktionen in der Mitte und Techniken im unteren Bereich](images/d3d10-effect-intro.png)

Das obige Diagramm zeigt die Kategorien des Wirkungs Zustands.

Die Definition des Effekt Binär Formats finden Sie in \\ der "effectbinaryformat. h"-Datei im Effekt Quell Code.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                   | BESCHREIBUNG                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Syntax der Effekt Variablen](d3d11-effect-variable-syntax.md)<br/>   | Eine Effekt Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>                                 |
| [Syntax der Anmerkung](d3d11-effect-annotation-syntax.md)<br/>      | Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der in diesem Abschnitt beschriebenen Syntax deklariert wird.<br/> |
| [Syntax der Effekt Funktion](d3d11-effect-function-syntax.md)<br/>   | Eine Effekt Funktion ist in HLSL geschrieben und wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>          |
| [Syntax der Effekt Technik](d3d11-effect-technique-syntax.md)<br/> | Eine Effekt Technik wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>                                |
| [Effekt Zustands Gruppen](d3d11-effect-states.md)<br/>               | Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.<br/>                                          |
| [Effekt Gruppen Syntax](d3d11-effect-group-syntax.md)<br/>         | Eine Effekt Gruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswirkung 11-Referenz](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





