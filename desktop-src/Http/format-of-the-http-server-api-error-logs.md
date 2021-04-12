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
# <a name="format-of-the-http-server-api-error-logs"></a><span data-ttu-id="cb4db-104">Format der HTTP-Server-API-Fehlerprotokolle</span><span class="sxs-lookup"><span data-stu-id="cb4db-104">Format of the HTTP Server API Error Logs</span></span>

<span data-ttu-id="cb4db-105">Im Allgemeinen haben Fehlerprotokoll Dateien der HTTP-Server-API das gleiche Format wie die W3C-Fehlerprotokolle, mit der Ausnahme, dass die Fehlerprotokoll Dateien der HTTP Server-API keine Spaltenüberschriften enthalten</span><span class="sxs-lookup"><span data-stu-id="cb4db-105">In general, HTTP Server API error log files have the same format as W3C error logs except that HTTP Server API error log files do not contain column headings.</span></span> <span data-ttu-id="cb4db-106">Jede Zeile eines HTTP-Server-API-Fehler Protokolls zeichnet einen Fehler mit Feldern in einer bestimmten Reihenfolge auf.</span><span class="sxs-lookup"><span data-stu-id="cb4db-106">Each line of an HTTP Server API error log records one error with fields in a specific order.</span></span> <span data-ttu-id="cb4db-107">Jedes Feld ist von dem vorangehenden Feld durch ein einzelnes Leerzeichen (0x0020) getrennt.</span><span class="sxs-lookup"><span data-stu-id="cb4db-107">Each field is separated from the preceding field by a single space character (0x0020).</span></span> <span data-ttu-id="cb4db-108">Innerhalb jedes Felds werden Leerzeichen, Tabstopps und nicht druckbare Steuerzeichen durch Pluszeichen (0x002b) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cb4db-108">Within each field, space characters, tabs, and unprintable control characters are replaced by plus signs (0x002B).</span></span>

<span data-ttu-id="cb4db-109">In der folgenden Tabelle werden die Felder und die Reihenfolge der Felder in einem Fehlerprotokoll Daten Satz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cb4db-109">The following table identifies the fields and the order of the fields in an error log record.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb4db-110">Feld</span><span class="sxs-lookup"><span data-stu-id="cb4db-110">Field</span></span></th>
<th><span data-ttu-id="cb4db-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb4db-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb4db-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Datum</span><span class="sxs-lookup"><span data-stu-id="cb4db-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span></span><br/></td>
<td><span data-ttu-id="cb4db-113">Das Datumsfeld folgt dem W3C-Format und basiert auf der koordinierten Weltzeit (UTC). Das Datumsfeld weist immer 10 Zeichen in der Form &quot; yyyy-mm-dd auf &quot; .</span><span class="sxs-lookup"><span data-stu-id="cb4db-113">The Date field follows the W3C format and is based on Coordinated Universal Time (UTC).The Date field is always 10 characters in the form of &quot;YYYY-MM-DD&quot;.</span></span> <span data-ttu-id="cb4db-114">Beispielsweise wird 1. Mai 2003 als 2003-05-01 ausgedrückt &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="cb4db-114">For example, May 1, 2003 is expressed as &quot;2003-05-01&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb4db-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="cb4db-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Time</span></span><br/></td>
<td><span data-ttu-id="cb4db-116">Das Zeitfeld folgt dem W3C-Format und basiert auf UTC.</span><span class="sxs-lookup"><span data-stu-id="cb4db-116">The Time field follows the W3C format and is based on UTC.</span></span> <span data-ttu-id="cb4db-117">Das Zeitfeld ist immer 8 Zeichen in der Form &quot; mm: hh: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="cb4db-117">The time field is always 8 characters in the form of &quot;MM:HH:SS&quot;.</span></span> <span data-ttu-id="cb4db-118">Beispielsweise wird 5:30 pm (UTC) als 17:30:00 ausgedrückt &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="cb4db-118">For example, 5:30 PM (UTC) is expressed as &quot;17:30:00&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb4db-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="cb4db-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client IP Address</span></span><br/></td>
<td><span data-ttu-id="cb4db-120">Die IP-Adresse des betroffenen Clients, bei der es sich entweder um eine IPv4-Adresse oder eine IPv6-Adresse handeln kann.</span><span class="sxs-lookup"><span data-stu-id="cb4db-120">The IP address of the affected client that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="cb4db-121">Wenn die Client-IP-Adresse eine IPv6-Adresse ist, ist das Feld "ScopeId" auch in der Adresse enthalten.</span><span class="sxs-lookup"><span data-stu-id="cb4db-121">If the client IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb4db-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>ClientPort</span><span class="sxs-lookup"><span data-stu-id="cb4db-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Client Port</span></span><br/></td>
<td><span data-ttu-id="cb4db-123">Die Portnummer für den betroffenen Client.</span><span class="sxs-lookup"><span data-stu-id="cb4db-123">The port number for the affected client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb4db-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="cb4db-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server IP Address</span></span><br/></td>
<td><span data-ttu-id="cb4db-125">Die IP-Adresse des betroffenen Servers, bei der es sich entweder um eine IPv4-Adresse oder eine IPv6-Adresse handeln kann.</span><span class="sxs-lookup"><span data-stu-id="cb4db-125">The IP address of the affected server that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="cb4db-126">Wenn die IP-Adresse des Servers eine IPv6-Adresse ist, ist das Feld "ScopeId" auch in der Adresse enthalten.</span><span class="sxs-lookup"><span data-stu-id="cb4db-126">If the server IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb4db-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Serverport</span><span class="sxs-lookup"><span data-stu-id="cb4db-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Server Port</span></span><br/></td>
<td><span data-ttu-id="cb4db-128">Die Portnummer des betroffenen Servers.</span><span class="sxs-lookup"><span data-stu-id="cb4db-128">The port number of the affected server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb4db-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protokoll Version</span><span class="sxs-lookup"><span data-stu-id="cb4db-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protocol Version</span></span><br/></td>
<td><span data-ttu-id="cb4db-130">Die Version des Protokolls, das verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb4db-130">The version of the protocol that is being used.</span></span> <br/>
<ul>
<li><span data-ttu-id="cb4db-131">Wenn die Verbindung nicht genug analysiert wurde, um die Protokollversion zu ermitteln, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb4db-131">If the connection has not been parsed enough to determine the protocol version, then a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
<li><span data-ttu-id="cb4db-132">Wenn die analysierte Haupt-oder neben Versionsnummer größer oder gleich 10 ist, wird die Version als &quot; http/?.? protokolliert &quot; .</span><span class="sxs-lookup"><span data-stu-id="cb4db-132">If either the major or minor version number parsed is greater than or equal to 10, the version is logged as &quot;HTTP/?.?&quot;.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb4db-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Ben</span><span class="sxs-lookup"><span data-stu-id="cb4db-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span><br/></td>
<td><span data-ttu-id="cb4db-134">Der Verb Zustand, der von der letzten analysierten Anforderung übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="cb4db-134">The verb state passed by the last request parsed.</span></span> <span data-ttu-id="cb4db-135">Unbekannte Verben sind eingeschlossen, aber jedes Verb, das mehr als 255 Bytes beträgt, wird auf diese Länge gekürzt.</span><span class="sxs-lookup"><span data-stu-id="cb4db-135">Unknown verbs are included, but any verb that is more than 255 bytes is truncated to this length.</span></span> <span data-ttu-id="cb4db-136">Wenn kein Verb verfügbar ist, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb4db-136">If a verb is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb4db-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>Cookedurl + Abfrage</span><span class="sxs-lookup"><span data-stu-id="cb4db-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query</span></span><br/></td>
<td><span data-ttu-id="cb4db-138">Die URL und jede Abfrage, die ihr zugeordnet ist, wird als ein Feld protokolliert, getrennt durch ein Fragezeichen (0x3f).</span><span class="sxs-lookup"><span data-stu-id="cb4db-138">The URL and any query associated with it are logged as one field, separated by a question mark (0x3F).</span></span> <span data-ttu-id="cb4db-139">Dieses Feld wird mit dem Längen Limit von 4096 Bytes abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="cb4db-139">This field is truncated at its length limit of 4096 bytes.</span></span>
<ul>
<li><span data-ttu-id="cb4db-140">Wenn diese URL analysiert ( &quot; gekocht &quot; ) wurde, wird Sie mit der lokalen Code Page Konvertierung protokolliert und als Unicode-Feld behandelt.</span><span class="sxs-lookup"><span data-stu-id="cb4db-140">If this URL has been parsed (&quot;cooked&quot;), it is logged with local code page conversion, and is treated as a Unicode field.</span></span></li>
<li><span data-ttu-id="cb4db-141">Wenn diese URL &quot; &quot; zum Zeitpunkt der Protokollierung nicht analysiert (gekocht) wurde, wird Sie genau kopiert, ohne dass eine Unicode-Konvertierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cb4db-141">If this URL has not been parsed (&quot;cooked&quot;) at the time of logging, it is copied exactly, without any Unicode conversion.</span></span></li>
<li><span data-ttu-id="cb4db-142">Wenn die HTTP-Server-API diese URL nicht analysieren kann, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb4db-142">If the HTTP Server API cannot parse this URL, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb4db-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protokoll Status</span><span class="sxs-lookup"><span data-stu-id="cb4db-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protocol Status</span></span><br/></td>
<td><span data-ttu-id="cb4db-144">Der Protokoll Status darf 999 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="cb4db-144">The protocol status cannot exceed 999.</span></span> <br/>
<ul>
<li><span data-ttu-id="cb4db-145">Wenn der Protokoll Status der Antwort auf eine Anforderung verfügbar ist, wird Sie in diesem Feld protokolliert.</span><span class="sxs-lookup"><span data-stu-id="cb4db-145">If the protocol status of the response to a request is available, it is logged in this field.</span></span></li>
<li><span data-ttu-id="cb4db-146">Wenn der Protokoll Status nicht verfügbar ist, wird ein Bindestrich (0x002d) als Platzhalter für das leere Feld verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb4db-146">If the protocol status is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb4db-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span><span class="sxs-lookup"><span data-stu-id="cb4db-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span></span><br/></td>
<td><span data-ttu-id="cb4db-148">Wird in dieser Version der HTTP-Server-API nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb4db-148">Not used in this version of the HTTP Server API.</span></span> <span data-ttu-id="cb4db-149">In diesem Feld wird immer ein Platzhalter-Bindestrich (0x002d) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb4db-149">A placeholder hyphen (0x002D) always appears in this field.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb4db-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="cb4db-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason Phrase</span></span><br/></td>
<td><span data-ttu-id="cb4db-151">Dieses Feld enthält eine Zeichenfolge, die angibt, welche Art von Fehler protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="cb4db-151">This field contains a string that identifies the kind of error that is being logged.</span></span> <span data-ttu-id="cb4db-152">Er wird nie leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="cb4db-152">It is never left empty.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cb4db-153">Die folgenden Beispiel Zeilen stammen aus einem HTTP-Server-API-Fehlerprotokoll:</span><span class="sxs-lookup"><span data-stu-id="cb4db-153">The following sample lines are from an HTTP Server API error log:</span></span>

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

 

 





