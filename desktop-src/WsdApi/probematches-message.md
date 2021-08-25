---
description: Eine WS-Discovery, die von einem Dienst als Antwort auf eine Clients-Testnachricht gesendet wird.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: ProbeMatches-Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa395557aac7c67a82163066cf1bfbb854348e1c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627866"
---
# <a name="probematches-message"></a>ProbeMatches-Nachricht

Eine ProbeMatches-Nachricht ist eine WS-Discovery, die von einem Dienst als Antwort auf die Testnachricht eines Clients [gesendet](probe-message.md) wird. Weitere Informationen zu ProbeMatches-Nachrichten finden Sie in Abschnitt 5.3 der [WS-Discovery Specification](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Eine ProbeMatches-Nachricht wird von UDP-Unicast an den Port gesendet, von dem die [Testnachricht](probe-message.md) des Clients gesendet wurde. ProbeMatches muss innerhalb von 4 Sekunden nach der Testnachricht gesendet werden. Andernfalls Windows Firewall das Paket möglicherweise ab.

Wenn keine XAddrs in der ProbeMatches-Nachricht enthalten sind, kann der Client eine Resolve-Nachricht per UDP-Multicast an Port 3702 senden. [](resolve-message.md) Der Client sendet nur dann eine Auflösungsnachricht, wenn eine HTTP-Nachricht (z. B. eine [Anforderung zum](get--metadata-exchange--http-request-and-message.md) Abrufen des Metadatenaustauschs oder eine Dienstnachricht) gesendet wird.

Jede DPWS-Anwendung, die [Testnachrichten](probe-message.md) sendet, erhält ProbeMatches-Nachrichten.

> [!Note]  
> Dieses Thema zeigt eine DPWS-Beispielmeldung, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-konforme Nachrichten, die nicht diesem Beispiel entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie [stattdessen das WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Die folgende SOAP-Nachricht zeigt eine ProbeMatches-Beispielmeldung.

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

Eine ProbeMatches-Meldung weist die folgenden Fokuspunkte auf.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>ProbeMatches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
</wsa:Action></code></pre></td>
<td>Die ProbeMatches SOAP-Aktion identifiziert die Nachricht als ProbeMatches-Nachricht.</td>
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
<td>Enthält Informationen zur Anwendungssequenzierung, mit denen die Sequenz von Nachrichten auch dann verwaltet werden kann, wenn sie nicht in der reihenfolgenfolgenden Reihenfolge empfangen werden. AppSequence wird wie unter <a href="appsequence-validation-rules.md">AppSequence Validation Rules (AppSequence-Validierungsregeln) beschrieben überprüft.</a></td>
</tr>
<tr class="even">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Endpunktadresse. Auf dieses Problem kann in einer <a href="resolve-message.md">Auflösungsmeldung verwiesen</a> werden.</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs sind Transportadressen, die für die Kommunikation zwischen Client und Dienst verwendet werden können. Add-Ins werden wie unter <a href="xaddr-validation-rules.md">XAddr-Validierungsregeln beschrieben überprüft.</a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Discovery and Metadata Exchange Messages](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Testmeldung](probe-message.md)
</dt> </dl>

 

 



