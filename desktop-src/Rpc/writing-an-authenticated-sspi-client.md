---
title: Schreiben eines authentifizierten SSPI-Clients
description: Schreiben eines authentifizierten SSPI-Clients und eines Remote Prozedur Aufrufs (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Schreiben eines authentifizierten SSPI-Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102027"
---
# <a name="writing-an-authenticated-sspi-client"></a><span data-ttu-id="0ace0-104">Schreiben eines authentifizierten SSPI-Clients</span><span class="sxs-lookup"><span data-stu-id="0ace0-104">Writing an Authenticated SSPI Client</span></span>

<span data-ttu-id="0ace0-105">Alle RPC-Client-/Serversitzungen erfordern eine Bindung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0ace0-105">All RPC client/server sessions require a binding between the client and the server.</span></span> <span data-ttu-id="0ace0-106">Zum Hinzufügen von Sicherheit zu Client-/Server-Anwendungen müssen die Programme eine authentifizierte Bindung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ace0-106">To add security to client/server applications, the programs must use an authenticated binding.</span></span> <span data-ttu-id="0ace0-107">In diesem Abschnitt wird beschrieben, wie Sie eine authentifizierte Bindung zwischen Client und Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ace0-107">This section describes the process of creating an authenticated binding between the client and the server.</span></span>

-   [<span data-ttu-id="0ace0-108">Erstellen von Client seitigen Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="0ace0-108">Creating Client-side Binding Handles</span></span>](#creating-client-side-binding-handles)
-   [<span data-ttu-id="0ace0-109">Bereitstellen von Client Anmelde Informationen für den Server</span><span class="sxs-lookup"><span data-stu-id="0ace0-109">Providing Client Credentials to the Server</span></span>](#providing-client-credentials-to-the-server)

<span data-ttu-id="0ace0-110">Weitere Informationen finden Sie unter [Prozeduren, die mit den meisten Sicherheitspaketen und Protokollen](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) im Platform Software Development Kit (SDK) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ace0-110">For related information, see [Procedures Used with Most Security Packages and Protocols](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) in the Platform Software Development Kit (SDK).</span></span>

## <a name="creating-client-side-binding-handles"></a><span data-ttu-id="0ace0-111">Erstellen von Client seitigen Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="0ace0-111">Creating Client-side Binding Handles</span></span>

<span data-ttu-id="0ace0-112">Zum Erstellen einer authentifizierten Sitzung mit einem Serverprogramm müssen Client Anwendungen Authentifizierungsinformationen mit Ihrem Bindungs handle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ace0-112">To create an authenticated session with a server program, client applications must provide authentication information with their binding handle.</span></span> <span data-ttu-id="0ace0-113">Zum Einrichten eines authentifizierten Bindungs Handles rufen Clients die [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) -oder [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="0ace0-113">To set up an authenticated binding handle, clients invoke the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function.</span></span> <span data-ttu-id="0ace0-114">Diese beiden Funktionen sind nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="0ace0-114">These two functions are nearly identical.</span></span> <span data-ttu-id="0ace0-115">Der einzige Unterschied besteht darin, dass der Client die Quality of Service mit der **rpcbindingsetauthinfoex** -Funktion angeben kann.</span><span class="sxs-lookup"><span data-stu-id="0ace0-115">The only difference between them is that the client can specify the quality of service with the **RpcBindingSetAuthInfoEx** function.</span></span>

<span data-ttu-id="0ace0-116">Das folgende Code Fragment zeigt, wie ein Aufrufen von [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="0ace0-116">The following code fragment shows how a call to [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) might look.</span></span>


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



<span data-ttu-id="0ace0-117">Nachdem der Client die Funktionen [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) erfolgreich aufgerufen hat, authentifiziert die RPC-Lauf Zeit Bibliothek automatisch alle RPC-Aufrufe für die Bindung.</span><span class="sxs-lookup"><span data-stu-id="0ace0-117">After the client successfully calls the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) functions, the RPC run-time library automatically authenticates all RPC calls on the binding.</span></span> <span data-ttu-id="0ace0-118">Die Sicherheitsstufe und die Authentifizierung, die vom Client ausgewählt werden, gelten nur für diesen Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="0ace0-118">The level of security and authentication that the client selects applies only to that binding handle.</span></span> <span data-ttu-id="0ace0-119">Vom Bindungs handle abgeleitete Kontext Handles verwenden die gleichen Sicherheitsinformationen. nachfolgende Änderungen am Bindungs handle werden jedoch nicht in den Kontext Handles widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="0ace0-119">Context handles derived from the binding handle will use the same security information, but subsequent modifications to the binding handle will not be reflected in the context handles.</span></span> <span data-ttu-id="0ace0-120">Weitere Informationen finden Sie unter [Kontext Handles](context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="0ace0-120">For more information, see [Context Handles](context-handles.md).</span></span>

<span data-ttu-id="0ace0-121">Die Authentifizierungs Ebene bleibt wirksam, bis der Client eine andere Ebene auswählt, oder bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ace0-121">The authentication level stays in effect until the client chooses another level, or until the process terminates.</span></span> <span data-ttu-id="0ace0-122">Die meisten Anwendungen erfordern keine Änderung der Sicherheitsstufe.</span><span class="sxs-lookup"><span data-stu-id="0ace0-122">Most applications will not require a change in the security level.</span></span> <span data-ttu-id="0ace0-123">Der Client kann ein beliebiges Bindungs handle Abfragen, um seine Autorisierungs Informationen abzurufen, indem er [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) aufruft und ihm das Bindungs handle übergibt.</span><span class="sxs-lookup"><span data-stu-id="0ace0-123">The client can query any binding handle to obtain its authorization information by invoking [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) and passing it the binding handle.</span></span>

## <a name="providing-client-credentials-to-the-server"></a><span data-ttu-id="0ace0-124">Bereitstellen von Client Anmelde Informationen für den Server</span><span class="sxs-lookup"><span data-stu-id="0ace0-124">Providing Client Credentials to the Server</span></span>

<span data-ttu-id="0ace0-125">Server verwenden die Bindungs Informationen des Clients, um die Sicherheit zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0ace0-125">Servers use the client's binding information to enforce security.</span></span> <span data-ttu-id="0ace0-126">Clients übergeben immer ein Bindungs Handle als ersten Parameter eines Remote Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="0ace0-126">Clients always pass a binding handle as the first parameter of a remote procedure call.</span></span> <span data-ttu-id="0ace0-127">Allerdings können Server das Handle nicht verwenden, es sei denn, Sie ist als erster Parameter für Remote Prozeduren in der IDL-Datei oder in der Anwendungs Konfigurationsdatei (ACF) des Servers deklariert.</span><span class="sxs-lookup"><span data-stu-id="0ace0-127">However, servers cannot use the handle unless it is declared as the first parameter to remote procedures in either the IDL file or in the server's application configuration file (ACF).</span></span> <span data-ttu-id="0ace0-128">Sie können das Bindungs Handle in der IDL-Datei auflisten, Dies zwingt jedoch alle Clients, das Bindungs Handle zu deklarieren und zu bearbeiten, anstatt eine automatische oder implizite Bindung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ace0-128">You can choose to list the binding handle in the IDL file, but this forces all clients to declare and manipulate the binding handle rather than using automatic or implicit binding.</span></span> <span data-ttu-id="0ace0-129">Weitere Informationen finden Sie in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="0ace0-129">For further information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="0ace0-130">Eine andere Methode besteht darin, die Bindungs Handles aus der IDL-Datei zu lassen und das **explizite \_ handle** -Attribut in der ACF des Servers zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="0ace0-130">Another method is to leave the binding handles out of the IDL file and to place the **explicit\_handle** attribute into the server's ACF.</span></span> <span data-ttu-id="0ace0-131">Auf diese Weise kann der Client den Bindungstyp verwenden, der am besten für die Anwendung geeignet ist, während der Server das Bindungs Handle verwendet, als ob er explizit deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="0ace0-131">In this way, the client can use the type of binding best suited to the application, while the server uses the binding handle as though it were declared explicitly.</span></span>

<span data-ttu-id="0ace0-132">Der Prozess zum Extrahieren der Client Anmelde Informationen aus dem Bindungs handle erfolgt wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0ace0-132">The process of extracting the client credentials from the binding handle occurs as follows:</span></span>

-   <span data-ttu-id="0ace0-133">RPC-Clients wenden [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) an und schließen Ihre Authentifizierungsinformationen als Teil der an den Server über gebenden Bindungs Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="0ace0-133">RPC clients call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) and include their authentication information as part of the binding information passed to the server.</span></span>
-   <span data-ttu-id="0ace0-134">Normalerweise ruft der Server [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) auf, damit er sich so verhält, als wäre er der Client.</span><span class="sxs-lookup"><span data-stu-id="0ace0-134">Usually, the server calls [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) in order to behave as though it were the client.</span></span> <span data-ttu-id="0ace0-135">Wenn das Bindungs Handle nicht authentifiziert ist, schlägt der Aufruf fehl, \_ und \_ es ist kein \_ Kontext \_ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0ace0-135">If the binding handle is not authenticated, the call fails with RPC\_S\_NO\_CONTEXT\_AVAILABLE.</span></span> <span data-ttu-id="0ace0-136">Um den Benutzernamen des Clients abzurufen, rufen Sie beim Identitätswechsel [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) auf, oder rufen Sie unter Windows XP oder neueren Windows-Versionen [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) auf, um den Autorisierungs Kontext abzurufen, und verwenden Sie dann Authz-Funktionen, um den Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0ace0-136">To obtain the client's user name, call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) while impersonating, or on Windows XP or later versions of Windows, call [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) to get the authorization context, then use Authz functions to retrieve the name.</span></span>
-   <span data-ttu-id="0ace0-137">Der Server ruft normalerweise " [**kreateprivateobjectsecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) " auf, um Objekte mit ACLs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ace0-137">The server will normally call [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) to create objects with ACLs.</span></span> <span data-ttu-id="0ace0-138">Anschließend werden spätere Sicherheitsüberprüfungen automatisch durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ace0-138">After this is accomplished, later security checks become automatic.</span></span>

 

 