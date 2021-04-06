---
title: Grundlegender OpenGL-Vorgang
description: Grundlegender OpenGL-Vorgang
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, grundlegende Vorgänge
- OpenGL, Datenverarbeitung
- OpenGL, Verarbeitungsphasen
- OpenGL, Anzeigen von Listen
- Anzeigelisten OpenGL
- OpenGL, Evaluators
- Evaluatoren OpenGL
- OpenGL-Vorgänge pro Scheitelpunkt
- pro-Vertex-Vorgänge OpenGL
- OpenGL, primitive Assembly
- primitiver Assembly OpenGL
- OpenGL, rasterization
- Rasterung OpenGL
- OpenGL-Vorgänge pro Fragment
- pro-Fragment-Vorgänge OpenGL
- Framebuffers, grundlegende Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961072"
---
# <a name="basic-opengl-operation"></a>Grundlegender OpenGL-Vorgang

Im folgenden Diagramm wird veranschaulicht, wie OpenGL Daten verarbeitet. Wie gezeigt, geben Befehle von Links aus ein und durchlaufen eine Verarbeitungs Pipeline. Einige Befehle geben geometrische Objekte an, die gezeichnet werden sollen, und andere Steuern, wie die Objekte während verschiedener Verarbeitungsphasen behandelt werden.

![Diagramm mit den OpenGL-Datenverarbeitungs-Pipeline Stufen.](images/basic01.png)

Die Verarbeitungsstufen im grundlegenden OpenGL-Vorgang lauten wie folgt:

-   **Liste anzeigen** Anstatt alle Befehle direkt durch die Pipeline zu übertragen, können Sie einige davon in einer Anzeigeliste für die spätere Verarbeitung sammeln.
-   **Evaluator** Die Auswertungs Phase der Verarbeitung bietet eine effiziente Möglichkeit, um die Kurven-und Oberflächengeometrie durch Auswerten von polynomialen Befehlen von Eingabe Werten zu berechnen.
-   **Pro-Vertex-Vorgänge und primitive Assembly** OpenGL verarbeitet geometrische primitivespunkte, Liniensegmente und polygonsalle, die von Vertices beschrieben werden. Vertices werden transformiert und beleuchtet, und primitive werden auf den Viewport zugeschnitten, um die rasterisierung vorzubereiten.
-   **Rasterisierung** Die Rasterung-Phase erzeugt eine Reihe von Frame Puffer Adressen und zugeordneten Werten unter Verwendung einer zweidimensionalen Beschreibung eines Punkts, eines Linien Segments oder eines Polygons. Jedes Fragment, das erstellt wird, wird in die letzte Phase, pro-Fragment-Vorgängen, eingefügt.
-   **Vorgänge pro Fragment** Dies sind die abschließenden Vorgänge, die für die Daten ausgeführt werden, bevor Sie als Pixel im Framebuffer gespeichert werden.

    Pro-Fragment-Vorgänge enthalten bedingte Aktualisierungen des framepufferers auf der Grundlage eingehender und zuvor gespeicherter z-Werte (bei z-Pufferung) und der Mischung eingehender Pixel Farben mit gespeicherten Farben sowie Maskierung und anderen logischen Vorgängen bei Pixelwerten.

Daten können in Form von Pixeln anstelle von Vertices eingegeben werden. Daten in Form von Pixeln, wie z. b. ein Bild zur Verwendung in der Textur Zuordnung beschreiben, überspringen die erste Phase der oben beschriebenen Verarbeitung und werden stattdessen als Pixel in der Phase Pixel Vorgänge verarbeitet. Die Pixeldaten sind folgende Pixel Vorgänge:

-   Wird als Texturspeicher für die Verwendung in der Rasterung-Phase gespeichert.
-   Rasterized, wobei die resultierenden Fragmente in den Frame Puffer zusammengeführt werden, als ob Sie aus geometrischen Daten generiert wurden.

 

 




