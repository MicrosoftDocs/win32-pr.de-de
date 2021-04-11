---
description: Streamende-Benachrichtigungen
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: Streamende-Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fcdfef1225aa5b93b56aeaa0d8ae9d0a8550c9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213972"
---
# <a name="end-of-stream-notifications"></a>Streamende-Benachrichtigungen

Wenn ein Quell Filter das Senden von Daten abgeschlossen hat, ruft er die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode für die downstreameingabepin auf. Der Downstream-Filter gibt den-Befehl an den nächsten Filter weiter usw. Wenn der **EndOfStream** -Aufruf den Renderer erreicht, sendet der Renderer ein [**EC \_ Complete**](ec-complete.md) -Ereignis an den Filter Graph-Manager. Wenn der Renderer über mehrere Eingabe Pins verfügt, wird das EC \_ Complete-Ereignis übermittelt, nachdem jede Eingabe-PIN die Benachrichtigung über das Ende des Datenstroms erhalten hat.

Ein Filter muss [**EndOf**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Aufrufe mit anderen streamingaufrufen serialisieren, wie z. b. [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive). (Mit anderen Worten, der Downstream-Filter muss immer die Aufrufe in der richtigen Reihenfolge empfangen.)

In einigen Fällen kann ein downstreamfilter das Ende des Streams erkennen, bevor der Quell Filter Dies bewirkt. (Z. b. kann der Downstream-Filter den Datenstrom auswerten.) In diesem Fall kann der Downstream-Filter das Ende der Datenstrom Benachrichtigung senden. in diesem Fall sollte er den Wert " \_ false" von [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) zurückgeben, bis der Graph beendet oder geleert wird. Der \_ Wert S false gibt den Quell Filter an, das Senden von Daten zu verhindern.

### <a name="default-handling-of-ec_complete"></a>Standardbehandlung von EC \_ Complete

Standardmäßig führt der Filter Graph-Manager nicht alle Ereignisse vom Typ "EC \_ Complete" an die Anwendung weiter. Stattdessen wartet Sie, bis alle Streams den Vorgang "EC Complete" signalisiert haben, \_ und sendet dann ein einzelnes "EC Complete"- \_ Ereignis. Folglich empfängt die Anwendung das Ereignis, nachdem jeder Stream abgeschlossen wurde.

Zum Ermitteln der Anzahl der Streams zählt der Filter Diagramm-Manager die Anzahl der Filter, die Suchvorgänge unterstützen (über [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) oder [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition)) und über eine *gerenderte* Eingabe-PIN verfügen, die als Eingabe-PIN ohne entsprechende Ausgaben definiert ist. Der Filter Graph-Manager bestimmt, ob eine PIN auf zwei Arten gerendert wird:

-   Die [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) -Methode der PIN gibt im *npin* -Parameter 0 (null) zurück.
-   Der Filter macht die [**iamfilterfehlflags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) -Schnittstelle verfügbar und gibt das Flag "am \_ Filter \_ misc \_ Flags \_ is \_ Renderer" zurück.

### <a name="end-of-stream-notifications-in-pull-mode"></a>Streamende-Benachrichtigungen im Pull-Modus

In einer [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Verbindung sendet der Quell Filter keine Benachrichtigung über das Ende des Datenstroms. Instread, dies erfolgt durch den downstreamfilter, bei dem es sich in der Regel um einen Parserfilter handelt. Der Parser sendet den [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Befehl Downstream. Eine upstreamdatei wird nicht an den Quell Filter gesendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Über das Ende des Streams](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



