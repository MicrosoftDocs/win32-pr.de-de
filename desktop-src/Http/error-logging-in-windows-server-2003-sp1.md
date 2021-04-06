---
title: Fehler Protokollierung in Windows Server 2003 SP1
description: Fehler Protokollierung in Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Fehler Protokollierung in Windows Server 2003 mit Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2019
ms.locfileid: "103719338"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a><span data-ttu-id="d3204-104">Fehler Protokollierung in Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="d3204-104">Error Logging in Windows Server 2003 SP1</span></span>

## <a name="addition-of-w3c-style-headers"></a><span data-ttu-id="d3204-105">Hinzufügen von W3C-Stil Headern</span><span class="sxs-lookup"><span data-stu-id="d3204-105">Addition of W3C Style Headers</span></span>

<span data-ttu-id="d3204-106">Ab Windows Server 2003 mit Service Pack 1 (SP1) umfasst das HTTP-Server-API-Fehlerprotokoll W3C-Stil Header, die die Analyse von Protokolldateien mithilfe von Standardprotokoll-Parser ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d3204-106">Starting with Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API error log includes W3C style headers allowing log files to be parsed using standard log parsers.</span></span> <span data-ttu-id="d3204-107">Die unten gezeigte Vorlage listet alle Felder auf, die in der http-Fehlerprotokoll Datei protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="d3204-107">The template shown below lists all the fields that can be logged in the http error log file.</span></span>

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a><span data-ttu-id="d3204-108">Protokollieren zusätzlicher Felder</span><span class="sxs-lookup"><span data-stu-id="d3204-108">Logging Additional Fields</span></span>

<span data-ttu-id="d3204-109">Das http-Fehlerprotokoll wurde erweitert und enthält neun weitere Felder zum Protokollieren von Daten zu Fehlern, die auftreten.</span><span class="sxs-lookup"><span data-stu-id="d3204-109">The HTTP error log has been extended to include nine more fields to log data about failures that occur.</span></span> <span data-ttu-id="d3204-110">Die neuen Fehler Felder sind unten aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d3204-110">The new error fields are listed below:</span></span>

-   <span data-ttu-id="d3204-111">Server Computer Name \[ S-Computername\]</span><span class="sxs-lookup"><span data-stu-id="d3204-111">Server Computer Name \[S-COMPUTERNAME\]</span></span>
-   <span data-ttu-id="d3204-112">Benutzer-Agent- \[ cs (Benutzer- \_ Agent)\]</span><span class="sxs-lookup"><span data-stu-id="d3204-112">User Agent \[CS(USER\_AGENT)\]</span></span>
-   <span data-ttu-id="d3204-113">Cookie- \[ cs (Cookie)\]</span><span class="sxs-lookup"><span data-stu-id="d3204-113">Cookie \[CS(COOKIE)\]</span></span>
-   <span data-ttu-id="d3204-114">referenrer- \[ cs (Verweiser)\]</span><span class="sxs-lookup"><span data-stu-id="d3204-114">referrer \[CS(referrer)\]</span></span>
-   <span data-ttu-id="d3204-115">Hostname \[ : cs-Host\]</span><span class="sxs-lookup"><span data-stu-id="d3204-115">Host Name \[CS-HOST\]</span></span>
-   <span data-ttu-id="d3204-116">Vom Server empfangene Bytes ( \[ SC-Bytes)\]</span><span class="sxs-lookup"><span data-stu-id="d3204-116">Bytes received by the server \[SC-BYTES\]</span></span>
-   <span data-ttu-id="d3204-117">Von der Server-cs-Bytes empfangene und verarbeitete Bytes \[ -Bytes\]</span><span class="sxs-lookup"><span data-stu-id="d3204-117">Bytes received and processed by the server \[CS-BYTES\]</span></span>
-   <span data-ttu-id="d3204-118">Benötigte Zeit für die Verarbeitung der Anforderungs \[ Zeit.\]</span><span class="sxs-lookup"><span data-stu-id="d3204-118">Time Taken to process the request \[TIME-TAKEN\]</span></span>
-   <span data-ttu-id="d3204-119">Queue-Name (reserviert für IIS) \[ S-QueueName\]</span><span class="sxs-lookup"><span data-stu-id="d3204-119">Queue-Name (Reserved for IIS) \[S-QUEUENAME\]</span></span>

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a><span data-ttu-id="d3204-120">Auswählen von "fLEDs" zum Protokollieren in der http-Fehlerprotokoll Datei</span><span class="sxs-lookup"><span data-stu-id="d3204-120">Selecting Fileds to Log in the HTTP Error Log File</span></span>

<span data-ttu-id="d3204-121">Der Registrierungsschlüssel **errorloggingfields** wurde hinzugefügt, um die Felder zu steuern, die im http-Fehlerprotokoll protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="d3204-121">The **ErrorLoggingFields** registry key has been added to control the fields logged into the HTTP error log.</span></span> <span data-ttu-id="d3204-122">Diese Registrierungs Werte befinden sich unter einem HTTP- \\ Parameter Schlüssel unter:</span><span class="sxs-lookup"><span data-stu-id="d3204-122">This registry values is located under an HTTP\\Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

<span data-ttu-id="d3204-123">Der **errorloggingfields** -Registrierungs Wert ist ein DWORD-Wert, der Bitwerte für jedes der Felder enthält, die protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="d3204-123">The **ErrorLoggingFields** registry value is a DWORD value that contains bit values for each of the fields that can be logged.</span></span> <span data-ttu-id="d3204-124">Legen Sie zum Aktivieren der Protokollierung eines bestimmten Felds den entsprechenden Bitwert auf 1 fest, und starten Sie den HTTP-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="d3204-124">To enable logging of a specific field, set its corresponding bit value to 1 and restart the HTTP service.</span></span> <span data-ttu-id="d3204-125">Legen Sie den Bitwert auf 0 fest, um die Protokollierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3204-125">To disable logging, set the bit value to 0.</span></span> <span data-ttu-id="d3204-126">Verwenden Sie zum Konfigurieren mehrerer Felder ein bitweises OR der einzelnen Werte.</span><span class="sxs-lookup"><span data-stu-id="d3204-126">To configure multiple fields, use a bitwise OR of the individual values.</span></span> <span data-ttu-id="d3204-127">Wenn Sie z. b. die Protokollierungs Felder Cookie und Referrer aktivieren möchten, sollte der Wert 0x00020000 \| 0x00040000 = 0x00060000 lauten.</span><span class="sxs-lookup"><span data-stu-id="d3204-127">For example, to turn on the Cookie and Referrer logging fields, the value should be 0x00020000 \| 0x00040000 = 0x00060000.</span></span> <span data-ttu-id="d3204-128">Wenn der Registrierungsschlüssel **errorloggingfields** nicht vorhanden ist, werden die Standard Felder protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d3204-128">If the **ErrorLoggingFields** registry key is absent, the default fields are logged.</span></span> <span data-ttu-id="d3204-129">Der Wert von **errorloggingfields** zum Protokollieren der Standard Felder lautet 0x7c884c7.</span><span class="sxs-lookup"><span data-stu-id="d3204-129">The **ErrorLoggingFields** value to log the default fields is 0x7c884c7.</span></span> <span data-ttu-id="d3204-130">Um die Protokollierung für alle Felder zu aktivieren, die in der folgenden Tabelle angezeigt werden, legen Sie den Wert auf 0x7dff4e7 fest.</span><span class="sxs-lookup"><span data-stu-id="d3204-130">To enable logging for all the fields shown in the table below, set the value to 0x7dff4e7.</span></span>

<span data-ttu-id="d3204-131">Die Felder für die Fehler Protokollierung sind in der folgenden Tabelle aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d3204-131">The error logging fields are listed in the following table:</span></span>



| <span data-ttu-id="d3204-132">Protokollfeld</span><span class="sxs-lookup"><span data-stu-id="d3204-132">Log field</span></span>            | <span data-ttu-id="d3204-133">Standardmäßig protokolliert</span><span class="sxs-lookup"><span data-stu-id="d3204-133">Logged by default</span></span> | <span data-ttu-id="d3204-134">Bitwert</span><span class="sxs-lookup"><span data-stu-id="d3204-134">Bit value</span></span>  |
|----------------------|-------------------|------------|
| <span data-ttu-id="d3204-135">Date</span><span class="sxs-lookup"><span data-stu-id="d3204-135">Date</span></span>                 | <span data-ttu-id="d3204-136">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-136">Yes</span></span>               | <span data-ttu-id="d3204-137">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d3204-137">0x00000001</span></span> |
| <span data-ttu-id="d3204-138">Time</span><span class="sxs-lookup"><span data-stu-id="d3204-138">Time</span></span>                 | <span data-ttu-id="d3204-139">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-139">Yes</span></span>               | <span data-ttu-id="d3204-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d3204-140">0x00000002</span></span> |
| <span data-ttu-id="d3204-141">Server Computer Name</span><span class="sxs-lookup"><span data-stu-id="d3204-141">Server Computer Name</span></span> | <span data-ttu-id="d3204-142">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-142">No</span></span>                | <span data-ttu-id="d3204-143">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d3204-143">0x00000020</span></span> |
| <span data-ttu-id="d3204-144">Client IP Address</span><span class="sxs-lookup"><span data-stu-id="d3204-144">Client IP Address</span></span>    | <span data-ttu-id="d3204-145">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-145">Yes</span></span>               | <span data-ttu-id="d3204-146">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d3204-146">0x00000004</span></span> |
| <span data-ttu-id="d3204-147">ClientPort</span><span class="sxs-lookup"><span data-stu-id="d3204-147">Client Port</span></span>          | <span data-ttu-id="d3204-148">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-148">Yes</span></span>               | <span data-ttu-id="d3204-149">0x00400000</span><span class="sxs-lookup"><span data-stu-id="d3204-149">0x00400000</span></span> |
| <span data-ttu-id="d3204-150">Server-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="d3204-150">Server IP Address</span></span>    | <span data-ttu-id="d3204-151">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-151">Yes</span></span>               | <span data-ttu-id="d3204-152">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d3204-152">0x00000040</span></span> |
| <span data-ttu-id="d3204-153">Serverport</span><span class="sxs-lookup"><span data-stu-id="d3204-153">Server Port</span></span>          | <span data-ttu-id="d3204-154">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-154">Yes</span></span>               | <span data-ttu-id="d3204-155">0x00008000</span><span class="sxs-lookup"><span data-stu-id="d3204-155">0x00008000</span></span> |
| <span data-ttu-id="d3204-156">Protokoll Version</span><span class="sxs-lookup"><span data-stu-id="d3204-156">Protocol Version</span></span>     | <span data-ttu-id="d3204-157">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-157">Yes</span></span>               | <span data-ttu-id="d3204-158">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d3204-158">0x00080000</span></span> |
| <span data-ttu-id="d3204-159">Methode</span><span class="sxs-lookup"><span data-stu-id="d3204-159">Method</span></span>               | <span data-ttu-id="d3204-160">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-160">Yes</span></span>               | <span data-ttu-id="d3204-161">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d3204-161">0x00000080</span></span> |
| <span data-ttu-id="d3204-162">URI</span><span class="sxs-lookup"><span data-stu-id="d3204-162">URI</span></span>                  | <span data-ttu-id="d3204-163">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-163">Yes</span></span>               | <span data-ttu-id="d3204-164">0x00800000</span><span class="sxs-lookup"><span data-stu-id="d3204-164">0x00800000</span></span> |
| <span data-ttu-id="d3204-165">Benutzer-Agent</span><span class="sxs-lookup"><span data-stu-id="d3204-165">User Agent</span></span>           | <span data-ttu-id="d3204-166">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-166">No</span></span>                | <span data-ttu-id="d3204-167">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d3204-167">0x00010000</span></span> |
| <span data-ttu-id="d3204-168">Cookie</span><span class="sxs-lookup"><span data-stu-id="d3204-168">Cookie</span></span>               | <span data-ttu-id="d3204-169">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-169">No</span></span>                | <span data-ttu-id="d3204-170">0x00020000</span><span class="sxs-lookup"><span data-stu-id="d3204-170">0x00020000</span></span> |
| <span data-ttu-id="d3204-171">Verweiser</span><span class="sxs-lookup"><span data-stu-id="d3204-171">referrer</span></span>             | <span data-ttu-id="d3204-172">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-172">No</span></span>                | <span data-ttu-id="d3204-173">0x00040000</span><span class="sxs-lookup"><span data-stu-id="d3204-173">0x00040000</span></span> |
| <span data-ttu-id="d3204-174">Host</span><span class="sxs-lookup"><span data-stu-id="d3204-174">Host</span></span>                 | <span data-ttu-id="d3204-175">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-175">No</span></span>                | <span data-ttu-id="d3204-176">0x00100000</span><span class="sxs-lookup"><span data-stu-id="d3204-176">0x00100000</span></span> |
| <span data-ttu-id="d3204-177">Protokoll Status</span><span class="sxs-lookup"><span data-stu-id="d3204-177">Protocol Status</span></span>      | <span data-ttu-id="d3204-178">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-178">Yes</span></span>               | <span data-ttu-id="d3204-179">0x00000400</span><span class="sxs-lookup"><span data-stu-id="d3204-179">0x00000400</span></span> |
| <span data-ttu-id="d3204-180">SC-Bytes</span><span class="sxs-lookup"><span data-stu-id="d3204-180">SC-Bytes</span></span>             | <span data-ttu-id="d3204-181">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-181">No</span></span>                | <span data-ttu-id="d3204-182">0x00001000</span><span class="sxs-lookup"><span data-stu-id="d3204-182">0x00001000</span></span> |
| <span data-ttu-id="d3204-183">CS-Bytes</span><span class="sxs-lookup"><span data-stu-id="d3204-183">CS-Bytes</span></span>             | <span data-ttu-id="d3204-184">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-184">No</span></span>                | <span data-ttu-id="d3204-185">0x00002000</span><span class="sxs-lookup"><span data-stu-id="d3204-185">0x00002000</span></span> |
| <span data-ttu-id="d3204-186">Benötigte Zeit</span><span class="sxs-lookup"><span data-stu-id="d3204-186">Time Taken</span></span>           | <span data-ttu-id="d3204-187">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-187">No</span></span>                | <span data-ttu-id="d3204-188">0x00004000</span><span class="sxs-lookup"><span data-stu-id="d3204-188">0x00004000</span></span> |
| <span data-ttu-id="d3204-189">SiteId</span><span class="sxs-lookup"><span data-stu-id="d3204-189">SiteId</span></span>               | <span data-ttu-id="d3204-190">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-190">Yes</span></span>               | <span data-ttu-id="d3204-191">0x01000000</span><span class="sxs-lookup"><span data-stu-id="d3204-191">0x01000000</span></span> |
| <span data-ttu-id="d3204-192">Reason-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="d3204-192">Reason Phrase</span></span>        | <span data-ttu-id="d3204-193">Ja</span><span class="sxs-lookup"><span data-stu-id="d3204-193">Yes</span></span>               | <span data-ttu-id="d3204-194">0x02000000</span><span class="sxs-lookup"><span data-stu-id="d3204-194">0x02000000</span></span> |
| <span data-ttu-id="d3204-195">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="d3204-195">Queue Name</span></span>           | <span data-ttu-id="d3204-196">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-196">No</span></span>                | <span data-ttu-id="d3204-197">0x04000000</span><span class="sxs-lookup"><span data-stu-id="d3204-197">0x04000000</span></span> |
| <span data-ttu-id="d3204-198">Stream-ID</span><span class="sxs-lookup"><span data-stu-id="d3204-198">Stream Id</span></span>            | <span data-ttu-id="d3204-199">Nein</span><span class="sxs-lookup"><span data-stu-id="d3204-199">No</span></span>                | <span data-ttu-id="d3204-200">0x????????</span><span class="sxs-lookup"><span data-stu-id="d3204-200">0x????????</span></span> |



 

## <a name="time-and-date-rollover"></a><span data-ttu-id="d3204-201">Zeit-und Datums-Rollover</span><span class="sxs-lookup"><span data-stu-id="d3204-201">Time and Date Rollover</span></span>

<span data-ttu-id="d3204-202">Standardmäßig wird eine neue http-Fehlerprotokoll Datei erstellt (als Dateirollover bezeichnet), wenn die aktuelle Protokolldatei eine bestimmte Größe erreicht.</span><span class="sxs-lookup"><span data-stu-id="d3204-202">By default, a new HTTP error log file is created (termed file rollover) when the current log file reaches a specified size.</span></span> <span data-ttu-id="d3204-203">Ab Windows Server 2003 mit SP1 können neue Fehlerprotokoll Dateien basierend auf Datum und Uhrzeit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d3204-203">Starting with Windows Server 2003 with SP1, new error log files can be created based on date and time.</span></span> <span data-ttu-id="d3204-204">Zeit-und Datums-Rollover werden von zwei neuen Registrierungs Werten gesteuert: **errorloggingrollovertype** und **errorlogginglocaltimerollover**.</span><span class="sxs-lookup"><span data-stu-id="d3204-204">Time and date rollover are controlled by two new registry values: **ErrorLoggingRolloverType** and **ErrorLoggingLocaltimeRollover**.</span></span> <span data-ttu-id="d3204-205">Diese Registrierungs Werte müssen der Registrierung hinzugefügt werden, um Zeit-und Datums-Rollover zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3204-205">To enable time and date rollover, these registry values must be added to the registry.</span></span> <span data-ttu-id="d3204-206">Der HTTP-Dienst muss neu gestartet werden, wenn diese Schlüssel der Registrierung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d3204-206">The Http service must be restarted when these keys are added to the registry.</span></span> <span data-ttu-id="d3204-207">Die Registrierungsschlüssel für das Rollover der Protokolldatei werden unter folgendem Schlüssel erstellt:</span><span class="sxs-lookup"><span data-stu-id="d3204-207">The log file rollover registry keys are created under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

<span data-ttu-id="d3204-208">Der Registrierungsschlüssel **errorloggingrollovertype** gibt den Typ des gewünschten Rollovers an und ist standardmäßig auf Größen basiertes Rollover festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3204-208">The **ErrorLoggingRolloverType** registry key indicates the type of rollover desired and is by default set to size based rollover.</span></span> <span data-ttu-id="d3204-209">Rollover kann auch täglich, wöchentlich, monatlich oder stündlich erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d3204-209">Rollover can also be set to occur on a daily, weekly, monthly, or hourly basis.</span></span> <span data-ttu-id="d3204-210">Wenn der Dateirollover auf der Zeit basiert, gibt ein **errorlogginglocaltimerollover** -Wert von 0 an, dass die rolloverzeit in GMT ausgedrückt wird, und der Wert 1 gibt an, dass die rolloverzeit in Ortszeit ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d3204-210">When file rollover is based on time, an **ErrorLoggingLocaltimeRollover** value of 0 indicates that the rollover time is expressed in GMT, and a value of 1 indicates that the rollover time is expressed in local time.</span></span> <span data-ttu-id="d3204-211">Der **errorloggingrollovertype** -Schlüssel kann einen Wert von 0 bis 4 annehmen, wie in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3204-211">The **ErrorLoggingRolloverType** key can take a value from 0 to 4 as listed in the following table.</span></span>



| <span data-ttu-id="d3204-212">Wert des Rollover-Typs</span><span class="sxs-lookup"><span data-stu-id="d3204-212">Rollover type value</span></span> | <span data-ttu-id="d3204-213">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3204-213">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3204-214">0</span><span class="sxs-lookup"><span data-stu-id="d3204-214">0</span></span>                   | <span data-ttu-id="d3204-215">Größen basierter Rollover.</span><span class="sxs-lookup"><span data-stu-id="d3204-215">Size based rollover.</span></span> <span data-ttu-id="d3204-216">Für Protokolldateien wird ein Rollover durchgeführt, wenn die Datei die Größe erreicht, die im Registrierungsschlüssel **errorlogfiletrungateesize** definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d3204-216">Log files are rolled over when the file reaches the size defined in the **ErrorLogFileTruncateSize** registry key.</span></span> |
| <span data-ttu-id="d3204-217">1</span><span class="sxs-lookup"><span data-stu-id="d3204-217">1</span></span>                   | <span data-ttu-id="d3204-218">Der Protokoll Dateirollover erfolgt täglich.</span><span class="sxs-lookup"><span data-stu-id="d3204-218">Log file rollover occurs daily.</span></span>                                                                                                         |
| <span data-ttu-id="d3204-219">2</span><span class="sxs-lookup"><span data-stu-id="d3204-219">2</span></span>                   | <span data-ttu-id="d3204-220">Der Protokoll Dateirollover erfolgt wöchentlich.</span><span class="sxs-lookup"><span data-stu-id="d3204-220">Log file rollover occurs weekly.</span></span>                                                                                                        |
| <span data-ttu-id="d3204-221">3</span><span class="sxs-lookup"><span data-stu-id="d3204-221">3</span></span>                   | <span data-ttu-id="d3204-222">Der Protokoll Dateirollover erfolgt monatlich.</span><span class="sxs-lookup"><span data-stu-id="d3204-222">Log file rollover occurs monthly.</span></span>                                                                                                       |
| <span data-ttu-id="d3204-223">4</span><span class="sxs-lookup"><span data-stu-id="d3204-223">4</span></span>                   | <span data-ttu-id="d3204-224">Der Protokoll Dateirollover erfolgt stündlich.</span><span class="sxs-lookup"><span data-stu-id="d3204-224">Log file rollover occurs hourly.</span></span>                                                                                                        |



 

<span data-ttu-id="d3204-225">Die Benennungs Konventionen für Dateien, in denen die Fehlerprotokolle gespeichert werden, unterscheiden sich für die Größen-, Datums-und zeitbasierten Rollover.</span><span class="sxs-lookup"><span data-stu-id="d3204-225">The naming conventions for files that store the error logs are different for size, date, and time based rollover.</span></span> <span data-ttu-id="d3204-226">In der folgenden Tabelle werden die Benennungs Konventionen für http-Protokolldateien aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d3204-226">The following table lists the naming conventions for Http log files.</span></span>



| <span data-ttu-id="d3204-227">Tollovertyp</span><span class="sxs-lookup"><span data-stu-id="d3204-227">Tollover type</span></span> | <span data-ttu-id="d3204-228">Protokolldateiname</span><span class="sxs-lookup"><span data-stu-id="d3204-228">Log file name</span></span>  | <span data-ttu-id="d3204-229">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3204-229">Description</span></span>                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3204-230">Size</span><span class="sxs-lookup"><span data-stu-id="d3204-230">Size</span></span>          | <span data-ttu-id="d3204-231">Httperrn. log</span><span class="sxs-lookup"><span data-stu-id="d3204-231">HTTPERRn.LOG</span></span>   | <span data-ttu-id="d3204-232">Die Protokolldatei wird wieder verwendet, wenn Sie eine bestimmte Größe erreicht.</span><span class="sxs-lookup"><span data-stu-id="d3204-232">The log file is recycled when it reaches a specific size.</span></span> <span data-ttu-id="d3204-233">n ist die Dateinummer und wird erhöht, wenn für die Protokolldatei ein Rollover durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3204-233">n is the file number and is incremented when the log file is rolled over.</span></span> |
| <span data-ttu-id="d3204-234">Täglich</span><span class="sxs-lookup"><span data-stu-id="d3204-234">Daily</span></span>         | <span data-ttu-id="d3204-235">"htyymmdd. log"</span><span class="sxs-lookup"><span data-stu-id="d3204-235">htYYMMDD.log</span></span>   | <span data-ttu-id="d3204-236">Die Protokolldatei wird täglich wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3204-236">The log file is recycled daily.</span></span>                                                                                                     |
| <span data-ttu-id="d3204-237">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="d3204-237">Weekly</span></span>        | <span data-ttu-id="d3204-238">"htyymmww. log"</span><span class="sxs-lookup"><span data-stu-id="d3204-238">htYYMMww.log</span></span>   | <span data-ttu-id="d3204-239">Die Protokolldatei wird wöchentlich wieder verwendet, wobei WW die Woche des Monats ist.</span><span class="sxs-lookup"><span data-stu-id="d3204-239">The log file is recycled weekly, where ww is the week of the month.</span></span>                                                                 |
| <span data-ttu-id="d3204-240">Monatlich</span><span class="sxs-lookup"><span data-stu-id="d3204-240">Monthly</span></span>       | <span data-ttu-id="d3204-241">"htyymm. log"</span><span class="sxs-lookup"><span data-stu-id="d3204-241">htYYMM.log</span></span>     | <span data-ttu-id="d3204-242">Die Protokolldatei wird monatlich wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3204-242">The log file is recycled every month.</span></span>                                                                                               |
| <span data-ttu-id="d3204-243">Stündlich</span><span class="sxs-lookup"><span data-stu-id="d3204-243">Hourly</span></span>        | <span data-ttu-id="d3204-244">htyymmddhh. log</span><span class="sxs-lookup"><span data-stu-id="d3204-244">htYYMMDDhh.log</span></span> | <span data-ttu-id="d3204-245">Die Protokolldatei wird stündlich wieder verwendet, wobei HH die Stunde des Tages ist, die in 0-24-Stunden-Notation ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d3204-245">The log file is recycled hourly, where hh is the hour of the day expressed in 0-24 hour notation.</span></span>                                   |



 

 

 




