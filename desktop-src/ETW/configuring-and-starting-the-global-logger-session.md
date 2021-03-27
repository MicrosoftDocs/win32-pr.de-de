---
description: Die Ereignis Ablauf Verfolgungs Sitzung für globale Protokollierung zeichnet Ereignisse auf, die früh im Betriebssystem-Startprozess auftreten.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Konfigurieren und Starten der globalen Protokollierungs Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8692e1f7321acc163e48cda7e3323f3d24adc1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980121"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Konfigurieren und Starten der globalen Protokollierungs Sitzung

Die Ereignis Ablauf Verfolgungs Sitzung für globale Protokollierung zeichnet Ereignisse auf, die früh im Betriebssystem-Startprozess auftreten. Anwendungen und Gerätetreiber können mithilfe der globalen Protokollierungs Sitzung Ablauf Verfolgungen erfassen, bevor sich der Benutzer anmeldet. Beachten Sie, dass einige Gerätetreiber, z. b. Datenträger-Gerätetreiber, nicht zum Zeitpunkt der globalen Protokollierungs Sitzung geladen werden.

> [!Note]  
> Wenn Sie eine globale Protokollierungs Sitzung unter Windows Vista erstellen, sollten Sie stattdessen eine [autologger-Sitzung](configuring-and-starting-an-autologger-session.md) erstellen.

 

Sie verwenden die Registrierung, um die globale Protokollierungs Sitzung zu konfigurieren. Fügen Sie den **globallogger** -Schlüssel dem folgenden Registrierungsschlüssel hinzu, wenn er nicht bereits vorhanden ist:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

In der folgenden Tabelle werden die Werte beschrieben, die Sie für den Schlüssel **Global Logger** definieren können. Sie müssen über Administratorrechte verfügen, um diese Registrierungs Werte angeben zu können. Die Registrierungs Werte wirken sich auf alle Anbieter aus, von denen Ereignisse in der globalen Protokollierungs Sitzung protokolliert werden. Der **Startwert** ist der einzige Wert, der zum Starten der globalen Protokollierungs Sitzung erforderlich ist. alle anderen Werte haben Standardeinstellungen, die verwendet werden, wenn der Wert nicht in der Registrierung vorhanden ist. Normalerweise sollten Sie die Standardwerte verwenden. Wenn Sie einen Wert angeben, der von etw nicht unterstützt werden kann, wird der Wert von etw überschrieben.



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
<td>Legen Sie diesen Wert auf 1 (ein) fest, um die globale Protokollierungs Sitzung beim nächsten Start des Systems zu starten. Um den Start der Sitzung zu beenden, legen Sie diesen Wert auf 0 (aus) fest. <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Größe der einzelnen Puffer in Kilobyte. Dieser Wert muss kleiner als 1 MB sein. Etw verwendet die Größe des physischen Speichers, um diesen Wert zu berechnen. <br/></td>
</tr>
<tr class="odd">
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
<tr class="even">
<td><strong>Enablekernelflags</strong></td>
<td><strong>REG_BINARY</strong></td>
<td>Verwenden Sie diesen Wert, um einen oder mehrere Kernel Anbieter zu aktivieren. Wenn Sie Kernel Anbieter aktivieren, benennt sich die globale Protokollierungs Sitzung beim Starten in NT Kernel Logger um. Mögliche Werte finden Sie unter dem <strong>enableflags</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>File Counter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die Anzahl der Ereignis Ablauf Verfolgungs Protokoll-Dateien, die von globalen Protokollierungs Sitzungen generiert werden. Das System erhöht diesen Wert, bis er den Wert von <strong>filemax</strong>erreicht. Anschließend wird der Wert auf 0 zurückgesetzt. Dieser Wert verhindert, dass das System eine Ablauf Verfolgungs Protokolldatei für die globale Protokollierung überschreibt. <br/></td>
</tr>
<tr class="even">
<td><strong>Filemax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl von Ereignis Ablauf Verfolgungs Protokoll-Dateien, die im System zulässig sind. Wenn die Anzahl der Ablauf Verfolgungs Protokolle den angegebenen maximalen Wert erreicht, beginnt das System mit dem Überschreiben der Protokolle, beginnend mit dem ältesten. <br/> Wenn die in <strong>filename</strong> angegebene Protokolldatei vorhanden ist, fügt ETW den <strong>filecounter</strong> -Wert an den Dateinamen an. Wenn z. b. der Standardname der Protokolldatei verwendet wird, lautet das Formular%systemroot%\System32\LogFiles\WMI\GlobalLogger.ETL.nnnn. <br/> Der Standardwert ist 0, was bedeutet, dass kein Maximum vorhanden ist. <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Der voll qualifizierte Pfad der Protokolldatei. Der Pfad zu dieser Datei muss vorhanden sein. Die Protokolldatei ist eine sequenzielle Protokolldatei. Beachten Sie, dass alle Anbieter, die Ereignisse in die globale Protokollierungs Sitzung schreiben, Ereignisse in diese Protokolldatei schreiben. Der Pfad ist auf 1024 Zeichen beschränkt. Wenn <strong>filename</strong> nicht angegeben wird, werden die Ereignisse in%SystemRoot%\system32\logfiles\wmi\globallogger.ETL geschrieben. <strong>Vor Windows Vista:</strong> Die Standarddatei ist%SystemRoot%\system32\logfiles\wmi\trace.log.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>Flushtimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Gibt an, wie oft die Ablauf Verfolgungs Puffer in Sekunden erzwungen werden. Die minimale Leerungs Zeit beträgt 1 Sekunde. Dieser erzwungene Löschvorgang erfolgt zusätzlich zu dem automatischen leeren, der auftritt, wenn ein Puffer voll ist und die Ablauf Verfolgungs Sitzung beendet wird. <br/> Bei einer echt Zeit Protokollierung bedeutet der Wert 0 (null) (der Standardwert), dass die Leerungs Zeit auf 1 Sekunde festgelegt wird. Eine echt Zeit Protokollierung ist, wenn <strong>logfilemode</strong> auf <strong>EVENT_TRACE_REAL_TIME_MODE</strong>festgelegt ist.<br/> Der Standardwert ist 0. Standardmäßig werden Puffer nur geleert, wenn Sie voll sind. <br/></td>
</tr>
<tr class="odd">
<td><strong>Logfilemode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Gibt Protokoll Sitzungs Optionen an. Informationen zu-Werten finden Sie unter <a href="logging-mode-constants.md">Protokollierungs Modus Konstanten</a>. Diese Werte werden unter Windows Vista und höher unterstützt. <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Anzahl der zuzuordnenden Puffer. In der Regel ist dieser Wert die minimale Anzahl von Puffern plus 20. Etw verwendet die Puffergröße und die Größe des physischen Speichers, um diesen Wert zu berechnen. Dieser Wert muss größer oder gleich dem Wert für <strong>minimumbuffers</strong>sein.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die maximale Größe der Ereignis Ablauf Verfolgungs Protokoll-Datei in Megabyte. Standardmäßig gibt es keine maximale Dateigröße.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Die minimale Anzahl von Puffern, die beim Start der globalen Protokollierungs Sitzung zuzuordnen sind. Die Mindestanzahl an Puffern, die Sie angeben können, sind zwei Puffer pro Prozessor. Beispielsweise ist auf einem Computer mit einem einzelnen Prozessor die Mindestanzahl an Puffern auf zwei. <br/> Der Standardwert für ein Einzel Prozessor System ist 0x3.<br/></td>
</tr>
<tr class="odd">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Der Startstatus der globalen Protokollierung. Wenn die globale Protokollierung nicht gestartet werden konnte, ist der Wert dieses Schlüssels der entsprechende Win32-Fehlercode. Wenn die globale Protokollierung erfolgreich gestartet wurde, ist der Wert dieses Schlüssels ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Nachdem die Registrierung geändert und der Computer neu gestartet wurde, wird die globale Protokollierungs Sitzung automatisch gestartet und wie jede andere Sitzung mit einer Ausnahme verwendet: Sie verwenden den konstanten Handle der WMI \_ Global \_ Logger \_ ID (definiert in wmistr. h), um auf die globale Protokollierungs Sitzung zu verweisen. Diese Konstante kann als Argument für jede Ereignis Ablauf Verfolgungs Funktion verwendet werden, die ein Sitzungs handle akzeptiert. Verwenden Sie in Funktionen, die einen Sitzungs Namen akzeptieren, den Namen der globalen Protokollierung \_ \_ .

Der globale Logger-Controller ruft die [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) -Funktion nicht auf, um Anbieter zu aktivieren. Der Anbieter ist dafür verantwortlich, zu bestimmen, ob die globale Protokollierungs Sitzung gestartet wurde und sich dann selbst aktiviert.

Um zu ermitteln, ob die globale Protokollierungs Sitzung gestartet wurde, können Sie die [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Funktion, die *SessionHandle* \_ -ID und die globale WMI-Protokollierungs \_ \_ -ID und *ControlCode* auf die Query-Ablauf **\_ Verfolgungs \_ \_ Abfrage** festlegen. Wenn der **controltrace** -Befehl erfolgreich ausgeführt wurde, ist die globale Protokollierungs Sitzung vorhanden, und der Anbieter kann sich selbst aktivieren und Ereignisse in der globalen Protokollierungs Sitzung protokollieren (die **controltrace** -Funktion gibt den Fehler zurück, \_ \_ \_ \_ Wenn die globale Protokollierung nicht aktiv ist).

In der Regel ist der Controller dafür zuständig, die Aktivierungsflags und die Ebene an den Anbieter zu übergeben, wenn er den Anbieter aktiviert, aber da der globale Protokollierungs Controller den Anbieter nicht aktiviert, ist es die Aufgabe des Anbieters, diese Informationen bei Bedarf an sich selbst zu übergeben.

Die globale Protokollierungs Sitzung ist eine begrenzte Ressource und sollte sparsam verwendet werden. Dienste, die während des Startvorgangs Informationen erfassen möchten, sollten in Erwägung gezogen werden, anstelle der globalen Protokollierungs Sitzung selbst Controller Logik hinzuzufügen.

Weitere Informationen zum Starten einer Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).

Weitere Informationen zum Starten einer privaten Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten einer Sitzung für private](configuring-and-starting-a-private-logger-session.md)Protokollierung.

Weitere Informationen zum Starten einer NT-Kernel Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md).

