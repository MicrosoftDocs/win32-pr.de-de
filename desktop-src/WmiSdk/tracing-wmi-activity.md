---
description: Ab Windows Vista verwendet der WMI-Dienst nicht die WMI-Protokolldateien. Stattdessen wird die Ereignis Ablauf Verfolgung für Windows (ETW) verwendet, und Ereignisse sind über Ereignisanzeige oder das Befehlszeilen Tool wevtutil verfügbar.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: WMI-Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758005"
---
# <a name="tracing-wmi-activity"></a><span data-ttu-id="9b7e3-104">WMI-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9b7e3-104">Tracing WMI Activity</span></span>

<span data-ttu-id="9b7e3-105">Ab Windows Vista verwendet der WMI-Dienst nicht die [WMI-Protokolldateien](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e3-105">Starting with Windows Vista, the WMI service does not use the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="9b7e3-106">Stattdessen wird die [Ereignis Ablauf Verfolgung für Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) verwendet, und Ereignisse sind über **Ereignisanzeige** oder das Befehlszeilen Tool wevtutil verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-106">Instead, it uses [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) and events are available through **Event Viewer** or the Wevtutil command-line tool.</span></span>

<span data-ttu-id="9b7e3-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="9b7e3-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="9b7e3-108">Abrufen von WMI-Ereignissen durch Ereignisanzeige</span><span class="sxs-lookup"><span data-stu-id="9b7e3-108">Obtaining WMI Events Through Event Viewer</span></span>](#obtaining-wmi-events-through-event-viewer)
-   [<span data-ttu-id="9b7e3-109">Aktivieren der WMI-Ablauf Verfolgung an der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="9b7e3-109">Enabling WMI Tracing at Command Prompt</span></span>](#enabling-wmi-tracing-at-command-prompt)
-   [<span data-ttu-id="9b7e3-110">Verwenden der WPP-basierten WMI-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9b7e3-110">Using WPP-based WMI Tracing</span></span>](#using-wpp-based-wmi-tracing)
-   [<span data-ttu-id="9b7e3-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b7e3-111">Related topics</span></span>](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a><span data-ttu-id="9b7e3-112">Abrufen von WMI-Ereignissen durch Ereignisanzeige</span><span class="sxs-lookup"><span data-stu-id="9b7e3-112">Obtaining WMI Events Through Event Viewer</span></span>

<span data-ttu-id="9b7e3-113">Die Datei "wmitracing. log" enthält die Ereignisse, die von WMI verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-113">The WMITracing.log file contains the events that WMI traces.</span></span> <span data-ttu-id="9b7e3-114">Dabei handelt es sich jedoch um eine Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-114">However, this is a binary file.</span></span> <span data-ttu-id="9b7e3-115">Um diese Ereignisse in einem Format anzuzeigen, das von Menschen lesbar ist, verwenden Sie die **Ereignisanzeige**.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-115">To see these events in a format readable by humans, use the **Event Viewer**.</span></span>

<span data-ttu-id="9b7e3-116">Standardmäßig werden keine WMI-Ereignisse verfolgt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-116">By default, WMI events are not traced.</span></span> <span data-ttu-id="9b7e3-117">In diesem Verfahren wird beschrieben, wie Sie mit **Ereignisanzeige** die WMI-Ereignis Ablauf Verfolgung aktivieren und WMI-Ereignisse suchen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-117">This procedure describes how to use **Event Viewer** to enable WMI event tracing and locate WMI events.</span></span> <span data-ttu-id="9b7e3-118">Sie können die gleichen Vorgänge auch über das Befehlszeilen Tool wevtutil ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-118">You can do the same operations through the wevtutil command-line tool.</span></span>

<span data-ttu-id="9b7e3-119">**So zeigen Sie WMI-Ereignisse in Ereignisanzeige an**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-119">**To view WMI Events in Event Viewer**</span></span>

1.  <span data-ttu-id="9b7e3-120">Öffnen Sie die **Ereignisanzeige**.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-120">Open **Event Viewer**.</span></span> <span data-ttu-id="9b7e3-121">Klicken Sie im Menü **Ansicht** auf **Analytische und Debugprotokolle einblenden**.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-121">On the **View** menu, click **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="9b7e3-122">Suchen Sie  unter Anwendungs-und Dienst Protokolle \| Microsoft \| Windows \| WMI-Aktivität nach dem Ablauf Verfolgungs Kanal Protokoll für WMI.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-122">Locate the **Trace** channel log for WMI under Applications and Service Logs \| Microsoft \| Windows \| WMI Activity.</span></span>
2.  <span data-ttu-id="9b7e3-123">Klicken Sie mit der rechten Maustaste auf das Ablauf **Verfolgungs** Protokoll, und wählen Sie **Log**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-123">Right-click the **Trace** log and select **Log Properties**.</span></span> <span data-ttu-id="9b7e3-124">Aktivieren Sie das Kontrollkästchen **Protokollierung aktivieren** , um die WMI-Ereignis Ablauf Verfolgung zu starten.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-124">Click the **Enable Logging** check box to start the WMI event tracing.</span></span> <span data-ttu-id="9b7e3-125">Weitere Informationen zu Kanälen finden Sie unter [Ereignisprotokolle und Kanäle im Windows-Ereignisprotokoll](/previous-versions//aa385225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b7e3-125">For more information about channels, see [Event Logs and Channels in Windows Event Log](/previous-versions//aa385225(v=vs.85)).</span></span>
3.  <span data-ttu-id="9b7e3-126">WMI-Ereignisse werden im Ereignisfenster für **WMI-Activity** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-126">WMI events appear in the event window for **WMI-Activity**.</span></span> <span data-ttu-id="9b7e3-127">Doppelklicken Sie auf ein Ereignis in der Liste, um die detaillierten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-127">Double-click an event in the list to see the detailed information.</span></span> <span data-ttu-id="9b7e3-128">Sie können ein Ereignis in der **XML-Ansicht** oder im **Anzeige Format anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="9b7e3-128">You can view an event in **XML View** or in **Friendly View** format.</span></span>

<span data-ttu-id="9b7e3-129">Das Feld **Ereignis-ID** zeigt einen Wert an, der die folgenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-129">The **Event ID** field displays a value that contains the following information.</span></span>

<dl> <dt>

<span data-ttu-id="9b7e3-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Ereignis 1</span><span class="sxs-lookup"><span data-stu-id="9b7e3-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Event 1</span></span>
</dt> <dd>

<span data-ttu-id="9b7e3-131">Beginn der Ereignis Sequenz für einen bestimmten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-131">Start of the event sequence for a specific operation.</span></span> <span data-ttu-id="9b7e3-132">Ein Vorkommen für jede Sequenz.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-132">One occurrence for each sequence.</span></span>

<span data-ttu-id="9b7e3-133">Die Ereignis Felder für ein Ereignis 1 lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9b7e3-133">The event fields for an Event 1 are:</span></span>

-   <span data-ttu-id="9b7e3-134">**Groupoperationid** ist ein eindeutiger Bezeichner, der für alle Ereignisse verwendet wird, die für einen bestimmten Client gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-134">**GroupOperationID** is a unique identifier that is used for all events reported for a specific client.</span></span>
-   <span data-ttu-id="9b7e3-135">**OperationId** gibt die Vorgangs Sequenz an.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-135">**OperationId** indicates the operation sequence.</span></span>
-   <span data-ttu-id="9b7e3-136">Der **Vorgang** gibt die Verbindung oder die WMI-Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-136">**Operation** specifies the connection or request to WMI.</span></span>
-   <span data-ttu-id="9b7e3-137">Der **Benutzer** gibt das Konto an, das eine WMI-Anforderung durch Ausführen eines Skripts oder mithilfe von CIM Studio sendet.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-137">**User** indicates the account that makes a request to WMI by running a script or through CIM Studio.</span></span>
-   <span data-ttu-id="9b7e3-138">**Namespace** zeigt den WMI-Namespace an, mit dem die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-138">**Namespace** shows the WMI namespace to which the connection is made.</span></span>

<span data-ttu-id="9b7e3-139">Beispielsweise kann ein Skript alle Instanzen einer WMI-Klasse, z. b. den [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service), anfordern.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-139">For example, a script may request all the instances of a WMI class, such as [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="9b7e3-140">Der erste Vorgang ist möglicherweise eine Verbindung mit WMI.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-140">The first operation may be a connection to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="9b7e3-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Ereignis 2</span><span class="sxs-lookup"><span data-stu-id="9b7e3-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Event 2</span></span>
</dt> <dd>

<span data-ttu-id="9b7e3-142">Ereignisse, die den Vorgang ausmachen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-142">Events that make up the operation.</span></span> <span data-ttu-id="9b7e3-143">Ein oder mehrere Vorkommen in der Sequenz.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-143">One or more occurrences in the sequence.</span></span>

<span data-ttu-id="9b7e3-144">Die Ereignis Felder für ein Ereignis 2 lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9b7e3-144">The event fields for an Event 2 are:</span></span>

-   <span data-ttu-id="9b7e3-145">**Groupoperationid** gibt die Reihenfolge an, in der das Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-145">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="9b7e3-146">**Groupoperationid** gibt die Reihenfolge an, in der das Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-146">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="9b7e3-147">**ProviderName** gibt den Namen des Anbieters an, der die Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-147">**ProviderName** indicates the name of the provider which supplies the data.</span></span>
-   <span data-ttu-id="9b7e3-148">**Path** ist der WMI-Pfad zum Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-148">**Path** is the WMI path to the object.</span></span>

<span data-ttu-id="9b7e3-149">Der Vorgang kann beispielsweise eine Enumeration des Win32- [**\_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service)sein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-149">For example, the operation may be an enumeration of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e3-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Ereignis 3</span><span class="sxs-lookup"><span data-stu-id="9b7e3-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Event 3</span></span>
</dt> <dd>

<span data-ttu-id="9b7e3-151">Ende der Ereignis Sequenz für einen bestimmten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-151">End of the event sequence for a specific operation.</span></span> <span data-ttu-id="9b7e3-152">Ein Vorkommen für jede Sequenz.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-152">One occurrence for each sequence.</span></span>

<span data-ttu-id="9b7e3-153">Nur **groupoperationid** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-153">Only the **GroupOperationID** is shown.</span></span>

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a><span data-ttu-id="9b7e3-154">Aktivieren der WMI-Ablauf Verfolgung an der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="9b7e3-154">Enabling WMI Tracing at Command Prompt</span></span>

<span data-ttu-id="9b7e3-155">Sie können die WMI-Ereignis Ablauf Verfolgung auch über das Befehlszeilen Tool "wevtutil" aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-155">You can also enable WMI event tracing through the Wevtutil command-line tool.</span></span> <span data-ttu-id="9b7e3-156">Verwenden Sie den folgenden Befehl: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-156">Use the following command: **Wevtutil.exe sl Microsoft-Windows-WMI-Activity/Trace /e:true**.</span></span> <span data-ttu-id="9b7e3-157">Die WMI-Ereignis Quelle lautet Microsoft-Windows-WMI.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-157">The WMI event source is Microsoft-Windows-WMI.</span></span> <span data-ttu-id="9b7e3-158">Weitere Informationen zu Wevtutil.exe finden Sie unter Informationen [zum Windows-Ereignisprotokoll](/previous-versions//aa382610(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b7e3-158">For more information about Wevtutil.exe, see [About Windows Event Log](/previous-versions//aa382610(v=vs.85)).</span></span>

## <a name="using-wpp-based-wmi-tracing"></a><span data-ttu-id="9b7e3-159">Verwenden der WPP-basierten WMI-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9b7e3-159">Using WPP-based WMI Tracing</span></span>

<span data-ttu-id="9b7e3-160">In Windows-Betriebssystemen ab Windows Vista erstellt WMI während des Startvorgangs einen aktiven Ablauf Verfolgungs Kanal.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-160">In Windows operating systems starting with Windows Vista, WMI creates an active trace channel during the boot process.</span></span> <span data-ttu-id="9b7e3-161">Der Name des Kanals lautet WMI-Ablauf \_ Verfolgungs \_ Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-161">The name of the channel is WMI\_Trace\_Session.</span></span> <span data-ttu-id="9b7e3-162">Nur Fehler werden im Kanal protokolliert.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-162">Only errors are logged to the channel.</span></span>

<span data-ttu-id="9b7e3-163">Der Windows-Ablaufverfolgungs-Präprozessor (WPP) zeichnet Informationen in einer Binärdatei auf.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-163">The Windows software trace preprocessor (WPP) records information in a binary file.</span></span> <span data-ttu-id="9b7e3-164">Um die Datei zu lesen, müssen Sie Sie zuerst in ein lesbares Textformat übersetzen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-164">To read the file, you must first translate it into a readable, text format.</span></span> <span data-ttu-id="9b7e3-165">Verwenden Sie zum Durchführen der Übersetzung ein Tool namens tracefmt.exe aus dem [Windows-Treiberkit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) .</span><span class="sxs-lookup"><span data-stu-id="9b7e3-165">You use a tool called tracefmt.exe from the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to do the translation.</span></span> <span data-ttu-id="9b7e3-166">Das Tool erfordert Informationen, die in einigen zugeordneten Dateien gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-166">The tool requires information stored in some associated files.</span></span> <span data-ttu-id="9b7e3-167">Die Dateien befinden sich im Verzeichnis "% SystemRoot% \\ system32 \\ WBEM \\ TMF" und haben die Dateinamenerweiterung ". TMF".</span><span class="sxs-lookup"><span data-stu-id="9b7e3-167">The files are located in the %SystemRoot%\\System32\\wbem\\tmf directory and have a .tmf file name extension.</span></span> <span data-ttu-id="9b7e3-168">Das Tool erfordert tatsächlich eine einzelne TMF-Datei.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-168">The tool actually requires a single .tmf file .</span></span> <span data-ttu-id="9b7e3-169">Sie erstellen diese einzelne Datei, indem Sie alle TMF-Dateien in einer anderen TMF-Datei verketten.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-169">You make that single file by concatenating all of the .tmf files into another .tmf file.</span></span> <span data-ttu-id="9b7e3-170">Weitere Informationen zu TMF-Dateien finden Sie unter [Format Datei der Ablauf Verfolgungs Meldung](/windows-hardware/drivers/devtest/trace-message-format-file).</span><span class="sxs-lookup"><span data-stu-id="9b7e3-170">For more information about .tmf files, see [Trace Message Format File](/windows-hardware/drivers/devtest/trace-message-format-file).</span></span>

<span data-ttu-id="9b7e3-171">Nachdem Sie das [Windows-Treiberkit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) zum Abrufen der tracelog.exe und tracefmt.exe Befehlszeilen Tools installiert haben, führen Sie die folgenden Schritte aus, um eine WPP-basierte WMI-Ablauf Verfolgung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-171">After installing the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to get the tracelog.exe and tracefmt.exe command-line tools, perform the following steps to collect a WPP-based WMI trace.</span></span>

<span data-ttu-id="9b7e3-172">**So zeigen Sie eine WPP-basierte WMI-Ablauf Verfolgung an**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-172">**To view a WPP-based WMI trace**</span></span>

1.  <span data-ttu-id="9b7e3-173">Öffnen Sie zum Erstellen der einzelnen TMF-Datei ein Eingabe Aufforderungs Fenster mit erhöhten Rechten, und navigieren Sie zum Verzeichnis% systemroot% \\ system32 \\ WBEM \\ TMF.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-173">To create the single .tmf file, open an elevated Command Prompt window and navigate to the %SystemRoot%\\System32\\wbem\\tmf directory.</span></span>

2.  <span data-ttu-id="9b7e3-174">Geben Sie **Copy/y% systemroot% \\ system32 \\ WBEM \\ TMF \\ \* . TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-174">Type **copy /y %SystemRoot%\\System32\\wbem\\tmf\\\*.tmf %SystemRoot%\\System32\\wbem\\tmf\\wmi.tmf**.</span></span> <span data-ttu-id="9b7e3-175">Dadurch wird eine Datei mit dem Namen "WMI. TMF" erstellt, die den Inhalt aller anderen TMF-Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-175">This will create a file named wmi.tmf that includes the contents of all of the other .tmf files.</span></span>

3.  <span data-ttu-id="9b7e3-176">Geben Sie **tracelog-WMI-Ablauf \_ Verfolgungs \_ Sitzung** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-176">Type **tracelog -flush WMI\_Trace\_Session**.</span></span> <span data-ttu-id="9b7e3-177">Dadurch werden die WPP-Puffer auf den Datenträger geleert.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-177">This will flush the WPP buffers on the disk.</span></span>
4.  <span data-ttu-id="9b7e3-178">Typsatz-Ablauf **Verfolgungs \_ Format \_ -Präfix = \[ %9! d! \] %8! 04x!. %3! 04x!. %3! 04x!:: %4! s! \[ %1! s! \] (%! Compname!:%! Func!: %2! s!)**.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-178">Type **set TRACE\_FORMAT\_PREFIX = \[%9!d!\]%8!04X!.%3!04X!.%3!04X!::%4!s!\[%1!s!\](%!COMPNAME!:%!FUNC !:%2!s!)**.</span></span> <span data-ttu-id="9b7e3-179">Das Tool tracefmt fügt jeder Ablauf Verfolgungs Meldung einige Standardinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-179">The tracefmt tool adds some default information to each trace message.</span></span> <span data-ttu-id="9b7e3-180">Sie können konfigurieren, welche Informationen eingeschlossen werden, indem Sie die \_ Umgebungsvariable "Trace Format Prefix" festlegen \_ .</span><span class="sxs-lookup"><span data-stu-id="9b7e3-180">You can configure what information is included by setting the TRACE\_FORMAT\_PREFIX environment variable.</span></span> <span data-ttu-id="9b7e3-181">Informationen zur verwendeten Syntax finden Sie unter [Präfix der Ablauf Verfolgungs Meldung](https://msdn.microsoft.com/library/aa139695.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b7e3-181">To learn about the syntax used, see [Trace Message Prefix](https://msdn.microsoft.com/library/aa139695.aspx).</span></span>
5.  <span data-ttu-id="9b7e3-182">Geben Sie **tracefmt-TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF-o OUTPUT.TXT% systemroot% \\ system32 \\ WBEM \\ Logs \\ wmitracing. log** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-182">Type **tracefmt -tmf %systemroot%\\system32\\wbem\\tmf\\wmi.tmf -o OUTPUT.TXT %systemroot%\\system32\\wbem\\logs\\WMITracing.log**.</span></span> <span data-ttu-id="9b7e3-183">Dadurch wird die Übersetzung vom Binärformat in das lesbare Textformat durchführt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-183">This performs the translation from binary format to readable text format.</span></span>
6.  <span data-ttu-id="9b7e3-184">Geben Sie **Editor% systemroot% \\ system32 \\ WBEM \\ TMF \\OUTPUT.TXT** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-184">Type **notepad %systemroot%\\system32\\wbem\\tmf\\OUTPUT.TXT**.</span></span> <span data-ttu-id="9b7e3-185">Dadurch wird die Ablauf Verfolgungs Datei in Notepad geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-185">This will open the trace file in Notepad.</span></span>

<span data-ttu-id="9b7e3-186">Im folgenden finden Sie einige weitere WPP-bezogene Aufgaben, die Sie möglicherweise ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-186">The following are some other WPP-related tasks you might need to perform.</span></span>

<span data-ttu-id="9b7e3-187">**So verhindern Sie die WPP-basierte WMI-Ablauf Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-187">**To stop WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="9b7e3-188">Geben Sie **tracelog-WMI-Ablauf \_ Verfolgungs \_ Sitzung Abbrechen** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-188">Type **tracelog -stop WMI\_Trace\_Session**.</span></span>

<span data-ttu-id="9b7e3-189">**So starten Sie die WPP-basierte WMI-Ablauf Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-189">**To start WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="9b7e3-190">Geben Sie **tracelog-Start WMI \_ Trace \_ Session-GUID \# 1ff6b227-2ca7-40F9-9a66-980eadaa602e-RT-Level 5-Flag 0x7-f mytrace ein. BIN**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-190">Type **tracelog -start WMI\_Trace\_Session -guid \#1FF6B227-2CA7-40f9-9A66-980EADAA602E -rt -level 5 -flag 0x7 -f MYTRACE.BIN**</span></span>

<span data-ttu-id="9b7e3-191">**Windows Vista:** Standardmäßig ist die WPP-basierte WMI-Ablauf Verfolgung auf Ebene 2 festgelegt, die nur Fehlermeldungen enthält.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-191">**Windows Vista:** By default, WPP-based WMI tracing is set to level 2 which includes only error messages.</span></span> <span data-ttu-id="9b7e3-192">Legen Sie die Ebene auf 4 fest, um auch Informationsmeldungen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-192">To include informational messages as well, set the level to 4.</span></span> <span data-ttu-id="9b7e3-193">Alle Bereiche von WMI werden standardmäßig verfolgt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-193">All areas of WMI are traced by default.</span></span> <span data-ttu-id="9b7e3-194">Es gibt drei verschiedene Bereiche, die verfolgt werden können: Core (Flag = 0x1), ESS (Flag = 0x2) und PROV (Flag = 0x4).</span><span class="sxs-lookup"><span data-stu-id="9b7e3-194">There are three distinct areas that can be traced: Core (flag=0x1), ESS (flag=0x2) and Prov (flag=0x4).</span></span> <span data-ttu-id="9b7e3-195">Im obigen Startbefehl bewirkt **Flag 0x7** , dass alle drei Bereiche nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-195">In the start command above, **flag 0x7** causes all three areas to be traced.</span></span>

<span data-ttu-id="9b7e3-196">**Windows 7:** Standardmäßig ist die WPP-basierte WMI-Ablauf Verfolgung deaktiviert und auf Ebene 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-196">**Windows 7:** By default, WPP-based WMI tracing is disabled and set to level 0.</span></span> <span data-ttu-id="9b7e3-197">Um die WPP-basierte WMI-Ablauf Verfolgung verwenden zu können, muss diese Funktion aktiviert und auf Ebene 2 für Fehlermeldungen oder Ebene 4 für Fehler-und Informationsmeldungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-197">To use WPP-based WMI tracing, this feature must be enabled and set to either level 2 for error messages or level 4 for both error and informational messages.</span></span>

<span data-ttu-id="9b7e3-198">**So Listen Sie alle WPP-Ablauf Verfolgungs Sitzungen auf**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-198">**To list all WPP trace sessions**</span></span>

-   <span data-ttu-id="9b7e3-199">Geben Sie **tracelog-l** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-199">Type **tracelog -l**.</span></span>

<span data-ttu-id="9b7e3-200">**So Listen Sie Informationen über die WPP-Ablauf Verfolgungs Sitzung auf**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-200">**To list info about the WMI WPP trace session**</span></span>

-   <span data-ttu-id="9b7e3-201">Geben Sie **tracelog-l \| findstr/i "WMI \_ Trace"** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-201">Type **tracelog -l \| findstr /i "wmi\_trace"**.</span></span>

<span data-ttu-id="9b7e3-202">**So zeigen Sie die Parameter für die WPP-Ablauf Verfolgungs Sitzung an**</span><span class="sxs-lookup"><span data-stu-id="9b7e3-202">**To view the WMI WPP trace session parameters**</span></span>

-   <span data-ttu-id="9b7e3-203">Geben Sie **tracelog-q WMI-Ablauf \_ Verfolgungs \_ Sitzung** ein.</span><span class="sxs-lookup"><span data-stu-id="9b7e3-203">Type **tracelog -q WMI\_Trace\_Session**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b7e3-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b7e3-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b7e3-205">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="9b7e3-205">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="9b7e3-206">WMI-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="9b7e3-206">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

 
