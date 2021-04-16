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
# <a name="setting-the-default-process-security-level-using-c"></a><span data-ttu-id="32f02-103">Festlegen der Standardprozess-Sicherheitsstufe mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="32f02-103">Setting the Default Process Security Level Using C++</span></span>

<span data-ttu-id="32f02-104">Wenn sich eine Client Anwendung zum ersten Mal bei Windows-Verwaltungsinstrumentation (WMI) anmeldet, muss Sie die Standardprozess-Sicherheitsstufe mit einem Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)festlegen.</span><span class="sxs-lookup"><span data-stu-id="32f02-104">When a client application logs on to Windows Management Instrumentation (WMI) for the first time, it must set the default process security level with a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="32f02-105">COM verwendet die Informationen im-Befehl, um zu bestimmen, wie viel Sicherheit ein anderer Prozess benötigt, um auf den Client Anwendungsprozess zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="32f02-105">COM uses the information in the call to determine how much security another process must have to access the client application process.</span></span>

<span data-ttu-id="32f02-106">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="32f02-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="32f02-107">Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="32f02-107">Changing the Default Authentication Credentials Using C++</span></span>](#changing-the-default-authentication-credentials-using-c)
-   [<span data-ttu-id="32f02-108">Ändern der standardmäßigen Identitätswechsel Ebenen mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="32f02-108">Changing the Default Impersonation Levels Using C++</span></span>](#changing-the-default-impersonation-levels-using-c)

<span data-ttu-id="32f02-109">Bei den meisten Client Anwendungen legen die im folgenden Beispiel gezeigten Argumente die Standard Sicherheit für WMI fest.</span><span class="sxs-lookup"><span data-stu-id="32f02-109">For most client applications the arguments shown in the following example set the default security for WMI.</span></span>


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



<span data-ttu-id="32f02-110">Der Code erfordert, dass die folgenden Verweise und \# include-Anweisungen ordnungsgemäß kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="32f02-110">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="32f02-111">Wenn die Authentifizierungs Ebene auf die **RPC- \_ C- \_ authn- \_ Ebene \_** festgelegt wird, kann DCOM die Authentifizierungs Ebene so aushandeln, dass Sie den Sicherheitsanforderungen des Ziel Computers entspricht.</span><span class="sxs-lookup"><span data-stu-id="32f02-111">Setting the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** allows DCOM to negotiate the authentication level to match the security demands of the target computer.</span></span> <span data-ttu-id="32f02-112">Weitere Informationen finden Sie unter [Ändern der standardmäßigen Anmelde Informationen für die Authentifizierung mit C++](#changing-the-default-authentication-credentials-using-c) und [Ändern der Standardeinstellungen für Identitätswechsel mithilfe von C++](#changing-the-default-impersonation-levels-using-c).</span><span class="sxs-lookup"><span data-stu-id="32f02-112">For more information, see [Changing the Default Authentication Credentials Using C++](#changing-the-default-authentication-credentials-using-c) and [Changing the Default Impersonation Settings Using C++](#changing-the-default-impersonation-levels-using-c).</span></span>

## <a name="changing-the-default-authentication-credentials-using-c"></a><span data-ttu-id="32f02-113">Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="32f02-113">Changing the Default Authentication Credentials Using C++</span></span>

<span data-ttu-id="32f02-114">Die Standard Anmelde Informationen für die Authentifizierung funktionieren in den meisten Situationen, aber Sie müssen möglicherweise unterschiedliche Anmelde Informationen für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="32f02-114">The default authentication credentials work for most situations, but you might need to use different authentication credentials in different situations.</span></span> <span data-ttu-id="32f02-115">Beispielsweise können Sie die Verschlüsselung den Authentifizierungs Prozeduren hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="32f02-115">For example, you might want to add encryption to the authentication procedures.</span></span>

<span data-ttu-id="32f02-116">In der folgenden Tabelle sind die verschiedenen Authentifizierungs Ebenen aufgeführt und beschrieben.</span><span class="sxs-lookup"><span data-stu-id="32f02-116">The following table lists and describes the different levels of authentication.</span></span>



| <span data-ttu-id="32f02-117">Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="32f02-117">Authentication level</span></span>                 | <span data-ttu-id="32f02-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32f02-118">Description</span></span>                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32f02-119">Standardwert für RPC- \_ C- \_ authn \_ \_</span><span class="sxs-lookup"><span data-stu-id="32f02-119">RPC\_C\_AUTHN\_LEVEL\_DEFAULT</span></span>        | <span data-ttu-id="32f02-120">Standard-Sicherheits Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="32f02-120">Default security authentication.</span></span>                                                      |
| <span data-ttu-id="32f02-121">RPC- \_ C- \_ authn- \_ Ebene \_ None</span><span class="sxs-lookup"><span data-stu-id="32f02-121">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="32f02-122">Keine Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="32f02-122">No authentication.</span></span>                                                                    |
| <span data-ttu-id="32f02-123">RPC- \_ C \_ authn \_ Level \_ Connect</span><span class="sxs-lookup"><span data-stu-id="32f02-123">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        | <span data-ttu-id="32f02-124">Authentifizierung nur, wenn der Client eine Beziehung mit dem Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="32f02-124">Authentication only when the client creates a relationship with the server.</span></span>           |
| <span data-ttu-id="32f02-125">RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf</span><span class="sxs-lookup"><span data-stu-id="32f02-125">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           | <span data-ttu-id="32f02-126">Authentifizierung immer dann, wenn der Server einen RPC empfängt.</span><span class="sxs-lookup"><span data-stu-id="32f02-126">Authentication each time the server receives an RPC.</span></span>                                  |
| <span data-ttu-id="32f02-127">Pkt der RPC- \_ C- \_ authn- \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="32f02-127">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            | <span data-ttu-id="32f02-128">Authentifizierung jedes Mal, wenn der Serverdaten von einem Client empfängt.</span><span class="sxs-lookup"><span data-stu-id="32f02-128">Authentication each time the server receives data from a client.</span></span>                      |
| <span data-ttu-id="32f02-129">\_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_</span><span class="sxs-lookup"><span data-stu-id="32f02-129">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="32f02-130">Authentifizierung, bei der keine Daten aus dem Paket geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="32f02-130">Authentication that no data from the packet has been modified.</span></span>                        |
| <span data-ttu-id="32f02-131">\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene</span><span class="sxs-lookup"><span data-stu-id="32f02-131">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="32f02-132">Schließt alle vorherigen Authentifizierungs Ebenen ein und verschlüsselt den Wert jedes RPC-Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="32f02-132">Includes all previous authentication levels, and encrypts the value of each RPC call.</span></span> |



 

<span data-ttu-id="32f02-133">Sie können die Standard Anmelde Informationen für die Authentifizierung für mehrere Benutzer angeben, indem Sie eine **einzige \_ Authentifizierungs \_ Listen** Struktur im *pauthlist* -Parameter von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)verwenden.</span><span class="sxs-lookup"><span data-stu-id="32f02-133">You can specify the default authentication credentials for multiple users by using a **SOLE\_AUTHENTICATION\_LIST** structure in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="32f02-134">Im folgenden Codebeispiel wird gezeigt, wie die Anmelde Informationen für die Authentifizierung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="32f02-134">The following code example shows how to change the authentication credentials.</span></span>


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



## <a name="changing-the-default-impersonation-levels-using-c"></a><span data-ttu-id="32f02-135">Ändern der standardmäßigen Identitätswechsel Ebenen mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="32f02-135">Changing the Default Impersonation Levels Using C++</span></span>

<span data-ttu-id="32f02-136">COM stellt Standard Sicherheitsstufen bereit, die aus der Systemregistrierung gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="32f02-136">COM provides default security levels read from the system registry.</span></span> <span data-ttu-id="32f02-137">Wenn jedoch nicht ausdrücklich geändert, legen die Registrierungs Einstellungen die Identitätswechsel Ebene zu niedrig fest, damit WMI funktioniert.</span><span class="sxs-lookup"><span data-stu-id="32f02-137">However, unless specifically modified, the registry settings set the impersonation level too low for WMI to function.</span></span> <span data-ttu-id="32f02-138">In der Regel handelt es sich bei der standardmäßigen Identitätswechsel Ebene um **RPC- \_ c- \_ IMP \_ \_**-Ebene, aber WMI benötigt mindestens eine IP- **Ebene der RPC-c- \_ \_ \_ Ebene \_** , damit Sie mit den meisten Anbietern funktioniert, und es kann eine Situation auftreten, in der Sie eine höhere Identitätswechsel Ebene festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="32f02-138">Typically, the default impersonation level is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, but WMI needs at least **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** to function with most providers, and you might encounter a situation where you need to set a higher level of impersonation.</span></span> <span data-ttu-id="32f02-139">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="32f02-139">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="32f02-140">In der folgenden Tabelle sind die unterschiedlichen Ebenen des Identitäts Wechsels aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="32f02-140">The following table lists the different levels of impersonation.</span></span>



| <span data-ttu-id="32f02-141">Ebene</span><span class="sxs-lookup"><span data-stu-id="32f02-141">Level</span></span>                           | <span data-ttu-id="32f02-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32f02-142">Description</span></span>                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f02-143">Standardwert für RPC- \_ C- \_ \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="32f02-143">RPC\_C\_IMP\_LEVEL\_DEFAULT</span></span>     | <span data-ttu-id="32f02-144">Das Betriebssystem wählt die Ebene des Identitäts Wechsels aus.</span><span class="sxs-lookup"><span data-stu-id="32f02-144">The operating system chooses the level of impersonation.</span></span>                                                      |
| <span data-ttu-id="32f02-145">RPC- \_ C- \_ IMP- \_ Ebene \_ Anonym</span><span class="sxs-lookup"><span data-stu-id="32f02-145">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   | <span data-ttu-id="32f02-146">Der Server kann die Identität des Clients annehmen, aber das Identitätswechsel Token kann für nichts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32f02-146">The server can impersonate the client, but the impersonation token cannot be used for anything.</span></span>               |
| <span data-ttu-id="32f02-147">RPC- \_ C- \_ IMP- \_ Stufe \_ identifizieren</span><span class="sxs-lookup"><span data-stu-id="32f02-147">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    | <span data-ttu-id="32f02-148">Der Server kann die Identität des Clients abrufen und die Identität des Clients für die ACL-Überprüfung annehmen.</span><span class="sxs-lookup"><span data-stu-id="32f02-148">The server can obtain the identity of the client and impersonate the client for ACL checking.</span></span>                 |
| <span data-ttu-id="32f02-149">Identitätswechsel auf RPC- \_ C- \_ \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="32f02-149">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> | <span data-ttu-id="32f02-150">Der Server kann die Identität des Clients über eine Computer Grenze hinweg annehmen.</span><span class="sxs-lookup"><span data-stu-id="32f02-150">The server can impersonate the client across one computer boundary.</span></span>                                           |
| <span data-ttu-id="32f02-151">RPC- \_ C- \_ IMP- \_ Stufen \_ Delegat</span><span class="sxs-lookup"><span data-stu-id="32f02-151">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    | <span data-ttu-id="32f02-152">Der Server kann die Identität des Clients über mehrere Grenzen hinweg annehmen und im Auftrag des Clients Anrufe tätigen.</span><span class="sxs-lookup"><span data-stu-id="32f02-152">The server can impersonate the client across multiple boundaries, and can make calls on behalf of the client.</span></span> |



 

 

 
