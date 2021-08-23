---
title: OpenGL-Standardvorgang
description: OpenGL-Standardvorgang
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, grundlegende Vorgänge
- OpenGL,Datenverarbeitung
- OpenGL,Verarbeitungsphasen
- OpenGL, Listen anzeigen
- Anzeigelisten OpenGL
- OpenGL,Evaluators
- Evaluators OpenGL
- OpenGL-Vorgänge pro Scheitelpunkt
- Pro-Scheitelpunkt-Vorgänge OpenGL
- OpenGL,primitive Assembly
- Primitive Assembly OpenGL
- OpenGL, Rasterisierung
- Rasterung von OpenGL
- OpenGL-Vorgänge pro Fragment
- OpenGL-Vorgänge pro Fragment
- framebuffers,basic operations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72f6abed7d06a93985b798e72efbf4d6ec0901e7ad9fb4614f5bf81590cefcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554715"
---
# <a name="basic-opengl-operation"></a>OpenGL-Standardvorgang

Das folgende Diagramm veranschaulicht, wie OpenGL Daten verarbeitet. Wie gezeigt, geben Befehle von links ein und fahren mit einer Verarbeitungspipeline fort. Einige Befehle geben geometrische Objekte an, die gezeichnet werden sollen, und andere steuern, wie die Objekte in verschiedenen Verarbeitungsphasen behandelt werden.

![Diagramm, das die Phasen der OpenGL-Datenverarbeitungspipeline zeigt.](images/basic01.png)

Die Verarbeitungsphasen im grundlegenden OpenGL-Vorgang lauten wie folgt:

-   **Anzeigeliste** Anstatt alle Befehle sofort über die Pipeline ausführen zu lassen, können Sie einige davon zur späteren Verarbeitung in einer Anzeigeliste sammeln.
-   **Auswertung** Die Auswertungsphase der Verarbeitung bietet eine effiziente Möglichkeit zur Ungefährung der Kurven- und Oberflächengeometrie, indem polynomiale Befehle von Eingabewerten bewertet werden.
-   **Vorgänge pro Scheitelpunkt und primitive Assembly** OpenGL verarbeitet geometrische Primitivepunkte, Liniensegmente und Polygone, von denen alle durch Scheitelpunkte beschrieben werden. Scheitelungen werden transformiert und beleuchtet, und Primitive werden als Vorbereitung für die Rasterung am Viewport abgeschnitten.
-   **Rasterung** Die Rasterungsphase erzeugt eine Reihe von Framepufferadressen und zugeordneten Werten unter Verwendung einer zweidimensionalen Beschreibung eines Punkts, Liniensegments oder Polygons. Jedes so erzeugte Fragment wird in die letzte Phase der Vorgänge pro Fragment eingespeist.
-   **Vorgänge pro Fragment** Dies sind die letzten Vorgänge, die für die Daten ausgeführt werden, bevor sie als Pixel im Framepuffer gespeichert werden.

    Vorgänge pro Fragment umfassen bedingte Aktualisierungen des Framepuffers basierend auf eingehenden und zuvor gespeicherten z-Werten (für Z-Pufferung) und dem Mischen eingehender Pixelfarben mit gespeicherten Farben sowie maskieren und andere logische Vorgänge für Pixelwerte.

Daten können in Form von Pixeln anstelle von Scheitelpunkten eingegeben werden. Daten in Form von Pixeln, z. B. beschreiben ein Bild zur Verwendung in der Texturzuordnung, überspringen die oben beschriebene erste Verarbeitungsphase und werden stattdessen in der Pixelvorgänge-Phase als Pixel verarbeitet. Bei den folgenden Pixelvorgängen sind die Pixeldaten entweder:

-   Wird als Texturspeicher für die Verwendung in der Rasterphase gespeichert.
-   Rastert, bei dem die resultierenden Fragmente im Framepuffer zusammengeführt werden, als würden sie aus geometrischen Daten generiert.

 

 




