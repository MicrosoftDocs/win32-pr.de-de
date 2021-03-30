---
description: Die folgenden Konstanten stellen die möglichen Protokollierungs Modi für eine Ereignis Ablauf Verfolgungs Sitzung dar.
ms.assetid: d12aaecb-776a-4476-9ba4-16af30fde9c2
title: Protokollierungs Modus-Konstanten
ms.topic: article
ms.date: 06/03/2020
ms.openlocfilehash: daa0233346718040653edbc75a10615f9fd31765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977825"
---
# <a name="logging-mode-constants"></a>Protokollierungs Modus-Konstanten

Die folgenden Konstanten stellen die möglichen Protokollierungs Modi für eine Ereignis Ablauf Verfolgungs Sitzung dar.

Die Konstanten werden in den **logfilemode** -Membern von [**Ereignis Ablauf \_ Verfolgungs \_ Protokolldatei**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea), [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) und [**\_ logfile- \_ Header**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header) Strukturen der Ablauf Verfolgung verwendet. Diese Konstanten werden in der Header Datei " *evntrace. h* " definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NONE</strong> (0x00000000)</td>
<td>Identisch mit <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> ohne angegebene maximale Dateigröße.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> (0x00000001)</td>
<td>Schreibt Ereignisse sequenziell in eine Protokolldatei. wird beendet, wenn die maximale Größe der Datei erreicht wird. Verwenden Sie nicht mit <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> oder <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> (0x00000002)</td>
<td>Schreibt Ereignisse in eine Protokolldatei. Nachdem die Datei die maximale Größe erreicht hat, werden die ältesten Ereignisse durch eingehende Ereignisse ersetzt. Beachten Sie, dass der Inhalt der Zirkel Protokolldatei auf Multiprozessorcomputern möglicherweise nicht in der richtigen Reihenfolge angezeigt wird.<br/> Verwenden Sie nicht mit <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>oder <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_APPEND</strong> (0x00000004)</td>
<td>Fügt Ereignisse an eine vorhandene sequenzielle Protokolldatei an. Wenn die Datei nicht vorhanden ist, wird Sie erstellt. Verwenden Sie nur, wenn Sie die <a href="wnode-header.md"><strong>Systemzeit</strong></a> für die Takt Auflösung angeben. andernfalls gibt <a href="/windows/win32/api/evntrace/nf-evntrace-processtrace"><strong>processtrace</strong></a> Ereignisse mit falschen Zeitstempeln zurück. Wenn Sie <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>verwenden, müssen die Werte für <strong>bufferSize</strong>, <strong>looofprocessor</strong>und <strong>clocktype</strong> explizit angegeben werden und müssen sowohl in der Protokollierung als auch in der angefügten Datei identisch sein.<br/> Verwenden Sie nicht mit <strong>EVENT_TRACE_REAL_TIME_MODE</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>oder <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>.<br/> <strong>Windows 2000:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> (0x00000008)</td>
<td>Wechselt automatisch zu einer neuen Protokolldatei, wenn die Datei die maximale Größe erreicht. Der <strong>maximumFileSize</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a> muss festgelegt werden. Der angegebene Dateiname muss eine formatierte Zeichenfolge sein (z. b. enthält die Zeichenfolge ein% d, z. b. "c:\test%d.ETL"). Jedes Mal, wenn eine neue Datei erstellt wird, wird ein Leistungswert erhöht, und sein Wert wird verwendet, die formatierte Zeichenfolge wird aktualisiert, und die resultierende Zeichenfolge wird als Dateiname verwendet.<br/> Diese Option ist für Ablauf Verfolgungs Sitzungen für private Ereignisse nicht zulässig und sollte nicht für NT-Kernel Protokollierungs Sitzungen verwendet werden.<br/> Verwenden Sie nicht mit <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> oder <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/> <strong>Windows 2000:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_PREALLOCATE</strong>(0x00000020)</td>
<td>Reserviert <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a> Bytes des Speicherplatzes für die Protokolldatei im voraus. Die Datei belegt den gesamten Speicherplatz während der Protokollierung sowohl für zirkuläre als auch für sequenzielle Protokolldateien. Wenn Sie die Sitzung beenden, wird die Protokolldatei auf die benötigte Größe reduziert. Sie müssen <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES festlegen. MaximumFileSize</strong></a>.<br/> Der Modus kann nicht für Ablauf Verfolgungs Sitzungen für private Ereignisse verwendet werden.<br/> <strong>Windows 2000:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NONSTOPPABLE_MODE</strong>(0x00000040)</td>
<td>Die Protokollierungs Sitzung kann nicht beendet werden. Dieser Modus wird nur von autologger unterstützt. diese Option wird unter Windows Vista und höher unterstützt.<br/>.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_SECURE_MODE</strong> (0x00000080)</td>
<td>Schränkt ein, wer der Sitzung Ereignisse mit <a href="/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol"><strong>TRACELOG_LOG_EVENT</strong></a> -Berechtigung protokollieren kann. Diese Option wird unter Windows Vista und höher unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_REAL_TIME_MODE</strong> (0x00000100)</td>
<td>Übermittelt die Ereignisse in Echtzeit an Consumer. Ereignisse werden übermittelt, wenn die Puffer geleert werden, und nicht zu dem Zeitpunkt, zu dem der Anbieter das Ereignis schreibt. Sie sollten den Echtzeitmodus nicht aktivieren, wenn keine Consumer vorhanden sind, um die Ereignisse zu verarbeiten, da der Aufruf von Protokoll Ereignissen schließlich zu einem Fehler führt, wenn die Puffer voll sind. Vor Windows Vista wurden die Ereignisse verworfen, wenn die Ereignisse nicht verbraucht wurden. Geben Sie nicht mehr als einen echt Zeit Consumer in einem Prozess unter Windows XP orwindows Server 2003 an. Verwenden Sie stattdessen einen Thread, der Ereignisse nutzt und die Ereignisse an andere verteilt.<br/> <strong>Vor Windows Vista:</strong> Sie sollten den Echtzeitmodus nicht verwenden, da die unterstützte Ereignisrate wesentlich niedriger ist als das Lesen aus der Protokolldatei (Ereignisse können gelöscht werden). Außerdem ist die Ereignis Reihenfolge auf Computern mit mehreren Prozessoren nicht sichergestellt. Der Echtzeitmodus eignet sich besser für Ereignisse mit geringem Datenverkehr und Benachrichtigungstyp.<br/> <br/> Sie können diesen Modus mit anderen Protokolldatei Modi kombinieren. Verwenden Sie diesen Modus jedoch nicht mit EVENT_TRACE_PRIVATE_LOGGER_MODE. Beachten Sie Folgendes: Wenn Sie diesen Modus mit anderen Protokolldatei Modi kombinieren, werden Puffer einmal pro Sekunde geleert, was dazu führt, dass teilweise gefüllte Puffer in die Protokolldatei geschrieben werden. Wenn Sie z. b. 64K-Puffer verwenden und die Protokollierungs Rate pro Sekunde 1 Ereignis beträgt, schreibt der Dienst 64K/Sekunde in Ihre Protokolldatei.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_DELAY_OPEN_FILE_MODE</strong>(0x00000200)</td>
<td>Dieser Modus wird verwendet, um das Öffnen der Protokolldatei zu verzögern, bis ein Ereignis auftritt. <br/>
<blockquote>
<strong>Hinweis:</strong><br />
Unter Windows Vista oder höher sollte dieser Modus nicht verwendet werden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_BUFFERING_MODE</strong> (0x00000400)</td>
<td>Dieser Modus schreibt Ereignisse in einen Zirkel Speicherpuffer. Ereignisse, die über die Gesamtgröße des Puffers hinaus geschrieben werden, entfernen die ältesten Ereignisse, die noch im Puffer verbleiben. Die Größe dieses Speicherpuffers ist das Produkt von <strong>minimumbuffers</strong> und <strong>bufferSize</strong> (siehe <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>). Infolge dieser Formel ignoriert jeder Puffer, der <strong>EVENT_TRACE_BUFFERING_MODE</strong> verwendet, den <strong>maximumbuffers</strong> -Wert.<br/> Ereignisse werden nicht in eine Protokolldatei geschrieben oder in Echtzeit übermittelt, und etw leert die Puffer nicht. Um eine Momentaufnahme des Puffers abzurufen, müssen Sie die <a href="/windows/win32/api/evntrace/nf-evntrace-flushtracea"><strong>flushtrace</strong></a> -Funktion aufrufen.<br/> Dieser Modus ist besonders nützlich für das Debuggen von Gerätetreibern in Verbindung mit der Möglichkeit, den Inhalt von Speicher internen Puffern mit der <a href="/windows-hardware/drivers/devtest/trace-session">wmitrace</a> -Kernel Debugger-Erweiterung anzuzeigen.<br/> Verwenden Sie nicht mit <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>oder <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> (0x00000800)</td>
<td>Erstellt eine Ereignis Ablauf Verfolgungs Sitzung im Benutzermodus, die im selben Prozess wie der Ereignis Ablauf Verfolgungs Anbieter ausgeführt wird. Der Arbeitsspeicher für Puffer stammt aus dem Arbeitsspeicher des Prozesses. Prozesse, die keine Daten aus dem Kernel benötigen, können den mit kernelmodusübergängen verbundenen Aufwand eliminieren, indem eine private Ereignis Ablauf Verfolgungs Sitzung verwendet wird.<br/> Wenn der Anbieter von mehreren Prozessen registriert wird, fügt ETW den Prozess Bezeichner an den Namen der Protokolldatei an, um einen eindeutigen Namen für die Protokolldatei zu erstellen. Wenn der Controller z. b. die Namen der Protokolldateien als c:\meinlogs\meineprivatelog.ETL angibt, erstellt etw die Protokolldatei als c:\meinlogs\ myprivatelog.etl_nnnn, wobei nnnn der Prozess Bezeichner ist. Der Prozess Bezeichner wird nicht an den ersten Prozess angehängt, der den Anbieter registriert. er wird nur an die nachfolgenden Prozesse angehängt, die den Anbieter registrieren.<br/> Für Ablauf Verfolgungs Sitzungen für private Ereignisse gelten die folgenden Einschränkungen:<br/>
<ul>
<li>Eine private Sitzung kann Ereignisse nur für die Threads des Prozesses aufzeichnen, in dem Sie ausgeführt wird.</li>
<li>Es können bis zu acht private Sitzungen pro Prozess vorhanden sein.</li>
<li>Private Sitzungen können nicht mit der Echt Zeit Übermittlung verwendet werden.</li>
<li>Ereignisse, die von einer privaten Sitzung generiert werden, beinhalten keine Ausführungszeit für den Kernel Modus im Vergleich zu benutzermodusanweisungen oder Details auf Thread Ebene der verwendeten CPU-Zeit.</li>
</ul>
Prozess-ID-Filter und ausführbare namens Filter können nun an Sitzungs Steuerungs-APIs weitergegeben werden, wenn systemweite private Protokollierungen gestartet werden. Um die besten Ergebnisse in prozessübergreifenden Szenarios zu erzielen, sollten die gleichen Filter während der Sitzung an jeden Steuerungs Vorgang übermittelt werden, einschließlich der Aktivierungs-/Dias-Aufrufe des Anbieters. Beachten Sie, dass die Filter das gleiche Format aufweisen wie die von <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a>verwendeten. <br/> Sie können diesen Modus in Verbindung mit dem <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> Modus verwenden.<br/> <strong>Vor Windows 10, Version 1703:</strong> Nur "LocalSystem", "Administrator" und "Benutzer" in der Administrator Gruppe, die in einem Prozess mit erhöhten Rechten ausgeführt werden, können eine private Sitzung erstellen. Wenn Sie das <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> -Flag einschließen, kann jeder Benutzer eine private Prozess interne Sitzung erstellen. Außerdem kann in früheren Versionen von Windows nur eine private Sitzung pro Prozess vorhanden sein (es sei denn, der EVENT_TRACE_PRIVATE_IN_PROC Modus wird ebenfalls angegeben. in diesem Fall können Sie bis zu drei in-Process private Sitzungen erstellen). <br/> <strong>Vor Windows Vista:</strong> Benutzer in der Gruppe Leistungs Protokoll Benutzer können auch eine private Sitzung erstellen.<br/> <br/> Verwenden Sie nicht mit EVENT_TRACE_REAL_TIME_MODE.<br/> <strong>Vor Windows 7 und Windows Server 2008 R2:</strong> Verwenden Sie nicht mit EVENT_TRACE_FILE_MODE_NEWFILE.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_ADD_HEADER_MODE</strong>(0x00001000)</td>
<td>Mit dieser Option wird der Protokolldatei ein-Header hinzugefügt.<br/>
<blockquote>
<strong>Hinweis:</strong><br />
Unter Windows Vista oder höher sollte dieser Modus nicht verwendet werden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_KBYTES_FOR_SIZE</strong>(0x00002000)</td>
<td>Verwenden Sie Kilobyte als Maßeinheit zum Angeben der Größe einer Datei. Die Standard Maßeinheit ist Megabytes. Dieser Modus gilt für den <strong>MaxFileSize</strong> -Registrierungs Wert für eine <a href="configuring-and-starting-an-autologger-session.md">autologger</a> -Sitzung und den <strong>maximumFileSize</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>. Diese Option wird unter Windows Vista und höher unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong>(0x00004000)</td>
<td>Verwendet Sequenznummern, die in Ereignis Ablauf Verfolgungs Sitzungen eindeutig sind. Dieser Modus gilt nur für Ereignisse, die mithilfe der <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>tracemess</strong></a> -Funktion protokolliert wurden. Weitere Informationen finden Sie unter Ablauf <strong>Verfolgungs</strong> Informationen.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> und <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> schließen sich gegenseitig aus.<br/> <strong>Windows 2000:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> (0x00008000)</td>
<td>Verwendet Sequenznummern, die nur für eine einzelne Ereignis Ablauf Verfolgungs Sitzung eindeutig sind. Dieser Modus gilt nur für Ereignisse, die mithilfe der <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>tracemess</strong></a> -Funktion protokolliert wurden. Weitere Informationen finden Sie unter Ablauf <strong>Verfolgungs</strong> Informationen.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> und <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> schließen sich gegenseitig aus.<br/> <strong>Windows 2000:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_RELOG_MODE</strong> (0x00010000 bis)</td>
<td>Protokolliert das Ereignis, ohne <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_header"><strong>EVENT_TRACE_HEADER</strong></a>einzubeziehen.
<blockquote>
<strong>Hinweis:</strong><br />
Dieser Modus sollte nicht verwendet werden. Sie ist für die interne Verwendung reserviert.
</blockquote>
<br/> <strong>Windows 2000:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> (0x00020000)</td>
<td>Verwenden Sie in Verbindung mit dem <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> Modus eine private Sitzung. Dieser Modus erzwingt, dass nur der Prozess, der die Anbieter-GUID registriert hat, die Protokollierungs Sitzung mit dieser GUID starten kann.<br/> Sie können bis zu drei Prozess interne private Sitzungen pro Prozess erstellen.<br/> Diese Option wird unter Windows Vista und höher unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_MODE_RESERVED</strong>(0x00100000)</td>
<td>Diese Option wird verwendet, um die Nachverfolgung von Heap und kritischen Abschnitten zu signalisieren. Diese Option wird unter Windows Vista und höher unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong>(0x00400000)</td>
<td>Mit dieser Option wird die Protokollierung von Hybrid Shutdown beendet. Wenn weder <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> noch <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> angegeben ist, wählt etw einen Standardwert aus, je nachdem, ob der Aufrufer aus Sitzung 0 stammt oder nicht. Diese Option wird unter Windows 8 und Windows Server 2012 unterstützt. <br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong>(0x00800000)</td>
<td>Mit dieser Option wird die Protokollierung bei Hybrid Shutdown fortgesetzt Wenn weder <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> noch <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> angegeben ist, wählt etw einen Standardwert aus, je nachdem, ob der Aufrufer aus Sitzung 0 stammt oder nicht. Diese Option wird unter Windows 8 und Windows Server 2012 unterstützt. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_PAGED_MEMORY</strong> (0x01000000)</td>
<td>Verwendet auslagerbare Speicher. Diese Einstellung wird empfohlen, damit Ereignisse nicht den nicht auslagerenden Speicher verwenden. Nicht auslagerbare Puffer verwenden nicht auslagerenden Arbeitsspeicher für den Puffer Speicherplatz. Da nicht auslagerbare Puffer nie ausgelagert werden, führt eine Protokollierungs Sitzung eine gute Leistung aus. Die Verwendung von kostenpflichtigen Puffern ist weniger ressourcenintensiv.<br/> Kernelmodusanbieter und System Protokollierungen können Ereignisse nicht in Sitzungen protokollieren, die diesen Protokollierungs Modus angeben.<br/> Dieser Modus wird ignoriert, wenn <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> festgelegt ist.<br/> Dieser Modus kann nicht mit der NT-Kernel Protokollierung verwendet werden.<br/> <strong>Windows 2000:</strong> Dieser Wert wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_SYSTEM_LOGGER_MODE</strong>(0x02000000)</td>
<td>Mit dieser Option werden Ereignisse von systemtraceprovider empfangen. Wenn der <a href="/windows/win32/api/evntrace/nf-evntrace-starttracea"><strong>starttrace</strong></a>-<em>Eigenschafts</em> Parameter <strong>logfilemode</strong> dieses Flag enthält, ist die Protokollierung eine Systemprotokollierung. Diese Option wird unter Windows 8 und Windows Server 2012 unterstützt. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_INDEPENDENT_SESSION_MODE</strong>(0x08000000)</td>
<td>Gibt an, dass eine Protokollierungs Sitzung von <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>Ereignis Schreib</strong></a> Fehlern in anderen Sitzungen nicht betroffen sein sollte. Ohne dieses Flag wird das Ereignis nicht in einer der Sitzungen veröffentlicht, wenn ein Ereignis nicht in einer der Sitzungen veröffentlicht werden kann, für die ein Anbieter aktiviert ist. Wenn dieses Flag festgelegt ist, führt ein Fehler beim Schreiben eines Ereignisses in eine Sitzung nicht dazu, dass die <strong>EventWrite</strong> -Funktion in anderen Sitzungen einen Fehlercode zurückgibt. <br/> Verwenden Sie nicht mit <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>. <br/> Diese Option wird auf Windows 8.1, Windows Server 2012 R2 und höher unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING</strong> (0x10000000)</td>
<td>Schreibt Ereignisse, die auf unterschiedlichen Prozessoren protokolliert wurden, in einen gemeinsamen Puffer. Wenn Sie diesen Modus verwenden, kann es vorkommen, dass Ereignisse nicht in der richtigen Reihenfolge auftreten, wenn Ereignisse mithilfe der Systemzeit auf unterschiedlichen Prozessoren veröffentlicht werden. Dieser Modus kann auch das Problem mit Zirkel Protokollen beseitigen, die zum Löschen von Ereignissen auf mehreren Prozessor Computern angezeigt werden.<br/> Wenn Sie diesen Modus nicht verwenden und die Systemzeit verwenden, werden die Ereignisse möglicherweise auf mehreren Prozessor Computern nicht in der richtigen Reihenfolge angezeigt. Dies liegt daran, dass etw-Puffer einem Prozessor anstatt einem Thread zugeordnet sind. Wenn ein Thread von einer CPU zu einer anderen gewechselt wird, kann der Puffer, der der letzteren CPU zugeordnet ist, auf den Datenträger geleert werden, bevor er mit der früheren CPU verknüpft ist.<br/> Wenn Sie eine große Anzahl von Ereignissen erwarten (z. b. mehr als 1.000 Ereignisse pro Sekunde), sollten Sie diesen Modus nicht verwenden.<br/> Beachten Sie, dass die Prozessornummer nicht im-Ereignis enthalten ist.<br/> Diese Option wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_ADDTO_TRIAGE_DUMP</strong>(0x80000000)</td>
<td>Diese Option fügt ETW-Puffer zu selektiert Dumps hinzu. Diese Option wird unter Windows 8 und Windows Server 2012 unterstützt. <br/></td>
</tr>
</tbody>
</table>
