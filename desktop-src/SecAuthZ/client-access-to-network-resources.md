---
description: Erläutert Strategien für den Zugriff auf Netzwerkressourcen.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Client Zugriff auf Netzwerkressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0873a10c708f9aab2e9c250375a63e8a2167873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343752"
---
# <a name="client-access-to-network-resources"></a>Client Zugriff auf Netzwerkressourcen

Ein Server kann die folgenden Strategien verwenden, um auf Netzwerkressourcen zuzugreifen:

-   Wenn der Server über den Kontonamen und das Kennwort eines Clients verfügt, kann er [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) mit den [*Anmelde*](/windows/desktop/SecGloss/c-gly) Informationen des Clients zum Zuordnen eines lokalen Laufwerk Buchstabens zu einer Netzwerkfreigabe verwenden.
-   Nach dem Aufruf von " [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) " mit Client Anmelde Informationen kann der Server die [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) -Funktion aufrufen, um [einen Prozess für den Client zu erstellen](processes-in-the-client-security-context.md). Dieser neue Client Prozess kann über den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly)des Clients auf Netzwerkressourcen zugreifen. Der Prozess kann z. b. die [**Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -Funktion" aufrufen, um eine Datei auf einem Remote Computer zu öffnen. Das System verwendet das [*primäre Token*](/windows/desktop/SecGloss/p-gly) des Clients, um Zugriffsversuche durch den Client Prozess zu überprüfen.
-   Ein Server kann [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) mit NULL-Anmelde Informationen aufrufen, um entweder eine Verbindung mit einer Netzwerkressource mit Server Zugriff oder einer Standardverbindung herzustellen. Wenn der Server unter dem Konto "LocalSystem" ausgeführt wird, wird er bei der Netzwerkressource im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Domänen Servers authentifiziert. Wenn der Server unter einem Dienst Konto ausgeführt wird, wird er als dieses Konto authentifiziert. Weitere Informationen finden Sie unter dem [Konto "LocalSystem](/windows/desktop/Services/localsystem-account)".

Weitere Informationen zum Schützen von Kenn Wörtern finden Sie unter Behandeln von Kenn [Wörtern](/windows/desktop/SecBP/handling-passwords). Weitere Informationen zum Abrufen von Anmelde Informationen finden Sie unter [anfordern von Anmelde Informationen für den Benutzer](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
