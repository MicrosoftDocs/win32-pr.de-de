---
description: Die Global Logger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die zu einem frühen Teil des Startprozesses des Betriebssystems auftreten.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Konfigurieren und Starten der globalen Protokollierungssitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc15ad9fdb5150a976b9d7bccfb6315649617271c5ece2a7c676fbdb9f6f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395495"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Konfigurieren und Starten der globalen Protokollierungssitzung

Die Global Logger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die zu einem frühen Teil des Startprozesses des Betriebssystems auftreten. Anwendungen und Gerätetreiber können die Global Logger-Sitzung verwenden, um Ablaufverfolgungen zu erfassen, bevor sich der Benutzer anmeldet. Beachten Sie, dass einige Gerätetreiber, z. B. Datenträgergerätetreiber, zum Zeitpunkt des Beginns der Globalen Protokollierungssitzung nicht geladen werden.

> [!Note]  
> Wenn Sie eine globale Protokollierungssitzung auf Windows Vista erstellen, sollten Sie stattdessen eine [AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md) erstellen.

 

Sie verwenden die Registrierung, um die Globale Protokollierungssitzung zu konfigurieren. Fügen Sie den **GlobalLogger-Schlüssel** dem folgenden Registrierungsschlüssel hinzu, sofern er noch nicht vorhanden ist:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

In der folgenden Tabelle werden die Werte beschrieben, die Sie für den **GlobalLogger-Schlüssel** definieren können. Sie müssen über Administratorrechte verfügen, um diese Registrierungswerte anzugeben. Die Registrierungswerte wirken sich auf alle Anbieter aus, die Ereignisse in der Globalen Protokollierungssitzung protokollieren. Der **Startwert** ist der einzige Wert, der zum Starten der globalen Protokollierungssitzung erforderlich ist. alle anderen Werte verfügen über Standardeinstellungen, die verwendet werden, wenn der Wert nicht in der Registrierung vorhanden ist. In der Regel sollten Sie die Standardwerte verwenden. Wenn Sie einen Wert angeben, der von ETW nicht unterstützt werden kann, überschreibt ETW den Wert.



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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Starten</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Legen Sie diesen Wert auf 1 (ein) fest, um die Globale Protokollierungssitzung beim nächsten Start des Systems zu starten. Um das Starten der Sitzung zu beenden, legen Sie diesen Wert auf 0 (aus) fest. <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Größe jedes Puffers in Kilobyte. Dieser Wert sollte kleiner als ein Megabyte sein. ETW verwendet die Größe des physischen Arbeitsspeichers, um diesen Wert zu berechnen. <br/></td>
</tr>
<tr class="odd">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Der Timer, der beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll.
<ul>
<li>1 = Leistungsindikatorwert (hohe Auflösung)</li>
<li>2 = Systemtimer</li>
<li>3 = CPU-Zykluszähler</li>
</ul>
Eine Beschreibung der einzelnen Uhrtypen finden Sie im <strong>ClientContext-Member</strong> von <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> Der Standardwert ist 1 (Leistungsindikatorwert) für Windows Vista und höher. Vor Windows Vista ist der Standardwert 2 (Systemtimer).<br/></td>
</tr>
<tr class="even">
<td><strong>EnableKernelFlags</strong></td>
<td><strong>REG_BINARY</strong></td>
<td>Verwenden Sie diesen Wert, um einen oder mehrere Kernelanbieter zu aktivieren. Wenn Sie Kernelanbieter aktivieren, benennt sich die Globale Protokollierungssitzung beim Start in NT Kernel Logger um. Mögliche Werte finden Sie im <strong>EnableFlags-Member</strong> von <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Anzahl der Ereignisablaufverfolgungsprotokolldateien, die von Globalen Protokollierungssitzungen generiert werden. Das System erhöht diesen Wert, bis er den Wert von <strong>FileMax</strong>erreicht. Anschließend wird der Wert auf 0 zurückgesetzt. Dieser Leistungsindikator verhindert, dass das System eine Global Logger-Ablaufverfolgungsprotokolldatei überschreibt. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl von Ereignisablaufverfolgungsprotokolldateien, die auf dem System zulässig sind. Wenn die Anzahl der Ablaufverfolgungsprotokolle den angegebenen Höchstwert erreicht, beginnt das System mit dem Überschreiben der Protokolle, beginnend mit dem ältesten Protokoll. <br/> Wenn die in <strong>FileName</strong> angegebene Protokolldatei vorhanden ist, fügt ETW den <strong>FileCounter-Wert</strong> an den Dateinamen an. Wenn beispielsweise der Standardprotokolldateiname verwendet wird, lautet das Formular %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNNN. <br/> Der Standardwert ist 0, was bedeutet, dass kein Maximum vorhanden ist. <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Der vollqualifizierte Pfad der Protokolldatei. Der Pfad zu dieser Datei muss vorhanden sein. Die Protokolldatei ist eine sequenzielle Protokolldatei. Beachten Sie, dass alle Anbieter, die Ereignisse in die Global Logger-Sitzung schreiben, Ereignisse in diese Protokolldatei schreiben. Der Pfad ist auf 1024 Zeichen beschränkt. Wenn <strong>FileName</strong> nicht angegeben ist, werden Ereignisse in %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl geschrieben. <strong>Vor Windows Vista:</strong> Die Standarddatei ist %SystemRoot%\System32\LogFiles\WMI\Trace.log.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Gibt an, wie oft die Ablaufverfolgungspuffer in Sekunden zwangsmäßig geleert werden. Die mindeste Leerungszeit beträgt 1 Sekunde. Diese erzwungene Leerung erfolgt zusätzlich zur automatischen Leerung, die auftritt, wenn ein Puffer voll ist und die Ablaufverfolgungssitzung beendet wird. <br/> Bei einer Echtzeitprotokollierung bedeutet der Wert 0 (Standardwert) , dass die Leerungszeit auf 1 Sekunde festgelegt wird. Eine Echtzeitprotokollierung ist , wenn <strong>LogFileMode</strong> auf <strong>EVENT_TRACE_REAL_TIME_MODE</strong>festgelegt ist.<br/> Der Standardwert ist 0. Standardmäßig werden Puffer nur geleert, wenn sie voll sind. <br/></td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Gibt Protokollsitzungsoptionen an. Werte finden Sie unter <a href="logging-mode-constants.md">Protokollierungsmoduskonstanten.</a> Diese Werte werden ab Windows Vista unterstützt. <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl der zuzuordnenden Puffer. In der Regel entspricht dieser Wert der Mindestanzahl von Puffern plus 20. ETW verwendet die Puffergröße und die Größe des physischen Arbeitsspeichers, um diesen Wert zu berechnen. Dieser Wert muss größer oder gleich dem Wert für <strong>MinimumBuffers</strong>sein.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Größe der Ereignisablaufverfolgungsprotokolldatei in Megabyte. Standardmäßig gibt es keine maximale Dateigröße.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Mindestanzahl von Puffern, die beim Start der Globalen Protokollierungssitzung zugeordnet werden sollen. Die Mindestanzahl von Puffern, die Sie angeben können, beträgt zwei Puffer pro Prozessor. Auf einem einzelnen Prozessorcomputer beträgt die Mindestanzahl von Puffern beispielsweise zwei. <br/> Der Standardwert für ein Einzelprozessorsystem ist 0x3.<br/></td>
</tr>
<tr class="odd">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Der Startstatus der globalen Protokollierung. Wenn die globale Protokollierung nicht gestartet werden konnte, ist der Wert dieses Schlüssels der entsprechende Win32-Fehlercode. Wenn die globale Protokollierung erfolgreich gestartet wurde, lautet der Wert dieses Schlüssels ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Nachdem die Registrierung geändert und der Computer neu gestartet wurde, wird die Global Logger-Sitzung automatisch gestartet und wie jede andere Sitzung mit einer Ausnahme verwendet: Sie verwenden das konstanten Handle WMI \_ GLOBAL \_ LOGGER \_ ID (definiert in Wmistr.h), um auf die globale Protokollierungssitzung zu verweisen. Diese Konstante kann als Argument für jede Ereignisablaufverfolgungsfunktion verwendet werden, die ein Sitzungshandle akzeptiert. Verwenden Sie in Funktionen, die einen Sitzungsnamen akzeptieren, GLOBAL \_ LOGGER \_ NAME.

Der globale Protokollierungscontroller aufruft die [**EnableTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) nicht, um Anbieter zu aktivieren. Der Anbieter ist dafür verantwortlich, zu bestimmen, ob die globale Protokollierungssitzung gestartet wird, und sich dann selbst zu aktivieren.

Um zu ermitteln, ob die globale Protokollierungssitzung gestartet wird, können Sie die [**ControlTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-controltracea) aufrufen und *SessionHandle* auf WMI GLOBAL LOGGER ID und ControlCode auf \_ EVENT TRACE CONTROL QUERY \_ \_ **\_ \_ \_ festlegen.**  Wenn der **ControlTrace-Aufruf** erfolgreich ist, ist die Globale Protokollierungssitzung vorhanden, und der Anbieter kann sich selbst aktivieren und Ereignisse in der globalen Protokollierungssitzung protokollieren (die **ControlTrace-Funktion** gibt ERROR WMI INSTANCE NOT FOUND zurück, wenn die globale Protokollierung nicht aktiv \_ \_ \_ \_ ist).

In der Regel ist der Controller dafür verantwortlich, die Aktivierungsflags und die Ebene an den Anbieter zu übergeben, wenn er den Anbieter aktiviert. Da der globale Protokollierungscontroller den Anbieter jedoch nicht aktiviert, liegt es in der Verantwortung des Anbieters, diese Informationen bei Bedarf an sich selbst zu übergeben.

Die Globale Protokollierungssitzung ist eine begrenzte Ressource und sollte nur wenig verwendet werden. Dienste, die Informationen während des Startprozesses erfassen möchten, sollten erwägen, sich selbst Controllerlogik hinzufügen, anstatt die Globale Protokollierungssitzung zu verwenden.

Weitere Informationen zum Starten einer Ereignisablaufverfolgungssitzung finden Sie unter Konfigurieren und [Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

Weitere Informationen zum Starten einer privaten Protokollierungssitzung finden Sie unter Konfigurieren und [Starten einer privaten Protokollierungssitzung.](configuring-and-starting-a-private-logger-session.md)

Weitere Informationen zum Starten einer NT-Kernelprotokollierungssitzung finden Sie unter Konfigurieren und [Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)

