---
title: OpenGL-Verarbeitungspipeline
description: OpenGL-Verarbeitungspipeline
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL,Verarbeitungspipeline
- Processing Pipeline OpenGL
- Pipeline OpenGL
- framebuffers, Verarbeitungspipeline
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

Viele OpenGL-Funktionen werden speziell zum Zeichnen von Objekten wie Punkten, Linien, Polygonen und Bitmaps verwendet. Einige Funktionen steuern die Art und Weise, wie ein Teil dieser Zeichnung auftritt (z. B. solche, die Antialiasing oder Texturing ermöglichen). Andere Funktionen sind speziell auf framebuffer manipulation (Framebuffer-Manipulation) besennt. In den Themen in diesem Abschnitt wird beschrieben, wie alle OpenGL-Funktionen zusammenarbeiten, um die OpenGL-Verarbeitungspipeline zu erstellen. In diesem Abschnitt werden auch die Phasen näher erläutert, in denen Daten tatsächlich verarbeitet werden, und diese Phasen mit OpenGL-Funktionen verbunden.

Das folgende Diagramm zeigt die OpenGL-Verarbeitungspipeline. Für die meisten Pipelines werden drei vertikale Pfeile zwischen den Hauptstufen angezeigt. Diese Pfeile stellen Scheitelpfeile und die beiden primären Datentypen dar, die Scheitelungen zugeordnet werden können: Farbwerte und Texturkoordinaten. Beachten Sie auch, dass Scheitelpunkte zu Primitiven, dann zu Fragmenten und schließlich zu Pixeln im Framepuffer zusammengestellt werden. Dieser Fortschritt wird unter [](vertices.md)Scheitelpunkte, [Primitive,](primitives.md) [Fragmente und Pixel](fragments.md) [ausführlicher erläutert.](pixels.md)

![Diagramm, das die OpenGL-Verarbeitungspipeline zeigt.](images/proc01.png)

 

 




