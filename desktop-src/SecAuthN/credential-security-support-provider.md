---
description: Das Credential Security Support Provider-Protokoll (CredSSP) ist ein Sicherheitssupportanbieter, der mithilfe der Security Support Provider Interface (SSPI) implementiert wird.
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Anmeldeinformationssicherheits-Supportanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4059da0dcc1e6c963ab011ad03415175849191374732f3d1df395914aebe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008738"
---
# <a name="credential-security-support-provider"></a>Anmeldeinformationssicherheits-Supportanbieter

Das Credential Security Support Provider-Protokoll (CredSSP) ist ein Sicherheitssupportanbieter, der mithilfe der Security Support Provider Interface[(SSPI)](sspi.md)implementiert wird. CredSSP ermöglicht einer Anwendung, die Anmeldeinformationen des Benutzers für die Remoteauthentifizierung vom Client an den Zielserver zu delegieren. CredSSP stellt einen verschlüsselten [Transport Layer Security Protokollkanal](transport-layer-security-protocol.md) bereit. Der Client wird über den verschlüsselten Kanal authentifiziert, indem das SPNEGO-Protokoll (Simple and Protected Negotiate) mit [Microsoft Kerberos](microsoft-kerberos.md) oder [Microsoft NTLM](microsoft-ntlm.md)verwendet wird.

> [!Caution]  
> Dies ist keine eingeschränkte Delegierung. CredSSP übergibt die vollständigen Anmeldeinformationen des Benutzers ohne Einschränkung an den Server.

 

Informationen zu SPNEGO finden Sie unter [Microsoft Negotiate](microsoft-negotiate.md).

Nachdem der Client und der Server authentifiziert wurden, übergibt der Client die Anmeldeinformationen des Benutzers an den Server. Die Anmeldeinformationen werden doppelt unter den SPNEGO- und TLS-Sitzungsschlüsseln verschlüsselt. CredSSP unterstützt sowohl die kennwortbasierte Anmeldung als auch die Smartcardanmeldung basierend auf [*X.509*](/windows/desktop/SecGloss/x-gly) und PKINIT.

> [!IMPORTANT]
> CredSSP unterstützt keine Wow64-Clients.

 

Weitere Informationen zu CredSSP finden Sie in den folgenden Themen.



| Thema                                                                         | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [CredSSP-Gruppenrichtlinie Einstellungen](credssp-group-policy-settings.md)<br/> | Die Delegierung von Anmeldeinformationen durch CredSSP kann mithilfe von Gruppenrichtlinieneinstellungen gesteuert werden.<br/> |



 

 

