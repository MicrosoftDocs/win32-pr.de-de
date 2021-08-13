---
description: 'Das Ereignisprotokoll enthält die folgenden Standardprotokolle sowie benutzerdefinierte Protokolle:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Eventlog-Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eed1e64d3084d6b952693957c65766b257cb552a861c9989ea0550111e9b224
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383770"
---
# <a name="eventlog-key"></a>Eventlog-Schlüssel

Das Ereignisprotokoll enthält die folgenden Standardprotokolle sowie benutzerdefinierte Protokolle:



| Protokoll             | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anwendung** | Enthält von Anwendungen protokollierte Ereignisse. Beispielsweise kann eine Datenbankanwendung einen Dateifehler aufzeichnen. Der Anwendungsentwickler entscheidet, welche Ereignisse erfasst werden sollen.                                                                             |
| **Sicherheit**    | Enthält Ereignisse wie gültige und ungültige Anmeldeversuche sowie Ereignisse im Zusammenhang mit der Ressourcenverwendung, z. B. das Erstellen, Öffnen oder Löschen von Dateien oder anderen Objekten. Ein Administrator kann die Überwachung starten, um Ereignisse im Sicherheitsprotokoll aufzuzeichnen. |
| **System**      | Enthält Ereignisse, die von Systemkomponenten protokolliert werden, z. B. der Fehler eines Treibers oder einer anderen Systemkomponente, die während des Starts geladen werden soll.                                                                                                               |
| *CustomLog*     | Enthält Ereignisse, die von Anwendungen protokolliert werden, die ein benutzerdefiniertes Protokoll erstellen. Mithilfe eines benutzerdefinierten Protokolls kann eine Anwendung die Größe des Protokolls steuern oder ACLs aus Sicherheitsgründen anfügen, ohne dass sich dies auf andere Anwendungen auswirkt.                         |



 

Der Ereignisprotokollierungsdienst verwendet die im **Eventlog-Registrierungsschlüssel** gespeicherten Informationen. Der **Eventlog-Schlüssel** enthält mehrere Unterschlüssel, die als *Protokolle* bezeichnet werden. Jedes Protokoll enthält Informationen, die der Ereignisprotokollierungsdienst verwendet, um Ressourcen zu suchen, wenn eine Anwendung in das Ereignisprotokoll schreibt und daraus liest.

Die Struktur des **Eventlog-Schlüssels** sieht wie folgt aus:

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

Beachten Sie, dass Domänencontroller Ereignisse im **Verzeichnisdienst** und **Dateireplikations-Dienstprotokolle** aufzeichnen, und DNS-Server Ereignisse im **DNS-Server aufzeichnen.**

Jedes Protokoll kann die folgenden Registrierungswerte enthalten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Registrierungswert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CustomSD</strong></td>
<td>Schränkt den Zugriff auf das Ereignisprotokoll ein. Dieser Wert ist vom Typ REG_SZ. Das verwendete Format ist <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL). Erstellen Sie eine ACL, die mindestens eine der folgenden Rechte gewährt:<dl> Clear (0x0004)<br />
Lesen (0x0001)<br />
Schreiben (0x0002)<br />
</dl> Um eine syntaktisch gültige SDDL zu sein, muss der CustomSD-Wert einen Besitzer und einen Gruppenbesitzer angeben (z.B. O:BAG:SY), aber der Besitzer und der Gruppenbesitzer werden nicht verwendet. Wenn CustomSD auf einen falschen Wert festgelegt ist, wird beim Starten des Ereignisprotokolldiensts ein Ereignis im Systemereignisprotokoll ausgelöst, und das Ereignisprotokoll erhält einen Standardsicherheitsdeskriptor, der mit dem ursprünglichen CustomSD-Wert für das Anwendungsprotokoll identisch ist. SACLs werden nicht unterstützt.<br/> Weitere Informationen finden Sie unter <a href="event-logging-security.md">Ereignisprotokollierungssicherheit.</a><br/> <strong>Windows Server 2003:</strong> SACLs werden unterstützt.<br/> <strong>Windows XP/2000:</strong> Dieser Wert wird nicht unterstützt.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>DisplayNameFile</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Name der Datei, in der der lokalisierte Name des Ereignisprotokolls gespeichert wird. Der in dieser Datei gespeicherte Name wird als Protokollname in Ereignisanzeige angezeigt. Wenn dieser Eintrag nicht in der Registrierung für ein Ereignisprotokoll angezeigt wird, zeigt Ereignisanzeige den Namen des Registrierungsunterschlüssels als Protokollnamen an. Dieser Wert ist vom Typ REG_EXPAND_SZ. Der Standardwert ist %SystemRoot%\system32\els.dll.<br/></td>
</tr>
<tr class="odd">
<td><strong>DisplayNameID</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Nachrichten-ID der Protokollnamenzeichenfolge. Diese Zahl gibt die Meldung an, in der der lokalisierte Anzeigename angezeigt wird. Die Nachricht wird in der Durch den <strong>DisplayNameFile-Wert</strong> angegebenen Datei gespeichert. Dieser Wert ist vom Typ REG_DWORD.<br/></td>
</tr>
<tr class="even">
<td><strong>File</strong></td>
<td>Vollqualifizierte Pfad zu der Datei, in der jedes Ereignisprotokoll gespeichert wird. Dadurch können Ereignisanzeige und andere Anwendungen die Protokolldateien suchen. Dieser Wert ist vom Typ REG_SZ oder REG_EXPAND_SZ. Dieser Wert ist optional. Wenn der Wert nicht angegeben ist, wird standardmäßig %SystemRoot%\system32\winevt\logs\ gefolgt von einem Dateinamen verwendet, der auf dem Namen des Registrierungsschlüssels des Ereignisprotokolls basiert. Der spezifische Pfad der Ereignisprotokolldatei sollte mithilfe des Befehlszeilen-Hilfsprogramms wevtutil.exe oder mithilfe der <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty-Funktion</strong></a> mit EvtChannelLoggingConfigLogFilePath festgelegt werden, die an den <em>PropertyId-Parameter</em> übergeben wird.<br/> Wenn eine bestimmte Datei festgelegt ist, stellen Sie sicher, dass der Ereignisprotokolldienst über vollständige Berechtigungen für die Datei verfügt.<br/> Dieser Wert muss ein gültiger Dateiname für eine Datei sein, die sich in einem lokalen Verzeichnis befindet (kein Remotecomputer, kein DOS-Gerät, keine Diskette und keine Pipe). Wenn die Dateieinstellung falsch ist, wird beim Starten des Ereignisprotokolldiensts ein Ereignis im Systemereignisprotokoll ausgelöst.<br/> Verwenden Sie im Pfad zur Datei keine Umgebungsvariablen, die im Kontext des Ereignisprotokolldiensts nicht erweitert werden können.<br/> <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist standardmäßig auf %SystemRoot%\system32\config\ gefolgt von einem Dateinamen, der auf dem Namen des Registrierungsschlüssels des Ereignisprotokolls basiert. Wenn die Einstellung Datei auf einen ungültigen Wert festgelegt ist, wird das Protokoll entweder nicht ordnungsgemäß initialisiert, oder alle Anforderungen werden automatisch in das Standardprotokoll (Anwendung) geändert.<br/></td>
</tr>
<tr class="odd">
<td><strong>Maxsize</strong></td>
<td>Maximale Größe der Protokolldatei in Bytes. Dieser Wert ist vom Typ REG_DWORD. Der Wert muss für ein System-, Anwendungs- oder Sicherheitsprotokoll auf ein Vielfaches von 64 KB festgelegt werden. Der Standardwert ist 1 MB. <strong>Windows Server 2003 und Windows XP/2000:</strong> Der Wert ist auf 0xFFFFFFFF beschränkt, und der Standardwert ist 512 KB.<br/></td>
</tr>
<tr class="even">
<td><strong>PrimaryModule</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist der Name des Unterschlüssels, der die Standardwerte für die Einträge im Unterschlüssel für die Ereignisquelle enthält. Dieser Wert ist vom Typ REG_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>Vermerkdauer</strong></td>
<td>Dieser Wert ist vom Typ REG_DWORD. Der Standardwert ist 0. Wenn dieser Wert 0 ist, werden die Datensätze von Ereignissen immer überschrieben. Wenn dieser Wert 0xFFFFFFFF oder ein Wert ungleich 0 (null) ist, werden Datensätze nie überschrieben. Wenn die Protokolldatei die maximale Größe erreicht, müssen Sie das Protokoll manuell löschen. Andernfalls werden neue Ereignisse verworfen. Sie müssen das Protokoll auch löschen, bevor Sie seine Größe ändern können. <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist das Zeitintervall in Sekunden, in dem Datensätze von Ereignissen vor dem Überschreiben geschützt werden. Wenn das Alter eines Ereignisses diesen Wert erreicht oder überschreitet, kann es überschrieben werden.<br/></td>
</tr>
<tr class="even">
<td><strong>Sources</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Namen der Anwendungen, Dienste oder Gruppen von Anwendungen, die Ereignisse in dieses Protokoll schreiben. Dieser Wert sollte nur gelesen und nicht geändert werden. Der Ereignisprotokolldienst verwaltet die Liste basierend auf jedem Programm, das in einem Unterschlüssel unter dem Protokoll aufgeführt ist. Dieser Wert ist vom Typ REG_MULTI_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>AutoBackupLogFiles</strong></td>
<td>Dieser Wert ist vom Typ REG_DWORD und wird vom Ereignisprotokolldienst verwendet, um zu bestimmen, ob ein Ereignisprotokoll automatisch gespeichert werden soll. Der Standardwert ist 0, wodurch die automatische Sicherung deaktiviert wird. Der Dienst wird die Protokolldatei nur sichern, wenn der Aufbewahrungswert -1 (0xFFFFFFFF) ist. Andere Werte werden ignoriert. <strong>Windows Server 2003:</strong> Die Aufbewahrung kann auf -1 (0xFFFFFFFF) oder 1 (0x00000001) festgelegt werden, damit AutoBackupLogFiles funktioniert. Andere Werte werden ignoriert.<br/></td>
</tr>
<tr class="even">
<td><strong>RestrictGuestAccess</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows XP/2000:</strong> Dieser Wert ist vom Typ REG_DWORD, und der Standardwert ist 1. Wenn der Wert auf 1 festgelegt ist, schränkt er den Zugriff des Gastkontos und des anonymen Kontos auf das Ereignisprotokoll ein, und wenn dieser Wert 0 ist, ermöglicht er dem Gastkonto den Zugriff auf das Ereignisprotokoll.<br/></td>
</tr>
<tr class="odd">
<td><strong>Isolation</strong></td>
<td>Definiert die Standardzugriffsberechtigungen für das Protokoll. Dieser Wert ist vom Typ REG_SZ. Sie können einen der folgenden Werte angeben:
<ul>
<li><strong>Anwendung</strong></li>
<li><strong>System</strong></li>
<li><strong>Benutzerdefiniert</strong></li>
</ul>
Die Standardisolation ist <strong>Application</strong>. Die Standardberechtigungen <strong>für Anwendung</strong> sind (mit SDDL dargestellt): <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
Die Standardberechtigungen <strong>für System</strong> sind (mit SDDL dargestellt): <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre>
Die Standardberechtigungen für <strong>die benutzerdefinierte</strong> Isolation sind identisch mit anwendungsspezifischen Berechtigungen.<br/> <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist nicht verfügbar.<br/></td>
</tr>
</tbody>
</table>



 

Jedes Protokoll enthält auch Ereignisquellen. Weitere Informationen finden Sie unter [Ereignisquellen.](event-sources.md)

