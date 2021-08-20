---
title: Format der Fehlerprotokolle der HTTP-Server-API
description: Im Allgemeinen haben Fehlerprotokolldateien der HTTP Server-API das gleiche Format wie W3C-Fehlerprotokolle, mit der Ausnahme, dass Fehlerprotokolldateien der HTTP-Server-API keine Spaltenüberschriften enthalten.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- HTTP-Server-API, Fehlerprotokollformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5747e172aa19720a0ae992117000b08402e78d88a66501a9af7b12859a0ac88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014798"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Format der Fehlerprotokolle der HTTP-Server-API

Im Allgemeinen haben Fehlerprotokolldateien der HTTP Server-API das gleiche Format wie W3C-Fehlerprotokolle, mit der Ausnahme, dass Fehlerprotokolldateien der HTTP-Server-API keine Spaltenüberschriften enthalten. Jede Zeile eines HTTP Server-API-Fehlerprotokolls zeichnet einen Fehler mit Feldern in einer bestimmten Reihenfolge auf. Jedes Feld wird durch ein einzelnes Leerzeichen (0x0020. In jedem Feld werden Leerzeichen, Tabstopps und nicht druckbare Steuerzeichen durch Pluszeichen (0x002B.

In der folgenden Tabelle sind die Felder und die Reihenfolge der Felder in einem Fehlerprotokolldatensatz aufgeführt.



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
<td>Das Feld Date folgt dem W3C-Format und basiert auf koordinierte Weltzeit (UTC). Das Datumsfeld besteht immer aus 10 Zeichen in der Form &quot; YYYY-MM-DD &quot; . Beispielsweise wird der 1. Mai 2003 als &quot; 2003-05-01 &quot; ausgedrückt.<br/></td>
</tr>
<tr class="even">
<td><span id="Time"></span><span id="time"></span><span id="TIME"></span>Zeit<br/></td>
<td>Das Feld Zeit folgt dem W3C-Format und basiert auf UTC. Das Zeitfeld besteht immer aus 8 Zeichen in Form von &quot; MM:HH:SS &quot; . Beispielsweise wird 17:30:00 Uhr (UTC) &quot; als &quot; ausgedrückt.<br/></td>
</tr>
<tr class="odd">
<td><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client-IP-Adresse<br/></td>
<td>Die IP-Adresse des betroffenen Clients, die entweder eine IPv4-Adresse oder eine IPv6-Adresse sein kann. Wenn es sich bei der Client-IP-Adresse um eine IPv6-Adresse handelt, ist auch das Feld ScopeId in der Adresse enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Clientport<br/></td>
<td>Die Portnummer für den betroffenen Client.<br/></td>
</tr>
<tr class="odd">
<td><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server-IP-Adresse<br/></td>
<td>Die IP-Adresse des betroffenen Servers, die entweder eine IPv4-Adresse oder eine IPv6-Adresse sein kann. Wenn die IP-Adresse des Servers eine IPv6-Adresse ist, ist auch das Feld ScopeId in der Adresse enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Serverport<br/></td>
<td>Die Portnummer des betroffenen Servers.<br/></td>
</tr>
<tr class="odd">
<td><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protokollversion<br/></td>
<td>Die Version des protokolls, das verwendet wird. <br/>
<ul>
<li>Wenn die Verbindung nicht genug analysiert wurde, um die Protokollversion zu bestimmen, wird ein Bindestrich (0x002D) als Platzhalter für das leere Feld verwendet.</li>
<li>Wenn die analysierte Haupt- oder Nebenversionsnummer größer oder gleich 10 ist, wird die Version als &quot; &quot; HTTP/?.?.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb<br/></td>
<td>Der Verbzustand, der von der zuletzt analysierten Anforderung übergeben wurde. Unbekannte Verben sind enthalten, aber alle Verben, die mehr als 255 Bytes umfassen, werden auf diese Länge abgeschnitten. Wenn ein Verb nicht verfügbar ist, wird ein Bindestrich (0x002D) als Platzhalter für das leere Feld verwendet.<br/></td>
</tr>
<tr class="odd">
<td><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>ZeichenfolgeURL + Abfrage<br/></td>
<td>Die URL und alle damit verbundenen Abfragen werden als ein Feld protokolliert, getrennt durch ein Fragezeichen (0x3F). Dieses Feld wird mit einem Längenlimit von 4.096 Bytes abgeschnitten.
<ul>
<li>Wenn diese URL analysiert wurde (= ), wird sie mit lokaler Codepagekonvertierung protokolliert &quot; &quot; und als Unicode-Feld behandelt.</li>
<li>Wenn diese URL zum Zeitpunkt der Protokollierung nicht analysiert wurde (1: ), wird sie ohne &quot; &quot; Unicode-Konvertierung genau kopiert.</li>
<li>Wenn die HTTP-Server-API diese URL nicht analysieren kann, wird ein Bindestrich (0x002D) als Platzhalter für das leere Feld verwendet.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protokollstatus<br/></td>
<td>Der Protokollstatus darf 999 nicht überschreiten. <br/>
<ul>
<li>Wenn der Protokollstatus der Antwort auf eine Anforderung verfügbar ist, wird er in diesem Feld protokolliert.</li>
<li>Wenn der Protokollstatus nicht verfügbar ist, wird ein Bindestrich (0x002D) als Platzhalter für das leere Feld verwendet.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>Siteid<br/></td>
<td>Wird in dieser Version der HTTP-Server-API nicht verwendet. Ein Platzhalter bindestrich (0x002D) wird immer in diesem Feld angezeigt.<br/></td>
</tr>
<tr class="even">
<td><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Grundbegriff<br/></td>
<td>Dieses Feld enthält eine Zeichenfolge, die die Art des protokollierten Fehlers identifiziert. Sie wird nie leer gelassen.<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Beispielzeilen sind aus einem HTTP-Server-API-Fehlerprotokoll:

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

 

 





