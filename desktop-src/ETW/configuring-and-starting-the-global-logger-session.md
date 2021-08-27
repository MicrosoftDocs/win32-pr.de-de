---
description: Die Global Logger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die früh im Startprozess des Betriebssystems auftreten.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Konfigurieren und Starten der globalen Protokollierungssitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a928cba5eb782ca4a57f7dba4776de79f42d7af
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477046"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Konfigurieren und Starten der globalen Protokollierungssitzung

Die Global Logger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die früh im Startprozess des Betriebssystems auftreten. Anwendungen und Gerätetreiber können die globale Protokollierungssitzung verwenden, um Ablaufverfolgungen zu erfassen, bevor sich der Benutzer anmeldet. Beachten Sie, dass einige Gerätetreiber, z. B. Datenträgergerätetreiber, zum Zeitpunkt des Beginns der Global Logger-Sitzung nicht geladen werden.

> [!Note]  
> Wenn Sie eine globale Protokollierungssitzung auf Windows Vista erstellen, sollten Sie stattdessen eine [AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md) erstellen.

 

Sie verwenden die Registrierung, um die Globale Protokollierungssitzung zu konfigurieren. Fügen Sie **den GlobalLogger-Schlüssel** dem folgenden Registrierungsschlüssel hinzu, falls er noch nicht vorhanden ist:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

In der folgenden Tabelle werden die Werte beschrieben, die Sie für den **GlobalLogger-Schlüssel definieren** können. Sie müssen über Administratorrechte verfügen, um diese Registrierungswerte anzugeben. Die Registrierungswerte wirken sich auf alle Anbieter aus, die Ereignisse in der Globalen Protokollierungssitzung protokollieren. Der **Startwert** ist der einzige Wert, der zum Starten der globalen Protokollierungssitzung erforderlich ist. Alle anderen Werte verfügen über Standardeinstellungen, die verwendet werden, wenn der Wert nicht in der Registrierung vorhanden ist. In der Regel sollten Sie die Standardwerte verwenden. Wenn Sie einen Wert angeben, der von ETW nicht unterstützt werden kann, überschreibt ETW den Wert.




| Wert | type | Beschreibung | 
|-------|------|-------------|
| <strong>Starten</strong> | <strong>REG_DWORD</strong> | Legen Sie diesen Wert auf 1 (ein) fest, um die globale Protokollierungssitzung beim nächsten Systemstart zu starten. Um zu verhindern, dass die Sitzung gestartet wird, legen Sie diesen Wert auf 0 (aus) fest. <br /> | 
| <strong>BufferSize</strong> | <strong>REG_DWORD</strong> | Die Größe der einzelnen Puffer in Kilobyte. Dieser Wert sollte kleiner als ein Megabyte sein. ETW verwendet die Größe des physischen Speichers, um diesen Wert zu berechnen. <br /> | 
| <strong>ClockType</strong> | <strong>REG_DWORD</strong> | Der Timer, der beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll.<ul><li>1 = Leistungsindikatorwert (hohe Auflösung)</li><li>2 = Systemzeiter</li><li>3 = CPU-Zykluszähler</li></ul>Eine Beschreibung der einzelnen Uhrtypen finden Sie unter dem <strong>ClientContext-Member</strong> von <a href="wnode-header.md"><strong>WNODE_HEADER.</strong></a><br /> Der Standardwert ist 1 (Leistungsindikatorwert) für Windows Vista und höher. Vor der Windows Vista ist der Standardwert 2 (Systemzeiter).<br /> | 
| <strong>EnableKernelFlags</strong> | <strong>REG_BINARY</strong> | Verwenden Sie diesen Wert, um einen oder mehrere Kernelanbieter zu aktivieren. Wenn Sie Kernelanbieter aktivieren, benennt sich die Globale Protokollierungssitzung beim Start in NT Kernel Logger um. Mögliche Werte finden Sie im <strong>EnableFlags-Member</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br /> | 
| <strong>FileCounter</strong> | <strong>REG_DWORD</strong> | Die Anzahl der Ereignisverfolgungsprotokolldateien, die von globalen Protokollierungssitzungen generiert werden. Das System erhöht diesen Wert, bis er den Wert von <strong>FileMax erreicht.</strong> Anschließend wird der Wert auf 0 zurückgesetzt. Dieser Leistungsindikator verhindert, dass das System eine Ablaufverfolgungsprotokolldatei der globalen Protokollierung überschreiben kann. <br /> | 
| <strong>FileMax</strong> | <strong>REG_DWORD</strong> | Die maximale Anzahl von Ereignisverfolgungsprotokolldateien, die auf dem System zulässig sind. Wenn die Anzahl der Ablaufverfolgungsprotokolle das angegebene Maximum erreicht, beginnt das System, die Protokolle zu überschreiben, beginnend mit dem ältesten Protokoll. <br /> Wenn die in <strong>FileName</strong> angegebene Protokolldatei vorhanden ist, fügt ETW den <strong>FileCounter-Wert</strong> an den Dateinamen an. Wenn beispielsweise der Standardprotokolldateiname verwendet wird, ist das Format %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br /> Der Standardwert ist 0, d. h., es gibt kein Maximum. <br /> | 
| <strong>FileName</strong> | <strong>REG_SZ</strong> | Vollqualifizierter Pfad der Protokolldatei. Der Pfad zu dieser Datei muss vorhanden sein. Die Protokolldatei ist eine sequenzielle Protokolldatei. Beachten Sie, dass alle Anbieter, die Ereignisse in die Globale Protokollierungssitzung schreiben, Ereignisse in diese Protokolldatei schreiben. Der Pfad ist auf 1024 Zeichen beschränkt. Wenn <strong>FileName nicht</strong> angegeben wird, werden Ereignisse in %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl geschrieben. <strong>Vor der Windows Vista:</strong> Die Standarddatei ist %SystemRoot%\System32\LogFiles\WMI\Trace.log.<br /><br /> | 
| <strong>FlushTimer</strong> | <strong>REG_DWORD</strong> | Gibt an, wie oft die Ablaufverfolgungspuffer in Sekunden erzürnt werden. Die minimale Leerungszeit beträgt 1 Sekunde. Diese erzwungene Leerung erfolgt zusätzlich zur automatischen Leerung, die auftritt, wenn ein Puffer voll ist und die Ablaufverfolgungssitzung beendet wird. <br /> Bei einer Echtzeitprotokollierung bedeutet der Wert 0 (Standardwert) , dass die Leerungszeit auf 1 Sekunde festgelegt wird. Eine Echtzeitprotokollierung ist , wenn <strong>LogFileMode</strong> auf <strong>EVENT_TRACE_REAL_TIME_MODE.</strong><br /> Der Standardwert ist 0. Standardmäßig werden Puffer nur geleert, wenn sie voll sind. <br /> | 
| <strong>LogFileMode</strong> | <strong>REG_DWORD</strong> | Gibt Protokollsitzungsoptionen an. Werte finden Sie unter <a href="logging-mode-constants.md">Konstanten für den Protokollierungsmodus.</a> Diese Werte werden auf Windows Vista und höher unterstützt. <br /> | 
| <strong>MaximumBuffers</strong> | <strong>REG_DWORD</strong> | Die maximale Anzahl der zu reservierenden Puffer. In der Regel ist dieser Wert die Mindestanzahl von Puffern plus 20. ETW verwendet die Puffergröße und die Größe des physischen Speichers, um diesen Wert zu berechnen. Dieser Wert muss größer oder gleich dem Wert für <strong>MinimumBuffers sein.</strong><br /> | 
| <strong>MaxFileSize</strong> | <strong>REG_DWORD</strong> | Die maximale Größe der Ereignisverfolgungsprotokolldatei in Megabyte. Standardmäßig gibt es keine maximale Dateigröße.<br /> | 
| <strong>MinimumBuffers</strong> | <strong>REG_DWORD</strong> | Die Mindestanzahl von Puffern, die beim Starten der globalen Protokollierungssitzung reserviert werden müssen. Die Mindestanzahl von Puffern, die Sie angeben können, beträgt zwei Puffer pro Prozessor. Auf einem einzelnen Prozessorcomputer beträgt die Mindestanzahl von Puffern beispielsweise zwei. <br /> Der Standardwert auf einem Einzelprozessorsystem ist 0x3.<br /> | 
| <strong>Status</strong> | <strong>REG_DWORD</strong> | Der Startstatus der globalen Protokollierung. Wenn die globale Protokollierung nicht gestartet werden konnte, ist der Wert dieses Schlüssels der entsprechende Win32-Fehlercode. Wenn die globale Protokollierung erfolgreich gestartet wurde, wird der Wert dieses Schlüssels ERROR_SUCCESS (0) angezeigt.<br /> | 




 

Nachdem die Registrierung geändert und der Computer neu gestartet wurde, wird die Globale Protokollierungssitzung automatisch gestartet und wie jede andere Sitzung mit einer Ausnahme verwendet: Sie verwenden das konstanten Handle der WMI \_ GLOBAL \_ LOGGER \_ ID (definiert in Wmistr.h), um auf die globale Protokollierungssitzung zu verweisen. Diese Konstante kann als Argument für jede Ereignisablaufverfolgungsfunktion verwendet werden, die ein Sitzungshand handle akzeptiert. Verwenden Sie in Funktionen, die einen Sitzungsnamen akzeptieren, GLOBAL \_ LOGGER \_ NAME.

Der Global Logger-Controller ruft die [**EnableTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) nicht auf, um Anbieter zu aktivieren. Der Anbieter ist dafür verantwortlich, zu bestimmen, ob die Globale Protokollierungssitzung gestartet und dann selbst aktiviert wird.

Um zu bestimmen, ob die Globale Protokollierungssitzung gestartet wird, können Sie die [**ControlTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-controltracea) aufrufen und *SessionHandle* auf WMI \_ GLOBAL \_ LOGGER \_ ID und *ControlCode* auf **EVENT TRACE CONTROL \_ \_ \_ QUERY** festlegen. Wenn der **ControlTrace-Aufruf** erfolgreich ist, ist die Globale Protokollierungssitzung vorhanden, und der Anbieter kann sich selbst aktivieren und Ereignisse in der globalen Protokollierungssitzung protokollieren (die **ControlTrace-Funktion** gibt ERROR \_ WMI \_ INSTANCE NOT FOUND \_ \_ zurück, wenn die globale Protokollierung nicht aktiv ist).

In der Regel ist der Controller für die Übergabe der Aktivierungsflags und der Ebene an den Anbieter verantwortlich, wenn er den Anbieter aktiviert. Da der globale Protokollierungscontroller den Anbieter jedoch nicht aktiviert, ist der Anbieter dafür verantwortlich, diese Informationen bei Bedarf an sich selbst zu übergeben.

Die Global Logger-Sitzung ist eine eingeschränkte Ressource und sollte nur selten verwendet werden. Dienste, die Informationen während des Startvorgangs erfassen möchten, sollten erwägen, sich selbst Controllerlogik hinzuzufügen, anstatt die Globale Protokollierungssitzung zu verwenden.

Ausführliche Informationen zum Starten einer Ereignisablaufverfolgungssitzung finden Sie unter [Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

Ausführliche Informationen zum Starten einer privaten Protokollierungssitzung finden Sie unter [Konfigurieren und Starten einer privaten Protokollierungssitzung.](configuring-and-starting-a-private-logger-session.md)

Ausführliche Informationen zum Starten einer NT-Kernelprotokollierungssitzung finden Sie unter [Konfigurieren und Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)

