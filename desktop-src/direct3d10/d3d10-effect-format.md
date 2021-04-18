---
description: Ein Effekt (der häufig in einer Datei mit der Dateierweiterung ". FX" gespeichert ist) deklariert den Pipeline Status, der durch einen Effekt festgelegt wird.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Effekt Format (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393221"
---
# <a name="effect-format-direct3d-10"></a>Effekt Format (Direct3D 10)

Ein Effekt (der häufig in einer Datei mit der Dateierweiterung ". FX" gespeichert ist) deklariert den Pipeline Status, der durch einen Effekt festgelegt wird. Der Effekt Zustand kann ungefähr in drei Kategorien unterteilt werden:

-   [Variablen](d3d10-effect-variable-syntax.md), die in der Regel am Anfang eines Effekts deklariert werden.
-   [Funktionen](d3d10-effect-function-syntax.md), die Shader-Code implementieren oder von anderen Funktionen als Hilfsfunktionen verwendet werden.
-   [Eine Technik](d3d10-effect-technique-syntax.md), die renderingsequenzen mit einem oder mehreren Effekt Sequenzen implementiert. Jeder Durchlauf legt eine oder mehrere [Zustands Gruppen fest](d3d10-effect-states.md) und ruft Shaderfunktionen auf.

![Diagramm der Kategorien des Wirkungs Zustands](images/d3d10-effect-intro.png)

Das obige Diagramm zeigt die Kategorien des Wirkungs Zustands.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Referenz](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



