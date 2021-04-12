---
title: Ablaufverfolgung
description: Die Ablauf Verfolgung verwendet die Ereignis Ablauf Verfolgung für Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Ablauf Verfolgung von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391238"
---
# <a name="tracing"></a><span data-ttu-id="a4b8d-106">Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="a4b8d-106">Tracing</span></span>

<span data-ttu-id="a4b8d-107">Die Ablauf Verfolgung verwendet die Ereignis Ablauf Verfolgung für Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-107">Tracing uses Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="a4b8d-108">Wenn Sie die in Windows Server 2008 R2 verfügbaren Ablauf Verfolgungs Tools nutzen möchten, installieren Sie die Microsoft Windows SDK von der [MSDN-Download](https://www.microsoft.com/download/details.aspx?id=8279) Website.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-108">To take advantage of the tracing tools available with Windows Server 2008 R2, install the Microsoft Windows SDK from the [MSDN Downloads](https://www.microsoft.com/download/details.aspx?id=8279) site.</span></span>


<span data-ttu-id="a4b8d-109">Es werden drei Ablauf Verfolgungs Ebenen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-109">There are three tracing levels supported:</span></span>

-   <span data-ttu-id="a4b8d-110">Ausführlich (alle verfügbaren Ablauf Verfolgungen).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-110">Verbose (all available traces).</span></span>
-   <span data-ttu-id="a4b8d-111">Info (Informations Ablauf Verfolgungen).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-111">Info (informational traces).</span></span>
-   <span data-ttu-id="a4b8d-112">Fehler (Fehler Ablauf Verfolgungen).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-112">Error (error traces).</span></span>

<span data-ttu-id="a4b8d-113">Die folgenden Ereignisse werden nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-113">The following events are traced:</span></span>

-   <span data-ttu-id="a4b8d-114">Alle Fehler (Level = Error, Level = Info oder Level = verbose).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-114">Any errors (Level=Error, Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="a4b8d-115">Eingang/Ende einer API (Level = Info oder Level = verbose).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-115">Entry/Exit of an API (Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="a4b8d-116">Start und Abschluss aller e/a-Vorgänge (Level = Info oder Level = verbose)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-116">Start and completion of any IO (Level=Info or Level=Verbose)</span></span>
-   <span data-ttu-id="a4b8d-117">Ausgetauschte SOAP-Nachrichten (Level = Verbose, verfügbar unter Windows 2003 SP1 und höher)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-117">Exchanged SOAP messages (Level=Verbose, available on Windows 2003 SP1 and later)</span></span>

## <a name="generating-and-viewing-wwsapi-traces"></a><span data-ttu-id="a4b8d-118">Erstellen und Anzeigen von wwsapi-Ablauf Verfolgungen</span><span class="sxs-lookup"><span data-stu-id="a4b8d-118">Generating and Viewing WWSAPI Traces</span></span>

<span data-ttu-id="a4b8d-119">Wwsapi verwendet die Manifest-basierten Ereignisse unter Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-119">WWSAPI uses the manifest based events on Windows Vista and above.</span></span> <span data-ttu-id="a4b8d-120">Folglich hat die Ablauf Verfolgung einige Unterschiede basierend auf der Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-120">As a result, the tracing experience has some differences based on the operating system version.</span></span> <span data-ttu-id="a4b8d-121">Etw-Ablauf Verfolgungen können mithilfe der in-Box-etw-Tools auf allen unterstützten Plattformen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-121">Generating ETW traces can be done by using the in-box ETW tools on all supported platforms.</span></span> <span data-ttu-id="a4b8d-122">Das Anzeigen der etw-Ablauf Verfolgungen in einem netten Format erfordert jedoch benutzerdefinierte Tools unter Windows XP SP2 und Windows 2003 SP1.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-122">However viewing the ETW traces in a nice format requires custom tools on Windows XP SP2 and Windows 2003 SP1.</span></span> <span data-ttu-id="a4b8d-123">Abhängig von der Betriebssystemversion gibt es verschiedene Methoden zum Erfassen und Anzeigen von wwsapi-ETW-Ereignis Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-123">There are few different ways of collecting and viewing WWSAPI ETW event traces depending on the operating system version.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a><span data-ttu-id="a4b8d-124">Aktivieren und Anzeigen von wwsapi-Ablauf Verfolgungen in Ereignisanzeige (funktioniert unter Windows Vista und höher)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-124">Enabling and Viewing WWSAPI traces in Event Viewer (works on Windows Vista and above)</span></span>

-   <span data-ttu-id="a4b8d-125">Führen Sie eventvwr. msc über die Befehlszeile oder das Menü ausführen aus.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-125">Run eventvwr.msc from command line or run menu.</span></span>
-   <span data-ttu-id="a4b8d-126">Klicken Sie im Aktionsbereich auf der rechten Seite auf den Link Ansicht, und aktivieren Sie die Option analytische und Debugprotokolle anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-126">Click the view link on the Actions pane on the right and enable Show Analytic and Debug logs option.</span></span>
-   <span data-ttu-id="a4b8d-127">Navigieren Sie im linken Bereich zu Anwendungs-und Dienst Protokolle \\ Microsoft \\ Windows- \\ Webdienste-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-127">Browse to Application and Service Logs\\Microsoft\\Windows\\WebServices providers on the left pane.</span></span>
-   <span data-ttu-id="a4b8d-128">Klicken Sie mit der rechten Maustaste auf den Ablauf Verfolgungs Anbieter und wählen Sie Protokoll</span><span class="sxs-lookup"><span data-stu-id="a4b8d-128">Right click the Tracing provider and select Enable log.</span></span>
-   <span data-ttu-id="a4b8d-129">Führen Sie das Szenario aus.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-129">Run your scenario.</span></span>
-   <span data-ttu-id="a4b8d-130">Wenn Sie die Seite Ereignisanzeige aktualisieren, sollten Sie die wwsapi-Ablauf Verfolgungs Einträge sehen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-130">When you refresh the event viewer page, you should start seeing the WWSAPI tracing entries.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a><span data-ttu-id="a4b8d-131">Aktivieren und Anzeigen von wwsapi-Ablauf Verfolgungen mithilfe Wstrace.bat Skripts (funktioniert auf XP SP2 und höher)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-131">Enabling and Viewing WWSAPI traces using Wstrace.bat Script (works on XPSP2 and above)</span></span>

<span data-ttu-id="a4b8d-132">Die wstrace.bat Batchdatei bietet eine bequeme Möglichkeit, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-132">The wstrace.bat batch file provides a convenient way to:</span></span>

-   <span data-ttu-id="a4b8d-133">Erstellen eines Ablauf Verfolgungs Protokolls</span><span class="sxs-lookup"><span data-stu-id="a4b8d-133">Create a trace log</span></span>
-   <span data-ttu-id="a4b8d-134">Löschen eines Ablauf Verfolgungs Protokolls</span><span class="sxs-lookup"><span data-stu-id="a4b8d-134">Delete a trace log</span></span>
-   <span data-ttu-id="a4b8d-135">Aktivieren und Deaktivieren der Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="a4b8d-135">Enable and disable tracing</span></span>
-   <span data-ttu-id="a4b8d-136">Aktualisieren der Ablauf Verfolgungs Ebene (Info/Fehler/verbose)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-136">Update the tracing level (info/error/verbose)</span></span>
-   <span data-ttu-id="a4b8d-137">Umstellen von Ablauf Verfolgungs Protokollen in CSV-Dateien</span><span class="sxs-lookup"><span data-stu-id="a4b8d-137">Converting trace logs to CSV files</span></span>

<span data-ttu-id="a4b8d-138">Die Batchdatei verwendet logman.exe für alle Befehle, mit der Ausnahme, dass die Protokolle in eine CSV-Datei umgerechnet werden, die ein benutzerdefiniertes Tool (wstracedump.exe) erfordert.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-138">The batch file uses logman.exe for all commands, with the exception of converting the logs to CSV file, which requires a custom tool (wstracedump.exe).</span></span>

## <a name="using-tracing-commands"></a><span data-ttu-id="a4b8d-139">Verwenden von Ablauf Verfolgungs Befehlen</span><span class="sxs-lookup"><span data-stu-id="a4b8d-139">Using tracing commands</span></span>

<span data-ttu-id="a4b8d-140">Mit dem folgenden Befehl wird ein Protokoll erstellt, das die Ebene Info, Error oder ausführliche verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-140">The following command creates a log that uses info, error or verbose level.</span></span> <span data-ttu-id="a4b8d-141">Dieser Befehl erfordert erhöhte Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-141">This command requires elevated privileges.</span></span>

<span data-ttu-id="a4b8d-142">**Fehler bei derwstrace.bat Create \[ Info- \| Fehler \|\]**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-142">**wstrace.bat create \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="a4b8d-143">Der folgende Befehl löscht das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-143">The following command deletes the log.</span></span> <span data-ttu-id="a4b8d-144">Dieser Befehl erfordert erhöhte Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-144">This command requires elevated privileges.</span></span>

<span data-ttu-id="a4b8d-145">**wstrace.bat löschen**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-145">**wstrace.bat delete**</span></span>

<span data-ttu-id="a4b8d-146">Der folgende Befehl aktiviert die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-146">The following command enables tracing.</span></span> <span data-ttu-id="a4b8d-147">Sie müssen zuerst ein Protokoll erstellen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-147">You must first create a log.</span></span>

<span data-ttu-id="a4b8d-148">**wstrace.bat**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-148">**wstrace.bat on**</span></span>

<span data-ttu-id="a4b8d-149">Die Ablauf Verfolgungs Ebene (Info, Error oder verbose) kann wie folgt geändert werden:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-149">The tracing level (info, error or verbose) can be modified as follows:</span></span>

<span data-ttu-id="a4b8d-150">**Fehler bei derwstrace.bat Update \[ Informationen \| \|\]**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-150">**wstrace.bat update \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="a4b8d-151">Verwenden Sie den folgenden Befehl, um die Ausgabe der Ablauf Verfolgung zu speichern:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-151">To dump the trace output, use the following command:</span></span>

<span data-ttu-id="a4b8d-152">**wstrace.bat > temp.csv**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-152">**wstrace.bat dump > temp.csv**</span></span>

<span data-ttu-id="a4b8d-153">Die Ereignisse werden in die CSV-Datei gekippt, bis STRG + C gedrückt wird oder die Ablauf Verfolgung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-153">The events will be dumped to the CSV file until Ctrl-C is pressed or tracing is disabled.</span></span>

## <a name="tracing-file-format"></a><span data-ttu-id="a4b8d-154">Format der Ablauf Verfolgungs Datei</span><span class="sxs-lookup"><span data-stu-id="a4b8d-154">Tracing File format</span></span>

<span data-ttu-id="a4b8d-155">Die von wstrace.bat erstellten CSV-Dateien sind einfache Textdateien mit Komma getrennter Variable.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-155">The CSV files created by wstrace.bat are simple comma-separated-variable text files.</span></span> <span data-ttu-id="a4b8d-156">Diese Dateien können in Excel, Notepad usw. geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-156">These files may be opened in Excel, Notepad, etc.</span></span>

<span data-ttu-id="a4b8d-157">Die Spalten der Datei lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-157">The columns of the file are as follows:</span></span>

-   <span data-ttu-id="a4b8d-158">Zeitstempel-Zeitstempel des Zeitrahmens, zu dem das Ereignis aufgezeichnet wurde</span><span class="sxs-lookup"><span data-stu-id="a4b8d-158">TimeStamp - Time stamp of when the event was recorded</span></span>
-   <span data-ttu-id="a4b8d-159">ProcessID-ULONG-ID des Prozesses, der das Ereignis aufzeichnen soll.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-159">ProcessID - ULONG ID of the process recording the event</span></span>
-   <span data-ttu-id="a4b8d-160">ThreadID-ULONG-ID des Threads, der das Ereignis aufzeichnen hat</span><span class="sxs-lookup"><span data-stu-id="a4b8d-160">ThreadID - ULONG ID of the thread recording the event</span></span>
-   <span data-ttu-id="a4b8d-161">Der ereignisenumerationswert des Ereignis Typs ist möglicherweise ("API Enter" "API Enter", API Pending "" API \| \| exitsyncsuccess " \| " API exitsyncfailure " \| " API exitasyncsuccess "" API exitasyncfailure "" IO Started "" e/a-Vorgang abgeschlossen "" e/a- \| \| \| \| Fehler "" \| Fehler " \| " empfangener Nachrichten Start " \| \| \| \| \| " empfangene Meldung "" empfangene Nachricht wird beendet</span><span class="sxs-lookup"><span data-stu-id="a4b8d-161">Event - Enumerated value of the event type may be ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")</span></span>
-   <span data-ttu-id="a4b8d-162">Operation: der Name des aufgerufenen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-162">Operation - The name of the operation being invoked.</span></span> <span data-ttu-id="a4b8d-163">In der Regel wird dies der API zugeordnet, die aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-163">Typically this maps to the API being called.</span></span>
-   <span data-ttu-id="a4b8d-164">Fehler: optionale HRESULT-Fehlernummer</span><span class="sxs-lookup"><span data-stu-id="a4b8d-164">Error - Optional HRESULT error number</span></span>
-   <span data-ttu-id="a4b8d-165">Info: optionale Informationen zum Ereignis</span><span class="sxs-lookup"><span data-stu-id="a4b8d-165">Info - Optional information about the event</span></span>

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a><span data-ttu-id="a4b8d-166">Sammeln einer wwsapi-etw-Ablauf Verfolgungs Datei mithilfe von etw-Tools (funktioniert auf XP SP2 und höher)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-166">Collecting WWSAPI ETW Trace File using ETW tools (works on XPSP2 and above)</span></span>

<span data-ttu-id="a4b8d-167">Aktivieren der etw-Ablauf Verfolgung für wwsapi</span><span class="sxs-lookup"><span data-stu-id="a4b8d-167">Enabling ETW tracing for WWSAPI</span></span>

<span data-ttu-id="a4b8d-168">**logman Start wstrace-SB 64-ft 1-RT-p Microsoft-Windows-Webservices \[ Flags \[ Level \] \] \[ -o <EtlLogFileName> \] -ETS**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-168">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[flags \[level\]\] \[-o <EtlLogFileName>\] -ets**</span></span>

<span data-ttu-id="a4b8d-169">, um die ETW-Ablauf Verfolgungs Sitzung zu erstellen und zu starten.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-169">to create and start the ETW tracing session.</span></span> <span data-ttu-id="a4b8d-170">Logman.exe ist ein in-Box-etw-Tool, das auf allen unterstützten Plattformen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-170">Logman.exe is an in-box ETW tool available on all supported platforms.</span></span> <span data-ttu-id="a4b8d-171">Beachten Sie, dass Sie Microsoft \_ Windows \_ -Webdienste als Anbieter Namen auf XP SP2 und W2K3 verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-171">Note that you need to use Microsoft\_Windows\_WebServices as the provider name on XPSP2 and W2K3.</span></span> <span data-ttu-id="a4b8d-172">Sie können Logman Query Providers ausführen, um die Liste der registrierten Anbieter anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-172">You can run logman query providers to see the list of registered providers.</span></span> <span data-ttu-id="a4b8d-173">Der Anbieter Microsoft-Windows-Webservices (oder Microsoft \_ Windows \_ Webservices) sollte aufgeführt werden, es sei denn, er ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-173">Microsoft-Windows-WebServices (or Microsoft\_Windows\_WebServices) provider should be listed unless it is not registered.</span></span> <span data-ttu-id="a4b8d-174">Der Anbieter wird normalerweise während des Setups registriert.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-174">The provider is normally registered during setup.</span></span> <span data-ttu-id="a4b8d-175">Sie kann jedoch auch manuell durch Ausführen von wevtutil.exe im <ManifestFileName> (unter Windows Vista und höher) oder mofcomp.exe <MofFileName> (auf XP SP2 und W2K3) registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-175">However it can also be manually registered by running wevtutil.exe im <ManifestFileName> (on Windows Vista and Later) or mofcomp.exe <MofFileName> (on XPSP2 and W2K3).</span></span>

<span data-ttu-id="a4b8d-176">Flags können verwendet werden, um die Ablauf Verfolgungen nach ihrer Art zu filtern.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-176">Flags can be used to filter the traces by their kind.</span></span> <span data-ttu-id="a4b8d-177">Der Wert kann oder ein Wert der folgenden Ablauf Verfolgungs Arten sein.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-177">It can be OR'd value of the following trace kinds.</span></span> <span data-ttu-id="a4b8d-178">Wenn keine Angabe erfolgt, werden alle Ablauf Verfolgungs Arten aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-178">If not supplied, all trace kinds are enabled.</span></span>

-   <span data-ttu-id="a4b8d-179">0x1-API-Eintrags-und Beendigungs Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-179">0x1 - API entry/exit traces.</span></span>
-   <span data-ttu-id="a4b8d-180">0x2-Fehler Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-180">0x2 - Error traces.</span></span>
-   <span data-ttu-id="a4b8d-181">0x4-e/a-Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-181">0x4 - IO traces.</span></span>
-   <span data-ttu-id="a4b8d-182">0x8: SOAP-Nachrichten Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-182">0x8 - SOAP message traces.</span></span>
-   <span data-ttu-id="a4b8d-183">0x10-binäre Nachrichten Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-183">0x10 - Binary message traces.</span></span>

<span data-ttu-id="a4b8d-184">Die Ebene kann verwendet werden, um die Ablauf Verfolgungen nach ihrer Ebene zu filtern.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-184">Level can be used to filter the traces by their level.</span></span> <span data-ttu-id="a4b8d-185">Es muss sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-185">It should be one of the following values.</span></span> <span data-ttu-id="a4b8d-186">Wenn keine Angabe erfolgt, werden alle Ablauf Verfolgungs Ebenen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-186">If not supplied, all trace levels are enabled.</span></span>

-   <span data-ttu-id="a4b8d-187">0x1-schwerwiegende Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-187">0x1 - Fatal traces.</span></span>
-   <span data-ttu-id="a4b8d-188">0x2-Fehler Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-188">0x2 - Error traces.</span></span>
-   <span data-ttu-id="a4b8d-189">0x3-Warnungs Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-189">0x3 - Warning traces.</span></span>
-   <span data-ttu-id="a4b8d-190">0x4-Informations Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-190">0x4 - Informational traces.</span></span>
-   <span data-ttu-id="a4b8d-191">0x5-ausführliche Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-191">0x5 - Verbose traces.</span></span>

<span data-ttu-id="a4b8d-192">Etllogfilename ist der Pfad zu der zu erstellenden etw-Ereignisprotokoll Datei (ETL-Erweiterung verwenden).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-192">EtlLogFileName is the path to the ETW event log file to be created (use .etl extension).</span></span> <span data-ttu-id="a4b8d-193">Wenn kein Wert angegeben wird, wählt etw einen zufälligen Namen aus, der später abgefragt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-193">If not provided, ETW will pick a random name which can be queried later.</span></span> <span data-ttu-id="a4b8d-194">Diese Datei darf sich nicht im Profilverzeichnis des Benutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-194">This file should not reside on user's profile directory.</span></span> <span data-ttu-id="a4b8d-195">Die ETW-Ereignisprotokoll Datei (ETL-Datei) liegt im Binärformat vor.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-195">ETW event log file (.etl file) is in binary format.</span></span> <span data-ttu-id="a4b8d-196">Sie kann von etw-Anwendungen genutzt werden, ist aber nicht in einem lesbaren Format.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-196">It can be consumed by ETW applications, but it is not in human readable format.</span></span> <span data-ttu-id="a4b8d-197">Im nächsten Schritt wird beschrieben, wie der Inhalt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-197">Next step describes how to view its content.</span></span>

<span data-ttu-id="a4b8d-198">Ausführen Ihres Szenarios</span><span class="sxs-lookup"><span data-stu-id="a4b8d-198">Run your scenario</span></span>

<span data-ttu-id="a4b8d-199">Die ETW-Ereignisprotokoll Datei wird gesammelt.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-199">Collecting ETW event log file.</span></span>

<span data-ttu-id="a4b8d-200">**logman stoppt wstrace-ETS.**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-200">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="a4b8d-201">zum Abbrechen der etw-Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-201">to stop the ETW tracing session.</span></span> <span data-ttu-id="a4b8d-202">Dies ist der Fall, wenn etw die Protokollierung der Ereignisse beendet.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-202">This is when ETW stops logging the events.</span></span> <span data-ttu-id="a4b8d-203">Die ETW-Ereignisprotokoll Datei (angegeben im etllogfilename-Parameter) ist einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-203">ETW event log file (specified in EtlLogFileName parameter) is ready to consume.</span></span> <span data-ttu-id="a4b8d-204">Sie können entweder lokal (Anweisungen unten) angezeigt oder zur Untersuchung an die Produktgruppe gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-204">It can either be viewed locally (instructions are given below) or sent to the product group for investigation.</span></span>

<span data-ttu-id="a4b8d-205">End-to-End-Beispiel mit etw-Tools:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-205">End to end example using ETW tools:</span></span>

<span data-ttu-id="a4b8d-206">**logman Start wstrace-b 64-ft 1-RT-p Microsoft-Windows-Webservices-o mytrace. ETL-ETS**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-206">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**</span></span>

<span data-ttu-id="a4b8d-207">**Echo. Führen Sie das Szenario aus.**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-207">**echo .. run your scenario..**</span></span>

<span data-ttu-id="a4b8d-208">**logman stoppt wstrace-ETS.**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-208">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="a4b8d-209">**tracerpt mytrace. ETL-o mytrace.xml**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-209">**tracerpt mytrace.etl -o mytrace.xml**</span></span>

<span data-ttu-id="a4b8d-210">**wstrace.htm**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-210">**wstrace.htm**</span></span>

<span data-ttu-id="a4b8d-211">**Echo. Verwenden Sie in der geöffneten Seite mytrace.xml und wstrace. Xsl.**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-211">**echo .. use mytrace.xml and wstrace.xsl in the opened page ..**</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a><span data-ttu-id="a4b8d-212">Anzeigen von Ablauf Verfolgungen der wwsapi-etw-Ablauf Verfolgungs Datei mit wstracedump.exe Tool (funktioniert unter Windows XP und höher)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-212">Viewing WWSAPI ETW Trace File traces using wstracedump.exe tool (works on Windows XP and above)</span></span>

<span data-ttu-id="a4b8d-213">Wstracedump.exe ist ein benutzerdefiniertes etw-consumertool, das Ereignisse in der wwsapi-etw-Ablauf Verfolgungs Datei verarbeitet und eine lesbare Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-213">Wstracedump.exe is a custom developed ETW consumer tool which processes events in the WWSAPI ETW trace file and produces human readable output.</span></span> <span data-ttu-id="a4b8d-214">Sie kann die Ausgabe von allen unterstützten Plattformen liefern.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-214">It can produce output from all supported platforms.</span></span> <span data-ttu-id="a4b8d-215">Weitere Informationen finden Sie in der Verwendung (wstracedump.exe-?).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-215">See its usage (wstracedump.exe -?) for more information.</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a><span data-ttu-id="a4b8d-216">Anzeigen von wwsapi-etw-Ablauf Verfolgungs Datei-Ablauf Verfolgungen mit etw-Tools (funktioniert unter Windows Vista und höher)</span><span class="sxs-lookup"><span data-stu-id="a4b8d-216">Viewing WWSAPI ETW Trace File traces using ETW tools (works on Windows Vista and above)</span></span>

<span data-ttu-id="a4b8d-217">Tracerpt.exe ist das Tool, um den Inhalt einer etw-Ereignisprotokoll Datei anzuzeigen und auf allen unterstützten Plattformen verfügbar zu sein.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-217">Tracerpt.exe is the tool to view the content of an ETW event log file and available on all supported platforms.</span></span> <span data-ttu-id="a4b8d-218">Es kann zum Generieren von CSV-, evtx-oder XML-Dumpdateien aus einer etw-Ereignisprotokoll Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-218">It can be used to generate CSV, EVTX or XML dump files from an ETW event log file.</span></span> <span data-ttu-id="a4b8d-219">Die generierte Ausgabedatei enthält jedoch nur in Windows Vista und höher lesbare Ablauf Verfolgungen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-219">However the generated output file has human readable traces only on Windows Vista and later.</span></span> <span data-ttu-id="a4b8d-220">In diesen Anweisungen wird beschrieben, wie die XML-Dumpdatei generiert und zusammen mit einer XSL-Datei verwendet wird, um die Ablauf Verfolgungen in einem schönen Format anzuzeigen (die XSL-Datei ist sehr trivial und kann geändert werden, wenn verschiedene Formate gewünscht werden).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-220">These instructions describes how to generate the XML dump file and use it along with an xsl file to display the traces in a nice format (xsl file is very trivial and may be altered if different formats are desired).</span></span>

-   <span data-ttu-id="a4b8d-221">Ausführen</span><span class="sxs-lookup"><span data-stu-id="a4b8d-221">Run</span></span>

    <span data-ttu-id="a4b8d-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span></span>

    <span data-ttu-id="a4b8d-223">zum Erstellen eines XML-Dumps aus der binären ETL-Datei (tracerpt.exe erstellt die Ausgabedatei standardmäßig im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-223">to create an XML dump from the binary ETL file (tracerpt.exe creates the output file in XML format by default.</span></span> <span data-ttu-id="a4b8d-224">Führen Sie tracerpt-? aus.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-224">Run tracerpt -?</span></span> <span data-ttu-id="a4b8d-225">Um andere verfügbare Formate anzuzeigen).</span><span class="sxs-lookup"><span data-stu-id="a4b8d-225">To see other available formats).</span></span>

-   <span data-ttu-id="a4b8d-226">An diesem Punkt können Sie die Ablauf Verfolgungs Informationen in der XML-Datei sehen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-226">At this point, you can see the tracing information in the XML file.</span></span> <span data-ttu-id="a4b8d-227">Außerdem können Sie die wstrace.htm Datei öffnen und die XML-Dumpdatei und die wstrace. XSL-Datei verwenden, um die Ablauf Verfolgungen in einem günstigeren Format anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-227">Additionally, you can open the wstrace.htm file and use the xml dump file and the wstrace.xsl file to see the traces in a nicer format.</span></span> <span data-ttu-id="a4b8d-228">Beachten Sie, dass sich die Dateien auf dem lokalen Computer befinden müssen, damit diese HTML-Datei auf IE verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-228">Note that the files need to be on the local machine to be able to use this html file on IE.</span></span>

## <a name="security"></a><span data-ttu-id="a4b8d-229">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a4b8d-229">Security</span></span>

<span data-ttu-id="a4b8d-230">Beim Aktivieren der Ablauf Verfolgung sollten Administratoren berücksichtigen, dass Sie zusätzlichen Speicherplatz und Rechenleistung beansprucht.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-230">When enabling tracing, administrators should take into account that it consumes additional disk space and computation power.</span></span> <span data-ttu-id="a4b8d-231">Ein böswilliger Client oder eine Anwendung kann Systemressourcen abschöpfen, es sei denn, die Ablauf Verfolgungs Einstellungen sind mit angemessenen Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="a4b8d-231">A malicious client or application may exhaust system resources unless tracing settings are configured with reasonable limits.</span></span> <span data-ttu-id="a4b8d-232">Bei Verwendung der Nachrichten Ablauf Verfolgung können Nachrichten, die vertrauliche Informationen wie Anmelde Informationen, persönliche Informationen usw. verwenden, auf dem Datenträger persistent gespeichert werden oder von jedem Benutzer mit Zugriff auf die System Ereignisanzeige angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-232">When using message tracing feature, messages carrying sensitive information such as credentials, personal information, etc. may be persisted to the disk or be viewed by anyone who has access to the system event viewer.</span></span> <span data-ttu-id="a4b8d-233">Um dieses Problem zu beheben, kann die Ablauf Verfolgung von System-oder Administrator Benutzern unter Windows 2003 und höher aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-233">As a mitigation to this issue, tracing can be enabled by System or Administrator users on Windows 2003 and later.</span></span> <span data-ttu-id="a4b8d-234">Die Nachrichten Ablauf Verfolgung ist unter Windows XP deaktiviert, auf der alle Benutzer die Ablauf Verfolgung aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="a4b8d-234">Message tracing is disabled on Windows XP on which any user can turn tracing on.</span></span>

<span data-ttu-id="a4b8d-235">Die folgende Enumeration wird für die Ablauf Verfolgung verwendet:</span><span class="sxs-lookup"><span data-stu-id="a4b8d-235">The following enumeration is used with tracing:</span></span>

-   [<span data-ttu-id="a4b8d-236">**WS- \_ Trace- \_ API**</span><span class="sxs-lookup"><span data-stu-id="a4b8d-236">**WS\_TRACE\_API**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




