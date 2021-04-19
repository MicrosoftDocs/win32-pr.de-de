---
description: Beispiel für einen inftee-Filter
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Beispiel für einen inftee-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346825"
---
# <a name="inftee-filter-sample"></a>Beispiel für einen inftee-Filter

## <a name="description"></a>BESCHREIBUNG

Der inftee-Filter stellt eine Beispiel Implementierung des DirectShow-Ausgabefilters für [unendliche Pin](infinite-pin-tee-filter.md) bereit. Der Filter verfügt über eine Eingabe-PIN und eine dynamische Anzahl von Ausgabe Pins. Alle an den Filter gesendeten Medien Beispiele werden gleichzeitig von allen Ausgabe Pins übermittelt.

Dieser Filter wird in GraphEdit unter dem Namen "Sample Infinite Pin Tee" angezeigt, um ihn vom standardmäßigen unendlichen Pin-Tee-Filter zu unterscheiden, der in DirectShow bereitgestellt wird.

## <a name="usage"></a>Verbrauch

Da mit diesem Filter nicht die empfangenen Daten geändert werden, müssen alle Pins dem gleichen Medientyp zustimmen. Während des Verbindungs Vorgangs stellt der Filter möglicherweise eine Verbindung mit einigen Pins her, damit die Medientypen einander entsprechen.

Daten, die bei der Eingabe-PIN eintreffen, werden nicht kopiert, bevor Sie an die Ausgabe Pins gesendet werden. Der Filter stellt außerdem sicher, dass die Daten an die downstreamfilter übermittelt werden, um sicherzustellen, dass beide Ausgaben einen rechtzeitigen Dienst empfangen. Insbesondere, wenn eine der Ausgaben in der [**coutputqueue:: Receive**](coutputqueue-receive.md) -Member-Funktion blockiert werden kann, startet der Tee einen Thread, um das Beispiel zu übermitteln. Wenn kein Thread zum Übermitteln des Beispiels vorhanden ist, kann der Thread, der das Beispiel an die Tee-Eingabe-PIN übergibt, die Daten an einen downstreamfilter übergeben. an diesem Punkt wird es möglicherweise blockieren, dass Daten aus dem anderen downstreamfilter über einen längeren Zeitraum hinweg aufbewahrt werden.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] root* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Info.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



