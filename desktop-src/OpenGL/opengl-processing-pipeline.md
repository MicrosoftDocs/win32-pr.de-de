---
title: OpenGL-Verarbeitungspipeline
description: OpenGL-Verarbeitungspipeline
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, Verarbeitungspipeline
- Verarbeitungspipeline OpenGL
- OpenGL-Pipeline
- Framepuffer, Verarbeitungspipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b52568de344404e9bddbedbacc40beda064b09d3e3af96c2657f670e677c32a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936864"
---
# <a name="opengl-processing-pipeline"></a>OpenGL-Verarbeitungspipeline

Viele OpenGL-Funktionen werden speziell zum Zeichnen von Objekten wie Punkten, Linien, Polygonen und Bitmaps verwendet. Einige Funktionen steuern die Art und Weise, wie ein Teil dieser Zeichnung auftritt (z. B. solche, die Antialiasing oder Texturierung ermöglichen). Andere Funktionen befassen sich speziell mit der Framepufferbearbeitung. In den Themen in diesem Abschnitt wird beschrieben, wie alle OpenGL-Funktionen zusammenarbeiten, um die OpenGL-Verarbeitungspipeline zu erstellen. In diesem Abschnitt werden auch die Phasen näher betrachtet, in denen Daten tatsächlich verarbeitet werden, und diese Phasen werden mit OpenGL-Funktionen verknüpft.

Im folgenden Diagramm wird die OpenGL-Verarbeitungspipeline ausführlich dargestellt. Für die meisten Pipelines werden drei vertikale Pfeile zwischen den Hauptphasen angezeigt. Diese Pfeile stellen Scheitelpunkte und die beiden primären Datentypen dar, die Scheitelpunkten zugeordnet werden können: Farbwerte und Texturkoordinaten. Beachten Sie auch, dass Scheitelpunkte zu Primitiven, dann zu Fragmenten und schließlich zu Pixeln im Framepuffer zusammengestellt werden. Dieser Fortschritt wird unter [Scheitelpunkte,](vertices.md) [Primitive,](primitives.md) [Fragmente](fragments.md)und [Pixel](pixels.md)ausführlicher erläutert.

![Diagramm der OpenGL-Verarbeitungspipeline](images/proc01.png)

 

 




