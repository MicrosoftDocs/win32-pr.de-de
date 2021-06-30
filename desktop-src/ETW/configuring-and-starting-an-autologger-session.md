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
# <a name="configuring-and-starting-an-autologger-session"></a>Konfigurieren und Starten einer AutoLogger-Sitzung

Die AutoLogger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die früh im Startprozess des Betriebssystems auftreten. Anwendungen und Gerätetreiber können die AutoLogger-Sitzung verwenden, um Ablaufverfolgungen zu erfassen, bevor sich der Benutzer anmeldet. Beachten Sie, dass einige Gerätetreiber, z. B. Datenträgergerätetreiber, zum Zeitpunkt des Beginns der AutoLogger-Sitzung nicht geladen werden.

Die AutoLogger unterscheidet sich wie folgt von der globalen Protokollierung:

-   Sie können eine oder mehrere AutoLogger-Sitzungen angeben (die globale Protokollierung war eine einzelne Sitzung, in der alle Ereignisse protokolliert haben).
-   Die AutoLogger-Funktion sendet beim Starten der Sitzung eine Aktivierungsbenachrichtigung an die Anbieter (die globale Protokollierung hat keine Aktivierungsbenachrichtigung an die Anbieter gesendet, sodass die Anbieter sich auf andere Mittel verlassen mussten, um zu wissen, ob die Globale Protokollierungssitzung gestartet wurde, um mit der Protokollierung von Ereignissen zu beginnen).
-   Die AutoLogger-Funktion unterstützt keine Protokollierung von NT-Kernelprotokollierungsereignissen (siehe **EnableFlags-Member** von [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)). Zum Protokollieren von NT-Kernelprotokollierungsereignissen müssen Sie die [globale Protokollierung](configuring-and-starting-the-global-logger-session.md)verwenden.

Weitere Informationen zur Globalen Protokollierung finden Sie unter [Konfigurieren und Starten der globalen Protokollierungssitzung.](configuring-and-starting-the-global-logger-session.md)

> [!Note]  
> ETW unterstützt die AutoLogger-Funktion unter Windows Vista und höher. Verwenden Sie die [globale Protokollierung](configuring-and-starting-the-global-logger-session.md) unter früheren Betriebssystemen.

 

Sie verwenden die Registrierung, um die AutoLogger-Sitzung zu konfigurieren. Fügen Sie den folgenden Registrierungsschlüssel hinzu, falls er noch nicht vorhanden ist:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

Erstellen Sie unter dem Schlüssel **Autologger** einen Schlüssel für jede AutoLogger-Sitzung, die Sie konfigurieren möchten, wie im folgenden Beispiel gezeigt.

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

Erstellen Sie für jede Sitzung einen Schlüssel für jeden Anbieter, den Sie für die Sitzung aktivieren möchten. Verwenden Sie die GUID des Anbieters als Schlüssel.

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

In der folgenden Tabelle werden die Werte beschrieben, die Sie für jede AutoLogger-Sitzung definieren können. Sie müssen über Administratorrechte verfügen, um diese Registrierungswerte anzugeben. Der **Start-** und **guid-Wert** sind die einzigen Werte, die zum Starten der AutoLogger-Sitzung erforderlich sind. alle anderen Werte verfügen über Standardeinstellungen, die verwendet werden, wenn der Wert nicht in der Registrierung vorhanden ist. In der Regel sollten Sie die Standardwerte verwenden. Wenn Sie einen Wert angeben, der von ETW nicht unterstützt werden kann, überschreibt ETW den Wert.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Größe jedes Puffers in Kilobyte. Sollte kleiner als ein Megabyte sein. ETW verwendet die Größe des physischen Arbeitsspeichers, um diesen Wert zu berechnen.<br/></td>
</tr>
<tr class="even">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Der Timer, der beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll.
<ul>
<li>1 = Leistungsindikatorwert (hohe Auflösung)</li>
<li>2 = Systemtimer</li>
<li>3 = CPU-Zykluszähler</li>
</ul>
Eine Beschreibung der einzelnen Uhrtypen finden Sie im <strong>ClientContext-Member</strong> von <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> Der Standardwert ist 1 (Leistungsindikatorwert) unter Windows Vista und höher. Vor Windows Vista ist der Standardwert 2 (Systemtimer).<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Legen Sie diesen Wert auf 1 fest, um die Echtzeitpersistenz zu deaktivieren. Der Standardwert ist 0 (aktiviert) für Echtzeitsitzungen.<br/> Wenn Die Echtzeitpersistenz aktiviert ist, werden Echtzeitereignisse beibehalten, die zum Zeitpunkt des Herunterfahrens des Computers nicht übermittelt wurden. Die Ereignisse werden dann an den Consumer übermittelt, wenn der Consumer das nächste Mal eine Verbindung mit der Sitzung herstellt. <br/></td>
</tr>
<tr class="even">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Legen Sie diesen Wert nicht fest, oder ändern Sie diesen Wert nicht. Dieser Wert ist die Seriennummer, die verwendet wird, um den Protokolldateinamen zu erhöhen, wenn <strong>FileMax</strong> angegeben ist. Wenn der Wert ungültig ist, wird 1 angenommen.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Der vollqualifizierte Pfad der Protokolldatei. Der Pfad zu dieser Datei muss vorhanden sein. Die Protokolldatei ist eine sequenzielle Protokolldatei. Der Pfad ist auf 1024 Zeichen beschränkt.<br/> Wenn <strong>FileName</strong> nicht angegeben ist, werden Ereignisse in %SystemRoot%\System32\LogFiles\WMI \& lt;Sitzungsname &gt; .etl geschrieben. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl von Instanzen der Protokolldatei, die ETW erstellt. Wenn die in <strong>FileName</strong> angegebene Protokolldatei vorhanden ist, fügt ETW den <strong>FileCounter-Wert</strong> an den Dateinamen an. Wenn beispielsweise der Standardprotokolldateiname verwendet wird, lautet das Formular %SystemRoot%\System32\LogFiles\WMI \& lt;Sitzungsname &gt; .etl. Nnnn. <br/> Wenn der Computer zum ersten Mal gestartet wird, lautet der Dateiname &lt; sitzungsname &gt; .etl.0001, das zweite Mal ist der Dateiname &lt; Sitzungsname &gt; .etl.0002 usw. Wenn <strong>FileMax</strong> gleich 3 ist, setzt ETW den Zähler beim vierten Neustart des Computers auf 1 zurück und überschreibt den &lt; Sitzungsnamen &gt; .etl.0001, sofern vorhanden.<br/> Die maximale Anzahl der unterstützten Instanzen der Protokolldatei beträgt 16.<br/> Verwenden Sie dieses Feature nicht mit dem <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> Protokolldateimodus.<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Gibt an, wie oft die Ablaufverfolgungspuffer in Sekunden zwangsmäßig geleert werden. Die mindeste Leerungszeit beträgt 1 Sekunde. Diese erzwungene Leerung erfolgt zusätzlich zur automatischen Leerung, die auftritt, wenn ein Puffer voll ist und die Ablaufverfolgungssitzung beendet wird. <br/> Bei einer Echtzeitprotokollierung bedeutet der Wert 0 (Standardwert) , dass die Leerungszeit auf 1 Sekunde festgelegt wird. Eine Echtzeitprotokollierung ist , wenn <strong>LogFileMode</strong> auf <strong>EVENT_TRACE_REAL_TIME_MODE</strong>festgelegt ist.<br/> Der Standardwert ist 0. Standardmäßig werden Puffer nur geleert, wenn sie voll sind. <br/></td>
</tr>
<tr class="even">
<td><strong>Guid</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Eine Zeichenfolge, die eine GUID enthält, die die Sitzung eindeutig identifiziert. Dieser Wert ist erforderlich.</td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Geben Sie einen oder mehrere Protokollmodi an. Mögliche Werte finden Sie unter <a href="logging-mode-constants.md">Protokollierungsmoduskonstanten.</a> Der Standardwert ist <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. Anstatt in eine Protokolldatei zu schreiben, können Sie entweder <strong>EVENT_TRACE_BUFFERING_MODE</strong> oder <strong>EVENT_TRACE_REAL_TIME_MODE</strong>angeben.<br/> Wenn <strong>Sie EVENT_TRACE_BUFFERING_MODE</strong> angeben, werden die Kosten für das Leeren des Sitzungsinhalts auf den Datenträger vermieden, wenn das Dateisystem verfügbar wird. <br/> Beachten Sie, dass die Verwendung <strong>von EVENT_TRACE_BUFFERING_MODE</strong> bewirkt, dass das System den <strong>MaximumBuffers-Wert</strong> ignoriert, da die Puffergröße stattdessen das Produkt von <strong>MinimumBuffers</strong> und <strong>BufferSize</strong>ist.<br/> AutoLogger-Sitzungen unterstützen den <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> Protokollierungsmodus nicht.<br/> Wenn <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> angegeben wird, muss <strong>BufferSize</strong> explizit bereitgestellt werden und sowohl in der Protokollierung als auch in der datei, die angefügt wird, identisch sein.<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Dateigröße der Protokolldatei in Megabyte. Die Sitzung wird geschlossen, wenn die maximale Größe erreicht wird, es sei denn, Sie befinden sich im zirkulären Protokolldateimodus. Um kein Limit anzugeben, legen Sie den Wert auf 0 fest. Der Standardwert ist 100 MB, falls nicht festgelegt. Das Verhalten, das auftritt, wenn die maximale Dateigröße erreicht wird, hängt vom Wert von <strong>LogFileMode</strong>ab.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl der zu reservierenden Puffer. In der Regel ist dieser Wert die Mindestanzahl von Puffern plus 20. ETW verwendet die Puffergröße und die Größe des physischen Speichers, um diesen Wert zu berechnen. Dieser Wert muss größer oder gleich dem Wert für <strong>MinimumBuffers sein.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Mindestanzahl von Puffern, die beim Start reserviert werden. Die Mindestanzahl von Puffern, die Sie angeben können, beträgt zwei Puffer pro Prozessor. Auf einem einzelnen Prozessorcomputer beträgt die Mindestanzahl von Puffern beispielsweise zwei.<br/></td>
</tr>
<tr class="odd">
<td><strong>Starten</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Legen Sie diesen Wert auf 1 fest, damit die AutoLogger-Sitzung beim nächsten Neustart des Computers gestartet wird. Legen Sie andernfalls diesen Wert auf 0 fest.<br/></td>
</tr>
<tr class="even">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Der Startstatus der AutoLogger. Wenn die AutoLogger nicht gestartet werden konnte, ist der Wert dieses Schlüssels der entsprechende Win32-Fehlercode. Wenn die AutoLogger erfolgreich gestartet wurde, wird der Wert dieses Schlüssels <strong>ERROR_SUCCESS</strong> (0) angezeigt.<br/></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Werte beschrieben, die Sie für jeden Anbieter definieren können, den Sie für Ihre Sitzung aktivieren möchten. Sie müssen über Administratorrechte verfügen, um diese Registrierungswerte anzugeben. Wenn Sie einen Wert angeben, der von ETW nicht unterstützt werden kann, überschreibt ETW den Wert.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Enabled</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Bestimmt, ob der Anbieter aktiviert ist. Legen Sie diesen Wert auf 1 fest, um den Anbieter zu aktivieren. Um den Anbieter zu deaktivieren, legen Sie diesen Wert auf 0 fest. Die Standardeinstellung ist 0.</td>
</tr>
<tr class="even">
<td><strong>EnableFlags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Vom Anbieter definierter Wert, der die Ereignisklasse angibt, für die der Anbieter Ereignisse generiert. Weitere Informationen finden Sie im <em>EnableFlags-Parameter</em> der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace-Funktion.</strong></a> Geben Sie diesen Wertnamen an, wenn der Anbieter <strong>MatchAnyKeyword</strong> oder <strong>MatchAllKeyword nicht unterstützt.</strong></td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Vom Anbieter definierter Wert, der die Detailebene angibt, die im Ereignis enthalten ist. Sie können diesen Wert beispielsweise verwenden, um den Schweregrad der Ereignisse (Information, Warnung, Fehler) anzugeben, die der Anbieter generiert. Eine Liste vordefinierter Ebenen finden Sie unter dem <em>level-Parameter</em> der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx-Funktion.</strong></a></td>
</tr>
<tr class="even">
<td><strong>EnableProperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Verwenden Sie diesen Wert, um eines oder mehrere der folgenden Elemente in die Protokolldatei ein-/ausderherzustellen:
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Schließen Sie die Sicherheits-ID (SID) des Benutzers in die erweiterten Daten ein.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Schließen Sie den Terminalsitzungsbezeichner in die erweiterten Daten ein.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Schließen Sie in die erweiterten Daten eine Aufrufliste-Ablaufverfolgung für Ereignisse ein, die mit <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite geschrieben wurden.</strong></a></li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filtert alle Ereignisse heraus, für die kein Schlüsselwort ohne Null angegeben ist.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Gibt an, dass dieser Aufruf von <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> anstelle eines einzelnen Ereignisanbieters eine Anbietergruppe aktivieren soll. <a href="provider-traits.md"></a></li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Schließen Sie den Prozessstartschlüssel in die erweiterten Daten ein.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Schließen Sie den Ereignisschlüssel in die erweiterten Daten ein.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filtert alle Ereignisse heraus, die entweder als InPrivate-Ereignis markiert sind oder von einem Als InPrivate markierten Prozess stammen.</li>
</ul>
Weitere Informationen zu diesen Elementen finden Sie unter <strong>EnableProperty</strong> der <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> Struktur.<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Bitmaske von Schlüsselwörtern, die die Kategorie der Ereignisse bestimmen, die der Anbieter schreiben soll. Der Anbieter schreibt das Ereignis, wenn eines der Schlüsselwortbits des Ereignisses mit einem der in dieser Maske festgelegten Bits übereinstimmen. Um anzugeben, dass der Anbieter alle Ereignisse schreibt, legen Sie diesen Wert auf 0 (null) fest. Ein Beispiel finden Sie im Abschnitt "Hinweise" der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx-Funktion.</strong></a></td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Diese Bitmaske ist optional. Diese Maske schränkt die Kategorie der Ereignisse weiter ein, die der Anbieter schreiben soll. Wenn das Schlüsselwort des Ereignisses die <em>MatchAnyKeyword-Bedingung</em> erfüllt, schreibt der Anbieter das Ereignis nur, wenn alle Bits in dieser Maske im Schlüsselwort des Ereignisses vorhanden sind. Diese Maske wird nicht verwendet, <em>wenn MatchAnyKeyword</em> 0 (null) ist. Ein Beispiel finden Sie im Abschnitt "Hinweise" der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx-Funktion.</strong></a></td>
</tr>
</tbody>
</table>



 

Nachdem die Registrierung geändert wurde, wird die AutoLogger-Sitzung beim nächsten Neustart des Computers gestartet. Die AutoLogger-Sitzung ruft die [**EnableTraceEx-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) auf, um die Anbieter zu aktivieren.

Die AutoLogger-Sitzungen erhöhen die Systemstartzeit und sollten nur wenig verwendet werden. Dienste, die Während des Startvorgangs Informationen erfassen möchten, sollten erwägen, sich selbst Controllerlogik hinzufügen, anstatt die AutoLogger-Sitzung zu verwenden.

Um eine AutoLogger-Sitzung zu beenden, rufen Sie die [**ControlTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-controltracea) auf. Der Sitzungsname, den Sie an die Funktion übergeben, ist der Name des Registrierungsschlüssels, den Sie zum Definieren der Sitzung in der Registrierung verwendet haben.

Unter Windows 8.1, Windows Server 2012 R2 und höher können Ereignisnutzlast-, Bereichs- und Stapelüberwachungsfilter von der [**EnableTraceEx2-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) und den [**ENABLE TRACE \_ \_ PARAMETERS-**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**EVENT \_ \_ FILTER-DESCRIPTOR-Strukturen**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungssitzung zu filtern. Weitere Informationen zu Ereignisnutzlastfiltern finden Sie in den Funktionen [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)und [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) sowie in den **STRUKTUREN ENABLE TRACE \_ \_ PARAMETERS,** **EVENT FILTER \_ \_ DESCRIPTOR** und [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Weitere Informationen zum Starten einer Ereignisablaufverfolgungssitzung finden Sie unter Konfigurieren und [Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

Weitere Informationen zum Starten einer privaten Protokollierungssitzung finden Sie unter Konfigurieren und [Starten einer privaten Protokollierungssitzung.](configuring-and-starting-a-private-logger-session.md)

Weitere Informationen zum Starten einer NT-Kernelprotokollierungssitzung finden Sie unter Konfigurieren und [Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**AKTIVIEREN VON \_ ABLAUFVERFOLGUNGSPARAMETERN \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_ \_ EREIGNISFILTERDESKRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_ \_ NUTZLASTFILTER-PRÄDIKAT**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aktualisieren einer Ereignisablaufverfolgungssitzung](updating-an-event-tracing-session.md)
</dt> </dl>
