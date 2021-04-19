---
description: Eine WS-Discovery Nachricht, die als Reaktion auf eine Testnachricht für Clients von einem Dienst gesendet wird.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: Probe Matches-Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd856cda51d558073585f41f3db23c75fea7f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349436"
---
# <a name="probematches-message"></a>Probe Matches-Meldung

Eine Probe Matches-Nachricht ist eine WS-Discovery Nachricht, die von einem Dienst als Antwort [auf die Test](probe-message.md) Nachricht eines Clients gesendet wird. Weitere Informationen zu Probe Matches-Meldungen finden Sie im Abschnitt 5,3 der [WS-Discovery-Spezifikation](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Eine Probe Matches-Meldung wird von UDP Unicast an den Port gesendet, von dem aus die Test [Nachricht des Clients](probe-message.md) gesendet wurde. Probe Matches muss innerhalb von 4 Sekunden der Testnachricht gesendet werden. Andernfalls kann das Paket von der Windows-Firewall gelöscht werden.

Wenn keine xaddrs in der probematches-Nachricht enthalten sind, sendet der Client möglicherweise eine [Auflösungs](resolve-message.md) Meldung von UDP-Multicast an Port 3702. Der Client sendet nur dann eine Auflösungs Nachricht, wenn eine HTTP-Nachricht (z. b. eine [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Anforderung oder eine Dienst Nachricht) gesendet wird.

Alle DPWS-Anwendungen, die Test [Nachrichten senden, empfangen Probe Matches](probe-message.md) -Nachrichten.

> [!Note]  
> Dieses Thema zeigt eine DPWS-Beispiel Nachricht, die von WSDAPI-Clients und-Hosts generiert wurde. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die nicht diesem Beispiel entsprechen. Verwenden Sie dieses Beispiel nicht zum Überprüfen der DPWS-Interoperabilität. Verwenden Sie stattdessen das [WSDAPI-grundlegende Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Die folgende SOAP-Nachricht zeigt eine Probe Matches-Beispiel Nachricht.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:967d0036-fe69-40ad-8191-dd1fc8ef64ab
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="9">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ProbeMatches>
        <wsd:ProbeMatch>
            <wsa:EndpointReference>
                <wsa:Address>
                    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                </wsa:Address>
            </wsa:EndpointReference>
            <wsd:Types>wsdp:Device</wsd:Types>
            <wsd:XAddrs>
                https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsd:XAddrs>
            <wsd:MetadataVersion>2</wsd:MetadataVersion>
        </wsd:ProbeMatch>
    </wsd:ProbeMatches>
</soap:Body>
</soap:Envelope>
```

Eine Probe Matches-Nachricht weist die folgenden Schwerpunkt Punkte auf.



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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Probe Matches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
</wsa:Action></code></pre></td>
<td>Die Aktion Probe Matches SOAP identifiziert die Nachricht als Probe Matches-Nachricht.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:RelatesTo></code></pre></td>
<td>Der Bezeichner der Nachricht, auf die der Dienst antwortet. Dieser Header entspricht der MessageId in der <a href="probe-message.md">Testnachricht.</a></td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;9&quot;>
</wsd:AppSequence></code></pre></td>
<td>Enthält Informationen zur Anwendungs Sequenzierung, die die Reihenfolge der Nachrichten auch dann beibehalten, wenn Sie nicht in der richtigen Reihenfolge empfangen werden. Die appsequence wird wie in <a href="appsequence-validation-rules.md">appsequence-Validierungsregeln</a>beschrieben überprüft.</td>
</tr>
<tr class="even">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Endpunkt Adresse. Auf diese adressierte Meldung kann in einer <a href="resolve-message.md">Auflösungs</a> Meldung verwiesen werden.</td>
</tr>
<tr class="odd">
<td>Xaddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>Xaddrs sind Transport Adressen, die für die Kommunikation zwischen Client und Dienst verwendet werden können. Addrs werden wie in <a href="xaddr-validation-rules.md">xaddr-Validierungsregeln</a>beschrieben überprüft.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs-und metadatenaustauschnachrichten](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Testnachricht](probe-message.md)
</dt> </dl>

 

 



