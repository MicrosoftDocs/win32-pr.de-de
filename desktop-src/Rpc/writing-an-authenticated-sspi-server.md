---
title: Schreiben eines authentifizierten SSPI-Servers
description: Vor der Authentifizierung zwischen den Client-und Serverprogrammen muss der Server seine Authentifizierungsinformationen registrieren.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Schreiben eines authentifizierten SSPI-Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036913"
---
# <a name="writing-an-authenticated-sspi-server"></a><span data-ttu-id="7c12d-104">Schreiben eines authentifizierten SSPI-Servers</span><span class="sxs-lookup"><span data-stu-id="7c12d-104">Writing an Authenticated SSPI Server</span></span>

<span data-ttu-id="7c12d-105">Vor der Authentifizierung zwischen den Client-und Serverprogrammen muss der Server seine Authentifizierungsinformationen registrieren.</span><span class="sxs-lookup"><span data-stu-id="7c12d-105">Before authenticated communication can take place between the client and server programs, the server must register its authentication information.</span></span> <span data-ttu-id="7c12d-106">Insbesondere muss der Server seinen Prinzipal Namen registrieren und den Authentifizierungsdienst angeben, den er verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c12d-106">In particular, the server must register its principal name and specify the authentication service it uses.</span></span> <span data-ttu-id="7c12d-107">Weitere Informationen zu Prinzipal Namen finden Sie unter [Prinzipal Namen](principal-names.md).</span><span class="sxs-lookup"><span data-stu-id="7c12d-107">For more information on principal names, see [Principal Names](principal-names.md).</span></span> <span data-ttu-id="7c12d-108">Weitere Informationen zu Authentifizierungsdiensten finden Sie unter [Authentifizierungsdienste](authentication-services.md).</span><span class="sxs-lookup"><span data-stu-id="7c12d-108">For details about authentication services, see [Authentication Services](authentication-services.md).</span></span>

<span data-ttu-id="7c12d-109">Zum Registrieren der Authentifizierungsinformationen wird von den Servern die [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7c12d-109">To register its authentication information, servers call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function.</span></span> <span data-ttu-id="7c12d-110">Übergeben Sie einen Zeiger auf den Prinzipal Namen als Wert des ersten Parameters.</span><span class="sxs-lookup"><span data-stu-id="7c12d-110">Pass a pointer to the principal name as the value of the first parameter.</span></span> <span data-ttu-id="7c12d-111">Legen Sie den zweiten Parameter auf eine Konstante fest, die den Authentifizierungsdienst angibt, der von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c12d-111">Set the second parameter to a constant indicating the authentication service that the application will use.</span></span> <span data-ttu-id="7c12d-112">Eine Beschreibung der Authentifizierungsdienste finden Sie unter [Authentication-Service-Konstanten](authentication-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7c12d-112">For a description of authentication services, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="7c12d-113">Der Server übergibt möglicherweise auch die Adresse einer Schlüssel Erwerbs Funktion als Wert des dritten Parameters.</span><span class="sxs-lookup"><span data-stu-id="7c12d-113">The server may also pass the address of a key acquisition function as the value of the third parameter.</span></span> <span data-ttu-id="7c12d-114">Siehe [Schlüsselerwerbs Funktionen](key-acquisition-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7c12d-114">See [Key Acquisition Functions](key-acquisition-functions.md).</span></span> <span data-ttu-id="7c12d-115">Legen Sie den dritten Parameter auf **null** fest, um die standardmäßige Schlüssel Erwerbs Funktion für den ausgewählten Authentifizierungsdienst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c12d-115">To use the default key acquisition function for the selected authentication service, set the third parameter to **NULL**.</span></span> <span data-ttu-id="7c12d-116">Der letzte Parameter für die [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion ist ein Zeiger Daten, der an die Schlüssel Erwerbs Funktion übergeben werden soll, wenn Sie eine Schlüssel Erwerbs Funktion bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c12d-116">The last parameter to the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function is a pointer data to pass to the key acquisition function, if you provide a key acquisition function.</span></span> <span data-ttu-id="7c12d-117">Ein Aufrufen von **rpcserverregisterauthinfo** ist im folgenden Code Fragment dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c12d-117">A call to **RpcServerRegisterAuthInfo** is shown in the following code fragment.</span></span>


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



<span data-ttu-id="7c12d-118">Außerdem kann der Server die RPC-Lauf Zeit Bibliothek mit einer Autorisierungs Funktion bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c12d-118">In addition, the server may provide the RPC run-time library with an authorization function.</span></span> <span data-ttu-id="7c12d-119">Um eine Autorisierungs Funktion festzulegen, nennen Sie die [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7c12d-119">To set an authorization function, call the [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) function.</span></span>

<span data-ttu-id="7c12d-120">Der Serverteil einer verteilten Anwendung kann die Funktion [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) oder [**rpcbindinginqauthclientex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) zum Abfragen eines Bindungs Handles für Authentifizierungsinformationen aufruft.</span><span class="sxs-lookup"><span data-stu-id="7c12d-120">The server portion of a distributed application can call the function [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to query a binding handle for authentication information.</span></span>

<span data-ttu-id="7c12d-121">Wenn Ihr Server bei einem Security Support Provider registriert wird, werden keine Client Aufrufe mit ungültigen Anmelde Informationen gesendet.</span><span class="sxs-lookup"><span data-stu-id="7c12d-121">If your server registers with a security support provider, client calls with invalid credentials will not be dispatched.</span></span> <span data-ttu-id="7c12d-122">Allerdings werden Aufrufe ohne Anmelde Informationen gesendet.</span><span class="sxs-lookup"><span data-stu-id="7c12d-122">However, calls with no credentials will be dispatched.</span></span> <span data-ttu-id="7c12d-123">Es gibt drei Möglichkeiten, dies zu verhindern:</span><span class="sxs-lookup"><span data-stu-id="7c12d-123">There are three ways to prevent this from happening:</span></span>

-   <span data-ttu-id="7c12d-124">Registrieren Sie die Schnittstelle mithilfe von [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), mit einer Sicherheits Rückruffunktion. Dies bewirkt, dass die RPC-Lauf Zeit Bibliothek nicht authentifizierte Aufrufe an diese Schnittstelle automatisch ablehnt.</span><span class="sxs-lookup"><span data-stu-id="7c12d-124">Register the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), with a security callback function; this will cause the RPC run-time library to automatically reject unauthenticated calls to that interface.</span></span> <span data-ttu-id="7c12d-125">Das Registrieren einer Rückruffunktion ist mit anderen Methoden zum Überprüfen von Zugriffs Anmelde Informationen kompatibel. die Rückruffunktion kann selbst die Funktionen [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)oder [**rpcbindinginqauthclientex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7c12d-125">Registering a callback function is compatible with other methods of checking access credentials; the callback function can itself call the [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) functions, or others.</span></span> <span data-ttu-id="7c12d-126">Diese Funktionen können jedoch nicht die Argumente verwenden, die an die Funktion übermittelt werden, da Sie an diesem Punkt nicht gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="7c12d-126">However, these functions cannot use the arguments passed to the function, as they are not unmarshalled at that point.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c12d-127">Das Registrieren der-Schnittstelle mithilfe von [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) mit einer Sicherheits Rückruffunktion ist die am häufigsten empfohlene Methode zum Überprüfen von Client Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="7c12d-127">Registering the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) with a security callback function is the most heavily recommended method of checking client credentials.</span></span>

 

-   <span data-ttu-id="7c12d-128">Wenden Sie [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) an, um die Sicherheitsstufe zu ermitteln, die vom Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c12d-128">Call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) to determine the security level that the client is using.</span></span> <span data-ttu-id="7c12d-129">Der Stub kann dann einen Fehler zurückgeben, wenn der Client nicht authentifiziert ist.</span><span class="sxs-lookup"><span data-stu-id="7c12d-129">Your stub can then return an error if the client is unauthenticated.</span></span>

 

 




