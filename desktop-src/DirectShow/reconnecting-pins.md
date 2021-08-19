---
description: Erneutes Verbinden von Pins
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Erneutes Verbinden von Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8bb214307a5c17639d98ae07284abddca4d5beb11b966150d8b7ec46013853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072774"
---
# <a name="reconnecting-pins"></a>Erneutes Verbinden von Pins

Während einer Pinverbindung kann ein Filter wie folgt eine Verbindung mit einem der anderen Pins trennen und erneut herstellen:

1.  Der Filter ruft [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) am Pin des anderen Filters auf und gibt den neuen Medientyp an.
2.  Wenn **QueryAccept** S \_ OK zurückgibt, ruft der Filter [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) auf, um die Pins erneut zu verbinden.

Im Folgenden sind einige Beispiele dafür aufgeführt, wann ein Filter möglicherweise erneut eine Verbindung mit Pins herstellen muss:

-   **Teefilter.** Ein *Teefilter* teilt einen Eingabestream in mehrere Ausgaben auf, ohne die Daten im Datenstrom zu ändern. Ein Teefilter kann einen Bereich von Medientypen akzeptieren, aber die Typen müssen über alle Stecknadelverbindungen hinweg übereinstimmen. Wenn der Eingabepin eine Verbindung herstellt, muss der Filter daher ggf. alle vorhandenen Verbindungen auf den Ausgabepins neu aushandeln und umgekehrt. Ein Beispiel finden Sie im [InfTee-Filterbeispiel.](inftee-filter-sample.md)
-   **Trans-in-Place-Filter.** Ein *trans-in-place-Filter* ändert die Eingabedaten im ursprünglichen Puffer, anstatt die Daten in einen separaten Ausgabepuffer zu kopieren. Ein trans-in-place-Filter muss den gleichen Allocator sowohl für die Upstream- als auch für die Downstreamverbindung verwenden. Der erste Stecknadel, mit dem eine Verbindung hergestellt werden soll (Eingabe oder Ausgabe), handelt eine Zuweisung wie gewohnt aus. Wenn der andere Pin eine Verbindung herstellt, ist die erste Zuweisung jedoch möglicherweise nicht akzeptabel. In diesem Fall wählt der zweite Stecknadel eine andere Zuweisung aus, und der erste Stecknadel stellt die Verbindung mithilfe der neuen Zuweisung wieder her. Eine Beispielimplementierungen finden Sie in der [**CTransInPlaceFilter-Klasse.**](ctransinplacefilter.md)

In der **ReconnectEx-Methode** trennt der Filter Graph Manager die Verbindung mit den Pins asynchron und verbindet sie erneut. Der Filter darf nicht versuchen, die Verbindung wiederherzustellen, es sei **denn, QueryAccept** gibt S \_ OK zurück. Andernfalls wird die Verbindung mit der Stecknadel getrennt, was zu Graphfehlern führt. Außerdem sollte der Filter die erneute Verbindung innerhalb der [**IPin::Verbinden-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) im selben Thread anfordern. Wenn die **Verbinden-Methode** für einen Thread zurückgegeben wird, während ein anderer Thread die Anforderung zur erneuten Verbindung sendet, führt der Filter Graph Manager das Diagramm möglicherweise aus, bevor die Verbindung wiederhergestellt wird. Dies führt zu Graphfehlern.

 

 



