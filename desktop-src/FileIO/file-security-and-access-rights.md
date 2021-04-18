---
description: Da es sich bei Dateien um Sicherungs fähige Objekte handelt, wird der Zugriff darauf durch das Zugriffs Steuerungsmodell reguliert, das den Zugriff auf alle anderen Sicherungs fähigen Objekte in Windows steuert.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Datei Sicherheit und Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b161dd78c7585cf6de2781d7339787a22bde95dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347080"
---
# <a name="file-security-and-access-rights"></a>Datei Sicherheit und Zugriffsrechte

Da es sich bei Dateien um Sicherungs [fähige Objekte](/windows/desktop/SecAuthZ/securable-objects)handelt, wird der Zugriff darauf durch das Zugriffs Steuerungsmodell reguliert, das den Zugriff auf alle anderen Sicherungs fähigen Objekte in Windows steuert. Eine ausführliche Erläuterung dieses Modells finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Sie können eine [Sicherheits Beschreibung](/windows/desktop/api/winnt/ns-winnt-security_descriptor) für eine Datei oder ein Verzeichnis [**angeben, wenn Sie die Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)"up", " [**kreatedirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)" oder " [**kreatedirectoryex**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) " aufrufen. Wenn Sie für den *lpsecurityattribute* -Parameter **null** angeben, erhält die Datei oder das Verzeichnis eine Standard Sicherheits Beschreibung. Die Zugriffs Steuerungs Listen (Access Control Lists, ACL) in der Standard Sicherheits Beschreibung für eine Datei oder ein Verzeichnis werden von ihrem übergeordneten Verzeichnis geerbt. Beachten Sie, dass eine Standard Sicherheits Beschreibung nur zugewiesen wird, wenn eine Datei oder ein Verzeichnis neu erstellt wird, und nicht, wenn Sie umbenannt oder verschoben wird.

Um die Sicherheits Beschreibung eines Datei-oder Verzeichnis Objekts abzurufen, rufen Sie die [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) -oder [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) -Funktion auf. Um die Sicherheits Beschreibung eines Datei-oder Verzeichnis Objekts zu ändern, müssen Sie die Funktion [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) oder [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) aufrufen.

Zu den gültigen Zugriffsrechten für Dateien und Verzeichnisse gehören die Berechtigungen **Löschen**, **Lese \_ Steuerung**, **Schreib- \_ DAC**, **\_ Besitzer schreiben** und [Standard Zugriff](/windows/desktop/SecAuthZ/standard-access-rights) **Synchronisieren** . In der Tabelle unter [**Datei Zugriffsrechte Konstanten**](file-access-rights-constants.md) werden die Zugriffsrechte aufgelistet, die für Dateien und Verzeichnisse spezifisch sind.

Obwohl das **Synchronisierungs** Zugriffsrecht in der [Standard-Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) Liste als Recht zum Angeben eines Datei Handles in einer der Warte Funktionen definiert ist, sollten Sie bei Verwendung asynchroner Datei-e/a-Vorgänge auf das Ereignis Handle warten, das in einer ordnungsgemäß konfigurierten [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur enthalten ist, anstatt das Datei Handle mit dem **Synchronisierungs** Zugriffsrecht für die Synchronisierung zu verwenden.

Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für Dateien und Verzeichnisse.



<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FILE_GENERIC_EXECUTE</strong></td>
<td><dl> <strong>FILE_EXECUTE</strong><br />
<strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows vergleicht die angeforderten Zugriffsrechte und die Informationen im Zugriffs Token des Threads mit den Informationen in der Sicherheits Beschreibung des Datei-oder Verzeichnis Objekts. Wenn beim Vergleich nicht alle angeforderten Zugriffsrechte erteilt werden, wird ein Handle für das Objekt an den Thread zurückgegeben, und die Zugriffsrechte werden gewährt. Weitere Informationen zu diesem Prozess finden Sie unter [Interaktion zwischen Threads und Sicherungs fähigen Objekten](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects).

Standardmäßig wird die Autorisierung für den Zugriff auf eine Datei oder ein Verzeichnis strikt durch die ACLs in der Sicherheits Beschreibung gesteuert, die mit dieser Datei oder diesem Verzeichnis verknüpft ist. Insbesondere wird die Sicherheits Beschreibung eines übergeordneten Verzeichnisses nicht verwendet, um den Zugriff auf untergeordnete Dateien oder Verzeichnisse zu steuern. Das [Zugriffsrecht](/windows/desktop/SecAuthZ/access-rights-and-access-masks) " **Datei \_** durchlaufen" kann erzwungen werden, indem die **Umgehungs \_ \_ Überprüfungs** [Berechtigung](/windows/desktop/SecAuthZ/privileges) "Bypass" von Benutzern entfernt wird. Dies wird im Allgemeinen nicht empfohlen, da viele Programme Verzeichnis Durchlauf Fehler nicht ordnungsgemäß behandeln. Der primäre Verwendungszweck des **Datei \_** Zugriffs auf Verzeichnisse besteht darin, die Konformität mit bestimmten IEEE-und ISO POSIX-Standards zu aktivieren, wenn die Interoperabilität mit UNIX-Systemen erforderlich ist.

Das Windows-Sicherheitsmodell bietet die Möglichkeit, ein untergeordnetes Verzeichnis zu erben bzw. zu verhindern, dass eines oder mehrere der ACEs in der Sicherheits Beschreibung des übergeordneten Verzeichnisses vererbt werden. Jeder ACE enthält Informationen, die bestimmen, wie er geerbt werden kann, und ob er Auswirkungen auf das erbende Verzeichnis Objekt hat. Einige geerbte ACEs Steuern beispielsweise den Zugriff auf das geerbte Verzeichnis Objekt, und diese werden als *effektive ACEs* bezeichnet. Alle anderen ACEs werden als *Vererbung-only-ACEs* bezeichnet.

Das Windows-Sicherheitsmodell erzwingt auch die automatische Vererbung von ACEs zu untergeordneten Objekten gemäß den [ACE-Vererbungs Regeln](/windows/desktop/SecAuthZ/ace-inheritance-rules). Diese automatische Vererbung bestimmt zusammen mit den Vererbungs Informationen in jedem ACE, wie Sicherheitseinschränkungen in der Verzeichnishierarchie nach unten weitergegeben werden.

Beachten Sie, dass Sie einen Access-denied-ACE nicht verwenden können, um nur den **generischen \_ Lese** Zugriff oder nur den **generischen \_ Schreib** Zugriff auf eine Datei abzulehnen Dies liegt daran, dass bei Datei Objekten die generischen Zuordnungen sowohl für den **generischen \_ Lese** -als auch für den **generischen \_ Schreib** Zugriff das **Synchronisierungs** Zugriffsrecht Wenn ein ACE **generischen \_ Schreib** Zugriff auf einen Vertrauens nehmer verweigert und der Treuhänder **generischen \_ Lese** Zugriff anfordert, schlägt die Anforderung fehl, da die Anforderung implizit den **Synchronisierungs** Zugriff einschließt, der vom ACE implizit verweigert wird, und umgekehrt. Anstatt Zugriffs Verweigerungs-ACEs zu verwenden, verwenden Sie Zugriffs zulässige ACEs, um die zulässigen Zugriffsrechte explizit zuzulassen.

Eine weitere Möglichkeit, den Zugriff auf Speicher Objekte zu verwalten, ist die Verschlüsselung. Bei der Implementierung der Dateisystem Verschlüsselung in Windows handelt es sich um das verschlüsselte Dateisystem (EFS). EFS verschlüsselt nur Dateien und keine Verzeichnisse. Der Vorteil der Verschlüsselung besteht darin, dass Sie zusätzlichen Schutz für Dateien bietet, die auf die Medien angewendet werden, nicht über das Dateisystem und die standardmäßige Windows-Zugriffs Steuerungsarchitektur. Weitere Informationen zur Dateiverschlüsselung finden Sie unter [Dateiverschlüsselung](file-encryption.md).

In den meisten Fällen ist die Möglichkeit, die Sicherheitseinstellungen eines Datei-oder Verzeichnis Objekts zu lesen und zu schreiben, auf Kernel Modus-Prozesse beschränkt. Es ist natürlich nicht ratsam, dass ein Benutzer Prozess in der Lage ist, den Besitz oder die Zugriffsbeschränkung für die private Datei oder das Verzeichnis zu ändern. Allerdings kann eine Sicherungs Anwendung die Sicherung der Datei nicht durchführen, wenn die Zugriffsbeschränkungen, die Sie für die Datei oder das Verzeichnis festgelegt haben, den Benutzermodusprozess der Anwendung nicht zulassen. Sicherungs Anwendungen müssen in der Lage sein, die Sicherheitseinstellungen von Datei-und Verzeichnis Objekten außer Kraft zu setzen, um eine komplette Sicherung sicherzustellen. Wenn eine Sicherungs Anwendung versucht, eine Sicherungskopie der Datei über die Datenträger residente Kopie zu schreiben, und Sie explizit Schreibberechtigungen für den Sicherungs Anwendungsprozess verweigern, kann der Wiederherstellungs Vorgang nicht beendet werden. In diesem Fall muss die Sicherungs Anwendung in der Lage sein, die Zugriffs Steuerungseinstellungen der Datei zu überschreiben.

Die Berechtigungen " **SE \_ Backup \_ Name** " und " **SE \_ Restore \_ Name** Access" wurden speziell erstellt, um die Möglichkeit zum Sichern von Anwendungen bereitzustellen. Wenn diese Berechtigungen im Zugriffs Token des Sicherungs Anwendungsprozesses erteilt und aktiviert wurden, kann Sie dann die Datei oder das Verzeichnis für die [**Sicherung aufrufen,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um die Datei oder das Verzeichnis für die Sicherung zu öffnen. dabei wird der standardmäßige **Lese \_ Steuer** Element-Zugriffsrecht als Wert des *dwDesiredAccess* -Parameters angegeben. Um den aufrufenden Prozess jedoch als Sicherungsprozess zu identifizieren, muss der Aufruf von **CreateFile** das **Dateiflag für die \_ \_ Sicherungs \_ Semantik** in den *dwflagsandattributs-Parameter* einschließen. Die vollständige Syntax des Funktions Aufrufes lautet wie folgt:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Dadurch kann der Sicherungs Anwendungsprozess Ihre Datei öffnen und die Standard Sicherheitsüberprüfung außer Kraft setzen. Zum Wiederherstellen der Datei verwendet die Sicherungs Anwendung die folgende Syntax [](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) des aufrufungsdateiaufrufes, wenn Sie die Datei öffnen, die geschrieben werden soll.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Es gibt Situationen, in denen eine Sicherungs Anwendung in der Lage sein muss, die Zugriffs Steuerungseinstellungen einer Datei oder eines Verzeichnisses zu ändern. Dies ist beispielsweise der Fall, wenn sich die Zugriffs Steuerungseinstellungen der Datenträger Residenten Kopie einer Datei oder eines Verzeichnisses von der Sicherungskopie unterscheiden. Dies wäre der Fall, wenn diese Einstellungen geändert wurden, nachdem die Datei oder das Verzeichnis gesichert wurde, oder wenn Sie beschädigt war.

Das Flag für die **\_ \_ Sicherungs \_ Semantik der Datei** Kennzeichen, das im Aufrufen von " [**anatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " angegeben wird, erteilt der Sicherungs Anwendungsprozess Berechtigung zum Lesen der Zugriffs Steuerungseinstellungen der Datei oder des Verzeichnisses. Mit dieser Berechtigung kann der Sicherungs Anwendungsprozess [**getkernelobjectsecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) und [**setkernelobjectsecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) aufrufen, um die Einstellungen für die Zugriffs Steuerung zu lesen und zu übersetzen.

Wenn eine Sicherungs Anwendung Zugriff auf die Einstellungen für die [Zugriffs Steuerung](/windows/desktop/SecAuthZ/access-control-lists)auf Systemebene haben muss, muss das Sicherheitskennzeichen des **Zugriffs \_ \_ Systems** im *dwDesiredAccess* -Parameterwert angegeben werden, der an " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" übergeben wird.

Sicherungs Anwendungen rufen [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) auf, um die Dateien und Verzeichnisse zu lesen, die für den Wiederherstellungs Vorgang angegeben wurden, und [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) , um Sie zu schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
