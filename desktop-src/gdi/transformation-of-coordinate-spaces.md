---
description: Ein Koordinatenraum ist ein planarer Raum, der auf dem kartesischen Koordinatensystem basiert.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Transformation von Koordinaten Räumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1bca3d7190c4566ea7548166134ff745cc5e2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869123"
---
# <a name="transformation-of-coordinate-spaces"></a>Transformation von Koordinaten Räumen

Ein *Koordinatenraum* ist ein planarer Raum, der auf dem kartesischen Koordinatensystem basiert. Dieses System ermöglicht das Angeben des Speicher Orts der einzelnen Punkte auf einer Ebene. Er erfordert zwei Achsen, die senkrecht und gleich lang sind. Die folgende Abbildung zeigt einen Koordinatenraum.

![Darstellung eines Koordinaten Raums, der den Ursprung, beide Achsen und die maximalen und minimalen Werte jeder Achse anzeigt](images/cstrn-07.png)

Das System unterstützt vier Koordinaten Bereiche, wie in der folgenden Tabelle beschrieben.



| Koordinaten Bereich | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Wird optional als Ausgangs Koordinaten Bereich für Grafik Transformationen verwendet. Sie ermöglicht das Skalieren, übersetzen, drehen, Scheren und Reflektion. Welt Raum Measures 2 ^ 32 Einheiten High um 2 ^ 32 Einheiten breit.                                                                                                                                                                                                                                                                |
| Seite (page)             | Wird entweder als Nächster Bereich nach dem Raum der Welt oder als Ausgangs Raum für Grafik Transformationen verwendet. Der Mapping-Modus wird festgelegt. Der Seitenbereich misst auch 2 ^ 32 Einheiten mit einer Breite von 2 ^ 32 Einheiten.                                                                                                                                                                                                                                                                              |
| device           | Wird als Nächster Bereich nach dem Seitenbereich verwendet. Sie ermöglicht nur die Übersetzung, wodurch sichergestellt wird, dass der Ursprung des geräteraums dem richtigen Speicherort im physischen Speicherplatz zugeordnet wird. Geräteraum Measures 2 ^ 27 Einheiten High x 2 ^ 27 Einheiten breit.                                                                                                                                                                                                                                          |
| physisches Gerät  | Der endgültige (Ausgabe-) Bereich für Grafik Transformationen. Dies bezieht sich normalerweise auf den Client Bereich des Anwendungsfensters. Dies kann jedoch auch den gesamten Desktop, ein vollständiges Fenster (einschließlich Frame, Titelleiste und Menüleiste) oder eine Seite mit Drucker-oder Plotpapier enthalten, abhängig von der Funktion, die das Handle für den Gerätekontext abgerufen hat. Die Abmessungen physischer Geräte variieren je nach den Dimensionen, die von der Anzeige, der Drucker oder der plottechnologie festgelegt wurden. |



 

Der Seitenbereich kann mit dem Gerätebereich verwendet werden, um Anwendungen geräteunabhängige Einheiten, wie z. b. Millimeter und Zoll, bereitzustellen. Diese Übersicht bezieht sich sowohl auf den Raum als auch auf den Seiten Raum als logischen Raum.

Um die Ausgabe auf einem physischen Gerät darzustellen, kopiert das System einen rechteckigen Bereich von einem Koordinaten Bereich in den nächsten, wobei eine Transformation verwendet wird, bis die Ausgabe vollständig auf dem physischen Gerät angezeigt wird. Die Zuordnung beginnt im Raum der Anwendungs Welt, wenn die Anwendung die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion aufgerufen hat. Andernfalls erfolgt die Zuordnung im Seitenbereich. Wenn das System jeden Punkt innerhalb des rechteckigen Bereichs von einem Bereich in einen anderen kopiert, wird ein Algorithmus, der als Transformation bezeichnet wird, angewendet. Eine *Transformation* ändert die Größe, Ausrichtung und Form von Objekten, die von einem Koordinaten Bereich in einen anderen kopiert werden, oder wandelt sie um. Obwohl eine Transformation auf ein Objekt als Ganzes wirkt, wird es auf jeden Punkt oder jede Zeile im Objekt angewendet.

Die folgende Abbildung zeigt eine typische Transformation, die mit der [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion ausgeführt wird.

![Darstellung eines Rechtecks, das Größe und Position ändert, wie es im Raum, im Seiten Raum, im Gerätebereich und im Gerät angezeigt wird](images/cstrn-08.png)

 

 



