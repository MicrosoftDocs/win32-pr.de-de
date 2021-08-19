---
description: Ein Server mit der berechtigung SE \_ TCB \_ NAME, z. B. ein Windows Dienst, der im LocalSystem-Konto ausgeführt wird, kann die LogonUser-Funktion aufrufen, um einen Client auf dem Computer zu authentifizieren, auf dem der Server ausgeführt wird.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Clientanmeldungssitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baafdc46800cc5b334a5496be5502b97e18d4702bdf9b839d8431a92110c3d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783022"
---
# <a name="client-logon-sessions"></a>Clientanmeldungssitzungen

Ein Server mit der berechtigung SE \_ TCB \_ NAME, z. B. ein Windows Dienst, der im [LocalSystem-Konto](/windows/desktop/Services/localsystem-account)ausgeführt wird, kann die [**LogonUser-Funktion**](/windows/desktop/api/winbase/nf-winbase-logonusera) aufrufen, um einen Client auf dem Computer zu [*authentifizieren,*](/windows/desktop/SecGloss/a-gly) auf dem der Server ausgeführt wird. Die **LogonUser-Funktion** startet eine neue [*Anmeldesitzung*](/windows/desktop/SecGloss/s-gly) und gibt ein [*primäres Zugriffstoken*](/windows/desktop/SecGloss/p-gly) zurück, das die Sicherheitsinformationen des Clients enthält. Sie können dieses primäre Token verwenden, um die [**Funktion ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) aufzurufen, um die Identität des Clients zu annehmen, oder indem Sie die [**CreateProcessAsUser-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) aufrufen, um einen Prozess zu erstellen, der im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Clients ausgeführt wird.

Der Vorteil der Authentifizierung des Clients auf diese Weise besteht darin, dass der Server, der die Identität des authentifizierten Clients an sich nimmt, oder ein [*Prozess,*](/windows/desktop/SecGloss/p-gly) der im Kontext des authentifizierten Clients erstellt wurde, eine Verbindung mit Remotenetzwerkressourcen als Client herstellen kann. Wenn diese Authentifizierung nicht erfolgt, kann der Server nur dann eine Verbindung mit Netzwerkressourcen herstellen, wenn er den Kontonamen und das Kennwort des Clients für die Übergabe an die [**WNetAddConnection2-Funktion**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) erhalten hat.

Der Nachteil der Authentifizierung des Clients auf diese Weise besteht darin, dass der Server die [*Anmeldeinformationen*](/windows/desktop/SecGloss/c-gly) des Clients (Domänenname, Benutzername und Kennwort) erhalten haben muss. Wenn ein Remoteclient diese Anmeldeinformationen an den Server übermittelt, liegt es in der Verantwortung des Clients und Servers, sicherzustellen, dass die Anmeldeinformationen sicher übertragen werden.

 

 
