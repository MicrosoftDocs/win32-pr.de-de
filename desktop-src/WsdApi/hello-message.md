---
description: Eine WS-Discovery, die verwendet wird, um das Vorhandensein eines Geräts oder Diensts im Netzwerk ankündigen.
ms.assetid: a7402e02-9bdc-49ec-ba93-8a32f55b9dd8
title: Hello Message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3fe850c4df51fba75c33e202a0bd742226cfb38
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882571"
---
# <a name="hello-message"></a>Hello Message

Eine Hello-Nachricht ist eine WS-Discovery, die verwendet wird, um das Vorhandensein eines Geräts oder Diensts im Netzwerk ankündigen. Hello-Nachrichten werden auch in anderen Szenarien gesendet. Weitere Informationen zu Hello-Nachrichten finden Sie in Abschnitt 4.1 der [WS-Discovery-Spezifikation.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Eine Hello-Nachricht wird von UDP-Multicast an Port 3702 gesendet. Diese Meldung ist nicht angefordert.

> [!Note]  
> Dieses Thema zeigt eine DPWS-Beispielmeldung, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-konforme Nachrichten, die nicht diesem Beispiel entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie [stattdessen das WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

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

Eine Hello-Nachricht weist die folgenden Fokuspunkte auf.



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
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
&lt;/wsa:Action&gt;</code></pre></td>
<td>Die Hello SOAP-Aktion identifiziert die Nachricht als Hello-Nachricht.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;14&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Enthält Informationen zur Anwendungssequenzierung, mit denen die Sequenz von Nachrichten auch dann verwaltet werden kann, wenn sie nicht in der reihenfolgenfolgenden Reihenfolge empfangen werden. AppSequence wird wie unter <a href="appsequence-validation-rules.md">AppSequence Validation Rules (AppSequence-Validierungsregeln) beschrieben überprüft.</a></td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Enthält die Endpunktadresse. Auf dieses Problem kann in einer <a href="resolve-message.md">Auflösungsmeldung verwiesen</a> werden.</td>
</tr>
<tr class="even">
<td>Typen</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:Types&gt;wsdp:Device</wsd:Types></code></pre></td>
<td>Enthält die WS-Discovery typen, die vom Host angekündigt werden.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Discovery and Metadata Exchange Messages](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Bye-Nachricht](bye-message.md)
</dt> </dl>

 

 



