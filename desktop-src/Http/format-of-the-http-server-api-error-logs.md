---
title: Format der HTTP-Server-API-Fehlerprotokolle
description: Im Allgemeinen haben Fehlerprotokoll Dateien der HTTP-Server-API das gleiche Format wie die W3C-Fehlerprotokolle, mit der Ausnahme, dass die Fehlerprotokoll Dateien der HTTP Server-API keine Spaltenüberschriften enthalten
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- HTTP-Server-API, Fehlerprotokoll Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206456"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Format der HTTP-Server-API-Fehlerprotokolle

Im Allgemeinen haben Fehlerprotokoll Dateien der HTTP-Server-API das gleiche Format wie die W3C-Fehlerprotokolle, mit der Ausnahme, dass die Fehlerprotokoll Dateien der HTTP Server-API keine Spaltenüberschriften enthalten Jede Zeile eines HTTP-Server-API-Fehler Protokolls zeichnet einen Fehler mit Feldern in einer bestimmten Reihenfolge auf. Jedes Feld ist von dem vorangehenden Feld durch ein einzelnes Leerzeichen (0x0020) getrennt. Innerhalb jedes Felds werden Leerzeichen, Tabstopps und nicht druckbare Steuerzeichen durch Pluszeichen (0x002b) ersetzt.

In der folgenden Tabelle werden die Felder und die Reihenfolge der Felder in einem Fehlerprotokoll Daten Satz identifiziert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feld</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Date"></span><span id="date"></span><span id="DATE"></span>Datum<br/></td>
<td>Das Datumsfeld folgt dem W3C-Format und basiert auf der koordinierten Weltzeit (UTC). Das Datumsfeld weist immer 10 Zeichen in der Form &quot; yyyy-mm-dd auf &quot; . Beispielsweise wird 1. Mai 2003 als 2003-05-01 ausgedrückt &quot; &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="Time"></span><span id="time"></span><span id="TIME"></span>Zeit<br/></td>
<td>Das Zeitfeld folgt dem W3C-Format und basiert auf UTC. Das Zeitfeld ist immer 8 Zeichen in der Form &quot; mm: hh: SS &quot; . Beispielsweise wird 5:30 pm (UTC) als 17:30:00 ausgedrückt &quot; &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client-IP-Adresse<br/></td>
<td>Die IP-Adresse des betroffenen Clients, bei der es sich entweder um eine IPv4-Adresse oder eine IPv6-Adresse handeln kann. Wenn die Client-IP-Adresse eine IPv6-Adresse ist, ist das Feld "ScopeId" auch in der Adresse enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>ClientPort<br/></td>
<td>Die Portnummer für den betroffenen Client.<br/></td>
</tr>
<tr class="odd">
<td><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server-IP-Adresse<br/></td>
<td>Die IP-Adresse des betroffenen Servers, bei der es sich entweder um eine IPv4-Adresse oder eine IPv6-Adresse handeln kann. Wenn die IP-Adresse des Servers eine IPv6-Adresse ist, ist das Feld "ScopeId" auch in der Adresse enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Serverport<br/></td>
<td>Die Portnummer des betroffenen Servers.<br/></td>
</tr>
<tr class="odd">
<td><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protokoll Version<br/></td>
<td>Die Version des Protokolls, das verwendet wird. <br/>
<ul>
<li>Wenn die Verbindung nicht genug analysiert wurde, um die Protokollversion zu ermitteln, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.</li>
<li>Wenn die analysierte Haupt-oder neben Versionsnummer größer oder gleich 10 ist, wird die Version als &quot; http/?.? protokolliert &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Ben<br/></td>
<td>Der Verb Zustand, der von der letzten analysierten Anforderung übermittelt wurde. Unbekannte Verben sind eingeschlossen, aber jedes Verb, das mehr als 255 Bytes beträgt, wird auf diese Länge gekürzt. Wenn kein Verb verfügbar ist, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.<br/></td>
</tr>
<tr class="odd">
<td><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>Cookedurl + Abfrage<br/></td>
<td>Die URL und jede Abfrage, die ihr zugeordnet ist, wird als ein Feld protokolliert, getrennt durch ein Fragezeichen (0x3f). Dieses Feld wird mit dem Längen Limit von 4096 Bytes abgeschnitten.
<ul>
<li>Wenn diese URL analysiert ( &quot; gekocht &quot; ) wurde, wird Sie mit der lokalen Code Page Konvertierung protokolliert und als Unicode-Feld behandelt.</li>
<li>Wenn diese URL &quot; &quot; zum Zeitpunkt der Protokollierung nicht analysiert (gekocht) wurde, wird Sie genau kopiert, ohne dass eine Unicode-Konvertierung erfolgt.</li>
<li>Wenn die HTTP-Server-API diese URL nicht analysieren kann, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protokoll Status<br/></td>
<td>Der Protokoll Status darf 999 nicht überschreiten. <br/>
<ul>
<li>Wenn der Protokoll Status der Antwort auf eine Anforderung verfügbar ist, wird Sie in diesem Feld protokolliert.</li>
<li>Wenn der Protokoll Status nicht verfügbar ist, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId<br/></td>
<td>Wird in dieser Version der HTTP-Server-API nicht verwendet. In diesem Feld wird immer ein Platzhalter-Bindestrich (0x002d) angezeigt.<br/></td>
</tr>
<tr class="even">
<td><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason-Ausdruck<br/></td>
<td>Dieses Feld enthält eine Zeichenfolge, die angibt, welche Art von Fehler protokolliert wird. Er wird nie leer gelassen.<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Beispiel Zeilen stammen aus einem HTTP-Server-API-Fehlerprotokoll:

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





