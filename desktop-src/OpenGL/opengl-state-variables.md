---
title: OpenGL-Zustandsvariablen
description: In den folgenden Themen werden die Namen von Zustandsvariablen aufgelistet, die abgefragt werden können.
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- OpenGL-Zustandsvariablen
- Zustandsvariablen, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342266"
---
# <a name="opengl-state-variables"></a>OpenGL-Zustandsvariablen

In den folgenden Themen werden die Namen von Zustandsvariablen aufgelistet, die abgefragt werden können:

-   [**Zustandsvariablen für aktuelle Werte und zugehörige Daten**](state-variables-for-current-values-and-associated-data.md)
-   [**Transformations Zustandsvariablen**](transformation-state-variables.md)
-   [**Farb Statusvariablen**](coloring-state-variables.md)
-   [**Beleuchtungs Zustandsvariablen**](lighting-state-variables.md)
-   [**Rasterization-Zustandsvariablen**](rasterization-state-variables.md)
-   [**Texturierungsstatusvariablen**](texturing-state-variables.md)
-   [**Pixel Vorgänge**](pixel-operations.md)
-   [**Statusvariablen des Framebuffer-Steuer Elements**](framebuffer-control-state-variables.md)
-   [**Pixel Zustandsvariablen**](pixel-state-variables.md)
-   [**Evaluatorstatusvariablen**](evaluator-state-variables.md)
-   [**Hinweis Zustandsvariablen**](hint-state-variables.md)
-   [**Implementierungs abhängige Zustandsvariablen**](implementation-dependent-state-variables.md)
-   [**Von der Implementierung abhängige Pixel-Depth Zustandsvariablen**](implementation-dependent-pixel-depth-state-variables.md)
-   [**Diverse Zustandsvariablen**](miscellaneous-state-variables.md)

Für jede Variable werden im Thema eine Beschreibung, eine Attribut Gruppe, ein ursprünglicher oder ein Minimalwert sowie die vorgeschlagene Funktion " [**glget \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) " aufgeführt, die für die Beschaffung verwendet werden soll.

Zustandsvariablen, die Sie mit " [**glgetbooleanv**](glgetbooleanv.md)", " [**glgetintegerv**](glgetintegerv.md)", " [**glgetfloatv**](glgetfloatv.md)" oder " [**glgetdoublev**](glgetdoublev.md) " abrufen können, werden mit nur einer dieser Funktionalitäten aufgelistet, die am besten für den Typ der zurück zugegenden Daten geeignet ist. Diese Zustandsvariablen können nicht mithilfe von " [**glisenabled**](glisenabled.md)" abgerufen werden. Sie können jedoch Zustandsvariablen abrufen, für die " **glisenabled** " als Abfragefunktion mit " **glgetbooleanv**", " **glgetintegerv**", " **glgetfloatv**" und " **glgetdoublev**" aufgeführt ist. Mit dieser Funktion können Sie Zustandsvariablen abrufen, für die eine andere Funktion als Abfragefunktion aufgeführt ist. Wenn keine Attribut Gruppe aufgeführt ist, gehört die Variable keiner Gruppe an. Alle Zustandsvariablen, die Sie Abfragen können, mit Ausnahme derjenigen, die von der Implementierung abhängen, haben Anfangswerte. Um den Anfangswert einer Variablen zu ermitteln, für die kein Anfangswert aufgelistet ist, lesen Sie den Verweis der Variablen oder den

*OpenGL-Referenzhandbuch*.

 

 




