---
description: Eine WS-Discovery Meldung, mit der das Vorhandensein eines Geräts oder Diensts im Netzwerk angekündigt wird.
ms.assetid: a7402e02-9bdc-49ec-ba93-8a32f55b9dd8
title: Hello Message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49562d212bb113bba2c1fca0a352b0f1a81cea76
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627586"
---
# <a name="hello-message"></a>Hello Message

Eine Hello-Nachricht ist eine WS-Discovery Nachricht, mit der das Vorhandensein eines Geräts oder Diensts im Netzwerk angekündigt wird. Hello-Nachrichten werden auch in anderen Szenarien gesendet. Weitere Informationen zu Hello-Nachrichten finden Sie in Abschnitt 4.1 der [WS-Discovery-Spezifikation.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Eine Hello-Nachricht wird von UDP Multicast an Port 3702 gesendet. Diese Nachricht wird nicht angefordert.

> [!Note]  
> In diesem Thema wird eine DPWS-Beispielnachricht gezeigt, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die diesem Beispiel nicht entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie stattdessen das [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Die folgende SOAP-Nachricht zeigt eine Hello-Beispielnachricht.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:0f5d604c-81ac-4abc-8010-51dbffad55f2
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="14">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Hello>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
        <wsd:Types>wsdp:Device</wsd:Types>
        <wsd:MetadataVersion>2</wsd:MetadataVersion>
    </wsd:Hello>
</soap:Body>
```

Eine Hello-Nachricht hat die folgenden Fokuspunkte.



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
<td>Hallo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
</wsa:Action></code></pre></td>
<td>Die Hello SOAP-Aktion identifiziert die Nachricht als Hello-Nachricht.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;14&quot;>
</wsd:AppSequence></code></pre></td>
<td>Enthält Informationen zur Anwendungssequenzierung, mit denen die Sequenz von Nachrichten auch dann beibehalten werden kann, wenn sie nicht in der angegebenen Reihenfolge empfangen werden. Die AppSequence wird wie unter <a href="appsequence-validation-rules.md">AppSequence Validation Rules (AppSequence-Validierungsregeln)</a>beschrieben überprüft.</td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Endpunktadresse. Auf diese Adresse kann in einer <a href="resolve-message.md">Resolve-Meldung</a> verwiesen werden.</td>
</tr>
<tr class="even">
<td>Typen</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Enthält die vom Host angekündigten WS-Discovery Typen.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange-Meldungen](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Bye-Nachricht](bye-message.md)
</dt> </dl>

 

 



