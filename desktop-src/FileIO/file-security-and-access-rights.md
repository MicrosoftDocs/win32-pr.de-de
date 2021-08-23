---
description: Da Dateien sicherungsfähige Objekte sind, wird der Zugriff darauf durch das Zugriffssteuerungsmodell reguliert, das den Zugriff auf alle anderen sicherungsfähige Objekte in Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Dateisicherheit und Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f33df8117debef1d7f8349ae2fb479974e59ec582d7be758a753726706b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696250"
---
# <a name="file-security-and-access-rights"></a>Dateisicherheit und Zugriffsrechte

Da Dateien [sicherungsfähige Objekte sind,](/windows/desktop/SecAuthZ/securable-objects)wird der Zugriff darauf durch das Zugriffssteuerungsmodell reguliert, das den Zugriff auf alle anderen sicherungsfähige Objekte in Windows. Eine ausführliche Erläuterung dieses Modells finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Sie können einen [Sicherheitsdeskriptor](/windows/desktop/api/winnt/ns-winnt-security_descriptor) für eine Datei oder ein Verzeichnis angeben, wenn Sie die [**Funktion CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)oder [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) aufrufen. Wenn Sie NULL **für** den *lpSecurityAttributes-Parameter* angeben, erhält die Datei oder das Verzeichnis einen Standardsicherheitsdeskriptor. Die Zugriffssteuerungslisten (Access Control Lists, ACL) im Standardsicherheitsdeskriptor für eine Datei oder ein Verzeichnis werden vom übergeordneten Verzeichnis geerbt. Beachten Sie, dass eine Standardsicherheitsbeschreibung nur zugewiesen wird, wenn eine Datei oder ein Verzeichnis neu erstellt wird, und nicht, wenn sie umbenannt oder verschoben wird.

Um den Sicherheitsdeskriptor einer Datei oder eines Verzeichnisobjekts abzurufen, rufen Sie die [**GetNamedSecurityInfo-**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) oder [**GetSecurityInfo-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) auf. Um die Sicherheitsbeschreibung einer Datei oder eines Verzeichnisobjekts zu ändern, rufen Sie die [**Funktion SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) oder [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) auf.

Die gültigen Zugriffsrechte für Dateien und Verzeichnisse umfassen die Standardzugriffsrechte **DELETE,** **READ \_ CONTROL,** **WRITE \_ DAC,** **WRITE \_ OWNER** [und](/windows/desktop/SecAuthZ/standard-access-rights) **SYNCHRONIZE.** In der Tabelle unter [**Dateizugriffsrechtekonstant sind**](file-access-rights-constants.md) die Zugriffsrechte aufgeführt, die für Dateien und Verzeichnisse spezifisch sind.

Obwohl das **SYNCHRONIZE-Zugriffsrecht** [](/windows/desktop/SecAuthZ/standard-access-rights) in der Standardzugriffsrechteliste als Das Recht definiert ist, ein Dateihandl in einer der Wartefunktionen anzugeben, sollten Sie bei Verwendung asynchroner Datei-E/A-Vorgänge auf das Ereignishandl warten, das in einer ordnungsgemäß konfigurierten [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) enthalten ist, anstatt das Dateihandl mit dem **Synchronize-Zugriffsrecht** für die Synchronisierung zu verwenden.

Im Folgenden finden Sie [die allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für Dateien und Verzeichnisse.



<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FILE_GENERIC_EXECUTE</strong></td>
<td><dl> <strong>FILE_EXECUTE</strong><br />
<strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>Synchronisieren</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>Synchronisieren</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>Synchronisieren</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows vergleicht die angeforderten Zugriffsrechte und die Informationen im Zugriffstoken des Threads mit den Informationen in der Sicherheitsbeschreibung des Datei- oder Verzeichnisobjekts. Wenn der Vergleich nicht verhindert, dass alle angeforderten Zugriffsrechte gewährt werden, wird ein Handle für das Objekt an den Thread zurückgegeben, und die Zugriffsrechte werden gewährt. Weitere Informationen zu diesem Prozess finden Sie unter [Interaktion zwischen Threads und sicherungsfähige Objekte.](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects)

Standardmäßig wird die Autorisierung für den Zugriff auf eine Datei oder ein Verzeichnis streng durch die ACLs in der Sicherheitsbeschreibung gesteuert, die dieser Datei oder diesem Verzeichnis zugeordnet ist. Insbesondere wird die Sicherheitsbeschreibung eines übergeordneten Verzeichnisses nicht verwendet, um den Zugriff auf untergeordnete Dateien oder Verzeichnisse zu steuern. Das **\_ ZUGRIFFsrecht FILE TRAVERSE** [kann](/windows/desktop/SecAuthZ/access-rights-and-access-masks) erzwungen werden, indem die Berechtigung **BYPASS \_ TRAVERSE \_ CHECKING** [von Benutzern](/windows/desktop/SecAuthZ/privileges) entfernt wird. Dies wird im allgemeinen Fall nicht empfohlen, da viele Programme Verzeichnisdurchlauffehler nicht ordnungsgemäß behandeln. Die Hauptnutzung für das **FILE \_ TRAVERSE-Zugriffsrecht** für Verzeichnisse besteht im Aktivieren der Konformität mit bestimmten IEEE- und ISO POSIX-Standards, wenn Interoperabilität mit Unix-Systemen eine Voraussetzung ist.

Das Windows-Sicherheitsmodell bietet eine Möglichkeit, damit ein untergeordnetes Verzeichnis eines oder mehrere ACEs im Sicherheitsdeskriptor des übergeordneten Verzeichnisses erben oder daran gehindert werden kann. Jeder ACE enthält Informationen, die bestimmen, wie er geerbt werden kann und ob er auswirkungen auf das erbende Verzeichnisobjekt hat. Einige geerbte ACEs steuern beispielsweise den Zugriff auf das geerbte Verzeichnisobjekt, und diese werden als effektive *ACEs bezeichnet.* Alle anderen ACEs werden als *aces(nur erben) bezeichnet.*

Das Windows Sicherheitsmodell erzwingt auch die automatische Vererbung von ACEs an untergeordnete Objekte gemäß den [ACE-Vererbungsregeln.](/windows/desktop/SecAuthZ/ace-inheritance-rules) Diese automatische Vererbung bestimmt zusammen mit den Vererbungsinformationen in jedem ACE, wie Sicherheitseinschränkungen in der Verzeichnishierarchie weitergegeben werden.

Beachten Sie, dass Sie einen ACE mit Zugriffsberechtigung nicht verwenden können, um nur **\_ generischen** LESE- oder nur **\_ GENERISCHEN SCHREIBzugriff** auf eine Datei zu verweigern. Dies liegt daran, dass die generischen Zuordnungen für Dateiobjekte sowohl für **GENERIC \_ READ** als auch **für GENERIC \_ WRITE** das **SYNCHRONIZE-Zugriffsrecht** enthalten. Wenn ein ACE generischen **\_ SCHREIBzugriff** für einen Vertrauenshänder verweigert und der Vertrauenshänder **generischen \_ LESEzugriff** an fordert, ist die Anforderung nicht möglich, da die Anforderung implizit **SYNCHRONIZE-Zugriff** enthält, der vom ACE implizit verweigert wird und umgekehrt. Verwenden Sie zugriffsgeschützte ACEs, anstatt zugriffsgeschützte ACEs zu verwenden, um die zulässigen Zugriffsrechte explizit zu ermöglichen.

Eine weitere Möglichkeit zum Verwalten des Zugriffs auf Speicherobjekte ist die Verschlüsselung. Die Implementierung der Dateisystemverschlüsselung in Windows ist das verschlüsselte Dateisystem oder EFS. EFS verschlüsselt nur Dateien und keine Verzeichnisse. Der Vorteil der Verschlüsselung ist, dass sie zusätzlichen Schutz für Dateien bietet, die auf das Medium angewendet werden, nicht über das Dateisystem und die Windows Zugriffssteuerungsarchitektur. Weitere Informationen zur Dateiverschlüsselung finden Sie unter [Dateiverschlüsselung.](file-encryption.md)

In den meisten Fällen ist die Fähigkeit zum Lesen und Schreiben der Sicherheitseinstellungen einer Datei oder eines Verzeichnisobjekts auf Kernelmodusprozesse beschränkt. Natürlich möchten Sie nicht, dass ein Benutzerprozess den Besitz oder die Zugriffseinschränkung für Ihre private Datei oder Ihr privates Verzeichnis ändern kann. Eine Sicherungsanwendung wäre jedoch nicht in der Lage, ihre Datei zu sichern, wenn die Zugriffseinschränkungen, die Sie für Ihre Datei oder Ihr Verzeichnis eingerichtet haben, nicht zulassen, dass der Benutzermodusprozess der Anwendung sie liest. Sicherungsanwendungen müssen in der Lage sein, die Sicherheitseinstellungen von Datei- und Verzeichnisobjekten außer Kraft zu setzen, um eine vollständige Sicherung sicherzustellen. Wenn eine Sicherungsanwendung versucht, eine Sicherungskopie Ihrer Datei über die auf dem Datenträger gespeicherte Kopie zu schreiben, und Sie explizit Schreibberechtigungen für den Sicherungsanwendungsprozess verweigern, kann der Wiederherstellungsvorgang entsprechend nicht abgeschlossen werden. In diesem Fall muss die Sicherungsanwendung auch in der Lage sein, die Zugriffssteuerungseinstellungen Ihrer Datei außer Kraft zu setzen.

Die **SE \_ BACKUP \_ NAME** und **SE RESTORE \_ NAME-Zugriffsberechtigungen \_** wurden speziell erstellt, um diese Möglichkeit zum Sichern von Anwendungen zu bieten. Wenn diese Berechtigungen im Zugriffstoken des Sicherungsanwendungsprozesses gewährt und aktiviert wurden, kann [**createFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) zum Öffnen der Datei oder des Verzeichnisses für die Sicherung verwendet werden. Dabei wird das Standardzugriffsrecht **READ \_ CONTROL** als Wert des *dwDesiredAccess-Parameters* angegeben. Um den aufrufenden Prozess jedoch als Sicherungsprozess zu identifizieren, muss der Aufruf von **CreateFile** das **FLAG FILE FLAG BACKUP \_ \_ \_ SEMANTICS** im *parameter dwFlagsAndAttributes* enthalten. Die vollständige Syntax des Funktionsaufrufs ist die folgende:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Dadurch kann der Sicherungsanwendungsprozess Ihre Datei öffnen und die Standardsicherheitsprüfung außer Kraft setzen. Zum Wiederherstellen der Datei verwendet die [](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Sicherungsanwendung die folgende CreateFile-Aufrufsyntax, wenn sie die zu schreibende Datei öffnet.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Es gibt Situationen, in denen eine Sicherungsanwendung in der Lage sein muss, die Zugriffssteuerungseinstellungen einer Datei oder eines Verzeichnisses zu ändern. Ein Beispiel ist, wenn sich die Zugriffssteuerungseinstellungen der auf dem Datenträger gespeicherten Kopie einer Datei oder eines Verzeichnisses von der Sicherungskopie unterscheiden. Dies geschieht, wenn diese Einstellungen geändert wurden, nachdem die Datei oder das Verzeichnis sichern wurde, oder wenn sie beschädigt wurde.

Das im Aufruf von [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) angegebene **FILE FLAG BACKUP \_ \_ \_ SEMANTICS-Flag** erteilt der Sicherungsanwendung die Berechtigung, die Zugriffssteuerungseinstellungen der Datei oder des Verzeichnisses zu lesen. Mit dieser Berechtigung kann der Sicherungsanwendungsprozess [**dann GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) und [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) aufrufen, um die Zugriffssteuerungseinstellungen zu lesen und zurückzusetzen.

Wenn eine Sicherungsanwendung Zugriff auf die Zugriffssteuerungseinstellungen auf Systemebene haben [muss,](/windows/desktop/SecAuthZ/access-control-lists)muss das **FLAG ACCESS SYSTEM \_ \_ SECURITY** im *parameter-Wert dwDesiredAccess* angegeben werden, der an [**CreateFile übergeben wird.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)

Sicherungsanwendungen rufen [**BackupRead auf,**](/windows/desktop/api/winbase/nf-winbase-backupread) um die für den Wiederherstellungsvorgang angegebenen Dateien und Verzeichnisse zu lesen, und [**BackupWrite,**](/windows/desktop/api/winbase/nf-winbase-backupwrite) um sie zu schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standardzugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
