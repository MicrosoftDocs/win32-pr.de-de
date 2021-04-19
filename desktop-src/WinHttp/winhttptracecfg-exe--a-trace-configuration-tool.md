---
description: Das Microsoft Windows HTTP-Dienste (WinHTTP) Trace Configuration Tool (WinHttpTraceCfg.exe) wird verwendet, um Ablauf Verfolgungs Funktionen für das Debuggen und das paketsniffing zu konfigurieren.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, ein Konfigurations Tool für die Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349004"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a><span data-ttu-id="9b183-103">WinHttpTraceCfg.exe, ein Konfigurations Tool für die Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9b183-103">WinHttpTraceCfg.exe, a Trace Configuration Tool</span></span>

<span data-ttu-id="9b183-104">Das [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md) Trace Configuration Tool (WinHttpTraceCfg.exe) wird verwendet, um Ablauf Verfolgungs Funktionen für das Debuggen und das paketsniffing zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9b183-104">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) trace configuration tool, WinHttpTraceCfg.exe, is used to configure trace capabilities for debugging and packet-sniffing purposes.</span></span> <span data-ttu-id="9b183-105">Die Fähigkeit zum Überwachen von WinHTTP-Funktionen und des entsprechenden Netzwerk Datenverkehrs ist wichtig.</span><span class="sxs-lookup"><span data-stu-id="9b183-105">The ability to monitor WinHTTP functions and their corresponding network traffic is important.</span></span> <span data-ttu-id="9b183-106">Das Debuggen von Anwendungen, die verschlüsselte Übertragungsprotokolle nutzen, wie z. b. Secure Sockets Layer (SSL), schließt das Auslagern von Paketen auf der Netzwerk Transport Ebene aus und erfordert die Möglichkeit, den Datenverkehr zwischen Client und Server abzufangen, nachdem er entschlüsselt wurde.</span><span class="sxs-lookup"><span data-stu-id="9b183-106">Debugging applications that utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="9b183-107">Die Microsoft Windows HTTP-Dienste (WinHTTP) stellen eine Ablauf Verfolgungs Funktion bereit, die über eine Reihe von Funktionen für das Abfangen des Datenverkehrs zwischen dem Client und dem Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="9b183-107">Microsoft Windows HTTP Services (WinHTTP) provides a trace facility that has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

<span data-ttu-id="9b183-108">Diese Ablauf Verfolgungs Funktion kann ein wertvolles Tool für das Debuggen sein.</span><span class="sxs-lookup"><span data-stu-id="9b183-108">This trace facility can be a valuable tool for debugging.</span></span> <span data-ttu-id="9b183-109">Sie kann z. b. verwendet werden, um Parameter anzuzeigen, die an verschiedene Funktionsaufrufe übermittelt werden, sowie um tatsächliche, von einer WinHTTP-Anwendung gesendete und empfangene Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b183-109">It can be used, for example, to view parameters passed to various function calls, as well as to view actual data sent and received by a WinHTTP application.</span></span>

-   [<span data-ttu-id="9b183-110">Verwenden der Ablauf Verfolgungs Funktion</span><span class="sxs-lookup"><span data-stu-id="9b183-110">Using the Trace Facility</span></span>](#using-the-trace-facility)
-   [<span data-ttu-id="9b183-111">Interpretieren von Ablauf Verfolgungs Daten</span><span class="sxs-lookup"><span data-stu-id="9b183-111">Interpreting Trace Data</span></span>](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a><span data-ttu-id="9b183-112">Verwenden der Ablauf Verfolgungs Funktion</span><span class="sxs-lookup"><span data-stu-id="9b183-112">Using the Trace Facility</span></span>

<span data-ttu-id="9b183-113">WinHTTP ruft Ablauf Verfolgungs Steuerungsparameter aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="9b183-113">WinHTTP obtains tracing control parameters from the registry.</span></span> <span data-ttu-id="9b183-114">Diese Steuerelement Parameter beeinflussen, wie WinHTTP eine Ablauf Verfolgungs Ausgabe erzeugt und wie diese Ausgabe formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="9b183-114">These control parameters affect how WinHTTP produces trace output, and how that output is formatted.</span></span> <span data-ttu-id="9b183-115">Alle Anwendungen, die WinHTTP verwenden, verwenden die gleichen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="9b183-115">All applications that use WinHTTP share the same settings.</span></span>

<span data-ttu-id="9b183-116">Ein Konfigurationstool für die Ablauf Verfolgungs Einrichtung (WinHttpTraceCfg.exe) ist als Download auf der [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) -Website verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b183-116">A trace facility configuration tool, WinHttpTraceCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="9b183-117">Das-Konfigurationstool legt die Registrierungs Einstellungen für die Ablauf Verfolgungs Einrichtung basierend auf den angegebenen Befehlszeilen Parametern fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="9b183-117">The configuration tool sets or retrieves the trace facility registry settings based on the specified command line parameters.</span></span>

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

<span data-ttu-id="9b183-118">In der folgenden Tabelle sind die möglichen Parameter für das-Konfigurationstool aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b183-118">The following table lists possible parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b183-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b183-119">Parameter</span></span></th>
<th><span data-ttu-id="9b183-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b183-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b183-121">-?</span><span class="sxs-lookup"><span data-stu-id="9b183-121">-?</span></span></td>
<td><span data-ttu-id="9b183-122">Zeigt Syntax Daten an.</span><span class="sxs-lookup"><span data-stu-id="9b183-122">Displays syntax data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b183-123">-E</span><span class="sxs-lookup"><span data-stu-id="9b183-123">-e</span></span></td>
<td><span data-ttu-id="9b183-124">Gibt an, ob die Ablauf Verfolgungs Funktion aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9b183-124">Specifies whether the trace facility is enabled or disabled.</span></span> <br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b183-125">0</span><span class="sxs-lookup"><span data-stu-id="9b183-125">0</span></span></td>
<td><span data-ttu-id="9b183-126">Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9b183-126">Default setting.</span></span> <span data-ttu-id="9b183-127">Deaktiviert die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="9b183-127">Disables tracing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b183-128">1</span><span class="sxs-lookup"><span data-stu-id="9b183-128">1</span></span></td>
<td><span data-ttu-id="9b183-129">Aktiviert die Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="9b183-129">Enables tracing.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b183-130">-l</span><span class="sxs-lookup"><span data-stu-id="9b183-130">-l</span></span></td>
<td><p><span data-ttu-id="9b183-131">Gibt ein Präfix für die Protokolldatei an.</span><span class="sxs-lookup"><span data-stu-id="9b183-131">Specifies a prefix for the log file.</span></span> <span data-ttu-id="9b183-132">Das Präfix kann einen Pfad enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b183-132">The prefix can include a path.</span></span> <span data-ttu-id="9b183-133">Die Protokolldatei wird in das aktuelle Verzeichnis oder das im Präfix angegebene Verzeichnis geschrieben und weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="9b183-133">The log file is written to the current directory or the directory specified in the prefix and has the following format.</span></span></p>
<p><span data-ttu-id="9b183-134"><<em>Präfix</em> > -< <em>Anwendungsname</em> > . <<em>time</em> > . log</span><span class="sxs-lookup"><span data-stu-id="9b183-134"><<em>prefix</em>>-<<em>application name</em>>.<<em>time</em>>.log</span></span></p>
<p><span data-ttu-id="9b183-135">Wenn kein Präfix angegeben ist, wird eine leere Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b183-135">If a prefix is not specified, an empty string is used.</span></span> <span data-ttu-id="9b183-136">Gibt &quot; \* &quot; an, dass ein vorhandenes Präfix gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9b183-136">Specify &quot;\*&quot; to delete an existing prefix.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b183-137">-d</span><span class="sxs-lookup"><span data-stu-id="9b183-137">-d</span></span></td>
<td><p><span data-ttu-id="9b183-138">Gibt an, ob die Ausgabe der Ablauf Verfolgung in einem Debugger angezeigt oder in eine Datei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9b183-138">Specifies whether the trace output is displayed in a debugger or written to a file.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b183-139">0</span><span class="sxs-lookup"><span data-stu-id="9b183-139">0</span></span></td>
<td><span data-ttu-id="9b183-140">Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9b183-140">Default setting.</span></span> <span data-ttu-id="9b183-141">Schreibt in die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="9b183-141">Writes to log file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b183-142">1</span><span class="sxs-lookup"><span data-stu-id="9b183-142">1</span></span></td>
<td><span data-ttu-id="9b183-143">Wird in einem Debugger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b183-143">Displays in a debugger.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b183-144">-S</span><span class="sxs-lookup"><span data-stu-id="9b183-144">-s</span></span></td>
<td><p><span data-ttu-id="9b183-145">Gibt an, wie Netzwerk Datenverkehr (Anforderungen und Antworten) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9b183-145">Specifies how network traffic (requests and responses) is displayed.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b183-146">0</span><span class="sxs-lookup"><span data-stu-id="9b183-146">0</span></span></td>
<td><span data-ttu-id="9b183-147">Zeigt nur HTTP-Header an.</span><span class="sxs-lookup"><span data-stu-id="9b183-147">Only displays HTTP headers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b183-148">1</span><span class="sxs-lookup"><span data-stu-id="9b183-148">1</span></span></td>
<td><span data-ttu-id="9b183-149">Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9b183-149">Default setting.</span></span> <span data-ttu-id="9b183-150">Zeigt den Netzwerk Datenverkehr im American National Standards Institute (ANSI)-Format an.</span><span class="sxs-lookup"><span data-stu-id="9b183-150">Shows network traffic in American National Standards Institute (ANSI) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b183-151">2</span><span class="sxs-lookup"><span data-stu-id="9b183-151">2</span></span></td>
<td><span data-ttu-id="9b183-152">Zeigt den Netzwerk Datenverkehr im Hexadezimal Format an.</span><span class="sxs-lookup"><span data-stu-id="9b183-152">Shows network traffic in hexadecimal format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b183-153">-t</span><span class="sxs-lookup"><span data-stu-id="9b183-153">-t</span></span></td>
<td><p><span data-ttu-id="9b183-154">Gibt an, ob Funktionsaufrufe der obersten Ebene in der Ablauf Verfolgung aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9b183-154">Specifies whether top-level function calls are recorded in the trace.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b183-155">0</span><span class="sxs-lookup"><span data-stu-id="9b183-155">0</span></span></td>
<td><span data-ttu-id="9b183-156">Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9b183-156">Default setting.</span></span> <span data-ttu-id="9b183-157">Funktionsaufrufe werden nicht aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b183-157">Function calls are not recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b183-158">1</span><span class="sxs-lookup"><span data-stu-id="9b183-158">1</span></span></td>
<td><span data-ttu-id="9b183-159">Funktionsaufrufe der obersten Ebene werden aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b183-159">Top-level function calls are recorded.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b183-160">-M</span><span class="sxs-lookup"><span data-stu-id="9b183-160">-m</span></span></td>
<td><p><span data-ttu-id="9b183-161">Gibt die maximale Größe (in Bytes) einer Protokolldatei an, die von der Ablauf Verfolgungs Funktion generiert wird.</span><span class="sxs-lookup"><span data-stu-id="9b183-161">Specifies the maximum size, in bytes, of a log file generated by the tracing facility.</span></span> <span data-ttu-id="9b183-162">Wenn diese Option ohne Größe angegeben wird, beträgt der Mindestwert 65.535 bytes.</span><span class="sxs-lookup"><span data-stu-id="9b183-162">If this option is specified without a size, the minimum value is 65,535 bytes.</span></span> <span data-ttu-id="9b183-163">Wenn eine Protokolldatei die maximale Größe erreicht, wird der Inhalt der Datei gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9b183-163">If a log file reaches the maximum size, the contents of the file are erased.</span></span> <span data-ttu-id="9b183-164">Ablauf Verfolgungs Daten werden weiterhin in die Protokolldatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b183-164">Trace data continues to be written to the log file.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9b183-165">Wenn Sie das Konfigurationstool für die Ablauf Verfolgungs Einrichtung ausführen und keine Parameter angeben, werden die aktuellen Registrierungs Einstellungen abgerufen und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b183-165">Running the trace facility configuration tool and specifying no parameters retrieves and displays the current registry settings.</span></span>

> [!Note]  
> <span data-ttu-id="9b183-166">Protokolldateien werden schnell vergrößert und beeinträchtigen die Anwendungsleistung.</span><span class="sxs-lookup"><span data-stu-id="9b183-166">Log files grow rapidly and degrade application performance.</span></span> <span data-ttu-id="9b183-167">Stellen Sie sicher, dass der erforderliche Festplattenspeicher verfügbar ist, bevor Sie die Ablauf Verfolgungs Funktion aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9b183-167">Ensure that the required hard disk drive space is available before enabling the trace facility.</span></span>

 

## <a name="interpreting-trace-data"></a><span data-ttu-id="9b183-168">Interpretieren von Ablauf Verfolgungs Daten</span><span class="sxs-lookup"><span data-stu-id="9b183-168">Interpreting Trace Data</span></span>

<span data-ttu-id="9b183-169">Der Datenstrom der Ablauf Verfolgungs Einrichtung reflektiert die in der Anwendung aufgerufenen WinHTTP-Funktionen und alle gesendeten oder empfangenen HTTP-Daten.</span><span class="sxs-lookup"><span data-stu-id="9b183-169">The trace facility data stream reflects WinHTTP functions called in the application and any HTTP data sent or received.</span></span> <span data-ttu-id="9b183-170">In einigen Fällen werden auch Funktionen angezeigt, die intern von WinHTTP aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9b183-170">In some cases, functions called internally by WinHTTP are also shown.</span></span>

<span data-ttu-id="9b183-171">Die folgende Abbildung zeigt einen Teil einer Protokolldatei, die von der Ablauf Verfolgungs Funktion generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b183-171">The following image shows a portion of a log file generated by the trace facility.</span></span> <span data-ttu-id="9b183-172">Mehrere Elemente werden hervorgehoben und bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b183-172">Several items are highlighted and labeled.</span></span>

![Beispiel Ablauf Verfolgung](images/ss-tracer-wco.png)

<span data-ttu-id="9b183-174">Jede Zeile der Ablauf Verfolgungs Ausgabe enthält Informationen in drei Spalten.</span><span class="sxs-lookup"><span data-stu-id="9b183-174">Each line of trace output contains information in three columns.</span></span> <span data-ttu-id="9b183-175">Die erste Spalte zeigt das Datum und die Uhrzeit der Aufzeichnung des Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="9b183-175">The first column shows the date and time when the entry was recorded.</span></span> <span data-ttu-id="9b183-176">In der zweiten Spalte wird eine Anforderungs Kennung (ID) angezeigt, die zur Unterscheidung zwischen mehreren Anforderungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b183-176">The second column shows a request identifier (ID) that can be used to differentiate between multiple requests.</span></span> <span data-ttu-id="9b183-177">Wenn der Protokolleintrag nicht mit einer bestimmten Anforderung übereinstimmt, \* \* wird in dieser Spalte "Session" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b183-177">If the log entry does not correspond to a specific request, "\*Session\*" is displayed in this column.</span></span> <span data-ttu-id="9b183-178">Es kann nützlich sein, die Protokolldatei auf Grundlage dieser ID zu sortieren, um nur Ereignisse anzuzeigen, die für eine einzelne Anforderung auftreten.</span><span class="sxs-lookup"><span data-stu-id="9b183-178">It can be useful to sort the log file based on this ID to see only events that occur for a single request.</span></span> <span data-ttu-id="9b183-179">Das folgende Beispiel zeigt einen Befehl, den Sie zum Sortieren der Protokolldatei verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9b183-179">The following example shows a command you can use to sort the log file.</span></span>

<span data-ttu-id="9b183-180">**findstr 00000001 Logfile. log**</span><span class="sxs-lookup"><span data-stu-id="9b183-180">**findstr 00000001 LogFile.log**</span></span>

<span data-ttu-id="9b183-181">Die dritte Spalte zeigt einen Funktions-und HTTP-Datenverkehr oder eine Statusmeldung, die zur Interpretation der Ablauf Verfolgung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9b183-181">The third column shows a function call, HTTP traffic, or a status message included to help interpret the trace.</span></span>

<span data-ttu-id="9b183-182">Wenn ein Protokolleintrag einem Funktions aufzurufen entspricht, werden die Parameter der Funktion ebenfalls aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b183-182">When a log entry corresponds to a function call, the parameters of the function are also recorded.</span></span> <span data-ttu-id="9b183-183">Speicheradressen werden als hexadezimal angezeigt, während alle anderen Werte als ASCII-Zeichenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b183-183">Memory addresses are displayed in hexadecimal while all other values are displayed as an ASCII string.</span></span> <span data-ttu-id="9b183-184">Die Ablauf Verfolgungs Funktion zeichnet auch die Rückgabezeit und den Wert für jede Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9b183-184">The trace facility also records the return time and value for each function.</span></span>

<span data-ttu-id="9b183-185">Das Format der HTTP-Daten hängt von den Registrierungs Einstellungen ab, die mit dem Konfigurationstool für die Ablauf Verfolgungs Einrichtung angegeben werden</span><span class="sxs-lookup"><span data-stu-id="9b183-185">The format of HTTP data depends on the registry settings specified with the trace facility configuration tool.</span></span> <span data-ttu-id="9b183-186">Wenn HTTP-Daten verschlüsselt werden, werden die entschlüsselten Daten auch in der Ausgabe der Ablauf Verfolgung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b183-186">When HTTP data is encrypted, the decrypted data is also shown in the trace output.</span></span>

 

 




