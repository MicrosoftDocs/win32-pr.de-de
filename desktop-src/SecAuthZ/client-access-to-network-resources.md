---
description: Erläutert Strategien für den Zugriff auf Netzwerkressourcen.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Clientzugriff auf Netzwerkressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a8886f474876080703d190efb3419d099027f24af17dd735736957452318e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783076"
---
# <a name="client-access-to-network-resources"></a>Clientzugriff auf Netzwerkressourcen

Ein Server kann die folgenden Strategien verwenden, um auf Netzwerkressourcen zuzugreifen:

-   Wenn der Server über den Kontonamen und das Kennwort eines Clients verfügt, kann er [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) mit den [*Anmeldeinformationen*](/windows/desktop/SecGloss/c-gly) des Clients aufrufen, um einer Netzwerkfreigabe einen lokalen Laufwerkbuchstaben zuzuordnen.
-   Nach dem Aufrufen von [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) mit Clientanmeldeinformationen kann der Server die [**CreateProcessAsUser-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) aufrufen, um einen Prozess für den Client zu [erstellen.](processes-in-the-client-security-context.md) Dieser neue Clientprozess kann über den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly)des Clients auf Netzwerkressourcen zugreifen. Beispielsweise kann der Prozess die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aufrufen, um eine Datei auf einem Remotecomputer zu öffnen. Das System verwendet das [*primäre Token*](/windows/desktop/SecGloss/p-gly) des Clients, um Zugriffsversuche durch den Clientprozess zu überprüfen.
-   Ein Server kann [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) mit NULL-Anmeldeinformationen aufrufen, um entweder eine Verbindung mit einer Netzwerkressource mit Serverzugriff oder eine Standardverbindung herzustellen. Wenn der Server als LocalSystem-Konto ausgeführt wird, authentifiziert er sich bei der Netzwerkressource im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Domänenservers. Wenn der Server unter einem Dienstkonto ausgeführt wird, wird er als dieses Konto authentifiziert. Weitere Informationen finden Sie unter [LocalSystem Account](/windows/desktop/Services/localsystem-account).

Informationen zum Schutz von Kennwörtern finden Sie unter [Behandeln von Kennwörtern.](/windows/desktop/SecBP/handling-passwords) Informationen zum Abrufen von Anmeldeinformationen finden Sie unter [Fragen des Benutzers nach Anmeldeinformationen.](/windows/desktop/SecBP/asking-the-user-for-credentials)

 

 
