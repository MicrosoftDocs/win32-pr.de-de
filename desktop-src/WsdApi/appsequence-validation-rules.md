---
description: AppSequence-Informationen, die in WS-Discovery Ankündigungs- und Antwortnachrichten (Hello, ProbeMatches und ResolveMatches) enthalten sind.
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: AppSequence-Überprüfungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f2acec9d9d3858b5d68b0240499d95dba059ac1bcac745f1dc69bebc2056a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738643"
---
# <a name="appsequence-validation-rules"></a>AppSequence-Überprüfungsregeln

AppSequence-Informationen, die in WS-Discovery Ankündigungs- und Antwortnachrichten enthalten sind ([Hello](hello-message.md), [ProbeMatches](probematches-message.md)und [ResolveMatches](resolvematches-message.md)). Diese Informationen werden von WSDAPI verarbeitet und überprüft, bevor diese Nachrichten an Komponenten über dem Stapel übergeben werden (z. B. Netzwerk-Explorer oder eine Anwendung, die WSDAPI aufruft).

Der folgende XML-Code zeigt ein AppSequence-Beispielelement. Das wsd-Präfix bezieht sich auf den Namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI ignoriert veraltete Nachrichten. Für jedes Gerät (eindeutig durch die Endpunktadresse im SOAP-Text identifiziert) ignoriert WSDAPI alle Nachrichten, deren AppSequence MessageNumber niedriger als die letzte angezeigte Nachricht ist.

WSDAPI ignoriert veraltete XAddr-Ankündigungen. Wenn die AppSequence-Instanz-ID niedriger als die zuletzt angezeigte InstanceId ist, ignoriert WSDAPI die im SOAP-Text angekündigten XAddrs. Wenn die InstanceId mit der vorherigen identisch ist, die MetadataVersion jedoch niedriger als die letzte MetadataVersion ist, ignoriert WSDAPI die XAddrs.

WSDAPI ignoriert doppelte WS-Discovery Nachrichten. Wenn zwei identische WS-Discovery Nachrichten an WSDAPI gesendet werden, wird nur der erste empfangene verarbeitet. Dies ist in der Regel nur für Anwendungen relevant, die die [**Schnittstellen IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) oder [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) direkt aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange Nachrichtenmuster](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



