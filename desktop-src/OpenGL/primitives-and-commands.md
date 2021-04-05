---
title: Primitive und Befehle
description: Primitive und Befehle
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitive
- OpenGL, Befehle
- Primitives OpenGL
- Befehle OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709461"
---
# <a name="primitives-and-commands"></a>Primitive und Befehle

OpenGL zeichnet *primitive* Punkte, Liniensegmente oder polygonssubject in mehreren auswählbaren Modi. Sie können Modi unabhängig voneinander steuern. Das Festlegen eines Modus wirkt sich nicht darauf aus, ob andere Modi festgelegt sind (obwohl viele Modi interagieren können, um zu bestimmen, was letztendlich im Framebuffer endet). Um primitive anzugeben, Modi festzulegen und andere OpenGL-Vorgänge auszuführen, geben Sie Befehle in Form von Funktionsaufrufen aus.

Primitive werden durch eine Gruppe mit einem oder mehreren *Vertices* definiert. Ein Scheitelpunkt definiert einen Punkt, einen Endpunkt einer Linie oder eine Ecke eines Polygons, in dem zwei Ränder übereinstimmen. Daten (bestehend aus Scheitelpunkt Koordinaten, Farben, normellen, Texturkoordinaten und randflags) werden einem Scheitelpunkt zugeordnet, und jeder Scheitelpunkt und die zugehörigen Daten werden unabhängig voneinander und in der richtigen Reihenfolge verarbeitet. Die einzige Ausnahme von dieser Regel sind Fälle, in denen die Gruppe der Vertices abgeschnitten werden muss, damit ein bestimmtes primitiv in einen angegebenen Bereich passt. In diesem Fall können Scheitelpunkt Daten geändert und neue Vertices erstellt werden. Der clippingtyp hängt davon ab, welches primitive die Gruppe von Vertices darstellt.

Befehle werden immer in der Reihenfolge verarbeitet, in der Sie empfangen werden, obwohl es möglicherweise zu einer unbestimmten Verzögerung kommt, bevor ein Befehl in Kraft tritt. Dies bedeutet, dass jedes primitive vollständig gezeichnet wird, bevor der nachfolgende Befehl in Kraft tritt. Dies bedeutet auch, dass Zustands Abfrage Befehle Daten zurückgeben, die mit der vollständigen Ausführung aller zuvor ausgestellten OpenGL-Befehle konsistent sind.

 

 




