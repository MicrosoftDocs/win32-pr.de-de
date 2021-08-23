---
title: Primitive und Befehle
description: Primitive und Befehle
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, Primitive
- OpenGL, Befehle
- Primitive OpenGL
- Befehle OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0729b71e9c25abf22045884910fcec3780d50aff2fe94dbe485f83f640cdeced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888060"
---
# <a name="primitives-and-commands"></a>Primitive und Befehle

OpenGL zeichnet *primitive* Punkte, Liniensegmente oder Polygone in mehrere auswählbare Modi. Sie können Modi unabhängig voneinander steuern. Das heißt, das Festlegen eines Modus wirkt sich nicht darauf aus, ob andere Modi festgelegt sind (obwohl viele Modi interagieren können, um zu bestimmen, was schließlich im Framepuffer endet). Um Primitive anzugeben, Modi festzulegen und andere OpenGL-Vorgänge auszuführen, geben Sie Befehle in Form von Funktionsaufrufen aus.

Primitive werden durch eine Gruppe von einem oder *mehreren Scheitelpunkten* definiert. Ein Scheitelpunkt definiert einen Punkt, einen Endpunkt einer Linie oder eine Ecke eines Polygons, an dem zwei Kanten aufeinandertreffen. Daten (bestehend aus Scheitelpunktkoordinaten, Farben, Normalwerten, Texturkoordinaten und Edgeflags) sind einem Scheitelpunkt zugeordnet, und jeder Scheitelpunkt und die zugehörigen Daten werden unabhängig, in der Reihenfolge und auf die gleiche Weise verarbeitet. Die einzigen Ausnahmen von dieser Regel sind Fälle, in denen die Gruppe von Scheitelpunkten abgeschnitten werden muss, damit ein bestimmter Primitiver in einen angegebenen Bereich passt. In diesem Fall können Scheitelpunktdaten geändert und neue Scheitelpunkte erstellt werden. Der Typ des Clippings hängt davon ab, welcher Primitive die Gruppe von Scheitelpunkten darstellt.

Befehle werden immer in der Reihenfolge verarbeitet, in der sie empfangen werden, obwohl es eine unbestimmte Verzögerung geben kann, bevor ein Befehl wirksam wird. Dies bedeutet, dass jedes Primitive vollständig gezeichnet wird, bevor ein nachfolgender Befehl wirksam wird. Dies bedeutet auch, dass Zustandsabfragebefehle Daten zurückgeben, die mit der vollständigen Ausführung aller zuvor ausgegebenen OpenGL-Befehle konsistent sind.

 

 




