---
description: Sie können einen Sicherheitsdeskriptor für eine Named Pipe angeben, wenn Sie die CreateNamedPipe-Funktion aufrufen. Der Sicherheitsdeskriptor steuert den Zugriff auf client- und serverseitige Enden der Named Pipe.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Named Pipe-Sicherheit und Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556987cf35845de249bf0e19f3a0b481aab18e891c3b6211f26eb51571704d7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451210"
---
# <a name="named-pipe-security-and-access-rights"></a>Named Pipe-Sicherheit und Zugriffsrechte

Windows Sicherheit können Sie den Zugriff auf Named Pipes steuern. Weitere Informationen zur Sicherheit finden Sie unter [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).

Sie können einen [Sicherheitsdeskriptor](/windows/desktop/SecAuthZ/security-descriptors) für eine Named Pipe angeben, wenn Sie die [**CreateNamedPipe-Funktion**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) aufrufen. Der Sicherheitsdeskriptor steuert den Zugriff auf client- und serverseitige Enden der Named Pipe. Wenn Sie **NULL** angeben, ruft die Named Pipe einen Standardsicherheitsdeskriptor ab. Die ACLs im Standardsicherheitsdeskriptor für eine Named Pipe gewähren dem LocalSystem-Konto, den Administratoren und dem Erstellerbesitzer vollste Kontrolle. Außerdem gewähren sie Mitgliedern der Gruppe Jeder und dem anonymen Konto Lesezugriff.

Um die Sicherheitsbeschreibung einer Named Pipe abzurufen, rufen Sie die [**GetSecurityInfo-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) auf. Um die Sicherheitsbeschreibung einer Named Pipe zu ändern, rufen Sie die [**SetSecurityInfo-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) auf.

Wenn ein Thread [**CreateNamedPipe aufruft,**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) um ein Handle für das Serverende einer vorhandenen Named Pipe zu öffnen, führt das System eine Zugriffsüberprüfung durch, bevor das Handle zurückgegeben wird. Die Zugriffsüberprüfung vergleicht das Zugriffstoken des Threads und die angeforderten [Zugriffsrechte](/windows/desktop/SecAuthZ/access-rights-and-access-masks) mit der DACL in der Sicherheitsbeschreibung der Named Pipe. Zusätzlich zu den angeforderten Zugriffsrechten muss die DACL dem aufrufenden Thread FILE \_ CREATE PIPE INSTANCE Zugriff auf die Named Pipe \_ \_ gewähren.

Wenn ein Client die [**CreateFile-**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) oder [**CallNamedPipe-Funktion aufruft,**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) um eine Verbindung mit dem Clientende einer Named Pipe herzustellen, führt das System eine Zugriffsüberprüfung aus, bevor dem Client Zugriff gewährt wird.

Das von der [**CreateNamedPipe-Funktion zurückgegebene**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Handle hat immer SYNCHRONIZE-Zugriff. Abhängig vom geöffneten Modus der Pipe verfügt es auch über GENERIC \_ READ, GENERIC \_ WRITE oder beides. Im Folgenden sind die Zugriffsrechte für jeden geöffneten Modus.



| Modus "Öffnen"                           | Zugriffsrechte                                              |
|-------------------------------------|------------------------------------------------------------|
| PIPE \_ ACCESS \_ DUPLEX (0x00000003)   | FILE \_ GENERIC \_ READ, FILE GENERIC WRITE und \_ \_ SYNCHRONIZE |
| PIPEZUGRIFF \_ \_ EINGEHEND (0x00000001)  | FILE \_ GENERIC READ und \_ SYNCHRONIZE                        |
| AUSGEHENDER \_ PIPEZUGRIFF \_ (0x00000002) | FILE \_ GENERIC WRITE und \_ SYNCHRONIZE                       |



 

FILE \_ GENERIC READ access for a named pipe kombiniert die Rechte zum Lesen von Daten aus der \_ Pipe, Lesen von Pipeattributen, Lesen erweiterter Attribute und Lesen der DACL der Pipe.

FILE \_ GENERIC \_ WRITE-Zugriff für eine Named Pipe kombiniert die Rechte zum Schreiben von Daten in die Pipe, zum Anfügen von Daten, zum Schreiben von Pipeattributen, zum Schreiben erweiterter Attribute und zum Lesen der DACL der Pipe. Da FILE \_ APPEND DATA und FILE CREATE PIPE INSTANCE die gleiche Definition \_ \_ \_ \_ haben, ermöglicht FILE GENERIC WRITE \_ die Berechtigung zum Erstellen der \_ Pipe. Um dieses Problem zu vermeiden, verwenden Sie die einzelnen Rechte anstelle von FILE \_ GENERIC \_ WRITE.

Sie können das Zugriffsrecht ACCESS \_ SYSTEM SECURITY auf ein Named \_ Pipe-Objekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffssteuerungslisten (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht.](/windows/desktop/SecAuthZ/sacl-access-right)

Um zu verhindern, dass Remotebenutzer oder Benutzer in einer anderen Terminaldienstsitzung auf eine benannte Pipe zugreifen, verwenden Sie die Anmelde-SID in der DACL für die Pipe. Die Anmelde-SID wird auch in ausführungsbasierten Anmeldungen verwendet. Dies ist die SID, die zum Schützen des Objektnamespace pro Sitzung verwendet wird. Weitere Informationen finden Sie unter [Abrufen der Anmelde-SID in C++](/previous-versions//aa446670(v=vs.85)).

 

 
