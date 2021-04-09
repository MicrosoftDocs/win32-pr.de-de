---
description: Verteilte (Client/Server) Anwendungen verwenden Sicherheitspakete zum Abrufen authentifizierter Verbindungen und zum Austauschen von Nachrichten.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Benutzermodusinitialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b06daf2e1c3612b02583d203ce4cd9afebabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960332"
---
# <a name="user-mode-initialization"></a>Benutzermodusinitialisierung

Verteilte (Client/Server) Anwendungen verwenden [*Sicherheitspakete*](../secgloss/s-gly.md) zum Abrufen authentifizierter Verbindungen und zum Austauschen von Nachrichten. Die Anwendung ruft Security Support Provider Schnittstellen Funktionen (SSPI) auf, die von [SSP/APS implementierte Funktionen](authentication-functions.md)zugeordnet sind, sowie Funktionen, die [von SSP/APS im Benutzermodus implementiert](authentication-functions.md)werden. Diese Zuordnung wird von der Sicherheitsanbieter-dll (Secur32.dll oder Security.dll) ausgeführt, die in die Client-und Server Prozesse dynamisch geladen werden kann. Die dll kann auch statisch mit Secur32. lib verknüpft werden. Sowohl die dll als auch die lib werden mit dem Microsoft Windows Software Development Kit (SDK) ausgeliefert.

Das Laden des Sicherheitspakets in den Client-oder Server Prozess wird vom System übernommen, wenn die SSP/AP-dll, die das Sicherheitspaket enthält, ordnungsgemäß registriert ist.

Der Server beginnt mit dem Abrufen einer sicheren Verbindung mit einem Client, indem er einen Port überwacht und darauf wartet, dass ein Client eine Nachricht sendet. Der Client beginnt mit dem Abrufen einer sicheren Verbindung zum Server durch Aufrufen der SSPI-Funktion [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Diese Funktion wird der [**spinitlsamodecontext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) -Funktion des benutzerdefinierten Sicherheitspakets zugeordnet. **Spinitlsamodecontext** gibt ein Token an den Client zurück, das es an den Server weiterleitet.

Wenn das Token vom Client empfangen wird, ruft der Server die SSPI-Funktion " [**Accept-SecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)" auf, die an die [**spaccept tlsamodecontext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) -Funktion des Sicherheitspakets gesendet wird. Wenn die **spaccept tlsamodecontext** -Funktion erfolgreich ist und keine weitere Verarbeitung erforderlich ist, um den Sicherheitskontext einzurichten, sollte die Funktion den Status Erfolg an den Aufrufer zurückgeben \_ . Wenn eine zusätzliche Verarbeitung erforderlich ist, sollte die Funktion Sekunden zurückgeben \_ , die ich \_ weiterhin \_ benötigter, und ein Token an den Server zurückgeben. Der Server leitet das Token an den Client weiter, der [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) erneut aufruft.

Dieser aufrufende Cycle kann so oft wie nötig wiederholt werden, bis eine authentifizierte Verbindung hergestellt ist oder fehlschlägt. Wenn während dieses Vorgangs die [**spaccept tlsamodecontext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) -oder [**spinitlsamodecontext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) -Funktion erfolgreich ausgeführt wird und keine weitere Verarbeitung erforderlich ist, um den [*Sicherheitskontext*](../secgloss/s-gly.md)einzurichten, sollte die Funktion den Status \_ Erfolg an den Aufrufer zurückgeben. Wenn eine zusätzliche Verarbeitung erforderlich ist, sollte die Funktion Sekunden zurückgeben, die \_ ich \_ weiterhin \_ benötigter, und ein Token an den Aufrufer zurückgeben, der für die Weiterleitung verantwortlich ist.

Das Protokoll, das vom Sicherheitspaket implementiert wird, bestimmt, wie oft dieser Cycle wiederholt wird. Beispielsweise ist in Sicherheitspaketen, die die dreiseitige gegenseitige Authentifizierung unterstützen, die Aufruf Sequenz wie folgt:

1.  Der Client ruft ein Token durch Aufrufen von [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)ab und sendet ihn an den Server. Der Server Ruft beim ersten Mal " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " auf und ruft ein Antwort Token zurück, das an den Client gesendet wird.
2.  Der Client verwendet das Token, das vom Server in einem zweiten [**callalizesecuritycontext-Befehl (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)empfangen wurde, und ruft ein endgültiges Token ab. Der Client sendet dieses Token an den Server.
3.  Der Server empfängt das in "bin 2" generierte Token, das im letzten Abruf von " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)" verwendet wird.

Wenn die [**spaccept tlsamodecontext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) -Funktion und die [**spinitlsamodecontext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) -Funktion erfolgreich sind und keine weitere Verarbeitung erforderlich ist, um den Sicherheitskontext einzurichten, sollten die Funktionen dem Aufrufer den Status Erfolg zurückgeben \_ . Wenn das benutzerdefinierte Sicherheitspaket die Funktionen unterstützt, die [von SSP/APS im Benutzermodus implementiert](authentication-functions.md)werden, muss **spaccept tlsamodecontext** und **spinitlsamodecontext** über den *mappedcontext* -Parameter **true** zurückgeben. Der *mappedcontext* -Wert wird nicht an die Anwendung zurückgegeben. Sie wird von der LSA abgefangen.

Wenn *mappedcontext* auf **true** festgelegt ist, ruft die LSA die [**spusermodeinitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) -Funktion der SSP/AP-dll auf. Diese Funktion stellt Tabellen mit Zeigern für die Benutzermodus-Funktionen bereit, die von den einzelnen Sicherheitspaketen implementiert werden. Die [**spinstanceiniit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) -Funktion jedes Pakets wird mithilfe der von **spusermodeinitialize** zurückgegebenen Funktionstabellen aufgerufen. **Spinstanceinit** empfängt eine Tabelle mit Zeigern auf [LSA-Funktionen, die von SSP/APS im Benutzermodus aufgerufen werden](authentication-functions.md).

 

 
