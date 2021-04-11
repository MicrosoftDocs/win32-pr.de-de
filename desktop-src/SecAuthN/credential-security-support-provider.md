---
description: Das Credential Security Support Provider Protocol (kredssp) ist ein Sicherheits Unterstützungs Anbieter, der mithilfe der Security Support Provider-Schnittstelle (Security Support Provider Interface, SSPI) implementiert wird.
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Anmelde Informationsanbieter für Sicherheitsunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214991"
---
# <a name="credential-security-support-provider"></a>Anmelde Informationsanbieter für Sicherheitsunterstützung

Das Credential Security Support Provider Protocol (kredssp) ist ein Sicherheits Unterstützungs Anbieter, der mithilfe der Security Support Provider-Schnittstelle (Security Support Provider Interface,[SSPI](sspi.md)) implementiert wird. Mit "kredssp" kann eine Anwendung die Anmelde Informationen des Benutzers vom Client an den Zielserver für die Remote Authentifizierung delegieren. "Kredssp" stellt einen verschlüsselten [Transport Layer Security Protokoll](transport-layer-security-protocol.md) Kanal bereit. Der Client wird über den verschlüsselten Kanal authentifiziert, indem das Simple and Protected Aushandlungs Protokoll (spnetgo) mit [Microsoft Kerberos](microsoft-kerberos.md) oder [Microsoft NTLM](microsoft-ntlm.md)verwendet wird.

> [!Caution]  
> Dies ist keine eingeschränkte Delegierung. "Kredssp" übergibt die vollständigen Anmelde Informationen des Benutzers ohne Einschränkung an den Server.

 

Weitere Informationen zu spnetgo finden Sie unter [Microsoft aushandeln](microsoft-negotiate.md).

Nachdem Client und Server authentifiziert wurden, übergibt der Client die Anmelde Informationen des Benutzers an den Server. Die Anmelde Informationen werden doppelt unter den spnetgo-und TLS-Sitzungs Schlüsseln verschlüsselt. "Kredssp" unterstützt die Kenn Wort basierte Anmeldung sowie die Smartcard-Anmeldung basierend auf " [*X. 509*](/windows/desktop/SecGloss/x-gly) " und "PKINIT".

> [!IMPORTANT]
> WOW64-Clients werden von "kredssp" nicht unterstützt.

 

Weitere Informationen zu "kredssp" finden Sie in den folgenden Themen.



| Thema                                                                         | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Einstellungen für den Gruppenrichtlinie ""](credssp-group-policy-settings.md)<br/> | Die Delegierung von Anmelde Informationen durch das-Skript kann mithilfe von Gruppenrichtlinien Einstellungen gesteuert werden.<br/> |



 

 

