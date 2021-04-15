---
description: PIN wird wieder hergestellt
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: PIN wird wieder hergestellt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc71b4d5a62ee066edaa5f97b4cc3332b2231d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521320"
---
# <a name="reconnecting-pins"></a>PIN wird wieder hergestellt

Während einer PIN-Verbindung kann ein Filter die Verbindung trennen und eine der anderen Pins wiederherstellen, wie im folgenden dargestellt:

1.  Der Filter ruft [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) in der PIN des anderen Filters auf und gibt den neuen Medientyp an.
2.  Wenn **queryaccept** S OK zurückgibt \_ , ruft der Filter [**IFilterGraph2:: reconnectex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) auf, um die Pins erneut zu verbinden.

Im folgenden finden Sie einige Beispiele für den Fall, dass ein Filter möglicherweise die Verbindung von Pins wiederherstellt:

-   **Tee-Filter.** Ein *Tee-Filter* teilt einen Eingabedaten Strom in mehrere Ausgaben auf, ohne die Daten im Stream zu ändern. Ein Tee-Filter kann eine Reihe von Medientypen akzeptieren, die Typen müssen jedoch über alle Pin-Verbindungen hinweg abgeglichen werden. Wenn die Eingabe-PIN eine Verbindung herstellt, muss der Filter daher möglicherweise vorhandene Verbindungen auf den Ausgabe Pins erneut aushandeln (und umgekehrt). Ein Beispiel finden Sie im Beispiel für den [inftee-Filter](inftee-filter-sample.md).
-   **Übersetzte Filter.** Ein *transdirekter* Filter ändert die Eingabedaten im ursprünglichen Puffer, anstatt die Daten in einen separaten Ausgabepuffer zu kopieren. Bei einem direkten Filter muss die gleiche Zuweisung für die Upstream-und downstreamverbindungen verwendet werden. Die erste PIN für Connect (Eingabe oder Ausgabe) aushandiert eine Zuweisung auf die übliche Weise. Wenn die andere Pin eine Verbindung herstellt, ist die erste Zuweisung jedoch möglicherweise nicht akzeptabel. In diesem Fall wählt die zweite Pin eine andere Zuweisung aus, und die erste Pin stellt erneut eine Verbindung mit der neuen Zuweisung her. Eine Beispiel Implementierung finden Sie unter der [**ctransinplacefilter**](ctransinplacefilter.md) -Klasse.

In der **reconnectex** -Methode trennt der Filter Graph-Manager asynchron die Verbindung mit den Pins und verbindet diese erneut. Der Filter darf nicht versuchen, die Verbindung erneut herzustellen, es sei denn, **queryaccept** gibt S \_ OK zurück. Andernfalls wird die PIN getrennt, was zu Diagramm Fehlern führt. Außerdem sollte der Filter die erneute Verbindung innerhalb der [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode im gleichen Thread anfordern. Wenn die **Connect** -Methode in einem Thread zurückgibt, während ein anderer Thread die Anforderung zur erneuten Verbindungs Herstellung ausführt, führt der Filter-Graph-Manager möglicherweise das Diagramm aus, bevor die Verbindung wieder hergestellt wird, was zu Diagramm Fehlern führt.

 

 



