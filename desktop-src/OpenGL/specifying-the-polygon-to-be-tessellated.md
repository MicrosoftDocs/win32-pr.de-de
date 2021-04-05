---
title: Angeben des zu Mosaik enden Polygons
description: Sie geben ein Polygon (möglicherweise enthaltende Löcher) an, das im Mosaik Prozess verwendet werden soll.
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948033"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a>Angeben des zu Mosaik enden Polygons

Sie geben ein Polygon (möglicherweise enthaltende Löcher) an, das mit dem Mosaik Prozess verwendet werden soll:

-   [**glubeginpolygon**](glubeginpolygon.md)
-   [**glutess Vertex**](glutessvertex.md)
-   [**glunextcontour**](glunextcontour.md)
-   [**gluendpolygon**](gluendpolygon.md)

Bei Polygonen ohne Löcher ist der Spezifikations Prozess genau so wie in OpenGL:

1.  Beginnen Sie mit " [**glubeginpolygon**](glubeginpolygon.md)".
2.  Ruft für jeden Scheitelpunkt in der Grenze " [**glutess Scheitel**](glutessvertex.md) Punkt" auf.
3.  Beenden Sie das Polygon mit einem-Befehl von " [**gluendpolygon**](gluendpolygon.md)".

Wenn ein Polygon aus mehreren Kontur besteht, einschließlich Lücken und Löcher innerhalb von Löchern, geben Sie die Kontur nacheinander vor jeder durch [**glunextcontour**](glunextcontour.md)an. Wenn Sie " [**gluendpolygon**](gluendpolygon.md)" aufgerufen haben, wird das Ende der abschließenden Kontur signalisiert und das Mosaik gestartet. Sie können den Aufrufe von **glunextcontour** vor der ersten Kontur weglassen. Die Funktion " [**glubeginpolygon**](glubeginpolygon.md) " beginnt mit der Spezifikation eines Polygons, das im Mosaik Prozess verwendet wird, und ordnet ihm ein Mosaik Objekt ( **tessobj**) zu. Die zu verwendenden Rückruf Funktionen sind diejenigen, die Sie mit " [*glutesscallback*](glutess.md)" an das Mosaik Objekt binden.

Die Funktion " [**glutess Vertex**](glutessvertex.md) " gibt einen Scheitelpunkt im Polygon an, der im Mosaik Prozess verwendet werden soll. Nennen Sie für jeden Scheitelpunkt im Polygon den Typ " **glutess Vertex** ". Der *tessobj* -Parameter der Funktion ist das zu verwendende Mosaik Objekt, " *v* " enthält die dreidimensionalen Scheitelpunkt Koordinaten, und " *Data* " ist ein beliebiger Zeiger, der an den dem " **glu \_ Vertex**" zugeordneten Rückruf gesendet wird. In der Regel enthalten *Daten* Scheitelpunkt Daten, Texturkoordinaten, Farbinformationen oder andere andere Anwendungen, die für die Anwendung erforderlich sind.

Die Funktion " [**glunextcontour**](glunextcontour.md) " markiert den Anfang der nächsten Kontur, wenn mehrere Kontur die Grenze des Polygons bilden, das im Mosaik Prozess verwendet werden soll. Der *Typparameter* der Funktion kann " **glu \_** extern", " **glu \_ Interior**", " **glu \_ CCW**", " **glu \_ CW**" oder " **glu \_ Unknown**" lauten. Diese Konstanten dienen nur als Hinweise für das Mosaik. Wenn Sie Sie richtig erhalten, kann der Mosaik Prozess schneller ausfallen. Wenn Sie Sie falsch erhalten, werden Sie ignoriert, und das Mosaik funktioniert weiterhin.

Bei einem Polygon mit Löchern ist eine Kontur die äußere Kontur und die anderen sind innen. Wenn Sie " **glunextcontour** " nicht unmittelbar nach " [**glubeginpolygon**](glubeginpolygon.md)" aufrufen, wird davon ausgegangen, dass die erste Kontur den Typ " **glu \_ outside**" hat.

**Glu \_ CW** und **glu \_ CCW** weisen auf den Uhrzeigersinn und gegen den Uhrzeigersinn ausgerichtete Polygone hin. Die Auswahl von im Uhrzeigersinn und den gegen den Uhrzeigersinn ist willkürlich in drei Dimensionen, aber in jeder Ebene gibt es zwei verschiedene Ausrichtungen: Verwenden Sie den VC **\_ CW** -und den **glu- \_ CCW** -Typ konsistent. Verwenden Sie " **glu \_ Unknown** ", wenn Sie nicht wissen, welche verwendet werden soll

Die Funktion " [**gluendpolygon**](gluendpolygon.md) " gibt das Ende der Polygon Spezifikation an. Außerdem gibt es an, dass das Mosaik Objekt das Mosaik Objekt *tessobj* verwenden kann.

 

 




