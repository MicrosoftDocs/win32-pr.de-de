---
description: Streamingthreads und der Filter Graph Manager
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streamingthreads und der Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3501f984880fad22399cbda8710acaf2be1d6c4223e07a4c0f6e4c180d0699cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329770"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Streamingthreads und der Filter Graph Manager

Wenn der Filter Graph-Manager das Diagramm beendet, wird gewartet, bis alle Streamingthreads heruntergefahren werden. Dies hat folgende Auswirkungen auf Filter:

-   Ein Filter darf niemals Methoden für den Filter Graph Manager aus einem Streamingthread aufrufen.

    Der Filter Graph Manager verwendet einen kritischen Abschnitt, um seine eigenen Vorgänge zu synchronisieren. Wenn ein Streamingthread versucht, diesen kritischen Abschnitt zu halten, kann dies zu einem Deadlock führen. Beispiel: Angenommen, ein anderer Thread beendet das Diagramm. Dieser Thread verwendet die Filterdiagrammsperre und wartet darauf, dass der Filter die Daten nicht mehr liefert. Wenn Ihr Filter auf die Sperre wartet, wird er nie stoppt, was zu einem Deadlock führt.

-   Ein Filter darf nie **AddRef oder** **QueryInterface** für den Filter Graph-Manager aus einem Streamingthread verwenden.

    Wenn der Filter einen Verweiszähler für den Filter-Graph-Manager enthält (über **AddRef** oder **QueryInterface),** wird er möglicherweise das letzte Objekt, das eine Verweisanzahl enthält. Wenn der Filter **Release aufruft,** zerstört sich Graph Manager selbst. In seiner Bereinigungsroutine versucht der Filter Graph-Manager, den Graphen zu beenden, sodass auf das Beenden des Streamingthreads gewartet wird. Er wartet jedoch innerhalb des Streamingthreads, sodass der Streamingthread nicht beendet werden kann. Das Ergebnis ist ein Deadlock.

 

 



