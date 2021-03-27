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
# <a name="configuring-and-starting-an-autologger-session"></a>Konfigurieren und Starten einer autologger-Sitzung

Die Ereignis Ablauf Verfolgungs Sitzung von autologger zeichnet Ereignisse auf, die früh im Betriebssystem-Startprozess auftreten. Anwendungen und Gerätetreiber können die autologger-Sitzung verwenden, um Ablauf Verfolgungen zu erfassen, bevor sich der Benutzer anmeldet. Beachten Sie, dass einige Gerätetreiber, z. b. Datenträger-Gerätetreiber, beim Beginn der autologger-Sitzung nicht geladen werden.

Der autologger unterscheidet sich wie folgt von der globalen Protokollierung:

-   Sie können mindestens eine autologger-Sitzung angeben (bei der globalen Protokollierung handelt es sich um eine einzelne Sitzung, für die alle Ereignisse protokolliert haben).
-   Der autologger sendet eine Aktivierungs Benachrichtigung an die Anbieter, wenn die Sitzung gestartet wird (die globale Protokollierung hat keine Aktivierungs Benachrichtigung an die Anbieter gesendet, sodass die Anbieter auf andere Weise wissen müssen, ob die globale Protokollierungs Sitzung gestartet wurde, um mit der Protokollierung von Ereignissen zu beginnen).
-   Der autologger unterstützt das Protokollieren von NT-Kernel Protokollierungs Ereignissen nicht (siehe **enableflags** -Member von [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)). Zum Protokollieren von NT-kernelprotokollierungs Ereignissen müssen Sie die [globale](configuring-and-starting-the-global-logger-session.md)Protokollierung verwenden.

Weitere Informationen zur globalen Protokollierungs seesion finden Sie unter [Konfigurieren und Starten der globalen](configuring-and-starting-the-global-logger-session.md)Protokollierungs Sitzung.

> [!Note]  
> Etw unterstützt den autologger unter Windows Vista und höher. Verwenden Sie die [globale](configuring-and-starting-the-global-logger-session.md) Protokollierung unter früheren Betriebssystemen.

 

Sie verwenden die Registrierung, um die autologger-Sitzung zu konfigurieren. Fügen Sie den folgenden Registrierungsschlüssel hinzu, wenn er nicht bereits vorhanden ist:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

Erstellen Sie unter dem Schlüssel **autologger** einen Schlüssel für jede autologger-Sitzung, die Sie konfigurieren möchten, wie im folgenden Beispiel gezeigt.

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

In der folgenden Tabelle werden die Werte beschrieben, die Sie für jede autologger-Sitzung definieren können. Sie müssen über Administratorrechte verfügen, um diese Registrierungs Werte angeben zu können. Der **Start** -und der **GUID** -Wert sind die einzigen Werte, die zum Starten der autologger-Sitzung erforderlich sind. alle anderen Werte haben Standardeinstellungen, die verwendet werden, wenn der Wert nicht in der Registrierung vorhanden ist. Normalerweise sollten Sie die Standardwerte verwenden. Wenn Sie einen Wert angeben, der von etw nicht unterstützt werden kann, wird der Wert von etw überschrieben.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Größe der einzelnen Puffer in Kilobyte. Sollte kleiner als 1 MB sein. Etw verwendet die Größe des physischen Speichers, um diesen Wert zu berechnen.<br/></td>
</tr>
<tr class="even">
<td><strong>Clocktype</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Der Zeitgeber, der verwendet werden soll, wenn der Zeitstempel für jedes Ereignis protokolliert wird.
<ul>
<li>1 = Leistungs Zählers Wert (hohe Auflösung)</li>
<li>2 = systemtimer</li>
<li>3 = CPU-Zyklen-Counter</li>
</ul>
Eine Beschreibung der einzelnen uhrtypen finden Sie im <strong>clientcontext</strong> -Member von <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> Der Standardwert ist 1 (Leistungs Leistungswert) unter Windows Vista und höher. Vor Windows Vista ist der Standardwert 2 (systemtimer).<br/></td>
</tr>
<tr class="odd">
<td><strong>Disablerealtimepersistenz</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Um die Echt Zeit Persistenz zu deaktivieren, legen Sie diesen Wert auf 1 fest. Der Standardwert ist 0 (aktiviert) für echt Zeit Sitzungen.<br/> Wenn die Echt Zeit Persistenz aktiviert ist, werden Echtzeitereignisse permanent gespeichert, die nicht von dem Zeitpunkt des herunter Fahrens des Computers zugestellt wurden. Die Ereignisse werden dann an den Consumer übermittelt, wenn der Consumer das nächste Mal eine Verbindung mit der Sitzung herstellt. <br/></td>
</tr>
<tr class="even">
<td><strong>File Counter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Dieser Wert kann nicht festgelegt oder geändert werden. Dieser Wert ist die Seriennummer, die verwendet wird, um den Namen der Protokolldatei zu erhöhen, wenn <strong>filemax</strong> angegeben wird. Wenn der Wert nicht gültig ist, wird 1 angenommen.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Der voll qualifizierte Pfad der Protokolldatei. Der Pfad zu dieser Datei muss vorhanden sein. Die Protokolldatei ist eine sequenzielle Protokolldatei. Der Pfad ist auf 1024 Zeichen beschränkt.<br/> Wenn <strong>filename</strong> nicht angegeben wird, werden die Ereignisse in%SystemRoot%\system32\logfiles\wmi\ <sessionname> . ETL geschrieben. <br/></td>
</tr>
<tr class="even">
<td><strong>Filemax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl von Instanzen der Protokolldatei, die von etw erstellt werden. Wenn die in <strong>filename</strong> angegebene Protokolldatei vorhanden ist, fügt ETW den <strong>filecounter</strong> -Wert an den Dateinamen an. Wenn z. b. der Standardname der Protokolldatei verwendet wird, lautet das Formular%systemroot%\system32\logfiles\wmi\ <sessionname> . ETL. NNNN. <br/> Wenn der Computer zum ersten Mal gestartet wird, lautet der Dateiname " <sessionname> . ETL. 0001", der Dateiname ist " <sessionname> . ETL. 0002" usw. Wenn <strong>filemax</strong> den Wert 3 hat, setzt etw beim vierten Neustart des Computers den Wert auf 1 zurück und überschreibt <sessionname> . ETL. 0001, falls vorhanden.<br/> Die maximal unterstützte Anzahl von Instanzen der Protokolldatei ist 16.<br/> Verwenden Sie diese Funktion nicht mit dem <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> Protokolldatei Modus.<br/></td>
</tr>
<tr class="odd">
<td><strong>Flushtimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Gibt an, wie oft die Ablauf Verfolgungs Puffer in Sekunden erzwungen werden. Die minimale Leerungs Zeit beträgt 1 Sekunde. Dieser erzwungene Löschvorgang erfolgt zusätzlich zu dem automatischen leeren, der auftritt, wenn ein Puffer voll ist und die Ablauf Verfolgungs Sitzung beendet wird. <br/> Bei einer echt Zeit Protokollierung bedeutet der Wert 0 (null) (der Standardwert), dass die Leerungs Zeit auf 1 Sekunde festgelegt wird. Eine echt Zeit Protokollierung ist, wenn <strong>logfilemode</strong> auf <strong>EVENT_TRACE_REAL_TIME_MODE</strong>festgelegt ist.<br/> Der Standardwert ist 0. Standardmäßig werden Puffer nur geleert, wenn Sie voll sind. <br/></td>
</tr>
<tr class="even">
<td><strong>GUID</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Eine Zeichenfolge, die eine GUID enthält, die die Sitzung eindeutig identifiziert. Dieser Wert ist erforderlich.</td>
</tr>
<tr class="odd">
<td><strong>Logfilemode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Geben Sie mindestens einen Protokollmodus an. Mögliche Werte finden Sie unter <a href="logging-mode-constants.md">Protokollierungs Modus-Konstanten</a>. Der Standardwert ist <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. Anstatt in eine Protokolldatei zu schreiben, können Sie entweder <strong>EVENT_TRACE_BUFFERING_MODE</strong> oder <strong>EVENT_TRACE_REAL_TIME_MODE</strong>angeben.<br/> Das Angeben von <strong>EVENT_TRACE_BUFFERING_MODE</strong> vermeidet die Kosten für das Leeren des Inhalts der Sitzung auf den Datenträger, wenn das Dateisystem verfügbar wird. <br/> Beachten Sie, dass die Verwendung von <strong>EVENT_TRACE_BUFFERING_MODE</strong> dazu führt, dass das System den <strong>maximumbuffers</strong> -Wert ignoriert, da die Puffergröße stattdessen das Produkt von <strong>minimumbuffers</strong> und <strong>bufferSize</strong>ist.<br/> Der <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> Protokollierungs Modus wird von autologger-Sitzungen nicht unterstützt.<br/> Wenn <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> angegeben wird, muss <strong>bufferSize</strong> explizit angegeben werden und muss sowohl in der Protokollierung als auch in der angefügten Datei identisch sein.<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Dateigröße der Protokolldatei in Megabytes. Die Sitzung wird geschlossen, wenn die maximale Größe erreicht wird, es sei denn, Sie befinden sich im Zirkel Protokolldatei Modus. Legen Sie den Wert auf 0 fest, um keine Beschränkung anzugeben. Der Standardwert ist 100 MB, wenn er nicht festgelegt ist. Das Verhalten, das auftritt, wenn die maximale Dateigröße erreicht wird, hängt vom Wert von <strong>logfilemode</strong>ab.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl der zuzuordnenden Puffer. In der Regel ist dieser Wert die minimale Anzahl von Puffern plus 20. Etw verwendet die Puffergröße und die Größe des physischen Speichers, um diesen Wert zu berechnen. Dieser Wert muss größer oder gleich dem Wert für <strong>minimumbuffers</strong>sein.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die minimale Anzahl von Puffern, die beim Start von zuzuordnen sind. Die Mindestanzahl an Puffern, die Sie angeben können, sind zwei Puffer pro Prozessor. Beispielsweise ist auf einem Computer mit einem einzelnen Prozessor die Mindestanzahl an Puffern auf zwei.<br/></td>
</tr>
<tr class="odd">
<td><strong>Starten</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Legen Sie diesen Wert auf 1 fest, damit die autologger-Sitzung beim nächsten Neustart des Computers gestartet wird. andernfalls legen Sie diesen Wert auf 0 fest.<br/></td>
</tr>
<tr class="even">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Der Startstatus des autologers. Wenn der autologger nicht gestartet werden konnte, ist der Wert dieses Schlüssels der entsprechende Win32-Fehlercode. Wenn der autologger erfolgreich gestartet wurde, ist der Wert dieses Schlüssels <strong>ERROR_SUCCESS</strong> (0).<br/></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Werte beschrieben, die Sie für jeden Anbieter definieren können, den Sie für Ihre Sitzung aktivieren möchten. Sie müssen über Administratorrechte verfügen, um diese Registrierungs Werte angeben zu können. Wenn Sie einen Wert angeben, der von etw nicht unterstützt werden kann, wird der Wert von etw überschrieben.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Aktiviert</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Bestimmt, ob der Anbieter aktiviert ist. Legen Sie diesen Wert auf 1 fest, um den Anbieter zu aktivieren. Um den Anbieter zu deaktivieren, legen Sie diesen Wert auf 0 fest. Die Standardeinstellung ist 0.</td>
</tr>
<tr class="even">
<td><strong>Enableflags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Vom Anbieter definierter Wert, der die Klasse der Ereignisse angibt, für die der Anbieter Ereignisse generiert. Weitere Informationen finden Sie unter dem <em>enableflags</em> -Parameter der <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> -Funktion. Geben Sie diesen Wert Namen an, wenn der Anbieter kein <strong>matchanykeyword</strong> oder <strong>matchallkeyword</strong>unterstützt.</td>
</tr>
<tr class="odd">
<td><strong>Enablelevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Anbieter definierter Wert, der die Detailebene angibt, die im Ereignis enthalten ist. Beispielsweise können Sie diesen Wert verwenden, um den Schweregrad der Ereignisse (Information, Warnung, Fehler) anzugeben, die vom Anbieter generiert werden. Eine Liste der vordefinierten Ebenen finden Sie unter dem <em>Level</em> -Parameter der Funktion <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>enabletraceex</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>Enableproperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Verwenden Sie diesen Wert, um ein oder mehrere der folgenden Elemente in die Protokolldatei einzubeziehen:
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = include in den erweiterten Daten die Sicherheits-ID (SID) des Benutzers.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = include in den erweiterten Daten den Bezeichner der Terminalsitzung.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = include in den erweiterten Daten eine aufrufsstapel-Ablauf Verfolgung für Ereignisse, die mithilfe von <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>geschrieben wurden.</li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtert alle Ereignisse heraus, für die kein Schlüsselwort ungleich 0 (null) angegeben ist.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = gibt an, dass dieser <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> -Aufrufe eine <a href="provider-traits.md">Anbieter Gruppe</a> anstelle eines einzelnen Ereignis Anbieters aktivieren soll.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = schließt den Prozess Start Schlüssel in die erweiterten Daten ein.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = schließt den Ereignis Schlüssel in die erweiterten Daten ein.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtert alle Ereignisse heraus, die entweder als InPrivate-Ereignis gekennzeichnet sind oder von einem Prozess stammen, der als InPrivate markiert ist.</li>
</ul>
Weitere Informationen zu diesen Elementen finden Sie unter <strong>enableproperty (enableproperty</strong> ) der <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> -Struktur.<br/></td>
</tr>
<tr class="odd">
<td><strong>Matchanykeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Bitmaske von Schlüsselwörtern, die die Kategorie der Ereignisse bestimmen, die der Anbieter schreiben soll. Der Anbieter schreibt das Ereignis, wenn eines der Schlüsselwort Bits eines Ereignisses mit einer der in dieser Maske festgelegten Bits identisch ist. Um anzugeben, dass der Anbieter alle Ereignisse schreibt, legen Sie diesen Wert auf 0 (null) fest. Ein Beispiel finden Sie im Abschnitt "Hinweise" der Funktion " <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>enabletraceex</strong></a> ".</td>
</tr>
<tr class="even">
<td><strong>Matchallschlüsselwort</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Diese Bitmaske ist optional. Diese Maske schränkt die Kategorie der Ereignisse ein, die der Anbieter schreiben soll. Wenn das Schlüsselwort des Ereignisses die <em>matchanykeyword</em> -Bedingung erfüllt, schreibt der Anbieter das Ereignis nur dann, wenn alle Bits in dieser Maske im Schlüsselwort des Ereignisses vorhanden sind. Diese Maske wird nicht verwendet, wenn <em>matchanykeyword</em> gleich 0 (null) ist. Ein Beispiel finden Sie im Abschnitt "Hinweise" der Funktion " <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>enabletraceex</strong></a> ".</td>
</tr>
</tbody>
</table>



 

Nachdem die Registrierung geändert wurde, wird die autologger-Sitzung beim nächsten Neustart des Computers gestartet. Die autologger-Sitzung ruft die [**enabletraceex**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) -Funktion auf, um die Anbieter zu aktivieren.

Die autologger-Sitzungen erhöhen die Systemstart Zeit und sollten sparsam verwendet werden. Dienste, die während des Startvorgangs Informationen erfassen möchten, sollten in Erwägung gezogen werden, anstelle der autologger-Sitzung selbst Controller Logik hinzuzufügen.

Um eine autologger-Sitzung zu beenden, wenden Sie die [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Funktion an. Der Sitzungsname, den Sie an die Funktion übergeben, ist der Name des Registrierungsschlüssels, den Sie zum Definieren der Sitzung in der Registrierung verwendet haben.

Unter Windows 8.1 können Windows Server 2012 R2 und höhere Ereignis Nutz Last-, Bereichs-und Stapel Durchlauf Filter von der [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion und den [**\_ \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) -Strukturen zum Aktivieren von Ablauf [**\_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und Ereignis Filtern verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungs Sitzung zu filtern. Weitere Informationen zu Ereignis Nutz Last Filtern finden Sie unter den Funktionen " [**tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)" und " [**tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) " und " **enable \_ Trace \_ Parameters**", **Ereignis \_ Filter \_ Deskriptor** und [**Payload \_ Filter \_ Predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) Structures.

Weitere Informationen zum Starten einer Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).

Weitere Informationen zum Starten einer privaten Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten einer Sitzung für private](configuring-and-starting-a-private-logger-session.md)Protokollierung.

Weitere Informationen zum Starten einer NT-Kernel Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer Sitzung für private Logger](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer systemtraceprovider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Aktivieren von Ablauf \_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**Ereignis \_ Filter \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**Nutz Last \_ Filter- \_ Prädikat**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**Tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**Tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung](updating-an-event-tracing-session.md)
</dt> </dl>
