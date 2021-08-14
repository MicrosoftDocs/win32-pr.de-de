---
description: InfTee-Filterbeispiel
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: InfTee-Filterbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd0bbbb4df30f549a8ea0ba15d33696dcb7c108cbeffa6658bbb1842291517d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398018"
---
# <a name="inftee-filter-sample"></a>InfTee-Filterbeispiel

## <a name="description"></a>BESCHREIBUNG

Der InfTee-Filter enthält eine Beispielimplementierung des DirectShow [Infinite Pin Tee-Filters.](infinite-pin-tee-filter.md) Der Filter verfügt über einen Eingabepin und eine dynamische Anzahl von Ausgabepins. Alle an den Filter gesendeten Medienbeispiele werden gleichzeitig von allen Ausgabepins übermittelt.

Dieser Filter wird in GraphEdit unter dem Namen "Sample Infinite Pin Tee" angezeigt, um ihn von dem Standardfilter Infinite Pin Tee zu unterscheiden, der in DirectShow bereitgestellt wird.

## <a name="usage"></a>Verbrauch

Da dieser Filter die empfangenen Daten nicht ändert, müssen alle Pins demselben Medientyp zustimmen. Während des Verbindungsprozesses kann der Filter einige Pins erneut verbinden, damit die Medientypen übereinstimmen.

Beim Eingabepin eintreffende Daten werden nicht kopiert, bevor sie an die Ausgabepins gesendet werden. Der Filter stellt außerdem sicher, dass die Daten an die Downstreamfilter übermittelt werden, um zu gewährleisten, dass beide Ausgaben rechtzeitig bereitgestellt werden. Insbesondere wenn eine der Ausgaben in der [**COutputQueue::Receive-Memberfunktion**](coutputqueue-receive.md) blockiert werden kann, wird der Thread durch die Tee ausgeschaltet, um das Beispiel zu liefern. Wenn kein Thread zum Liefern des Beispiels zur Verfügung steht, übergibt der Thread, der das Beispiel an den Tee-Eingabepin übergibt, die Daten möglicherweise an einen Downstreamfilter. An diesem Punkt kann sie blockieren und Daten aus dem anderen Downstreamfilter über einen längeren Zeitraum hinweg behalten.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Dieses Beispiel wird unter dem folgenden Pfad installiert: *\[ SDK Root \]* Samples Multimedia \\ \\ \\ DirectShow Filters \\ \\ InfTee.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



