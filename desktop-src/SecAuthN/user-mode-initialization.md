---
description: Verteilte Anwendungen (Client/Server) verwenden Sicherheitspakete, um authentifizierte Verbindungen zu erhalten und Nachrichten zu austauschen.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Initialisierung des Benutzermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be7c4c00937473e2ecc3d6b01bb7c59a2842085a133f381b5a8a10bd9b215f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915582"
---
# <a name="user-mode-initialization"></a>Initialisierung des Benutzermodus

Verteilte Anwendungen (Client/Server) verwenden [*Sicherheitspakete,*](../secgloss/s-gly.md) um authentifizierte Verbindungen zu erhalten und Nachrichten zu austauschen. Die Anwendung ruft SSPI-Funktionen (Security Support Provider Interface) auf, die funktionen zugeordnet sind, die von [SSP/APs](authentication-functions.md)implementiert werden, sowie Funktionen, die von [SSP/APs](authentication-functions.md)im Benutzermodus implementiert werden. Diese Zuordnung wird von der Sicherheitsanbieter-DLL (Secur32.dll oder Security.dll) durchgeführt, die dynamisch in die Client- und Serverprozesse geladen werden kann. Die DLL kann auch statisch mit Secur32.lib verknüpft werden. Sowohl die DLL als auch LIB sind im Microsoft Windows Software Development Kit (SDK) enthalten.

Das Laden des Sicherheitspakets in den Client- oder Serverprozess wird vom System verarbeitet, wenn die SSP/AP-DLL, die das Sicherheitspaket enthält, ordnungsgemäß registriert ist.

Der Server beginnt mit dem Herstellen einer sicheren Verbindung mit einem Client, indem er einen Port überwacht und darauf wartet, dass ein Client eine Nachricht sendet. Der Client beginnt mit dem Abrufen einer sicheren Verbindung mit dem Server, indem er die SSPI-Funktion [**InitializeSecurityContext (Allgemein) aufruft.**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Diese Funktion wird der [**SpInitLsaModeContext-Funktion**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) des benutzerdefinierten Sicherheitspakets zugeordnet. **SpInitLsaModeContext** gibt ein Token an den Client zurück, der es an den Server weitergibt.

Nach dem Empfang des Tokens vom Client ruft der Server die SSPI-Funktion [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)auf, die an die [**SpAcceptLsaModeContext-Funktion**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) des Sicherheitspakets gesendet wird. Wenn die **SpAcceptLsaModeContext-Funktion** erfolgreich ist und keine weitere Verarbeitung erforderlich ist, um den Sicherheitskontext zu erstellen, sollte die Funktion STATUS SUCCESS an den Aufrufer \_ zurückgeben. Wenn zusätzliche Verarbeitung erforderlich ist, sollte die Funktion SEC I CONTINUE NEEDED und ein Token an \_ \_ den Server \_ zurückgeben. Der Server gibt das Token an den Client weiter, der [**InitializeSecurityContext (Allgemein) erneut**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) aufruft.

Dieser Aufrufzyklus kann so oft wie nötig wiederholt werden, bis eine authentifizierte Verbindung hergestellt wird oder fehlschlägt. Wenn während dieses Prozesses die [**SpAcceptLsaModeContext-**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) oder [**SpInitLsaModeContext-Funktion**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) erfolgreich ist und keine weitere Verarbeitung erforderlich ist, um den Sicherheitskontext zu [*erstellen,*](../secgloss/s-gly.md)sollte die Funktion STATUS SUCCESS an den \_ Aufrufer zurückgeben. Wenn zusätzliche Verarbeitung erforderlich ist, sollte die Funktion SEC I CONTINUE NEEDED zurückgeben und ein Token an den Aufrufer zurückgeben, der für die \_ \_ Weiterleitung verantwortlich \_ ist.

Das vom Sicherheitspaket implementierte Protokoll bestimmt, wie oft dieser Zyklus wiederholt wird. In Sicherheitspaketen, die die gegenseitige Drei-Bei-Authentifizierung unterstützen, lautet die aufrufende Sequenz beispielsweise wie folgt:

1.  Der Client ruft ein Token durch Aufrufen von [**InitializeSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)ab und sendet es an den Server. Der Server ruft [**AcceptSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) zum ersten Mal auf und ruft ein Antworttoken ab, das er an den Client sendet.
2.  Der Client verwendet das token, das vom Server in einem zweiten Aufruf von [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)empfangen wurde, und ruft ein endgültiges Token ab. Der Client sendet dieses Token an den Server.
3.  Der Server empfängt das in Abschnitt 2 generierte Token, das er im letzten Aufruf von [**AcceptSecurityContext (General) verwendet.**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Wenn die [**Funktionen SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) und [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) erfolgreich sind und keine weitere Verarbeitung erforderlich ist, um den Sicherheitskontext zu erstellen, sollten die Funktionen STATUS SUCCESS an den \_ Aufrufer zurückgeben. Darüber hinaus müssen **SpAcceptLsaModeContext** und **SpInitLsaModeContext** **über** den *MappedContext-Parameter TRUE* zurückgeben, wenn das benutzerdefinierte Sicherheitspaket die von [SSP/APs](authentication-functions.md)im Benutzermodus implementierten Funktionen unterstützt. Der *MappedContext-Wert* wird nicht an die Anwendung übergeben. sie wird vom LSA abgefangen.

Wenn *MappedContext* true **ist,** ruft das LSA die [**SpUsermodeInitialize-Funktion**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) der SSP/AP-DLL auf. Diese Funktion stellt Tabellen mit Zeigern auf die Benutzermodusfunktionen zur Verfügung, die von den einzelnen Sicherheitspaketen implementiert werden. Die [**SpInstanceInit-Funktion jedes**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) Pakets wird mithilfe der von **SpUsermodeInitialize zurückgegebenen Funktionstabellen aufgerufen.** **SpInstanceInit empfängt** eine Tabelle mit Zeigern auf LSA-Funktionen, die von [SSP/APs im Benutzermodus aufgerufen werden.](authentication-functions.md)

 

 
