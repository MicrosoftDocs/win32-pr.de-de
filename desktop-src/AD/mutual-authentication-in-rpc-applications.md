---
title: Gegenseitige Authentifizierung in RPC-Anwendungen
description: RPC-Dienste können Dienst Verbindungspunkte verwenden, um sich selbst zu veröffentlichen, oder Sie können die RpcNs-APIs (RPC Name Service) verwenden.
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in RPC-Anwendungen AD
- Active Directory, Verwendung von gegenseitiger Authentifizierung, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858137"
---
# <a name="mutual-authentication-in-rpc-applications"></a><span data-ttu-id="ab0e9-105">Gegenseitige Authentifizierung in RPC-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ab0e9-105">Mutual Authentication in RPC Applications</span></span>

<span data-ttu-id="ab0e9-106">RPC-Dienste können Dienst Verbindungspunkte verwenden, um sich selbst zu veröffentlichen, oder Sie können die RpcNs-APIs (RPC Name Service) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-106">RPC services can use service connection points to publish themselves, or they can use the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="ab0e9-107">In diesem Thema wird erläutert, wie die gegenseitige Authentifizierung mit einem RPC-Dienst durchgeführt wird, der sich mit den RpcNs-APIs (RPC Name Service) selbst veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="ab0e9-107">This topic discusses how to perform mutual authentication with an RPC service that publishes itself using the RPC name service (RpcNs) APIs.</span></span>

<span data-ttu-id="ab0e9-108">**So registrieren Sie einen SPN im Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="ab0e9-108">**To register an SPN in the directory**</span></span>

1.  <span data-ttu-id="ab0e9-109">Aufrufen der [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) -Funktion zum Verfassen eines Dienst Prinzipal namens (SPN) für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-109">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose a service principal name (SPN) for the service.</span></span>
2.  <span data-ttu-id="ab0e9-110">Wenden Sie die [**dswrite-accountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) -Funktion an, um den SPN für das Dienst Konto oder das Computer Konto zu registrieren, in dessen Kontext der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-110">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPN on the service account or computer account in whose context the service will run.</span></span>

<span data-ttu-id="ab0e9-111">**So registrieren Sie einen Dienst beim RPC-Naming Service**</span><span class="sxs-lookup"><span data-stu-id="ab0e9-111">**To register a service with the RPC naming service**</span></span>

1.  <span data-ttu-id="ab0e9-112">Vergewissern Sie sich, dass die entsprechenden SPNs für das Konto, unter dem der Dienst ausgeführt wird, registriert sind.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-112">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="ab0e9-113">Weitere Informationen finden Sie unter [Anmelde Konto-Wartungs Tasks](logon-account-maintenance-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ab0e9-113">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>
2.  <span data-ttu-id="ab0e9-114">Wenden Sie die [**rpcserverregisterauthinfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion an, um den Dienst-SPN beim RPC-Authentifizierungsdienst zu registrieren, und geben Sie **RPC \_ C \_ authn \_ GSS \_ aushandeln** als Authentifizierungsdienst an, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-114">Call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function to register the service SPN with the RPC authentication service, and specify **RPC\_C\_AUTHN\_GSS\_NEGOTIATE** as the authentication service to use.</span></span>

<span data-ttu-id="ab0e9-115">Weitere Informationen zum Ausführen der gegenseitigen Authentifizierung in einem RPC-Dienst finden Sie unter [Schreiben eines authentifizierten SSPI-Servers](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span><span class="sxs-lookup"><span data-stu-id="ab0e9-115">For more information about performing mutual authentication in an RPC service, see [Writing an Authenticated SSPI Server](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span></span>

<span data-ttu-id="ab0e9-116">**So authentifizieren Sie den Dienst vom Client**</span><span class="sxs-lookup"><span data-stu-id="ab0e9-116">**To authenticate the service from the client**</span></span>

1.  <span data-ttu-id="ab0e9-117">Extrahieren Sie den Hostnamen aus der RPC-Bindung.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-117">Extract the host name from the RPC Binding.</span></span>
2.  <span data-ttu-id="ab0e9-118">Erstellen Sie den SPN für den Dienst, indem Sie die [**dsmakespn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) -Funktion mit der Dienstklasse, dem DNS-Hostnamen und dem Dienstnamen aufrufen. Dies ist der Distinguished Name des Verbindungs Punkts im Fall von RpcNs.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-118">Compose the SPN for the service by calling the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function with the service class, the DNS host name, and the service name; that is the distinguished name of the connection point in the case of RpcNs.</span></span>

    <span data-ttu-id="ab0e9-119">Weitere Informationen zum Erstellen eines SPN für einen RpcNs-Dienst finden Sie unter Verfassen von Dienst Prinzipal Namen ( [SPN) für einen RpcNs-Dienst](composing-spns-for-an-rpcns-service.md).</span><span class="sxs-lookup"><span data-stu-id="ab0e9-119">For more information about composing an SPN for an RpcNs service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

3.  <span data-ttu-id="ab0e9-120">Richten Sie eine [**RPC \_ - \_ sicherheitsqos**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) -Struktur ein, um die gegenseitige Authentifizierung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-120">Set up an [**RPC\_SECURITY\_QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) structure to request mutual authentication.</span></span>
4.  <span data-ttu-id="ab0e9-121">Aufrufen der Funktion [**rpcbindingsetauthinfoex**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) zum Festlegen der Authentifizierungsdaten für die RPC-Bindung.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-121">Call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="ab0e9-122">Der Client muss mindestens die **\_ \_ \_ \_ Pkt- \_ Integrität der RPC-C-authn-Ebene** anfordern, um sicherzustellen, dass die Kommunikation nicht manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-122">The client must request at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** to ensure that communications have not been tampered.</span></span> <span data-ttu-id="ab0e9-123">Um die Sicherheit zu erhöhen, muss der Client den **RPC- \_ C- \_ authn- \_ Level \_ Pkt \_ Privacy** angeben, um die Verschlüsselung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-123">For increased security, the client should specify **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** to request encryption.</span></span>
5.  <span data-ttu-id="ab0e9-124">Führen Sie den RPC-Aufruf aus.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-124">Perform the RPC call.</span></span>

<span data-ttu-id="ab0e9-125">Weitere Informationen zum Ausführen der gegenseitigen Authentifizierung bei einem RPC-Client finden Sie unter [Schreiben eines authentifizierten SSPI-Clients](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span><span class="sxs-lookup"><span data-stu-id="ab0e9-125">For more information about performing mutual authentication in an RPC client, see [Writing an Authenticated SSPI Client](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span></span>

<span data-ttu-id="ab0e9-126">**So authentifizieren Sie den Client über den Dienst**</span><span class="sxs-lookup"><span data-stu-id="ab0e9-126">**To authenticate the client from the service**</span></span>

1.  <span data-ttu-id="ab0e9-127">Zum Überprüfen der vom Client angegebenen Authentifizierungs Parameter wird die [**rpcbindinginqauthclient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-127">Call the [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) function to verify the authentication parameters specified by the client.</span></span> <span data-ttu-id="ab0e9-128">Wenn der Client die gewünschte Authentifizierungs Stufe nicht angefordert hat, lehnen Sie den-Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-128">If the client has not requested the desired level of authentication, reject the call.</span></span> <span data-ttu-id="ab0e9-129">Beachten Sie, dass ein RPC-Dienst bei jedem Aufruf die Authentifizierungs Ebene, den Authentifizierungsdienst und die Client Identität überprüfen muss, um sicherzustellen, dass der Client ordnungsgemäß authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-129">Be aware that an RPC service must verify the authentication level, authentication service, and client identity on every call to ensure that the client has been properly authenticated.</span></span>
2.  <span data-ttu-id="ab0e9-130">Zum Annehmen der Identität des Clients wird die [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-130">Call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate the client.</span></span>
3.  <span data-ttu-id="ab0e9-131">Führt den angeforderten Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-131">Perform the requested operation.</span></span>
4.  <span data-ttu-id="ab0e9-132">Aufrufen der [**rpkrevertteself**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) -Funktion, um zum Dienst Sicherheitskontext zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-132">Call the [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) function to revert to the service security context.</span></span>

<span data-ttu-id="ab0e9-133">Weitere Informationen zum Identitätswechsel des RPC-Clients finden Sie unter [Client](/windows/desktop/Rpc/client-impersonation)Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-133">For more information about RPC client impersonation, see [Client Impersonation](/windows/desktop/Rpc/client-impersonation).</span></span>

<span data-ttu-id="ab0e9-134">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="ab0e9-134">For more information, see:</span></span>

-   [<span data-ttu-id="ab0e9-135">Veröffentlichen mit dem RPC-Namensdienst (RPC Name Service, RpcNs)</span><span class="sxs-lookup"><span data-stu-id="ab0e9-135">Publishing with the RPC Name Service (RpcNs)</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="ab0e9-136">Grundlagen zu RPC</span><span class="sxs-lookup"><span data-stu-id="ab0e9-136">RPC Security Essentials</span></span>](/windows/desktop/Rpc/rpc-security-essentials)

 

 