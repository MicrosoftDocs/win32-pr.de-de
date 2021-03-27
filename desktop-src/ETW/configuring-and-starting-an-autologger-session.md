---
description: Die Ereignis Ablauf Verfolgungs Sitzung von autologger zeichnet Ereignisse auf, die früh im Betriebssystem-Startprozess auftreten.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Konfigurieren und Starten einer autologger-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980953"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="055e2-103">Konfigurieren und Starten einer autologger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="055e2-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="055e2-104">Die Ereignis Ablauf Verfolgungs Sitzung von autologger zeichnet Ereignisse auf, die früh im Betriebssystem-Startprozess auftreten.</span><span class="sxs-lookup"><span data-stu-id="055e2-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="055e2-105">Anwendungen und Gerätetreiber können die autologger-Sitzung verwenden, um Ablauf Verfolgungen zu erfassen, bevor sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="055e2-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="055e2-106">Beachten Sie, dass einige Gerätetreiber, z. b. Datenträger-Gerätetreiber, beim Beginn der autologger-Sitzung nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="055e2-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="055e2-107">Der autologger unterscheidet sich wie folgt von der globalen Protokollierung:</span><span class="sxs-lookup"><span data-stu-id="055e2-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="055e2-108">Sie können mindestens eine autologger-Sitzung angeben (bei der globalen Protokollierung handelt es sich um eine einzelne Sitzung, für die alle Ereignisse protokolliert haben).</span><span class="sxs-lookup"><span data-stu-id="055e2-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="055e2-109">Der autologger sendet eine Aktivierungs Benachrichtigung an die Anbieter, wenn die Sitzung gestartet wird (die globale Protokollierung hat keine Aktivierungs Benachrichtigung an die Anbieter gesendet, sodass die Anbieter auf andere Weise wissen müssen, ob die globale Protokollierungs Sitzung gestartet wurde, um mit der Protokollierung von Ereignissen zu beginnen).</span><span class="sxs-lookup"><span data-stu-id="055e2-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="055e2-110">Der autologger unterstützt das Protokollieren von NT-Kernel Protokollierungs Ereignissen nicht (siehe **enableflags** -Member von [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span><span class="sxs-lookup"><span data-stu-id="055e2-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="055e2-111">Zum Protokollieren von NT-kernelprotokollierungs Ereignissen müssen Sie die [globale](configuring-and-starting-the-global-logger-session.md)Protokollierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="055e2-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="055e2-112">Weitere Informationen zur globalen Protokollierungs seesion finden Sie unter [Konfigurieren und Starten der globalen](configuring-and-starting-the-global-logger-session.md)Protokollierungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="055e2-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="055e2-113">Etw unterstützt den autologger unter Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="055e2-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="055e2-114">Verwenden Sie die [globale](configuring-and-starting-the-global-logger-session.md) Protokollierung unter früheren Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="055e2-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="055e2-115">Sie verwenden die Registrierung, um die autologger-Sitzung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="055e2-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="055e2-116">Fügen Sie den folgenden Registrierungsschlüssel hinzu, wenn er nicht bereits vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="055e2-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="055e2-117">Erstellen Sie unter dem Schlüssel **autologger** einen Schlüssel für jede autologger-Sitzung, die Sie konfigurieren möchten, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="055e2-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

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

<span data-ttu-id="055e2-118">Erstellen Sie für jede Sitzung einen Schlüssel für jeden Anbieter, den Sie für die Sitzung aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="055e2-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="055e2-119">Verwenden Sie die GUID des Anbieters als Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="055e2-119">Use the provider's GUID as the key.</span></span>

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

<span data-ttu-id="055e2-120">In der folgenden Tabelle werden die Werte beschrieben, die Sie für jede autologger-Sitzung definieren können.</span><span class="sxs-lookup"><span data-stu-id="055e2-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="055e2-121">Sie müssen über Administratorrechte verfügen, um diese Registrierungs Werte angeben zu können.</span><span class="sxs-lookup"><span data-stu-id="055e2-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="055e2-122">Der **Start** -und der **GUID** -Wert sind die einzigen Werte, die zum Starten der autologger-Sitzung erforderlich sind. alle anderen Werte haben Standardeinstellungen, die verwendet werden, wenn der Wert nicht in der Registrierung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="055e2-123">Normalerweise sollten Sie die Standardwerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="055e2-123">Typically, you should use the default values.</span></span> <span data-ttu-id="055e2-124">Wenn Sie einen Wert angeben, der von etw nicht unterstützt werden kann, wird der Wert von etw überschrieben.</span><span class="sxs-lookup"><span data-stu-id="055e2-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="055e2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="055e2-125">Value</span></span></th>
<th><span data-ttu-id="055e2-126">type</span><span class="sxs-lookup"><span data-stu-id="055e2-126">Type</span></span></th>
<th><span data-ttu-id="055e2-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="055e2-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="055e2-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="055e2-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-130">Die Größe der einzelnen Puffer in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="055e2-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="055e2-131">Sollte kleiner als 1 MB sein.</span><span class="sxs-lookup"><span data-stu-id="055e2-131">Should be less than one megabyte.</span></span> <span data-ttu-id="055e2-132">Etw verwendet die Größe des physischen Speichers, um diesen Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="055e2-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-133"><strong>Clocktype</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="055e2-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-135">Der Zeitgeber, der verwendet werden soll, wenn der Zeitstempel für jedes Ereignis protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="055e2-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="055e2-136">1 = Leistungs Zählers Wert (hohe Auflösung)</span><span class="sxs-lookup"><span data-stu-id="055e2-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="055e2-137">2 = systemtimer</span><span class="sxs-lookup"><span data-stu-id="055e2-137">2 = System timer</span></span></li>
<li><span data-ttu-id="055e2-138">3 = CPU-Zyklen-Counter</span><span class="sxs-lookup"><span data-stu-id="055e2-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="055e2-139">Eine Beschreibung der einzelnen uhrtypen finden Sie im <strong>clientcontext</strong> -Member von <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="055e2-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="055e2-140">Der Standardwert ist 1 (Leistungs Leistungswert) unter Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="055e2-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="055e2-141">Vor Windows Vista ist der Standardwert 2 (systemtimer).</span><span class="sxs-lookup"><span data-stu-id="055e2-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-142"><strong>Disablerealtimepersistenz</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="055e2-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-144">Um die Echt Zeit Persistenz zu deaktivieren, legen Sie diesen Wert auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="055e2-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="055e2-145">Der Standardwert ist 0 (aktiviert) für echt Zeit Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="055e2-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="055e2-146">Wenn die Echt Zeit Persistenz aktiviert ist, werden Echtzeitereignisse permanent gespeichert, die nicht von dem Zeitpunkt des herunter Fahrens des Computers zugestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="055e2-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="055e2-147">Die Ereignisse werden dann an den Consumer übermittelt, wenn der Consumer das nächste Mal eine Verbindung mit der Sitzung herstellt.</span><span class="sxs-lookup"><span data-stu-id="055e2-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-148"><strong>File Counter</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="055e2-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-150">Dieser Wert kann nicht festgelegt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="055e2-150">Do not set or modify this value.</span></span> <span data-ttu-id="055e2-151">Dieser Wert ist die Seriennummer, die verwendet wird, um den Namen der Protokolldatei zu erhöhen, wenn <strong>filemax</strong> angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="055e2-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="055e2-152">Wenn der Wert nicht gültig ist, wird 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="055e2-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="055e2-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="055e2-155">Der voll qualifizierte Pfad der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="055e2-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="055e2-156">Der Pfad zu dieser Datei muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="055e2-156">The path to this file must exist.</span></span> <span data-ttu-id="055e2-157">Die Protokolldatei ist eine sequenzielle Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="055e2-157">The log file is a sequential log file.</span></span> <span data-ttu-id="055e2-158">Der Pfad ist auf 1024 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="055e2-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="055e2-159">Wenn <strong>filename</strong> nicht angegeben wird, werden die Ereignisse in%SystemRoot%\system32\logfiles\wmi\ <sessionname> . ETL geschrieben.</span><span class="sxs-lookup"><span data-stu-id="055e2-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-160"><strong>Filemax</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="055e2-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-162">Die maximale Anzahl von Instanzen der Protokolldatei, die von etw erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="055e2-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="055e2-163">Wenn die in <strong>filename</strong> angegebene Protokolldatei vorhanden ist, fügt ETW den <strong>filecounter</strong> -Wert an den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="055e2-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="055e2-164">Wenn z. b. der Standardname der Protokolldatei verwendet wird, lautet das Formular%systemroot%\system32\logfiles\wmi\ <sessionname> . ETL. NNNN.</span><span class="sxs-lookup"><span data-stu-id="055e2-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.NNNN.</span></span> <br/> <span data-ttu-id="055e2-165">Wenn der Computer zum ersten Mal gestartet wird, lautet der Dateiname " <sessionname> . ETL. 0001", der Dateiname ist " <sessionname> . ETL. 0002" usw.</span><span class="sxs-lookup"><span data-stu-id="055e2-165">The first time the computer is started, the file name is <sessionname>.etl.0001, the second time the file name is <sessionname>.etl.0002, and so on.</span></span> <span data-ttu-id="055e2-166">Wenn <strong>filemax</strong> den Wert 3 hat, setzt etw beim vierten Neustart des Computers den Wert auf 1 zurück und überschreibt <sessionname> . ETL. 0001, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="055e2-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites <sessionname>.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="055e2-167">Die maximal unterstützte Anzahl von Instanzen der Protokolldatei ist 16.</span><span class="sxs-lookup"><span data-stu-id="055e2-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="055e2-168">Verwenden Sie diese Funktion nicht mit dem <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> Protokolldatei Modus.</span><span class="sxs-lookup"><span data-stu-id="055e2-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-169"><strong>Flushtimer</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="055e2-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-171">Gibt an, wie oft die Ablauf Verfolgungs Puffer in Sekunden erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="055e2-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="055e2-172">Die minimale Leerungs Zeit beträgt 1 Sekunde.</span><span class="sxs-lookup"><span data-stu-id="055e2-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="055e2-173">Dieser erzwungene Löschvorgang erfolgt zusätzlich zu dem automatischen leeren, der auftritt, wenn ein Puffer voll ist und die Ablauf Verfolgungs Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="055e2-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="055e2-174">Bei einer echt Zeit Protokollierung bedeutet der Wert 0 (null) (der Standardwert), dass die Leerungs Zeit auf 1 Sekunde festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="055e2-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="055e2-175">Eine echt Zeit Protokollierung ist, wenn <strong>logfilemode</strong> auf <strong>EVENT_TRACE_REAL_TIME_MODE</strong>festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="055e2-176">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="055e2-176">The default value is 0.</span></span> <span data-ttu-id="055e2-177">Standardmäßig werden Puffer nur geleert, wenn Sie voll sind.</span><span class="sxs-lookup"><span data-stu-id="055e2-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-178"><strong>GUID</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="055e2-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="055e2-180">Eine Zeichenfolge, die eine GUID enthält, die die Sitzung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="055e2-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="055e2-181">Dieser Wert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="055e2-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-182"><strong>Logfilemode</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="055e2-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-184">Geben Sie mindestens einen Protokollmodus an.</span><span class="sxs-lookup"><span data-stu-id="055e2-184">Specify one or more log modes.</span></span> <span data-ttu-id="055e2-185">Mögliche Werte finden Sie unter <a href="logging-mode-constants.md">Protokollierungs Modus-Konstanten</a>.</span><span class="sxs-lookup"><span data-stu-id="055e2-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="055e2-186">Der Standardwert ist <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="055e2-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="055e2-187">Anstatt in eine Protokolldatei zu schreiben, können Sie entweder <strong>EVENT_TRACE_BUFFERING_MODE</strong> oder <strong>EVENT_TRACE_REAL_TIME_MODE</strong>angeben.</span><span class="sxs-lookup"><span data-stu-id="055e2-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="055e2-188">Das Angeben von <strong>EVENT_TRACE_BUFFERING_MODE</strong> vermeidet die Kosten für das Leeren des Inhalts der Sitzung auf den Datenträger, wenn das Dateisystem verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="055e2-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="055e2-189">Beachten Sie, dass die Verwendung von <strong>EVENT_TRACE_BUFFERING_MODE</strong> dazu führt, dass das System den <strong>maximumbuffers</strong> -Wert ignoriert, da die Puffergröße stattdessen das Produkt von <strong>minimumbuffers</strong> und <strong>bufferSize</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="055e2-190">Der <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> Protokollierungs Modus wird von autologger-Sitzungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="055e2-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="055e2-191">Wenn <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> angegeben wird, muss <strong>bufferSize</strong> explizit angegeben werden und muss sowohl in der Protokollierung als auch in der angefügten Datei identisch sein.</span><span class="sxs-lookup"><span data-stu-id="055e2-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="055e2-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-194">Die maximale Dateigröße der Protokolldatei in Megabytes.</span><span class="sxs-lookup"><span data-stu-id="055e2-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="055e2-195">Die Sitzung wird geschlossen, wenn die maximale Größe erreicht wird, es sei denn, Sie befinden sich im Zirkel Protokolldatei Modus.</span><span class="sxs-lookup"><span data-stu-id="055e2-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="055e2-196">Legen Sie den Wert auf 0 fest, um keine Beschränkung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="055e2-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="055e2-197">Der Standardwert ist 100 MB, wenn er nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="055e2-198">Das Verhalten, das auftritt, wenn die maximale Dateigröße erreicht wird, hängt vom Wert von <strong>logfilemode</strong>ab.</span><span class="sxs-lookup"><span data-stu-id="055e2-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="055e2-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-201">Die maximale Anzahl der zuzuordnenden Puffer.</span><span class="sxs-lookup"><span data-stu-id="055e2-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="055e2-202">In der Regel ist dieser Wert die minimale Anzahl von Puffern plus 20.</span><span class="sxs-lookup"><span data-stu-id="055e2-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="055e2-203">Etw verwendet die Puffergröße und die Größe des physischen Speichers, um diesen Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="055e2-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="055e2-204">Dieser Wert muss größer oder gleich dem Wert für <strong>minimumbuffers</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="055e2-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="055e2-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-207">Die minimale Anzahl von Puffern, die beim Start von zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="055e2-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="055e2-208">Die Mindestanzahl an Puffern, die Sie angeben können, sind zwei Puffer pro Prozessor.</span><span class="sxs-lookup"><span data-stu-id="055e2-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="055e2-209">Beispielsweise ist auf einem Computer mit einem einzelnen Prozessor die Mindestanzahl an Puffern auf zwei.</span><span class="sxs-lookup"><span data-stu-id="055e2-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-210"><strong>Starten</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="055e2-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-212">Legen Sie diesen Wert auf 1 fest, damit die autologger-Sitzung beim nächsten Neustart des Computers gestartet wird. andernfalls legen Sie diesen Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="055e2-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-213"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="055e2-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-215">Der Startstatus des autologers.</span><span class="sxs-lookup"><span data-stu-id="055e2-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="055e2-216">Wenn der autologger nicht gestartet werden konnte, ist der Wert dieses Schlüssels der entsprechende Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="055e2-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="055e2-217">Wenn der autologger erfolgreich gestartet wurde, ist der Wert dieses Schlüssels <strong>ERROR_SUCCESS</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="055e2-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="055e2-218">In der folgenden Tabelle werden die Werte beschrieben, die Sie für jeden Anbieter definieren können, den Sie für Ihre Sitzung aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="055e2-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="055e2-219">Sie müssen über Administratorrechte verfügen, um diese Registrierungs Werte angeben zu können.</span><span class="sxs-lookup"><span data-stu-id="055e2-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="055e2-220">Wenn Sie einen Wert angeben, der von etw nicht unterstützt werden kann, wird der Wert von etw überschrieben.</span><span class="sxs-lookup"><span data-stu-id="055e2-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="055e2-221">Wert</span><span class="sxs-lookup"><span data-stu-id="055e2-221">Value</span></span></th>
<th><span data-ttu-id="055e2-222">type</span><span class="sxs-lookup"><span data-stu-id="055e2-222">Type</span></span></th>
<th><span data-ttu-id="055e2-223">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="055e2-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="055e2-224"><strong>Aktiviert</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="055e2-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-226">Bestimmt, ob der Anbieter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="055e2-227">Legen Sie diesen Wert auf 1 fest, um den Anbieter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="055e2-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="055e2-228">Um den Anbieter zu deaktivieren, legen Sie diesen Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="055e2-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="055e2-229">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="055e2-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-230"><strong>Enableflags</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="055e2-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-232">Vom Anbieter definierter Wert, der die Klasse der Ereignisse angibt, für die der Anbieter Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="055e2-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="055e2-233">Weitere Informationen finden Sie unter dem <em>enableflags</em> -Parameter der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="055e2-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="055e2-234">Geben Sie diesen Wert Namen an, wenn der Anbieter kein <strong>matchanykeyword</strong> oder <strong>matchallkeyword</strong>unterstützt.</span><span class="sxs-lookup"><span data-stu-id="055e2-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-235"><strong>Enablelevel</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="055e2-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-237">Anbieter definierter Wert, der die Detailebene angibt, die im Ereignis enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="055e2-238">Beispielsweise können Sie diesen Wert verwenden, um den Schweregrad der Ereignisse (Information, Warnung, Fehler) anzugeben, die vom Anbieter generiert werden.</span><span class="sxs-lookup"><span data-stu-id="055e2-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="055e2-239">Eine Liste der vordefinierten Ebenen finden Sie unter dem <em>Level</em> -Parameter der Funktion <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>enabletraceex</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="055e2-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-240"><strong>Enableproperty</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="055e2-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-242">Verwenden Sie diesen Wert, um ein oder mehrere der folgenden Elemente in die Protokolldatei einzubeziehen:</span><span class="sxs-lookup"><span data-stu-id="055e2-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="055e2-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = include in den erweiterten Daten die Sicherheits-ID (SID) des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="055e2-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="055e2-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = include in den erweiterten Daten den Bezeichner der Terminalsitzung.</span><span class="sxs-lookup"><span data-stu-id="055e2-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="055e2-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = include in den erweiterten Daten eine aufrufsstapel-Ablauf Verfolgung für Ereignisse, die mithilfe von <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="055e2-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="055e2-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtert alle Ereignisse heraus, für die kein Schlüsselwort ungleich 0 (null) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="055e2-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = gibt an, dass dieser <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> -Aufrufe eine <a href="provider-traits.md">Anbieter Gruppe</a> anstelle eines einzelnen Ereignis Anbieters aktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="055e2-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="055e2-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = schließt den Prozess Start Schlüssel in die erweiterten Daten ein.</span><span class="sxs-lookup"><span data-stu-id="055e2-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="055e2-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = schließt den Ereignis Schlüssel in die erweiterten Daten ein.</span><span class="sxs-lookup"><span data-stu-id="055e2-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="055e2-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtert alle Ereignisse heraus, die entweder als InPrivate-Ereignis gekennzeichnet sind oder von einem Prozess stammen, der als InPrivate markiert ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="055e2-251">Weitere Informationen zu diesen Elementen finden Sie unter <strong>enableproperty (enableproperty</strong> ) der <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="055e2-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="055e2-252"><strong>Matchanykeyword</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="055e2-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-254">Bitmaske von Schlüsselwörtern, die die Kategorie der Ereignisse bestimmen, die der Anbieter schreiben soll.</span><span class="sxs-lookup"><span data-stu-id="055e2-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="055e2-255">Der Anbieter schreibt das Ereignis, wenn eines der Schlüsselwort Bits eines Ereignisses mit einer der in dieser Maske festgelegten Bits identisch ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="055e2-256">Um anzugeben, dass der Anbieter alle Ereignisse schreibt, legen Sie diesen Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="055e2-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="055e2-257">Ein Beispiel finden Sie im Abschnitt "Hinweise" der Funktion " <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>enabletraceex</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="055e2-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="055e2-258"><strong>Matchallschlüsselwort</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="055e2-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="055e2-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="055e2-260">Diese Bitmaske ist optional.</span><span class="sxs-lookup"><span data-stu-id="055e2-260">This bitmask is optional.</span></span> <span data-ttu-id="055e2-261">Diese Maske schränkt die Kategorie der Ereignisse ein, die der Anbieter schreiben soll.</span><span class="sxs-lookup"><span data-stu-id="055e2-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="055e2-262">Wenn das Schlüsselwort des Ereignisses die <em>matchanykeyword</em> -Bedingung erfüllt, schreibt der Anbieter das Ereignis nur dann, wenn alle Bits in dieser Maske im Schlüsselwort des Ereignisses vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="055e2-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="055e2-263">Diese Maske wird nicht verwendet, wenn <em>matchanykeyword</em> gleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="055e2-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="055e2-264">Ein Beispiel finden Sie im Abschnitt "Hinweise" der Funktion " <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>enabletraceex</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="055e2-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="055e2-265">Nachdem die Registrierung geändert wurde, wird die autologger-Sitzung beim nächsten Neustart des Computers gestartet.</span><span class="sxs-lookup"><span data-stu-id="055e2-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="055e2-266">Die autologger-Sitzung ruft die [**enabletraceex**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) -Funktion auf, um die Anbieter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="055e2-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="055e2-267">Die autologger-Sitzungen erhöhen die Systemstart Zeit und sollten sparsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="055e2-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="055e2-268">Dienste, die während des Startvorgangs Informationen erfassen möchten, sollten in Erwägung gezogen werden, anstelle der autologger-Sitzung selbst Controller Logik hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="055e2-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="055e2-269">Um eine autologger-Sitzung zu beenden, wenden Sie die [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="055e2-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="055e2-270">Der Sitzungsname, den Sie an die Funktion übergeben, ist der Name des Registrierungsschlüssels, den Sie zum Definieren der Sitzung in der Registrierung verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="055e2-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="055e2-271">Unter Windows 8.1 können Windows Server 2012 R2 und höhere Ereignis Nutz Last-, Bereichs-und Stapel Durchlauf Filter von der [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion und den [**\_ \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) -Strukturen zum Aktivieren von Ablauf [**\_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und Ereignis Filtern verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungs Sitzung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="055e2-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="055e2-272">Weitere Informationen zu Ereignis Nutz Last Filtern finden Sie unter den Funktionen " [**tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)" und " [**tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) " und " **enable \_ Trace \_ Parameters**", **Ereignis \_ Filter \_ Deskriptor** und [**Payload \_ Filter \_ Predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) Structures.</span><span class="sxs-lookup"><span data-stu-id="055e2-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="055e2-273">Weitere Informationen zum Starten einer Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="055e2-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="055e2-274">Weitere Informationen zum Starten einer privaten Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten einer Sitzung für private](configuring-and-starting-a-private-logger-session.md)Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="055e2-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="055e2-275">Weitere Informationen zum Starten einer NT-Kernel Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="055e2-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="055e2-276">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="055e2-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="055e2-277">Konfigurieren und Starten einer Sitzung für private Logger</span><span class="sxs-lookup"><span data-stu-id="055e2-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="055e2-278">Konfigurieren und Starten einer systemtraceprovider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="055e2-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="055e2-279">Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="055e2-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="055e2-280">Konfigurieren und Starten der NT Kernel Logger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="055e2-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="055e2-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="055e2-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="055e2-282">**Aktivieren von Ablauf \_ Verfolgungs \_ Parametern**</span><span class="sxs-lookup"><span data-stu-id="055e2-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="055e2-283">**Ereignis \_ Filter \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="055e2-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="055e2-284">**Nutz Last \_ Filter- \_ Prädikat**</span><span class="sxs-lookup"><span data-stu-id="055e2-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="055e2-285">**Tdhaggregatepayloadfilters**</span><span class="sxs-lookup"><span data-stu-id="055e2-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="055e2-286">**Tdhkreatepayloadfilter**</span><span class="sxs-lookup"><span data-stu-id="055e2-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="055e2-287">Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="055e2-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
