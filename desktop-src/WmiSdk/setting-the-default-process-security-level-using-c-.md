---
description: Wenn sich eine Clientanwendung zum ersten Mal bei Windows Management Instrumentation (WMI) anmeldet, muss sie die Standardprozesssicherheitsstufe mit einem Aufruf von CoInitializeSecurity festlegen.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Festlegen der Standardprozesssicherheitsstufe mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcaec4ebbcd39c8cee9ee8aae002621a4a5a1853d1e4cfd4282194115c15ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050288"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Festlegen der Standardprozesssicherheitsstufe mit C++

Wenn sich eine Clientanwendung zum ersten Mal bei Windows Management Instrumentation (WMI) anmeldet, muss sie die Standardprozesssicherheitsstufe mit einem Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)festlegen. COM verwendet die Informationen im Aufruf, um zu bestimmen, wie viel Sicherheit ein anderer Prozess für den Zugriff auf den Clientanwendungsprozess haben muss.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Ändern der Standardanmeldeinformationen für die Authentifizierung mit C++](#changing-the-default-authentication-credentials-using-c)
-   [Ändern der Standardidentitätswechselebenen mit C++](#changing-the-default-impersonation-levels-using-c)

Für die meisten Clientanwendungen legen die im folgenden Beispiel gezeigten Argumente die Standardsicherheit für WMI fest.


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



Der Code erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



Wenn Sie die Authentifizierungsebene auf **RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT** festlegen, kann DCOM die Authentifizierungsebene entsprechend den Sicherheitsanforderungen des Zielcomputers aushandeln. Weitere Informationen finden Sie unter [Ändern der Standardauthentifizierungsanmeldeinformationen mit C++](#changing-the-default-authentication-credentials-using-c) und [Ändern des Standardidentitätswechsels Einstellungen Verwenden von C++.](#changing-the-default-impersonation-levels-using-c)

## <a name="changing-the-default-authentication-credentials-using-c"></a>Ändern der Standardanmeldeinformationen für die Authentifizierung mit C++

Die Standardanmeldeinformationen für die Authentifizierung funktionieren in den meisten Situationen, aber Sie müssen möglicherweise in unterschiedlichen Situationen unterschiedliche Authentifizierungsanmeldeinformationen verwenden. Beispielsweise können Sie den Authentifizierungsverfahren Verschlüsselung hinzufügen.

In der folgenden Tabelle werden die verschiedenen Authentifizierungsebenen aufgelistet und beschrieben.



| Authentifizierungsebene                 | Beschreibung                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT        | Standardsicherheitsauthentifizierung.                                                      |
| RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           | Keine Authentifizierung                                                                    |
| RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        | Authentifizierung nur, wenn der Client eine Beziehung mit dem Server erstellt.           |
| RPC \_ \_ \_ C-AUFRUF AUF AUTHENTIFIZIERUNGSEBENE \_           | Authentifizierung jedes Mal, wenn der Server einen RPC empfängt.                                  |
| RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            | Authentifizierung jedes Mal, wenn der Server Daten von einem Client empfängt.                      |
| \_ \_ \_ \_ PKT-INTEGRITÄT AUF RPC-C-AUTHENTIFIZIERUNGSEBENE \_ | Authentifizierung, dass keine Daten aus dem Paket geändert wurden.                        |
| RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   | Schließt alle vorherigen Authentifizierungsebenen ein und verschlüsselt den Wert jedes RPC-Aufrufs. |



 

Sie können die Standardauthentifizierungsanmeldeinformationen für mehrere Benutzer angeben, indem Sie im *pAuthList-Parameter* von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)eine **SOLE AUTHENTICATION \_ \_ LIST-Struktur** verwenden.

Das folgende Codebeispiel zeigt, wie die Anmeldeinformationen für die Authentifizierung geändert werden.


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a>Ändern der Standardidentitätswechselebenen mit C++

COM stellt Standardsicherheitsstufen bereit, die aus der Systemregistrierung gelesen werden. Sofern nicht ausdrücklich geändert, legen die Registrierungseinstellungen die Identitätswechselebene jedoch zu niedrig fest, damit WMI funktioniert. In der Regel ist die Standardidentitätswechselebene **RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY**. WMI benötigt jedoch mindestens **RPC C \_ \_ IMP LEVEL \_ \_ IMPERSONATE,** um mit den meisten Anbietern zu funktionieren, und es kann vorkommen, dass Sie eine höhere Ebene des Identitätswechsels festlegen müssen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md) In der folgenden Tabelle sind die verschiedenen Identitätswechselebenen aufgeführt.



| Ebene                           | Beschreibung                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| RPC \_ C \_ IMP \_ LEVEL \_ DEFAULT     | Das Betriebssystem wählt die Ebene des Identitätswechsels aus.                                                      |
| RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   | Der Server kann die Identität des Clients annehmen, aber das Identitätswechseltoken kann für nichts verwendet werden.               |
| RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY    | Der Server kann die Identität des Clients abrufen und die Identität des Clients für die ACL-Überprüfung annehmen.                 |
| RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE | Der Server kann die Identität des Clients über eine Computergrenze hinweg annehmen.                                           |
| RPC \_ C \_ IMP \_ LEVEL \_ DELEGATE    | Der Server kann die Identität des Clients über mehrere Grenzen hinweg annehmen und Aufrufe im Namen des Clients durchführen. |



 

 

 
