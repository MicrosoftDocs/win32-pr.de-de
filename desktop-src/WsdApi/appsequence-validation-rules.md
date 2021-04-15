---
description: Appsequence-Informationen, die in WS-Discovery Ankündigungs-und Antwort Nachrichten (Hello, Probe Matches und resolvematches) enthalten sind.
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Appsequence-Validierungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528592"
---
# <a name="appsequence-validation-rules"></a>Appsequence-Validierungsregeln

Appsequence-Informationen, die in WS-Discovery Ankündigungs-und Antwort Nachrichten ([Hello](hello-message.md), [Probe Matches](probematches-message.md)und [resolvematches](resolvematches-message.md)) enthalten sind. Diese Informationen werden von WSDAPI verarbeitet und überprüft, bevor diese Nachrichten an Komponenten oberhalb des Stapels weitergeleitet werden (z. b. Netzwerk-Explorer oder eine Anwendung, die WSDAPI aufrufen).

Der folgende XML-Code zeigt ein Beispiel für ein appsequence-Element. Das WSD-Präfix verweist auf den-Namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI ignoriert veraltete Nachrichten. Für jedes Gerät (eindeutig durch die Endpunkt Adresse im SOAP-Text identifiziert) ignoriert WSDAPI alle Nachrichten mit einer appsequence-messagenzahl, die niedriger ist als die letzte angezeigte Meldung.

WSDAPI ignoriert veraltete xaddr-Ankündigungen. Wenn die appsequence-InstanceId niedriger als die letzte angezeigte instanceId ist, ignoriert WSDAPI die im SOAP-Text angekündigten xaddrs. Wenn die InstanceId gleich der vorherigen ist, aber MetadataVersion niedriger ist als die letzte MetadataVersion, ignoriert WSDAPI die xaddrs.

WSDAPI ignoriert doppelte WS-Discovery Meldungen. Wenn zwei identische WS-Discovery-Nachrichten an WSDAPI gesendet werden, wird nur der erste empfangene verarbeitet. Dies ist in der Regel nur für Anwendungen relevant, die direkt in die [**iwsdiscoverypublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) -oder [**iwsdiscoveryprovider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) -Schnittstellen aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs-und Metadatenaustausch-Nachrichten Muster](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



