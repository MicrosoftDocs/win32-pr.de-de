---
description: Ein Server mit der \_ namens Berechtigung "SE TCB", z. b. \_ ein Windows-Dienst, der im Konto "LocalSystem" ausgeführt wird, kann die Funktion "LogonUser" zum Authentifizieren eines Clients auf dem Computer, auf dem der Server ausgeführt wird, abrufen.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Client Anmelde Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1439b27637b0e46df3b468b42cb9c45ac8f759f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527641"
---
# <a name="client-logon-sessions"></a>Client Anmelde Sitzungen

Ein Server mit der \_ namens Berechtigung "SE TCB", z. b. \_ ein Windows-Dienst, der im [Konto "LocalSystem](/windows/desktop/Services/localsystem-account)" ausgeführt wird, kann die Funktion " [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) " zum [*Authentifizieren*](/windows/desktop/SecGloss/a-gly) eines Clients auf dem Computer, auf dem der Server ausgeführt wird, abrufen. Die **LogonUser** -Funktion startet eine neue Anmelde [*Sitzung*](/windows/desktop/SecGloss/s-gly) und gibt ein [*Primäres Zugriffs Token*](/windows/desktop/SecGloss/p-gly) zurück, das die Sicherheitsinformationen des Clients enthält. Sie können dieses primäre Token verwenden, [**um die Identität**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) des Clients anzunehmen oder die Funktion [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) aufrufen, um einen Prozess zu erstellen, der im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Clients ausgeführt wird.

Der Vorteil der Authentifizierung des Clients auf diese Weise besteht darin, dass der Server, der die Identität des authentifizierten Clients annimmt, oder ein [*Prozess*](/windows/desktop/SecGloss/p-gly) , der im Kontext des authentifizierten Clients erstellt wurde, eine Verbindung mit Remote Netzwerkressourcen als Client herstellen kann. Wenn diese Authentifizierung nicht durchgeführt wird, kann der Server nur dann eine Verbindung mit Netzwerkressourcen herstellen, wenn er den Kontonamen und das Kennwort des Clients abgerufen hat, die an die [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) -Funktion übergeben werden.

Der Nachteil der Client Authentifizierung auf diese Weise besteht darin, dass der Server die [*Anmelde*](/windows/desktop/SecGloss/c-gly) Informationen des Clients (Domänen Name, Benutzername und Kennwort) abgerufen haben muss. Wenn ein Remote Client diese Anmelde Informationen für den Server bereitstellt, liegt es in der Verantwortung des Clients und des Servers, sicherzustellen, dass die Anmelde Informationen auf sichere Weise übermittelt werden.

 

 
