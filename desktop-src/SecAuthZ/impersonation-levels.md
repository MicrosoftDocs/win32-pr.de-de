---
description: Die Enumeration der sicherheitsidentitäts Wechsel \_ \_ Ebene definiert vier Identitätswechsel Ebenen, die bestimmen, welche Vorgänge ein Server im Client Kontext ausführen kann.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Identitätswechsel Ebenen (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b91654f42a86e5c47069197bed084df56f5445dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359483"
---
# <a name="impersonation-levels-authorization"></a>Identitätswechsel Ebenen (Autorisierung)

Die Enumeration der [**sicherheitsidentitäts Wechsel \_ \_ Ebene**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) definiert vier Identitätswechsel Ebenen, die bestimmen, welche Vorgänge ein Server im Kontext des Clients durchführen kann.



| Ebene des Identitätswechsels    | BESCHREIBUNG                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| Securityanonymous      | Der Server kann den Client nicht annehmen oder ihn identifizieren.                                            |
| SecurityIdentification | Der Server kann die Identität und die Berechtigungen des Clients erhalten, kann jedoch nicht die Identität des Clients annehmen. |
| Securityidentitäts Wechsel  | Der Server kann den Sicherheitskontext des Clients auf dem lokalen System imitieren.                    |
| SecurityDelegation     | Der Server kann den Sicherheitskontext des Clients auf Remote Systemen imitieren.                      |



 

Der Client einer Named Pipe-, RPC-oder DDE-Verbindung kann die Identitätswechsel Ebene steuern. Ein Named Pipe Client kann z. b. die [**Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -Funktion" aufrufen, um ein Handle für eine Named Pipe zu öffnen und die Identitätswechsel Ebene des Servers anzugeben.

Wenn die Named Pipe-, RPC-oder DDE-Verbindung Remote ist, werden die Flags, die an die " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " übergeben werden, um die Identitätswechsel Ebene festzulegen, ignoriert In diesem Fall wird die Identitätswechsel Ebene des Clients durch die vom Server aktivierten Identitätswechsel Ebenen bestimmt, der durch ein Flag für das Konto des Servers im Verzeichnisdienst festgelegt wird. Wenn z. b. der Server für die Delegierung aktiviert ist, wird die Identitätswechsel Ebene des Clients auch auf Delegierung festgelegt, auch wenn die Flags, die an " **anatefile** " übergeben werden, die Identitäts Identitätswechsel Ebene angeben.

DDE-Clients verwenden die [**ddesetqualityofservice**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) -Funktion mit der [**Security \_ Quality \_ of \_ Service**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) -Struktur, um die Identitätswechsel Ebene anzugeben. Die Security-Identitätswechsel Ebene ist die Standardeinstellung für Named Pipe-, RPC-und DDE-Server. Die Funktionen Identität [**ateself**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself), [**duplicatetoken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)und [**duplicatetokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) ermöglichen es dem Aufrufer, eine Identitätswechsel Ebene anzugeben. Verwenden Sie die [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) -Funktion, um die Identitätswechsel Ebene eines [*Zugriffs*](/windows/desktop/SecGloss/a-gly)Tokens abzurufen.

Auf der Security-Identitätswechsel Ebene treten die meisten Aktionen des Threads im Sicherheitskontext des Identitätswechsel Tokens des Threads auf [*, nicht im*](/windows/desktop/SecGloss/i-gly) [*primären Token*](/windows/desktop/SecGloss/p-gly) des [*Prozesses*](/windows/desktop/SecGloss/p-gly) , der den Thread besitzt. Wenn ein Identitätswechsel Thread z. b. ein Sicherungs [fähiges Objekt](securable-objects.md)öffnet, verwendet das System das Identitätswechsel Token, um den Thread Zugriff zu überprüfen. Wenn ein Identitätswechsel Thread z. b. ein neues Objekt erstellt, z. b. durch Aufrufen der [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -Funktion, ist der Besitzer des neuen Objekts der Standard Besitzer aus dem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)des Clients.

Das System verwendet jedoch das primäre Token des Prozesses anstelle des Identitätswechsel Tokens des aufrufenden Threads in den folgenden Situationen:

-   Wenn ein Identitätswechsel Thread die Funktion " [**forateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " aufruft, erbt der neue Prozess immer das primäre Token des Prozesses.
-   Für Funktionen, die die "SE \_ TCB Name"-Berechtigung erfordern (z. b. \_ die [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) -Funktion), prüft das System immer, ob die Berechtigung im primären Token des Prozesses besteht.
-   Für Funktionen, die die Berechtigung "SE \_ Audit Name" erfordern \_ , wie z. b. die [**objectopenauditalarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) -Funktion, prüft das System immer, ob die Berechtigung im primären Token des Prozesses besteht.
-   Bei einem Aufrufen der [**openthumtotokenfunktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) kann ein Thread angeben, ob die Funktion das Identitätswechsel Token oder das primäre Token verwendet, um zu bestimmen, ob der angeforderte Zugriff gewährt werden soll.

 

 
