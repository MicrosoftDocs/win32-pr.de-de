---
description: 'Das Ereignisprotokoll enthält die folgenden Standardprotokolle sowie benutzerdefinierte Protokolle:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Eventlog-Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b60a2a935267ddeed52a82602c1192ff23d7005
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477806"
---
# <a name="eventlog-key"></a>Eventlog-Schlüssel

Das Ereignisprotokoll enthält die folgenden Standardprotokolle sowie benutzerdefinierte Protokolle:



| Log             | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anwendung** | Enthält Ereignisse, die von Anwendungen protokolliert werden. Beispielsweise kann eine Datenbankanwendung einen Dateifehler aufzeichnen. Der Anwendungsentwickler entscheidet, welche Ereignisse aufzeichnen werden.                                                                             |
| **Security**    | Enthält Ereignisse wie gültige und ungültige Anmeldeversuche sowie Ereignisse im Zusammenhang mit der Ressourcennutzung wie das Erstellen, Öffnen oder Löschen von Dateien oder anderen Objekten. Ein Administrator kann die Überwachung starten, um Ereignisse im Sicherheitsprotokoll zu erfassen. |
| **System**      | Enthält Ereignisse, die von Systemkomponenten protokolliert werden, z. B. der Fehler beim Laden eines Treibers oder einer anderen Systemkomponente während des Starts.                                                                                                               |
| *CustomLog*     | Enthält Ereignisse, die von Anwendungen protokolliert werden, die ein benutzerdefiniertes Protokoll erstellen. Mithilfe eines benutzerdefinierten Protokolls kann eine Anwendung die Größe des Protokolls steuern oder ACLs zu Sicherheitszwecken anfügen, ohne dass andere Anwendungen betroffen sind.                         |



 

Der Ereignisprotokollierungsdienst verwendet die im **Registrierungsschlüssel Eventlog gespeicherten** Informationen. Der **Eventlog-Schlüssel** enthält mehrere Unterschlüssel, die als *Protokolle bezeichnet werden.* Jedes Protokoll enthält Informationen, die der Ereignisprotokollierungsdienst verwendet, um Ressourcen zu suchen, wenn eine Anwendung in das Ereignisprotokoll schreibt und daraus liest.

Die Struktur des **Eventlog-Schlüssels** lautet wie folgt:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            Eventlog
               Application
               Security
               System
               CustomLog
```

Beachten Sie, dass Domänencontroller Ereignisse  im **Verzeichnisdienst** und im Dateireplikationsdienst protokollieren und DNS-Server Ereignisse im **DNS-Server aufzeichnen.**

Jedes Protokoll kann die folgenden Registrierungswerte enthalten.




| Registrierungswert | BESCHREIBUNG | 
|----------------|-------------|
| <strong>CustomSD</strong> | Schränkt den Zugriff auf das Ereignisprotokoll ein. Dieser Wert ist vom Typ REG_SZ. Das verwendete Format ist <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL). Erstellen Sie eine ACL, die mindestens eines der folgenden Rechte gewährt:<dl> Löschen (0x0004)<br />Lesen (0x0001)<br />Schreiben (0x0002)<br /></dl> Um eine syntaktisch gültige SDDL zu sein, muss der CustomSD-Wert einen Besitzer und einen Gruppenbesitzer (z. B. O:BAG:SY) angeben, aber der Besitzer und der Gruppenbesitzer werden nicht verwendet. Wenn CustomSD auf einen falschen Wert festgelegt ist, wird beim Starten des Ereignisprotokolldiensts ein Ereignis im Systemereignisprotokoll ausgelöst, und das Ereignisprotokoll ruft einen Standardsicherheitsdeskriptor ab, der mit dem ursprünglichen CustomSD-Wert für das Anwendungsprotokoll identisch ist. SACLs werden nicht unterstützt.<br /> Weitere Informationen finden Sie unter <a href="event-logging-security.md">Ereignisprotokollierungssicherheit.</a><br /><strong>Windows Server 2003:</strong> SACLs werden unterstützt.<br /><strong>Windows XP/2000:</strong> Dieser Wert wird nicht unterstützt.<br /><br /> | 
| <strong>DisplayNameFile</strong> | Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Name der Datei, in der der lokalisierte Name des Ereignisprotokolls gespeichert wird. Der in dieser Datei gespeicherte Name wird als Protokollname in Ereignisanzeige. Wenn dieser Eintrag nicht in der Registrierung für ein Ereignisprotokoll angezeigt wird, Ereignisanzeige den Namen des Registrierungsunterschlüssels als Protokollnamen an. Dieser Wert ist vom Typ REG_EXPAND_SZ. Der Standardwert ist %SystemRoot%\system32\els.dll.<br /> | 
| <strong>DisplayNameID</strong> | Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Meldungs-ID der Protokollnamenzeichenfolge. Diese Zahl gibt die Meldung an, in der der lokalisierte Anzeigename angezeigt wird. Die Meldung wird in der Datei gespeichert, die durch den <strong>DisplayNameFile-Wert angegeben</strong> wird. Dieser Wert ist vom Typ REG_DWORD.<br /> | 
| <strong>File</strong> | Vollqualifizierter Pfad zu der Datei, in der jedes Ereignisprotokoll gespeichert wird. Dies ermöglicht Ereignisanzeige und anderen Anwendungen, die Protokolldateien zu finden. Dieser Wert ist vom Typ REG_SZ oder REG_EXPAND_SZ. Dieser Wert ist optional. Wenn der Wert nicht angegeben wird, wird standardmäßig %SystemRoot%\system32\winevt\logs\ gefolgt von einem Dateinamen verwendet, der auf dem Namen des Registrierungsschlüssels des Ereignisprotokolls basiert. Der spezifische Pfad der Ereignisprotokolldatei sollte mit dem Befehlszeilenprogramm wevtutil.exe oder mithilfe der <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty-Funktion</strong></a> festgelegt werden, bei der EvtChannelLoggingConfigLogFilePath an den <em>PropertyId-Parameter</em> übergeben wird.<br /> Wenn eine bestimmte Datei festgelegt ist, stellen Sie sicher, dass der Ereignisprotokolldienst über vollständige Berechtigungen für die Datei verfügt.<br /> Dieser Wert muss ein gültiger Dateiname für eine Datei sein, die sich in einem lokalen Verzeichnis befindet (kein Remotecomputer, kein DOS-Gerät, keine Diskette und keine Pipe). Wenn die Dateieinstellung falsch ist, wird beim Starten des Ereignisprotokolldiensts ein Ereignis im Systemereignisprotokoll ausgelöst.<br /> Verwenden Sie keine Umgebungsvariablen im Pfad zur Datei, die im Kontext des Ereignisprotokolldiensts nicht erweitert werden können.<br /><strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist standardmäßig auf %SystemRoot%\system32\config\ gefolgt von einem Dateinamen festgelegt, der auf dem Namen des Registrierungsschlüssels des Ereignisprotokolls basiert. Wenn die Einstellung Datei auf einen ungültigen Wert festgelegt ist, wird das Protokoll entweder nicht ordnungsgemäß initialisiert, oder alle Anforderungen werden im Hintergrund zum Standardprotokoll (Anwendung) wechseln.<br /> | 
| <strong>Maxsize</strong> | Maximale Größe der Protokolldatei in Bytes. Dieser Wert ist vom Typ REG_DWORD. Der Wert muss für ein System-, Anwendungs- oder Sicherheitsprotokoll auf ein Vielfaches von 64.000 festgelegt werden. Der Standardwert ist 1 MB. <strong>Windows Server 2003 und Windows XP/2000:</strong> Der Wert ist auf 0xFFFFFFFF beschränkt, und der Standardwert ist 512.000.<br /> | 
| <strong>PrimaryModule</strong> | Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist der Name des Unterschlüssels, der die Standardwerte für die Einträge im Unterschlüssel für die Ereignisquelle enthält. Dieser Wert ist vom Typ REG_SZ.<br /> | 
| <strong>Vermerkdauer</strong> | Dieser Wert ist vom Typ REG_DWORD. Der Standardwert ist 0. Wenn dieser Wert 0 ist, werden die Datensätze von Ereignissen immer überschrieben. Wenn dieser Wert 0xFFFFFFFF oder ein Wert ungleich 0 ist, werden Datensätze nie überschrieben. Wenn die Protokolldatei ihre maximale Größe erreicht, müssen Sie das Protokoll manuell löschen. Andernfalls werden neue Ereignisse verworfen. Sie müssen das Protokoll auch löschen, bevor Sie seine Größe ändern können. <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist das Zeitintervall in Sekunden, in dem Datensätze von Ereignissen vor dem Überschreiben geschützt sind. Wenn das Alter eines Ereignisses diesen Wert erreicht oder überschreitet, kann es überschrieben werden.<br /> | 
| <strong>Sources</strong> | Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Namen der Anwendungen, Dienste oder Gruppen von Anwendungen, die Ereignisse in dieses Protokoll schreiben. Dieser Wert sollte nur gelesen und nicht geändert werden. Der Ereignisprotokolldienst verwaltet die Liste basierend auf jedem Programm, das in einem Unterschlüssel unter dem Protokoll aufgeführt ist. Dieser Wert ist vom Typ REG_MULTI_SZ.<br /> | 
| <strong>AutoBackupLogFiles</strong> | Dieser Wert ist vom Typ REG_DWORD und wird vom Ereignisprotokolldienst verwendet, um zu bestimmen, ob ein Ereignisprotokoll automatisch gespeichert werden soll. Der Standardwert ist 0, wodurch die automatische Sicherung deaktiviert wird. Der Dienst wird die Protokolldatei nur sichern, wenn der Aufbewahrungswert -1 (0xFFFFFFFF. Andere Werte werden ignoriert. <strong>Windows Server 2003:</strong> Die Aufbewahrungsdauer kann auf -1 (0xFFFFFFFF) oder 1 (0x00000001) festgelegt werden, damit AutoBackupLogFiles funktioniert. Andere Werte werden ignoriert.<br /> | 
| <strong>RestrictGuestAccess</strong> | Dieser Wert wird nicht verwendet. <strong>Windows XP/2000:</strong> Dieser Wert ist vom Typ REG_DWORD, und der Standardwert ist 1. Wenn der Wert auf 1 festgelegt ist, schränkt er den Zugriff des Gastkontos und des anonymen Kontos auf das Ereignisprotokoll ein, und wenn dieser Wert 0 ist, wird gastkontozugriff auf das Ereignisprotokoll ermöglicht.<br /> | 
| <strong>Isolation</strong> | Definiert die Standardzugriffsberechtigungen für das Protokoll. Dieser Wert ist vom Typ REG_SZ. Sie können einen der folgenden Werte angeben:<ul><li><strong>Anwendung</strong></li><li><strong>System</strong></li><li><strong>Benutzerdefiniert</strong></li></ul>Die Standardisolation ist <strong>Application</strong>. Die Standardberechtigungen für <strong>die Anwendung</strong> sind (mitHILFE von SDDL dargestellt): <br /><pre class="syntax" data-space="preserve"><code>            L"O:BAG:SYD:"            L"(A;;0xf0007;;;SY)"                // local system               (read, write, clear)            L"(A;;0x7;;;BA)"                    // built-in admins            (read, write, clear)            L"(A;;0x7;;;SO)"                    // server operators           (read, write, clear)            L"(A;;0x3;;;IU)"                    // INTERACTIVE LOGON          (read, write)            L"(A;;0x3;;;SU)"                    // SERVICES LOGON             (read, write)            L"(A;;0x3;;;S-1-5-3)"               // BATCH LOGON                (read, write)            L"(A;;0x3;;;S-1-5-33)"              // write restricted service   (read, write)            L"(A;;0x1;;;S-1-5-32-573)";         // event log readers          (read) </code></pre>Die Standardberechtigungen für <strong>System</strong> sind (mit SDDL dargestellt): <br /><pre class="syntax" data-space="preserve"><code>            L"O:BAG:SYD:"            L"(A;;0xf0007;;;SY)"                // local system             (read, write, clear)            L"(A;;0x7;;;BA)"                    // built-in admins          (read, write, clear)            L"(A;;0x3;;;BO)"                    // backup operators         (read, write)            L"(A;;0x5;;;SO)"                    // server operators         (read, clear)             L"(A;;0x1;;;IU)"                    // INTERACTIVE LOGON        (read)            L"(A;;0x3;;;SU)"                    // SERVICES LOGON           (read, write)            L"(A;;0x1;;;S-1-5-3)"               // BATCH LOGON              (read)            L"(A;;0x2;;;S-1-5-33)"              // write restricted service (write)            L"(A;;0x1;;;S-1-5-32-573)";         // event log readers        (read)</code></pre>Die Standardberechtigungen für <strong>die benutzerdefinierte</strong> Isolation sind identisch mit application.<br /><strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist nicht verfügbar.<br /> | 




 

Jedes Protokoll enthält auch Ereignisquellen. Weitere Informationen finden Sie unter [Ereignisquellen.](event-sources.md)

