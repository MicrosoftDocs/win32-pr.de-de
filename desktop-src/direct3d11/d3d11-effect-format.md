---
title: Effect-Format (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: Weitere Informationen zu Effect Format (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7644e433f6c19df20cb2417659cf575e0613f93b0d53f6494ad6ee1422a55b9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792070"
---
# <a name="effect-format-direct3d-11"></a>Effect-Format (Direct3D 11)

Ein Effekt (der häufig in einer Datei mit der Dateierweiterung .fx gespeichert wird) deklariert den durch einen Effekt festgelegten Pipelinezustand. Der Effektzustand kann grob in drei Kategorien unterteilt werden:

-   Variablen , die in der Regel am Anfang eines [Effekts](d3d11-effect-variable-syntax.md)deklariert werden.
-   [Funktionen,](d3d11-effect-function-syntax.md)die Shadercode implementieren oder von anderen Funktionen als Hilfsfunktionen verwendet werden.
-   [Techniken,](d3d11-effect-technique-syntax.md)die in Effektgruppen angeordnet werden können, und implementieren Renderingsequenzen mit einem oder mehr Effektüberläufen. Jeder Durchgang legt eine oder mehrere [Zustandsgruppen fest](d3d11-effect-states.md) und ruft Shaderfunktionen auf.

![Diagramm der Kategorien von Deklarationen für Effekte, einschließlich Variablen oben, Funktionen in der Mitte und Techniken am unteren Rand](images/d3d10-effect-intro.png)

Das obige Diagramm zeigt die Kategorien des Effektzustands.

Die Definition des Effektbinärformats finden Sie in Binary \\ EffectBinaryFormat.h im Quellcode der Effekte.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                   | Beschreibung                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Syntax der Effect-Variablen](d3d11-effect-variable-syntax.md)<br/>   | Eine Effect-Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>                                 |
| [Anmerkungssyntax](d3d11-effect-annotation-syntax.md)<br/>      | Eine Anmerkung ist eine benutzerdefinierte Information, die mit der in diesem Abschnitt beschriebenen Syntax deklariert wird.<br/> |
| [Effect-Funktionssyntax](d3d11-effect-function-syntax.md)<br/>   | Eine Effect-Funktion ist in HLSL geschrieben und wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>          |
| [Syntax der Effekttechnik](d3d11-effect-technique-syntax.md)<br/> | Eine Effekttechnik wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>                                |
| [Auswirkungszustandsgruppen](d3d11-effect-states.md)<br/>               | Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.<br/>                                          |
| [Syntax der Effektgruppe](d3d11-effect-group-syntax.md)<br/>         | Eine Effektgruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.<br/>                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Effekten 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





