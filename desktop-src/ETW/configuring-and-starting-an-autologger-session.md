---
description: Die AutoLogger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die früh im Startprozess des Betriebssystems auftreten.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Konfigurieren und Starten einer AutoLogger-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6560aece87506b1d064981ee5f49a56bbf0da19e
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102039"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="1daee-103">Konfigurieren und Starten einer AutoLogger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="1daee-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="1daee-104">Die AutoLogger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die früh im Startprozess des Betriebssystems auftreten.</span><span class="sxs-lookup"><span data-stu-id="1daee-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="1daee-105">Anwendungen und Gerätetreiber können die AutoLogger-Sitzung verwenden, um Ablaufverfolgungen zu erfassen, bevor sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="1daee-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="1daee-106">Beachten Sie, dass einige Gerätetreiber, z. B. Datenträgergerätetreiber, zum Zeitpunkt des Beginns der AutoLogger-Sitzung nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="1daee-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="1daee-107">Die AutoLogger unterscheidet sich wie folgt von der globalen Protokollierung:</span><span class="sxs-lookup"><span data-stu-id="1daee-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="1daee-108">Sie können eine oder mehrere AutoLogger-Sitzungen angeben (die globale Protokollierung war eine einzelne Sitzung, in der alle Ereignisse protokolliert haben).</span><span class="sxs-lookup"><span data-stu-id="1daee-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="1daee-109">Die AutoLogger-Funktion sendet beim Starten der Sitzung eine Aktivierungsbenachrichtigung an die Anbieter (die globale Protokollierung hat keine Aktivierungsbenachrichtigung an die Anbieter gesendet, sodass die Anbieter sich auf andere Mittel verlassen mussten, um zu wissen, ob die Globale Protokollierungssitzung gestartet wurde, um mit der Protokollierung von Ereignissen zu beginnen).</span><span class="sxs-lookup"><span data-stu-id="1daee-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="1daee-110">Die AutoLogger-Funktion unterstützt keine Protokollierung von NT-Kernelprotokollierungsereignissen (siehe **EnableFlags-Member** von [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span><span class="sxs-lookup"><span data-stu-id="1daee-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="1daee-111">Zum Protokollieren von NT-Kernelprotokollierungsereignissen müssen Sie die [globale Protokollierung](configuring-and-starting-the-global-logger-session.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1daee-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="1daee-112">Weitere Informationen zur Globalen Protokollierung finden Sie unter [Konfigurieren und Starten der globalen Protokollierungssitzung.](configuring-and-starting-the-global-logger-session.md)</span><span class="sxs-lookup"><span data-stu-id="1daee-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="1daee-113">ETW unterstützt die AutoLogger-Funktion unter Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="1daee-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="1daee-114">Verwenden Sie die [globale Protokollierung](configuring-and-starting-the-global-logger-session.md) unter früheren Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="1daee-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="1daee-115">Sie verwenden die Registrierung, um die AutoLogger-Sitzung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1daee-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="1daee-116">Fügen Sie den folgenden Registrierungsschlüssel hinzu, falls er noch nicht vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="1daee-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="1daee-117">Erstellen Sie unter dem Schlüssel **Autologger** einen Schlüssel für jede AutoLogger-Sitzung, die Sie konfigurieren möchten, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1daee-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="1daee-118">Erstellen Sie für jede Sitzung einen Schlüssel für jeden Anbieter, den Sie für die Sitzung aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1daee-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="1daee-119">Verwenden Sie die GUID des Anbieters als Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1daee-119">Use the provider's GUID as the key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="1daee-120">In der folgenden Tabelle werden die Werte beschrieben, die Sie für jede AutoLogger-Sitzung definieren können.</span><span class="sxs-lookup"><span data-stu-id="1daee-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="1daee-121">Sie müssen über Administratorrechte verfügen, um diese Registrierungswerte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1daee-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="1daee-122">Der **Start-** und **guid-Wert** sind die einzigen Werte, die zum Starten der AutoLogger-Sitzung erforderlich sind. alle anderen Werte verfügen über Standardeinstellungen, die verwendet werden, wenn der Wert nicht in der Registrierung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="1daee-123">In der Regel sollten Sie die Standardwerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="1daee-123">Typically, you should use the default values.</span></span> <span data-ttu-id="1daee-124">Wenn Sie einen Wert angeben, der von ETW nicht unterstützt werden kann, überschreibt ETW den Wert.</span><span class="sxs-lookup"><span data-stu-id="1daee-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1daee-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1daee-125">Value</span></span></th>
<th><span data-ttu-id="1daee-126">Typ</span><span class="sxs-lookup"><span data-stu-id="1daee-126">Type</span></span></th>
<th><span data-ttu-id="1daee-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1daee-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1daee-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="1daee-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-130">Die Größe jedes Puffers in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="1daee-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="1daee-131">Sollte kleiner als ein Megabyte sein.</span><span class="sxs-lookup"><span data-stu-id="1daee-131">Should be less than one megabyte.</span></span> <span data-ttu-id="1daee-132">ETW verwendet die Größe des physischen Arbeitsspeichers, um diesen Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1daee-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-133"><strong>ClockType</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="1daee-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-135">Der Timer, der beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1daee-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="1daee-136">1 = Leistungsindikatorwert (hohe Auflösung)</span><span class="sxs-lookup"><span data-stu-id="1daee-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="1daee-137">2 = Systemtimer</span><span class="sxs-lookup"><span data-stu-id="1daee-137">2 = System timer</span></span></li>
<li><span data-ttu-id="1daee-138">3 = CPU-Zykluszähler</span><span class="sxs-lookup"><span data-stu-id="1daee-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="1daee-139">Eine Beschreibung der einzelnen Uhrtypen finden Sie im <strong>ClientContext-Member</strong> von <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1daee-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="1daee-140">Der Standardwert ist 1 (Leistungsindikatorwert) unter Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="1daee-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="1daee-141">Vor Windows Vista ist der Standardwert 2 (Systemtimer).</span><span class="sxs-lookup"><span data-stu-id="1daee-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-142"><strong>DisableRealtimePersistence</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="1daee-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-144">Legen Sie diesen Wert auf 1 fest, um die Echtzeitpersistenz zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1daee-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="1daee-145">Der Standardwert ist 0 (aktiviert) für Echtzeitsitzungen.</span><span class="sxs-lookup"><span data-stu-id="1daee-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="1daee-146">Wenn Die Echtzeitpersistenz aktiviert ist, werden Echtzeitereignisse beibehalten, die zum Zeitpunkt des Herunterfahrens des Computers nicht übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="1daee-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="1daee-147">Die Ereignisse werden dann an den Consumer übermittelt, wenn der Consumer das nächste Mal eine Verbindung mit der Sitzung herstellt.</span><span class="sxs-lookup"><span data-stu-id="1daee-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-148"><strong>FileCounter</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="1daee-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-150">Legen Sie diesen Wert nicht fest, oder ändern Sie diesen Wert nicht.</span><span class="sxs-lookup"><span data-stu-id="1daee-150">Do not set or modify this value.</span></span> <span data-ttu-id="1daee-151">Dieser Wert ist die Seriennummer, die verwendet wird, um den Protokolldateinamen zu erhöhen, wenn <strong>FileMax</strong> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="1daee-152">Wenn der Wert ungültig ist, wird 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="1daee-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="1daee-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="1daee-155">Der vollqualifizierte Pfad der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="1daee-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="1daee-156">Der Pfad zu dieser Datei muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1daee-156">The path to this file must exist.</span></span> <span data-ttu-id="1daee-157">Die Protokolldatei ist eine sequenzielle Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="1daee-157">The log file is a sequential log file.</span></span> <span data-ttu-id="1daee-158">Der Pfad ist auf 1024 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1daee-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="1daee-159">Wenn <strong>FileName</strong> nicht angegeben ist, werden Ereignisse in %SystemRoot%\System32\LogFiles\WMI \& lt;Sitzungsname &gt; .etl geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1daee-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-160"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="1daee-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-162">Die maximale Anzahl von Instanzen der Protokolldatei, die ETW erstellt.</span><span class="sxs-lookup"><span data-stu-id="1daee-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="1daee-163">Wenn die in <strong>FileName</strong> angegebene Protokolldatei vorhanden ist, fügt ETW den <strong>FileCounter-Wert</strong> an den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="1daee-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="1daee-164">Wenn beispielsweise der Standardprotokolldateiname verwendet wird, lautet das Formular %SystemRoot%\System32\LogFiles\WMI \& lt;Sitzungsname &gt; .etl. Nnnn.</span><span class="sxs-lookup"><span data-stu-id="1daee-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.NNNN.</span></span> <br/> <span data-ttu-id="1daee-165">Wenn der Computer zum ersten Mal gestartet wird, lautet der Dateiname &lt; sitzungsname &gt; .etl.0001, das zweite Mal ist der Dateiname &lt; Sitzungsname &gt; .etl.0002 usw.</span><span class="sxs-lookup"><span data-stu-id="1daee-165">The first time the computer is started, the file name is &lt;sessionname&gt;.etl.0001, the second time the file name is &lt;sessionname&gt;.etl.0002, and so on.</span></span> <span data-ttu-id="1daee-166">Wenn <strong>FileMax</strong> gleich 3 ist, setzt ETW den Zähler beim vierten Neustart des Computers auf 1 zurück und überschreibt den &lt; Sitzungsnamen &gt; .etl.0001, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1daee-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites &lt;sessionname&gt;.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="1daee-167">Die maximale Anzahl der unterstützten Instanzen der Protokolldatei beträgt 16.</span><span class="sxs-lookup"><span data-stu-id="1daee-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="1daee-168">Verwenden Sie dieses Feature nicht mit dem <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> Protokolldateimodus.</span><span class="sxs-lookup"><span data-stu-id="1daee-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-169"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="1daee-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-171">Gibt an, wie oft die Ablaufverfolgungspuffer in Sekunden zwangsmäßig geleert werden.</span><span class="sxs-lookup"><span data-stu-id="1daee-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="1daee-172">Die mindeste Leerungszeit beträgt 1 Sekunde.</span><span class="sxs-lookup"><span data-stu-id="1daee-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="1daee-173">Diese erzwungene Leerung erfolgt zusätzlich zur automatischen Leerung, die auftritt, wenn ein Puffer voll ist und die Ablaufverfolgungssitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1daee-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="1daee-174">Bei einer Echtzeitprotokollierung bedeutet der Wert 0 (Standardwert) , dass die Leerungszeit auf 1 Sekunde festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1daee-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="1daee-175">Eine Echtzeitprotokollierung ist , wenn <strong>LogFileMode</strong> auf <strong>EVENT_TRACE_REAL_TIME_MODE</strong>festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="1daee-176">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="1daee-176">The default value is 0.</span></span> <span data-ttu-id="1daee-177">Standardmäßig werden Puffer nur geleert, wenn sie voll sind.</span><span class="sxs-lookup"><span data-stu-id="1daee-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-178"><strong>Guid</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="1daee-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="1daee-180">Eine Zeichenfolge, die eine GUID enthält, die die Sitzung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1daee-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="1daee-181">Dieser Wert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1daee-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-182"><strong>LogFileMode</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="1daee-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-184">Geben Sie einen oder mehrere Protokollmodi an.</span><span class="sxs-lookup"><span data-stu-id="1daee-184">Specify one or more log modes.</span></span> <span data-ttu-id="1daee-185">Mögliche Werte finden Sie unter <a href="logging-mode-constants.md">Protokollierungsmoduskonstanten.</a></span><span class="sxs-lookup"><span data-stu-id="1daee-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="1daee-186">Der Standardwert ist <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="1daee-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="1daee-187">Anstatt in eine Protokolldatei zu schreiben, können Sie entweder <strong>EVENT_TRACE_BUFFERING_MODE</strong> oder <strong>EVENT_TRACE_REAL_TIME_MODE</strong>angeben.</span><span class="sxs-lookup"><span data-stu-id="1daee-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="1daee-188">Wenn <strong>Sie EVENT_TRACE_BUFFERING_MODE</strong> angeben, werden die Kosten für das Leeren des Sitzungsinhalts auf den Datenträger vermieden, wenn das Dateisystem verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="1daee-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="1daee-189">Beachten Sie, dass die Verwendung <strong>von EVENT_TRACE_BUFFERING_MODE</strong> bewirkt, dass das System den <strong>MaximumBuffers-Wert</strong> ignoriert, da die Puffergröße stattdessen das Produkt von <strong>MinimumBuffers</strong> und <strong>BufferSize</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="1daee-190">AutoLogger-Sitzungen unterstützen den <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> Protokollierungsmodus nicht.</span><span class="sxs-lookup"><span data-stu-id="1daee-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="1daee-191">Wenn <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> angegeben wird, muss <strong>BufferSize</strong> explizit bereitgestellt werden und sowohl in der Protokollierung als auch in der datei, die angefügt wird, identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1daee-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="1daee-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-194">Die maximale Dateigröße der Protokolldatei in Megabyte.</span><span class="sxs-lookup"><span data-stu-id="1daee-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="1daee-195">Die Sitzung wird geschlossen, wenn die maximale Größe erreicht wird, es sei denn, Sie befinden sich im zirkulären Protokolldateimodus.</span><span class="sxs-lookup"><span data-stu-id="1daee-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="1daee-196">Um kein Limit anzugeben, legen Sie den Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="1daee-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="1daee-197">Der Standardwert ist 100 MB, falls nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1daee-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="1daee-198">Das Verhalten, das auftritt, wenn die maximale Dateigröße erreicht wird, hängt vom Wert von <strong>LogFileMode</strong>ab.</span><span class="sxs-lookup"><span data-stu-id="1daee-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="1daee-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-201">Die maximale Anzahl der zu reservierenden Puffer.</span><span class="sxs-lookup"><span data-stu-id="1daee-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="1daee-202">In der Regel ist dieser Wert die Mindestanzahl von Puffern plus 20.</span><span class="sxs-lookup"><span data-stu-id="1daee-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="1daee-203">ETW verwendet die Puffergröße und die Größe des physischen Speichers, um diesen Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1daee-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="1daee-204">Dieser Wert muss größer oder gleich dem Wert für <strong>MinimumBuffers sein.</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="1daee-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-207">Die Mindestanzahl von Puffern, die beim Start reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="1daee-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="1daee-208">Die Mindestanzahl von Puffern, die Sie angeben können, beträgt zwei Puffer pro Prozessor.</span><span class="sxs-lookup"><span data-stu-id="1daee-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="1daee-209">Auf einem einzelnen Prozessorcomputer beträgt die Mindestanzahl von Puffern beispielsweise zwei.</span><span class="sxs-lookup"><span data-stu-id="1daee-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-210"><strong>Starten</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="1daee-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-212">Legen Sie diesen Wert auf 1 fest, damit die AutoLogger-Sitzung beim nächsten Neustart des Computers gestartet wird. Legen Sie andernfalls diesen Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="1daee-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-213"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="1daee-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-215">Der Startstatus der AutoLogger.</span><span class="sxs-lookup"><span data-stu-id="1daee-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="1daee-216">Wenn die AutoLogger nicht gestartet werden konnte, ist der Wert dieses Schlüssels der entsprechende Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1daee-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="1daee-217">Wenn die AutoLogger erfolgreich gestartet wurde, wird der Wert dieses Schlüssels <strong>ERROR_SUCCESS</strong> (0) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1daee-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1daee-218">In der folgenden Tabelle werden die Werte beschrieben, die Sie für jeden Anbieter definieren können, den Sie für Ihre Sitzung aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1daee-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="1daee-219">Sie müssen über Administratorrechte verfügen, um diese Registrierungswerte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1daee-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="1daee-220">Wenn Sie einen Wert angeben, der von ETW nicht unterstützt werden kann, überschreibt ETW den Wert.</span><span class="sxs-lookup"><span data-stu-id="1daee-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1daee-221">Wert</span><span class="sxs-lookup"><span data-stu-id="1daee-221">Value</span></span></th>
<th><span data-ttu-id="1daee-222">Typ</span><span class="sxs-lookup"><span data-stu-id="1daee-222">Type</span></span></th>
<th><span data-ttu-id="1daee-223">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1daee-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1daee-224"><strong>Enabled</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="1daee-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-226">Bestimmt, ob der Anbieter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="1daee-227">Legen Sie diesen Wert auf 1 fest, um den Anbieter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1daee-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="1daee-228">Um den Anbieter zu deaktivieren, legen Sie diesen Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="1daee-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="1daee-229">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="1daee-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-230"><strong>EnableFlags</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="1daee-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-232">Vom Anbieter definierter Wert, der die Ereignisklasse angibt, für die der Anbieter Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="1daee-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="1daee-233">Weitere Informationen finden Sie im <em>EnableFlags-Parameter</em> der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace-Funktion.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1daee-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="1daee-234">Geben Sie diesen Wertnamen an, wenn der Anbieter <strong>MatchAnyKeyword</strong> oder <strong>MatchAllKeyword nicht unterstützt.</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-235"><strong>EnableLevel</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="1daee-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-237">Vom Anbieter definierter Wert, der die Detailebene angibt, die im Ereignis enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="1daee-238">Sie können diesen Wert beispielsweise verwenden, um den Schweregrad der Ereignisse (Information, Warnung, Fehler) anzugeben, die der Anbieter generiert.</span><span class="sxs-lookup"><span data-stu-id="1daee-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="1daee-239">Eine Liste vordefinierter Ebenen finden Sie unter dem <em>level-Parameter</em> der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx-Funktion.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1daee-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-240"><strong>EnableProperty</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="1daee-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-242">Verwenden Sie diesen Wert, um eines oder mehrere der folgenden Elemente in die Protokolldatei ein-/ausderherzustellen:</span><span class="sxs-lookup"><span data-stu-id="1daee-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="1daee-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Schließen Sie die Sicherheits-ID (SID) des Benutzers in die erweiterten Daten ein.</span><span class="sxs-lookup"><span data-stu-id="1daee-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="1daee-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Schließen Sie den Terminalsitzungsbezeichner in die erweiterten Daten ein.</span><span class="sxs-lookup"><span data-stu-id="1daee-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="1daee-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Schließen Sie in die erweiterten Daten eine Aufrufliste-Ablaufverfolgung für Ereignisse ein, die mit <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite geschrieben wurden.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1daee-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="1daee-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filtert alle Ereignisse heraus, für die kein Schlüsselwort ohne Null angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="1daee-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Gibt an, dass dieser Aufruf von <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> anstelle eines einzelnen Ereignisanbieters eine Anbietergruppe aktivieren soll. <a href="provider-traits.md"></a></span><span class="sxs-lookup"><span data-stu-id="1daee-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="1daee-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Schließen Sie den Prozessstartschlüssel in die erweiterten Daten ein.</span><span class="sxs-lookup"><span data-stu-id="1daee-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="1daee-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Schließen Sie den Ereignisschlüssel in die erweiterten Daten ein.</span><span class="sxs-lookup"><span data-stu-id="1daee-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="1daee-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filtert alle Ereignisse heraus, die entweder als InPrivate-Ereignis markiert sind oder von einem Als InPrivate markierten Prozess stammen.</span><span class="sxs-lookup"><span data-stu-id="1daee-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="1daee-251">Weitere Informationen zu diesen Elementen finden Sie unter <strong>EnableProperty</strong> der <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="1daee-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1daee-252"><strong>MatchAnyKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="1daee-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-254">Bitmaske von Schlüsselwörtern, die die Kategorie der Ereignisse bestimmen, die der Anbieter schreiben soll.</span><span class="sxs-lookup"><span data-stu-id="1daee-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="1daee-255">Der Anbieter schreibt das Ereignis, wenn eines der Schlüsselwortbits des Ereignisses mit einem der in dieser Maske festgelegten Bits übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="1daee-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="1daee-256">Um anzugeben, dass der Anbieter alle Ereignisse schreibt, legen Sie diesen Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="1daee-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="1daee-257">Ein Beispiel finden Sie im Abschnitt "Hinweise" der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx-Funktion.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1daee-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1daee-258"><strong>MatchAllKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="1daee-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="1daee-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="1daee-260">Diese Bitmaske ist optional.</span><span class="sxs-lookup"><span data-stu-id="1daee-260">This bitmask is optional.</span></span> <span data-ttu-id="1daee-261">Diese Maske schränkt die Kategorie der Ereignisse weiter ein, die der Anbieter schreiben soll.</span><span class="sxs-lookup"><span data-stu-id="1daee-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="1daee-262">Wenn das Schlüsselwort des Ereignisses die <em>MatchAnyKeyword-Bedingung</em> erfüllt, schreibt der Anbieter das Ereignis nur, wenn alle Bits in dieser Maske im Schlüsselwort des Ereignisses vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1daee-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="1daee-263">Diese Maske wird nicht verwendet, <em>wenn MatchAnyKeyword</em> 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="1daee-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="1daee-264">Ein Beispiel finden Sie im Abschnitt "Hinweise" der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx-Funktion.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1daee-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1daee-265">Nachdem die Registrierung geändert wurde, wird die AutoLogger-Sitzung beim nächsten Neustart des Computers gestartet.</span><span class="sxs-lookup"><span data-stu-id="1daee-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="1daee-266">Die AutoLogger-Sitzung ruft die [**EnableTraceEx-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) auf, um die Anbieter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1daee-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="1daee-267">Die AutoLogger-Sitzungen erhöhen die Systemstartzeit und sollten nur wenig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1daee-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="1daee-268">Dienste, die Während des Startvorgangs Informationen erfassen möchten, sollten erwägen, sich selbst Controllerlogik hinzufügen, anstatt die AutoLogger-Sitzung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1daee-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="1daee-269">Um eine AutoLogger-Sitzung zu beenden, rufen Sie die [**ControlTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-controltracea) auf.</span><span class="sxs-lookup"><span data-stu-id="1daee-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="1daee-270">Der Sitzungsname, den Sie an die Funktion übergeben, ist der Name des Registrierungsschlüssels, den Sie zum Definieren der Sitzung in der Registrierung verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="1daee-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="1daee-271">Unter Windows 8.1, Windows Server 2012 R2 und höher können Ereignisnutzlast-, Bereichs- und Stapelüberwachungsfilter von der [**EnableTraceEx2-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) und den [**ENABLE TRACE \_ \_ PARAMETERS-**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**EVENT \_ \_ FILTER-DESCRIPTOR-Strukturen**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungssitzung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="1daee-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="1daee-272">Weitere Informationen zu Ereignisnutzlastfiltern finden Sie in den Funktionen [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)und [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) sowie in den **STRUKTUREN ENABLE TRACE \_ \_ PARAMETERS,** **EVENT FILTER \_ \_ DESCRIPTOR** und [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)</span><span class="sxs-lookup"><span data-stu-id="1daee-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="1daee-273">Weitere Informationen zum Starten einer Ereignisablaufverfolgungssitzung finden Sie unter Konfigurieren und [Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)</span><span class="sxs-lookup"><span data-stu-id="1daee-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="1daee-274">Weitere Informationen zum Starten einer privaten Protokollierungssitzung finden Sie unter Konfigurieren und [Starten einer privaten Protokollierungssitzung.](configuring-and-starting-a-private-logger-session.md)</span><span class="sxs-lookup"><span data-stu-id="1daee-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="1daee-275">Weitere Informationen zum Starten einer NT-Kernelprotokollierungssitzung finden Sie unter Konfigurieren und [Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)</span><span class="sxs-lookup"><span data-stu-id="1daee-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1daee-276">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1daee-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1daee-277">Konfigurieren und Starten einer privaten Protokollierungssitzung</span><span class="sxs-lookup"><span data-stu-id="1daee-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="1daee-278">Konfigurieren und Starten einer SystemTraceProvider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="1daee-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="1daee-279">Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung</span><span class="sxs-lookup"><span data-stu-id="1daee-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="1daee-280">Konfigurieren und Starten der NT-Kernelprotokollierungssitzung</span><span class="sxs-lookup"><span data-stu-id="1daee-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="1daee-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="1daee-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="1daee-282">**AKTIVIEREN VON \_ ABLAUFVERFOLGUNGSPARAMETERN \_**</span><span class="sxs-lookup"><span data-stu-id="1daee-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="1daee-283">**\_ \_ EREIGNISFILTERDESKRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="1daee-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="1daee-284">**\_ \_ NUTZLASTFILTER-PRÄDIKAT**</span><span class="sxs-lookup"><span data-stu-id="1daee-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="1daee-285">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="1daee-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="1daee-286">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="1daee-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="1daee-287">Aktualisieren einer Ereignisablaufverfolgungssitzung</span><span class="sxs-lookup"><span data-stu-id="1daee-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
