---
description: Eine WS-Discovery Nachricht, die verwendet wird, um den Abgang eines Geräts oder Diensts aus dem Netzwerk anzukündigen.
ms.assetid: 7b9abfcc-28ab-4f29-af69-6dc68e3f51b6
title: Bye-Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8276c05314b31782442bfdf6de998dd41241391de9dc94947409041c8f4aa420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738652"
---
# <a name="bye-message"></a>Bye-Nachricht

Eine Bye-Nachricht ist eine WS-Discovery Nachricht, mit der das Verlassen eines Geräts oder Diensts aus dem Netzwerk angekündigt wird. Weitere Informationen zu Bye-Nachrichten finden Sie in Abschnitt 4.2 der [WS-Ermittlungsspezifikation.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Bye-Nachrichten werden nicht angefordert. Die Nachrichten sind optional.

> [!Note]  
> In diesem Thema wird eine DPWS-Beispielnachricht gezeigt, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die diesem Beispiel nicht entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie stattdessen das [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Die folgende SOAP-Nachricht zeigt eine Bye-Beispielnachricht.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:193ccfa0-347d-41a1-9285-f500b6b96a15
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="21">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Bye>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Bye>
</soap:Body>
```

Eine Bye-Nachricht hat die folgenden Fokuspunkte.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Fokuspunkt</th>
<th>XML</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Auf Wiedersehen</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
</wsa:Action></code></pre></td>
<td>Die Bye SOAP-Aktion identifiziert die Nachricht als Bye-Nachricht.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;21&quot;>
</wsd:AppSequence></code></pre></td>
<td>Enthält Informationen zur Anwendungssequenzierung, mit denen die Sequenz von Nachrichten auch dann beibehalten werden kann, wenn sie nicht in der angegebenen Reihenfolge empfangen werden. Die AppSequence wird wie unter <a href="appsequence-validation-rules.md">AppSequence Validation Rules (AppSequence-Validierungsregeln)</a>beschrieben überprüft.</td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Adresse des Endpunkts, der offline geschaltet wird.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange-Meldungen](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Hello Message](hello-message.md)
</dt> </dl>

 

 



