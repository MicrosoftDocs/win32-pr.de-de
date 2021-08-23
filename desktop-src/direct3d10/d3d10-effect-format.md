---
description: Ein Effekt (der häufig in einer Datei mit der Dateierweiterung .fx gespeichert wird) deklariert den durch einen Effekt festgelegten Pipelinezustand.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Effect-Format (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c9511304a3c24784381092017659fb1a6c593808253383443c8e9f6917c2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852825"
---
# <a name="effect-format-direct3d-10"></a>Effect-Format (Direct3D 10)

Ein Effekt (der häufig in einer Datei mit der Dateierweiterung .fx gespeichert wird) deklariert den durch einen Effekt festgelegten Pipelinezustand. Der Effektzustand kann grob in drei Kategorien unterteilt werden:

-   Variablen , die in der Regel am Anfang eines [Effekts](d3d10-effect-variable-syntax.md)deklariert werden.
-   [Funktionen,](d3d10-effect-function-syntax.md)die Shadercode implementieren oder von anderen Funktionen als Hilfsfunktionen verwendet werden.
-   [Ein Verfahren,](d3d10-effect-technique-syntax.md)das Renderingsequenzen mit einem oder mehr Effektüberläufen implementiert. Jeder Durchgang legt eine oder mehrere [Zustandsgruppen fest](d3d10-effect-states.md) und ruft Shaderfunktionen auf.

![Diagramm der Kategorien des Effektzustands](images/d3d10-effect-intro.png)

Das obige Diagramm zeigt die Kategorien des Effektzustands.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Effekten](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



