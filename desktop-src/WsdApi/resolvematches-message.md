---
description: Eine WS-Discovery Nachricht, die als Antwort an eine Clients gesendet wird. Lösen Sie die Nachricht durch einen übereinstimmenden Dienst auf.
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: ResolveMatches-Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1daffe985f3956e57ad69fd7c4fc4d199f0b24bd5fdab5677b7ef83765e5fcdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756800"
---
# <a name="resolvematches-message"></a>ResolveMatches-Nachricht

Eine ResolveMatches-Nachricht ist eine WS-Discovery Nachricht, die als Antwort auf die [Resolve-Nachricht](resolve-message.md) eines Clients durch einen übereinstimmenden Dienst gesendet wird. Weitere Informationen zu ResolveMatches-Meldungen finden Sie in Abschnitt 6.2 der [WS-Discovery-Spezifikation.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Eine ResolveMatches-Nachricht wird von UDP unicast an Port 3702 gesendet (der Port, von dem die [Resolve-Nachricht](resolve-message.md) des Clients gesendet wurde). ResolveMatches muss innerhalb von 4 Sekunden nach der Auflösungsmeldung gesendet werden. Andernfalls kann Windows Firewall das Paket löschen.

Jede DPWS-Anwendung, die [Resolve-Nachrichten](resolve-message.md) sendet, empfängt ResolveMatches-Nachrichten.

> [!Note]  
> In diesem Thema wird eine DPWS-Beispielnachricht gezeigt, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die diesem Beispiel nicht entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie stattdessen das [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Die folgende SOAP-Nachricht zeigt eine ResolveMatches-Beispielnachricht.

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

Eine ResolveMatches-Nachricht weist die folgenden Fokuspunkte auf.



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
<td>ResolveMatches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
</wsa:Action></code></pre></td>
<td>Die SOAP-Aktion ResolveMatches identifiziert die Nachricht als ResolveMatches-Nachricht.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:RelatesTo></code></pre></td>
<td>Der Bezeichner der Nachricht, auf die der Dienst antwortet. Dieser Header entspricht der MessageId in der <a href="resolve-message.md">Resolve-Nachricht.</a></td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
</wsd:AppSequence></code></pre></td>
<td>Enthält Informationen zur Anwendungssequenzierung, mit denen die Sequenz von Nachrichten auch dann beibehalten werden kann, wenn sie nicht in der angegebenen Reihenfolge empfangen werden. Die AppSequence wird wie unter <a href="appsequence-validation-rules.md">AppSequence Validation Rules (AppSequence-Validierungsregeln)</a>beschrieben überprüft.</td>
</tr>
<tr class="even">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Adresse des Endpunkts, der aufgelöst wird.</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs sind Transportadressen, die für die Kommunikation zwischen Client und Dienst verwendet werden können. Addr werden wie unter <a href="xaddr-validation-rules.md">XAddr-Validierungsregeln</a>beschrieben überprüft.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange-Meldungen](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Auflösen von Nachrichten](resolve-message.md)
</dt> </dl>

 

 



