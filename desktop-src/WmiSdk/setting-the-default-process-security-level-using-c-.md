---
description: Wenn sich eine Client Anwendung zum ersten Mal bei Windows-Verwaltungsinstrumentation (WMI) anmeldet, muss Sie die Standardprozess-Sicherheitsstufe mit einem Aufruf von CoInitializeSecurity festlegen.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Festlegen der Standardprozess-Sicherheitsstufe mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530134"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Festlegen der Standardprozess-Sicherheitsstufe mithilfe von C++

Wenn sich eine Client Anwendung zum ersten Mal bei Windows-Verwaltungsinstrumentation (WMI) anmeldet, muss Sie die Standardprozess-Sicherheitsstufe mit einem Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)festlegen. COM verwendet die Informationen im-Befehl, um zu bestimmen, wie viel Sicherheit ein anderer Prozess benötigt, um auf den Client Anwendungsprozess zuzugreifen.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von C++](#changing-the-default-authentication-credentials-using-c)
-   [Ändern der standardmäßigen Identitätswechsel Ebenen mithilfe von C++](#changing-the-default-impersonation-levels-using-c)

Bei den meisten Client Anwendungen legen die im folgenden Beispiel gezeigten Argumente die Standard Sicherheit für WMI fest.


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



Der Code erfordert, dass die folgenden Verweise und \# include-Anweisungen ordnungsgemäß kompiliert werden.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



Wenn die Authentifizierungs Ebene auf die **RPC- \_ C- \_ authn- \_ Ebene \_** festgelegt wird, kann DCOM die Authentifizierungs Ebene so aushandeln, dass Sie den Sicherheitsanforderungen des Ziel Computers entspricht. Weitere Informationen finden Sie unter [Ändern der standardmäßigen Anmelde Informationen für die Authentifizierung mit C++](#changing-the-default-authentication-credentials-using-c) und [Ändern der Standardeinstellungen für Identitätswechsel mithilfe von C++](#changing-the-default-impersonation-levels-using-c).

## <a name="changing-the-default-authentication-credentials-using-c"></a>Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von C++

Die Standard Anmelde Informationen für die Authentifizierung funktionieren in den meisten Situationen, aber Sie müssen möglicherweise unterschiedliche Anmelde Informationen für die Authentifizierung verwenden. Beispielsweise können Sie die Verschlüsselung den Authentifizierungs Prozeduren hinzufügen.

In der folgenden Tabelle sind die verschiedenen Authentifizierungs Ebenen aufgeführt und beschrieben.



| Authentifizierungs Ebene                 | BESCHREIBUNG                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| Standardwert für RPC- \_ C- \_ authn \_ \_        | Standard-Sicherheits Authentifizierung.                                                      |
| RPC- \_ C- \_ authn- \_ Ebene \_ None           | Keine Authentifizierung                                                                    |
| RPC- \_ C \_ authn \_ Level \_ Connect        | Authentifizierung nur, wenn der Client eine Beziehung mit dem Server erstellt.           |
| RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf           | Authentifizierung immer dann, wenn der Server einen RPC empfängt.                                  |
| Pkt der RPC- \_ C- \_ authn- \_ Ebene \_            | Authentifizierung jedes Mal, wenn der Serverdaten von einem Client empfängt.                      |
| \_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_ | Authentifizierung, bei der keine Daten aus dem Paket geändert wurden.                        |
| \_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene   | Schließt alle vorherigen Authentifizierungs Ebenen ein und verschlüsselt den Wert jedes RPC-Aufrufs. |



 

Sie können die Standard Anmelde Informationen für die Authentifizierung für mehrere Benutzer angeben, indem Sie eine **einzige \_ Authentifizierungs \_ Listen** Struktur im *pauthlist* -Parameter von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)verwenden.

Im folgenden Codebeispiel wird gezeigt, wie die Anmelde Informationen für die Authentifizierung geändert werden.


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



## <a name="changing-the-default-impersonation-levels-using-c"></a>Ändern der standardmäßigen Identitätswechsel Ebenen mithilfe von C++

COM stellt Standard Sicherheitsstufen bereit, die aus der Systemregistrierung gelesen werden. Wenn jedoch nicht ausdrücklich geändert, legen die Registrierungs Einstellungen die Identitätswechsel Ebene zu niedrig fest, damit WMI funktioniert. In der Regel handelt es sich bei der standardmäßigen Identitätswechsel Ebene um **RPC- \_ c- \_ IMP \_ \_**-Ebene, aber WMI benötigt mindestens eine IP- **Ebene der RPC-c- \_ \_ \_ Ebene \_** , damit Sie mit den meisten Anbietern funktioniert, und es kann eine Situation auftreten, in der Sie eine höhere Identitätswechsel Ebene festlegen müssen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md). In der folgenden Tabelle sind die unterschiedlichen Ebenen des Identitäts Wechsels aufgeführt.



| Ebene                           | BESCHREIBUNG                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| Standardwert für RPC- \_ C- \_ \_ Ebene \_     | Das Betriebssystem wählt die Ebene des Identitäts Wechsels aus.                                                      |
| RPC- \_ C- \_ IMP- \_ Ebene \_ Anonym   | Der Server kann die Identität des Clients annehmen, aber das Identitätswechsel Token kann für nichts verwendet werden.               |
| RPC- \_ C- \_ IMP- \_ Stufe \_ identifizieren    | Der Server kann die Identität des Clients abrufen und die Identität des Clients für die ACL-Überprüfung annehmen.                 |
| Identitätswechsel auf RPC- \_ C- \_ \_ Ebene \_ | Der Server kann die Identität des Clients über eine Computer Grenze hinweg annehmen.                                           |
| RPC- \_ C- \_ IMP- \_ Stufen \_ Delegat    | Der Server kann die Identität des Clients über mehrere Grenzen hinweg annehmen und im Auftrag des Clients Anrufe tätigen. |



 

 

 
