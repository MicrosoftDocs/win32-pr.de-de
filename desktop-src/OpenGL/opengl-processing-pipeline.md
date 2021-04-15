---
title: OpenGL-Verarbeitungs Pipeline
description: OpenGL-Verarbeitungs Pipeline
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, Verarbeitungs Pipeline
- Pipeline-OpenGL wird verarbeitet
- Pipeline-OpenGL
- Framebuffers, Verarbeitungs Pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570571"
---
# <a name="opengl-processing-pipeline"></a>OpenGL-Verarbeitungs Pipeline

Viele OpenGL-Funktionen werden speziell zum Zeichnen von Objekten verwendet, z. b. Punkte, Linien, Polygone und Bitmaps. Einige Funktionen steuern die Art und Weise, wie einige dieser Zeichen auftreten (z. b. solche, die Antialiasing oder Texturierung ermöglichen). Andere Funktionen betreffen speziell die Frame Puffer-Bearbeitung. In den Themen in diesem Abschnitt wird beschrieben, wie alle OpenGL-Funktionen zusammenarbeiten, um die OpenGL-Verarbeitungs Pipeline zu erstellen. In diesem Abschnitt werden auch die Phasen, in denen die Daten tatsächlich verarbeitet werden, genauer betrachtet und diese Phasen mit OpenGL-Funktionen verknüpft.

Im folgenden Diagramm wird die OpenGL-Verarbeitungs Pipeline ausführlich erläutert. Für den Großteil der Pipeline können Sie drei vertikale Pfeile zwischen den Hauptphasen sehen. Diese Pfeile stellen Scheitel Punkte und die beiden primären Datentypen dar, die Vertices zugeordnet werden können: Farbwerte und Texturkoordinaten. Beachten Sie außerdem, dass Scheitel Punkte in primitive und dann in Fragmente und schließlich in Pixel im Framebuffer zusammengefasst werden. Diese fort [Schritte werden in](vertices.md)Scheitel Punkten, [primitiven](primitives.md), [Fragmenten](fragments.md)und [Pixeln](pixels.md)ausführlicher erläutert.

![Diagramm mit der OpenGL-Verarbeitungs Pipeline.](images/proc01.png)

 

 




