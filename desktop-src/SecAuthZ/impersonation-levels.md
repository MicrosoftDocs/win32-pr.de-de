---
description: Die SECURITY \_ IMPERSONATION \_ LEVEL-Enumeration definiert vier Identitätswechselebenen, die die Vorgänge bestimmen, die ein Server im Clientkontext ausführen kann.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Identitätswechselebenen (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf80f4f6b84499a94659c137c629d66a041752e5171cb3fa7220506586f36e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414590"
---
# <a name="impersonation-levels-authorization"></a>Identitätswechselebenen (Autorisierung)

Die [**SECURITY \_ IMPERSONATION \_ LEVEL-Enumeration**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) definiert vier Identitätswechselebenen, die die Vorgänge bestimmen, die ein Server im Clientkontext ausführen kann.



| Ebene des Identitätswechsels    | Beschreibung                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | Der Server kann die Identität des Clients nicht annehmen oder identifizieren.                                            |
| SecurityIdentification | Der Server kann die Identität und die Berechtigungen des Clients abrufen, aber keine Identität des Clients annehmen. |
| SecurityImpersonation  | Der Server kann die Identität des Sicherheitskontexts des Clients auf dem lokalen System annehmen.                    |
| SecurityDelegation     | Der Server kann die Identität des Sicherheitskontexts des Clients auf Remotesystemen annehmen.                      |



 

Der Client einer Named Pipe-, RPC- oder DDE-Verbindung kann die Identitätswechselebene steuern. Beispielsweise kann ein Named Pipe-Client die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aufrufen, um ein Handle für eine Named Pipe zu öffnen und die Identitätswechselebene des Servers anzugeben.

Wenn die Named Pipe-, RPC- oder DDE-Verbindung remote ist, werden die an [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) übergebenen Flags zum Festlegen der Identitätswechselebene ignoriert. In diesem Fall wird die Identitätswechselebene des Clients durch die vom Server aktivierten Identitätswechselebenen bestimmt, die durch ein Flag für das Konto des Servers im Verzeichnisdienst festgelegt wird. Wenn der Server beispielsweise für die Delegierung aktiviert ist, wird die Identitätswechselebene des Clients auch dann auf Delegierung festgelegt, wenn die an **CreateFile** übergebenen Flags die Identitätswechselebene angeben.

DDE-Clients verwenden die [**DdeSetQualityOfService-Funktion**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) mit der [**SECURITY QUALITY OF \_ \_ \_ SERVICE-Struktur,**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) um die Identitätswechselebene anzugeben. Die SecurityImpersonation-Ebene ist die Standardeinstellung für Named Pipe-, RPC- und DDE-Server. Mit den Funktionen [**ImpersonateSelf,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)und [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) kann der Aufrufer eine Identitätswechselebene angeben. Verwenden Sie die [**GetTokenInformation-Funktion,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) um die Identitätswechselebene eines [*Zugriffstokens*](/windows/desktop/SecGloss/a-gly)abzurufen.

Auf der SecurityImpersonation-Ebene erfolgen die meisten Aktionen des Threads im Sicherheitskontext des [*Identitätswechseltokens*](/windows/desktop/SecGloss/i-gly) des Threads und nicht im [*primären Token*](/windows/desktop/SecGloss/p-gly) des [*Prozesses,*](/windows/desktop/SecGloss/p-gly) der den Thread besitzt. Wenn beispielsweise ein Thread mit Identitätswechsel ein [sicherungsfähiges Objekt](securable-objects.md)öffnet, verwendet das System das Identitätswechseltoken, um den Zugriff des Threads zu überprüfen. Analog dazu ist der Besitzer des neuen Objekts der Standardbesitzer aus dem [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly)des Clients, wenn ein Thread, der die Identität an sich nimmt, ein neues -Objekt erstellt, z. B. durch Aufrufen der [**CreateFile-Funktion.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

In den folgenden Situationen verwendet das System jedoch das primäre Token des Prozesses anstelle des Identitätswechseltokens des aufrufenden Threads:

-   Wenn ein Identitätswechselthread die [**CreateProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) aufruft, erbt der neue Prozess immer das primäre Token des Prozesses.
-   Für Funktionen, die die SE \_ TCB \_ NAME-Berechtigung erfordern, z. B. die [**LogonUser-Funktion,**](/windows/desktop/api/winbase/nf-winbase-logonusera) überprüft das System immer im primären Token des Prozesses nach der Berechtigung.
-   Für Funktionen, die die SE \_ AUDIT \_ NAME-Berechtigung erfordern, z. B. die [**ObjectOpenAuditAlarm-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) überprüft das System immer im primären Token des Prozesses nach der Berechtigung.
-   In einem Aufruf der [**OpenThreadToken-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) kann ein Thread angeben, ob die Funktion das Identitätswechseltoken oder das primäre Token verwendet, um zu bestimmen, ob dem angeforderten Zugriff gewährt werden soll.

 

 
