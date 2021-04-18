---
description: Streamingthreads und der Filter Graph-Manager
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streamingthreads und der Filter Graph-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359159"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Streamingthreads und der Filter Graph-Manager

Wenn der Filter Graph-Manager das Diagramm stoppt, wartet es, bis alle streamingthreads heruntergefahren sind. Dies hat folgende Auswirkungen auf Filter:

-   Ein Filter darf nie Methoden für den Filter Graph-Manager aus einem streamingthread aufzurufen.

    Der Filter Graph-Manager verwendet einen kritischen Abschnitt, um seine eigenen Vorgänge zu synchronisieren. Wenn ein streamingingthread versucht, diesen kritischen Abschnitt aufzunehmen, kann dies zu einem Deadlock führen. Beispiel: angenommen, ein anderer Thread hält das Diagramm an. Dieser Thread nimmt die Filter Diagramm Sperre an und wartet darauf, dass der Filter keine Daten mehr bereit liefert. Wenn der Filter auf die Sperre wartet, wird er nie beendet, was zu einem Deadlock führt.

-   Ein Filter muss niemals den Filter Graph-Manager aus einem streamingthread **adressieren** oder **QueryInterface** .

    Wenn der Filter einen Verweis Zähler für den Filter-Graph-Manager (über **adressf** oder **QueryInterface**) enthält, kann er zum letzten Objekt werden, das einen Verweis Zähler enthalten soll. Wenn der Filter die **Freigabe** aufruft, zerstört der Filter Graph-Manager sich selbst. Innerhalb der Bereinigungs Routine versucht der Filter Graph-Manager, das Diagramm zu beenden, sodass es darauf wartet, dass der streamingthread beendet wird. Er wartet jedoch innerhalb des streamingthreads, sodass der streamingthread nicht beendet werden kann. Das Ergebnis ist ein Deadlock.

 

 



