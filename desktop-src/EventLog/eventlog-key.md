---
description: 'Das Ereignisprotokoll enthält die folgenden Standardprotokolle sowie benutzerdefinierte Protokolle:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: EventLog-Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6965c850dd31ab722786cf4da41c7d3a67f5d980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755657"
---
# <a name="eventlog-key"></a>EventLog-Schlüssel

Das Ereignisprotokoll enthält die folgenden Standardprotokolle sowie benutzerdefinierte Protokolle:



| Log             | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anwendung** | Enthält Ereignisse, die von Anwendungen protokolliert werden. Beispielsweise kann eine Datenbankanwendung einen Datei Fehler aufzeichnen. Der Anwendungsentwickler entscheidet, welche Ereignisse aufgezeichnet werden.                                                                             |
| **Security**    | Enthält Ereignisse, wie z. b. gültige und ungültige Anmeldeversuche, sowie Ereignisse im Zusammenhang mit der Ressourcenverwendung, z. b. das Erstellen, öffnen oder Löschen von Dateien oder anderen Objekten. Ein Administrator kann die Überwachung starten, um Ereignisse im Sicherheitsprotokoll aufzuzeichnen. |
| **System**      | Enthält Ereignisse, die von Systemkomponenten protokolliert werden, z. b. Fehler beim Laden eines Treibers oder einer anderen Systemkomponente während des Starts.                                                                                                               |
| *CustomLog*     | Enthält von Anwendungen protokollierte Ereignisse, die ein benutzerdefiniertes Protokoll erstellen. Die Verwendung eines benutzerdefinierten Protokolls ermöglicht einer Anwendung, die Größe des Protokolls zu steuern oder Zugriffs Steuerungs Listen für Sicherheitszwecke anzufügen, ohne dass sich dies auf andere Anwendungen auswirkt.                         |



 

Der Ereignis Protokollierungs Dienst verwendet die im Registrierungsschlüssel **EventLog** gespeicherten Informationen. Der **EventLog** -Schlüssel enthält mehrere Unterschlüssel, die als *Protokolle* bezeichnet werden. Jedes Protokoll enthält Informationen, die vom Ereignis Protokollierungs Dienst zum Auffinden von Ressourcen verwendet werden, wenn eine Anwendung in das Ereignisprotokoll schreibt und daraus liest.

Die Struktur des **EventLog** -Schlüssels lautet wie folgt:

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

Beachten Sie, dass Domänen Controller Ereignisse in den **Verzeichnisdienst** -und **Datei Replikations Dienst** Protokollen und DNS-Servern aufzeichnen, um Ereignisse im **DNS-Server** aufzuzeichnen.

Jedes Protokoll kann die folgenden Registrierungs Werte enthalten.



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
<td>Schränkt den Zugriff auf das Ereignisprotokoll ein. Dieser Wert ist vom Typ REG_SZ. Das verwendete Format ist die <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL). Erstellen Sie eine ACL, die mindestens eines der folgenden Rechte erteilt:<dl> Clear (0x0004)<br />
Lesen (0x0001)<br />
Schreiben (0x0002)<br />
</dl> Um eine syntaktisch gültige SDDL zu sein, muss der CustomSD-Wert einen Besitzer und einen Gruppenbesitzer angeben (z. b. o:Bag: SY), der Besitzer und der Gruppenbesitzer werden jedoch nicht verwendet. Wenn CustomSD auf einen falschen Wert festgelegt ist, wird im System Ereignisprotokoll ein Ereignis ausgelöst, wenn der Ereignisprotokoll Dienst gestartet wird, und das Ereignisprotokoll erhält eine Standard Sicherheits Beschreibung, die mit dem ursprünglichen CustomSD-Wert für das Anwendungsprotokoll identisch ist. SACLs werden nicht unterstützt.<br/> Weitere Informationen finden Sie unter <a href="event-logging-security.md">Sicherheit bei der Ereignisprotokollierung</a>.<br/> <strong>Windows Server 2003:</strong> SACLs werden unterstützt.<br/> <strong>Windows XP/2000:</strong> Dieser Wert wird nicht unterstützt.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>Displaynamefile</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:  </strong> Der Name der Datei, in der der lokalisierte Name des Ereignis Protokolls gespeichert wird. Der in dieser Datei gespeicherte Name wird in Ereignisanzeige als Protokoll Name angezeigt. Wenn dieser Eintrag nicht in der Registrierung für ein Ereignisprotokoll angezeigt wird, zeigt Ereignisanzeige den Namen des Registrierungs unter Schlüssels als Protokollnamen an. Dieser Wert ist vom Typ REG_EXPAND_SZ. Der Standardwert ist% SystemRoot% \system32\els.dll.<br/></td>
</tr>
<tr class="odd">
<td><strong>Display Name Eid</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:  </strong> Die Nachrichten-ID der Protokollnamen Zeichenfolge. Diese Zahl gibt die Meldung an, in der der lokalisierte Anzeige Name angezeigt wird. Die Meldung wird in der Datei gespeichert, die durch den <strong>displaynamefile</strong> -Wert angegeben wird. Dieser Wert ist vom Typ REG_DWORD.<br/></td>
</tr>
<tr class="even">
<td><strong>File</strong></td>
<td>Voll qualifizierter Pfad zu der Datei, in der jedes Ereignisprotokoll gespeichert ist. Dadurch können Ereignisanzeige und andere Anwendungen die Protokolldateien finden. Dieser Wert ist vom Typ REG_SZ oder REG_EXPAND_SZ. Dieser Wert ist optional. Wenn der Wert nicht angegeben wird, wird standardmäßig%systemroot%\system32\winevt\logs\ gefolgt von einem Dateinamen verwendet, der auf dem Namen des Registrierungsschlüssels für den Ereignisprotokoll basiert. Der spezifische Ereignisprotokoll Dateipfad sollte mit dem Befehlszeilen-Hilfsprogramm wevtutil.exe oder mithilfe der <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>evtsetchannelconfigproperty</strong></a> -Funktion mit evtchannelloggingconfiglogfilepath festgelegt werden, die an den <em>PropertyId</em> -Parameter übergeben wird.<br/> Wenn eine bestimmte Datei festgelegt ist, stellen Sie sicher, dass der Ereignisprotokoll Dienst über vollständige Berechtigungen für die Datei verfügt.<br/> Dieser Wert muss ein gültiger Dateiname für eine Datei sein, die sich in einem lokalen Verzeichnis befindet (kein Remote Computer, kein DOS-Gerät, keine Diskette und keine Pipe). Wenn die Datei Einstellung falsch ist, wird im System Ereignisprotokoll ein Ereignis ausgelöst, wenn der Ereignisprotokoll Dienst gestartet wird.<br/> Verwenden Sie keine Umgebungsvariablen im Pfad zu der Datei, die im Kontext des Ereignisprotokoll Dienstanbieter nicht erweitert werden können.<br/> <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert wird standardmäßig auf%systemroot%\system32\config\ gefolgt von einem Dateinamen festgelegt, der auf dem Registrierungsschlüssel Namen des Ereignis Protokolls basiert. Wenn die Datei Einstellung auf einen ungültigen Wert festgelegt ist, wird das Protokoll entweder nicht ordnungsgemäß initialisiert, oder alle Anforderungen werden im Hintergrund in das Standardprotokoll (Anwendung) überlaufen.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxSize</strong></td>
<td>Maximale Größe der Protokolldatei in Byte. Dieser Wert ist vom Typ REG_DWORD. Der Wert muss für ein System, eine Anwendung oder ein Sicherheitsprotokoll auf ein Vielfaches von 64K festgelegt werden. Der Standardwert ist 1 MB. <strong>Windows Server 2003 und Windows XP/2000:</strong> Der Wert ist auf 0xFFFFFFFF beschränkt, und der Standardwert ist 512 KB.<br/></td>
</tr>
<tr class="even">
<td><strong>PrimaryModule</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:</strong> Dieser Wert ist der Name des unter Schlüssels, der die Standardwerte für die Einträge im Unterschlüssel für die Ereignis Quelle enthält. Dieser Wert ist vom Typ REG_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>Vermerkdauer</strong></td>
<td>Dieser Wert ist vom Typ REG_DWORD. Der Standardwert ist 0. Wenn dieser Wert 0 ist, werden die Datensätze von Ereignissen immer überschrieben. Wenn dieser Wert "0xffffffff" oder ein beliebiger Wert ungleich NULL ist, werden Datensätze nie überschrieben. Wenn die Protokolldatei die maximale Größe erreicht, müssen Sie das Protokoll manuell löschen. Andernfalls werden neue Ereignisse verworfen. Sie müssen das Protokoll auch löschen, bevor Sie seine Größe ändern können. <strong>Windows Server 2003 und Windows XP/2000:  </strong> Dieser Wert ist das Zeitintervall (in Sekunden), in dem Datensätze von Ereignissen vor dem Überschreiben geschützt werden. Wenn das Alter eines Ereignisses diesen Wert erreicht oder überschreitet, kann es überschrieben werden.<br/></td>
</tr>
<tr class="even">
<td><strong>Sources</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows Server 2003 und Windows XP/2000:  </strong> Namen der Anwendungen, Dienste oder Anwendungs Gruppen, die Ereignisse in dieses Protokoll schreiben. Dieser Wert sollte nur gelesen und nicht geändert werden. Der Ereignisprotokoll Dienst verwaltet die Liste basierend auf jedem Programm, das in einem Unterschlüssel unter dem Protokoll aufgeführt ist. Dieser Wert ist vom Typ REG_MULTI_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>AutoBackupLogFiles</strong></td>
<td>Dieser Wert ist vom Typ REG_DWORD und wird vom Ereignisprotokoll Dienst verwendet, um zu bestimmen, ob ein Ereignisprotokoll automatisch gespeichert werden soll. Der Standardwert ist 0 (null), wodurch die automatische Sicherung deaktiviert wird. Der Dienst sichert die Protokolldatei nur dann, wenn der Beibehaltungs Wert-1 (0xFFFFFFFF) ist. Andere Werte werden ignoriert. <strong>Windows Server 2003:  </strong> Die Beibehaltung kann auf-1 (0xFFFFFFFF) oder 1 (0x00000001) festgelegt werden, damit AutoBackupLogFiles funktioniert. Andere Werte werden ignoriert.<br/></td>
</tr>
<tr class="even">
<td><strong>RestrictGuestAccess</strong></td>
<td>Dieser Wert wird nicht verwendet. <strong>Windows XP/2000:  </strong> Dieser Wert ist vom Typ REG_DWORD, und der Standardwert ist 1. Wenn der Wert auf 1 festgelegt ist, schränkt der Gast-und anonyme Konto Zugriff auf das Ereignisprotokoll ein. Wenn dieser Wert 0 ist, ermöglicht er dem Gast Konto den Zugriff auf das Ereignisprotokoll.<br/></td>
</tr>
<tr class="odd">
<td><strong>Isolation</strong></td>
<td>Definiert die Standard Zugriffsberechtigungen für das Protokoll. Dieser Wert ist vom Typ REG_SZ. Sie können einen der folgenden Werte angeben:
<ul>
<li><strong>Anwendung</strong></li>
<li><strong>System</strong></li>
<li><strong>Benutzerdefiniert</strong></li>
</ul>
Die Standard Isolation ist die <strong>Anwendung</strong>. Die Standard Berechtigungen für die <strong>Anwendung</strong> werden (mit SDDL angezeigt): <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
Die Standard Berechtigungen für <strong>System</strong> lauten (mit SDDL angezeigt): <br/>
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
Die Standard Berechtigungen für die <strong>benutzerdefinierte</strong> Isolation sind identisch mit der Anwendung.<br/> <strong>Windows Server 2003 und Windows XP/2000:  </strong> Dieser Wert ist nicht verfügbar.<br/></td>
</tr>
</tbody>
</table>



 

Jedes Protokoll enthält auch Ereignis Quellen. Weitere Informationen finden Sie unter [Ereignis Quellen](event-sources.md).

