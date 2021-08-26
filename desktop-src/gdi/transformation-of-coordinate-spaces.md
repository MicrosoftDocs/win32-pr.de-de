---
description: Ein Koordinatenraum ist ein planarer Raum, der auf dem kartesischen Koordinatensystem basiert.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Transformation von Koordinatenbereichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ffaec6a6dab09b841f95f4704048a4145d2b2bd84c232658b2b659d26d37be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965160"
---
# <a name="transformation-of-coordinate-spaces"></a>Transformation von Koordinatenbereichen

Ein *Koordinatenraum* ist ein planarer Raum, der auf dem kartesischen Koordinatensystem basiert. Dieses System bietet eine Möglichkeit, die Position jedes Punkts auf einer Ebene anzugeben. Es sind zwei Achsen erforderlich, die senkrecht und gleich lang sind. Die folgende Abbildung zeigt einen Koordinatenbereich.

![Abbildung eines Koordinatenraums mit dem Ursprung, beiden Achsen und den maximalen und minimalen Werten jeder Achse](images/cstrn-07.png)

Das System unterstützt vier Koordinatenräume, wie in der folgenden Tabelle beschrieben.



| Koordinatenraum | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Wird optional als Startkoordinatenraum für Grafiktransformationen verwendet. Sie ermöglicht Skalierung, Übersetzung, Drehung, Schub und Reflektion. Der Weltraum misst eine Breite von 2^32 Einheiten und einer Breite von 2^32 Einheiten.                                                                                                                                                                                                                                                                |
| Seite (page)             | Wird entweder als nächster Raum nach dem Weltraum oder als Startbereich für Grafiktransformationen verwendet. Der Zuordnungsmodus wird festgelegt. Der Seitenbereich misst auch eine Höhe von 2^32 Einheiten und einer Breite von 2^32 Einheiten.                                                                                                                                                                                                                                                                              |
| device           | Wird als nächstes Leerzeichen nach dem Seitenbereich verwendet. Sie lässt nur die Übersetzung zu, wodurch sichergestellt wird, dass der Ursprung des Geräteraums der richtigen Position im physischen Gerätebereich zugeordnet wird. Der Geräteraum misst eine Breite von 2^27 Einheiten und einer Breite von 2^27 Einheiten.                                                                                                                                                                                                                                          |
| Physisches Gerät  | Der endgültige (Ausgabe-)Bereich für Grafiktransformationen. Er bezieht sich in der Regel auf den Clientbereich des Anwendungsfensters. Sie kann jedoch auch den gesamten Desktop, ein vollständiges Fenster (einschließlich Rahmen, Titelleiste und Menüleiste) oder eine Seite mit Drucker- oder Plotterdokumenten enthalten, je nachdem, welche Funktion das Handle für den Gerätekontext abgerufen hat. Die Abmessungen physischer Geräte variieren je nach den Dimensionen, die von der Anzeige-, Drucker- oder Plottertechnologie festgelegt werden. |



 

Der Seitenbereich arbeitet mit dem Gerätebereich zusammen, um Anwendungen geräteunabhängige Einheiten wie Millimeter und Zoll bereitzustellen. Diese Übersicht bezieht sich sowohl auf den Weltraum als auch auf den Seitenraum als logischen Raum.

Um die Ausgabe auf einem physischen Gerät darzustellen, kopiert (oder ordnet das System) einen rechteckigen Bereich mithilfe einer Transformation aus einem Koordinatenbereich in den nächsten, bis die Ausgabe vollständig auf dem physischen Gerät angezeigt wird. Die Zuordnung beginnt im Weltbereich der Anwendung, wenn die Anwendung die [**SetWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) aufgerufen hat. Andernfalls erfolgt die Zuordnung im Seitenbereich. Wenn das System jeden Punkt innerhalb des rechteckigen Bereichs aus einem Raum in einen anderen kopiert, wendet es einen Algorithmus an, der als Transformation bezeichnet wird. Eine *Transformation* ändert (oder transformiert) die Größe, Ausrichtung und Form von Objekten, die aus einem Koordinatenraum in einen anderen kopiert werden. Obwohl sich eine Transformation auf ein Objekt als Ganzes auswirkt, wird sie auf jeden Punkt oder jede Zeile im Objekt angewendet.

Die folgende Abbildung zeigt eine typische Transformation, die mithilfe der [**SetWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ausgeführt wird.

![Abbildung eines Rechtecks, das die Größe und Position ändert, wie es im Raum der Welt, im Seitenbereich, im Gerätebereich und auf dem Gerät angezeigt wird](images/cstrn-08.png)

 

 



