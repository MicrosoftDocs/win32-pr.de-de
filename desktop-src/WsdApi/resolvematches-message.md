---
description: Eine WS-Discovery Nachricht, die als Reaktion auf einen Client gesendet wird, der die Nachricht durch einen übereinstimmenden Dienst auflöst
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: Resolvematches-Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ab5c0d66541b93eeee13966d686c94eef9364d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351554"
---
# <a name="resolvematches-message"></a>Resolvematches-Nachricht

Eine resolvematches-Nachricht ist eine WS-Discovery Nachricht, die als Antwort auf die [Auflösungs](resolve-message.md) Nachricht eines Clients durch einen übereinstimmenden Dienst gesendet wird. Weitere Informationen zu resolvematches-Nachrichten finden Sie im Abschnitt 6,2 der [WS-Discovery-Spezifikation](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Eine resolvematches-Nachricht wird von UDP Unicast an Port 3702 gesendet (der Port, von dem aus die [Auflösungs](resolve-message.md) Nachricht des Clients gesendet wurde). Resolvematches müssen innerhalb von 4 Sekunden der Auflösungs Nachricht gesendet werden. Andernfalls kann das Paket von der Windows-Firewall gelöscht werden.

Alle DPWS-Anwendungen, die [Auflösungs](resolve-message.md) Meldungen senden, empfangen resolvematches-Nachrichten.

> [!Note]  
> Dieses Thema zeigt eine DPWS-Beispiel Nachricht, die von WSDAPI-Clients und-Hosts generiert wurde. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die nicht diesem Beispiel entsprechen. Verwenden Sie dieses Beispiel nicht zum Überprüfen der DPWS-Interoperabilität. Verwenden Sie stattdessen das [WSDAPI-grundlegende Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Die folgende SOAP-Nachricht zeigt eine Beispiel-resolvematches-Nachricht.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:64ddd01c-b0d6-4afd-aba6-6f1f161ce9d4
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="6">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ResolveMatches>
        <wsd:ResolveMatch>
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
        </wsd:ResolveMatch>
    </wsd:ResolveMatches>
</soap:Body>
</soap:Envelope>
```

Eine resolvematches-Nachricht weist die folgenden Schwerpunkt Punkte auf.



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
<td>Resolvematches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
</wsa:Action></code></pre></td>
<td>Die resolvematches-SOAP-Aktion identifiziert die Nachricht als resolvematches-Nachricht.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:RelatesTo></code></pre></td>
<td>Der Bezeichner der Nachricht, auf die der Dienst antwortet. Dieser Header entspricht der MessageId in der <a href="resolve-message.md">Auflösungs</a> Nachricht.</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
</wsd:AppSequence></code></pre></td>
<td>Enthält Informationen zur Anwendungs Sequenzierung, die die Reihenfolge der Nachrichten auch dann beibehalten, wenn Sie nicht in der richtigen Reihenfolge empfangen werden. Die appsequence wird wie in <a href="appsequence-validation-rules.md">appsequence-Validierungsregeln</a>beschrieben überprüft.</td>
</tr>
<tr class="even">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Adresse des zu lösenden Endpunkts.</td>
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

[Meldung auflösen](resolve-message.md)
</dt> </dl>

 

 



