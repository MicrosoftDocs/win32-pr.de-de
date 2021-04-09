---
title: Identitätswechsel Ebenen (com)
description: Wenn der Identitätswechsel erfolgreich ist, bedeutet dies, dass der Client zugestimmt hat, den Server zu einem gewissen Grad zu machen.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858483"
---
# <a name="impersonation-levels"></a><span data-ttu-id="ce08f-103">Identitätswechsel Ebenen</span><span class="sxs-lookup"><span data-stu-id="ce08f-103">Impersonation Levels</span></span>

<span data-ttu-id="ce08f-104">Wenn der Identitätswechsel erfolgreich ist, bedeutet dies, dass der Client zugestimmt hat, den Server zu einem gewissen Grad zu machen.</span><span class="sxs-lookup"><span data-stu-id="ce08f-104">If impersonation succeeds, it means that the client has agreed to let the server be the client to some degree.</span></span> <span data-ttu-id="ce08f-105">Die unterschiedlichen Stufen des Identitäts Wechsels werden als Identitätswechsel *Ebenen* bezeichnet und geben an, wie viel Autorität dem Server zugewiesen wird, wenn die Identität des Clients angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="ce08f-105">The varying degrees of impersonation are called *impersonation levels*, and they indicate how much authority is given to the server when it is impersonating the client.</span></span>

<span data-ttu-id="ce08f-106">Derzeit gibt es vier Identitätswechsel Ebenen: *Anonym*, *identifiziert* *, annehmen* und *delegieren*.</span><span class="sxs-lookup"><span data-stu-id="ce08f-106">Currently, there are four impersonation levels: *anonymous*, *identify*, *impersonate*, and *delegate*.</span></span> <span data-ttu-id="ce08f-107">In der folgenden Liste werden die einzelnen Identitätswechsel Ebenen kurz beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ce08f-107">The following list briefly describes each impersonation level:</span></span>

<dl> <dt>

<span data-ttu-id="ce08f-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>Anonym (RPC- \_ C- \_ IMP- \_ Ebene \_ Anonym)</span><span class="sxs-lookup"><span data-stu-id="ce08f-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC\_C\_IMP\_LEVEL\_ANONYMOUS)</span></span>
</dt> <dd>

<span data-ttu-id="ce08f-109">Der Client ist gegenüber dem Server anonym.</span><span class="sxs-lookup"><span data-stu-id="ce08f-109">The client is anonymous to the server.</span></span> <span data-ttu-id="ce08f-110">Der Serverprozess kann den Client imitieren, das Identitätswechseltoken enthält jedoch keine Informationen über den Client.</span><span class="sxs-lookup"><span data-stu-id="ce08f-110">The server process can impersonate the client, but the impersonation token does not contain any information about the client.</span></span> <span data-ttu-id="ce08f-111">Diese Ebene wird nur über den lokalen Kommunikationsprozess für die prozessübergreifende Kommunikation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce08f-111">This level is only supported over the local interprocess communication transport.</span></span> <span data-ttu-id="ce08f-112">Alle anderen Transporte Stufen diese Ebene im Hintergrund herauf, um Sie zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ce08f-112">All other transports silently promote this level to identify.</span></span>

</dd> <dt>

<span data-ttu-id="ce08f-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identifizieren (RPC \_ C \_ IMP- \_ Ebene \_ identifizieren)</span><span class="sxs-lookup"><span data-stu-id="ce08f-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY)</span></span>
</dt> <dd>

<span data-ttu-id="ce08f-114">Die Standardebene des Systems.</span><span class="sxs-lookup"><span data-stu-id="ce08f-114">The system default level.</span></span> <span data-ttu-id="ce08f-115">Der Server kann die Identität des Clients abrufen und den Client imitieren, um ACL-Überprüfungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ce08f-115">The server can obtain the client's identity, and the server can impersonate the client to do ACL checks.</span></span>

</dd> <dt>

<span data-ttu-id="ce08f-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Identität annehmen (RPC- \_ C- \_ IMP-Ebene Identität annehmen \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="ce08f-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE)</span></span>
</dt> <dd>

<span data-ttu-id="ce08f-117">Der Server kann als der Client auftreten und dabei dessen Sicherheitskontext imitieren.</span><span class="sxs-lookup"><span data-stu-id="ce08f-117">The server can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="ce08f-118">Der Server kann als Client auf lokale Ressourcen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ce08f-118">The server can access local resources as the client.</span></span> <span data-ttu-id="ce08f-119">Wenn der Server lokal ist, kann er auf Netzwerkressourcen als Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ce08f-119">If the server is local, it can access network resources as the client.</span></span> <span data-ttu-id="ce08f-120">Wenn der Server Remote ist, kann er nur auf Ressourcen zugreifen, die sich auf demselben Computer wie der Server befinden.</span><span class="sxs-lookup"><span data-stu-id="ce08f-120">If the server is remote, it can access only resources that are on the same computer as the server.</span></span>

</dd> <dt>

<span data-ttu-id="ce08f-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>Delegat (RPC \_ C \_ IMP-Ebene-Delegat \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="ce08f-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC\_C\_IMP\_LEVEL\_DELEGATE)</span></span>
</dt> <dd>

<span data-ttu-id="ce08f-122">Die umfassendste Ebene des Identitätswechsels.</span><span class="sxs-lookup"><span data-stu-id="ce08f-122">The most powerful impersonation level.</span></span> <span data-ttu-id="ce08f-123">Wenn diese Ebene ausgewählt wird, kann der Server (sowohl lokal als auch remote) als Client auftreten und dabei dessen Sicherheitskontext imitieren.</span><span class="sxs-lookup"><span data-stu-id="ce08f-123">When this level is selected, the server (whether local or remote) can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="ce08f-124">Während des Identitäts Wechsels können die Anmelde Informationen des Clients (sowohl lokal als auch Netzwerk) an eine beliebige Anzahl von Computern übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ce08f-124">During impersonation, the client's credentials (both local and network) can be passed to any number of computers.</span></span>

<span data-ttu-id="ce08f-125">Damit der Identitätswechsel auf der delegatebene funktioniert, müssen die folgenden Anforderungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="ce08f-125">For impersonation to work at the delegate level, the following requirements must be met:</span></span>

-   <span data-ttu-id="ce08f-126">Der Client muss die Identitätswechsel Ebene auf den RPC- \_ C- \_ IMP-Ebenen-Delegaten festlegen \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ce08f-126">The client must set the impersonation level to RPC\_C\_IMP\_LEVEL\_DELEGATE.</span></span>
-   <span data-ttu-id="ce08f-127">Das Client Konto darf nicht als "Konto ist vertraulich und kann nicht delegiert werden" im Active Directory-Dienst gekennzeichnet sein.</span><span class="sxs-lookup"><span data-stu-id="ce08f-127">The client account must not be marked "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>
-   <span data-ttu-id="ce08f-128">Das Server Konto muss mit dem Attribut "Trusted for Delegation" im Active Directory-Dienst gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ce08f-128">The server account must be marked with the "Trusted for delegation" attribute in the Active Directory Service.</span></span>
-   <span data-ttu-id="ce08f-129">Die Computer, auf denen der-Client, der-Server und alle Downstream-Server gehostet werden, müssen in einer Domäne ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ce08f-129">The computers hosting the client, the server, and any "downstream" servers must all be running in a domain.</span></span>

</dd> </dl>

<span data-ttu-id="ce08f-130">Durch Auswählen der Identitätswechsel Ebene teilt der Client dem Server mit, wie weit die Identität des Clients angenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce08f-130">By choosing the impersonation level, the client tells the server how far it can go in impersonating the client.</span></span> <span data-ttu-id="ce08f-131">Der Client legt die Identitätswechsel Ebene auf dem Proxy fest, der für die Kommunikation mit dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce08f-131">The client sets the impersonation level on the proxy it uses to communicate with the server.</span></span>

## <a name="setting-the-impersonation-level"></a><span data-ttu-id="ce08f-132">Festlegen der Identitätswechsel Ebene</span><span class="sxs-lookup"><span data-stu-id="ce08f-132">Setting the Impersonation Level</span></span>

<span data-ttu-id="ce08f-133">Es gibt zwei Möglichkeiten, die Identitätswechsel Ebene festzulegen:</span><span class="sxs-lookup"><span data-stu-id="ce08f-133">There are two ways to set the impersonation level:</span></span>

-   <span data-ttu-id="ce08f-134">Der Client kann ihn Processwide durch einen [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Rückruf festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce08f-134">The client can set it processwide, through a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="ce08f-135">Ein Client kann die Sicherheit auf Proxy Ebene für eine Schnittstelle eines Remote Objekts über einen [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) -Befehl (oder die Hilfsfunktion [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)) festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce08f-135">A client can set proxy-level security on an interface of a remote object through a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (or the helper function [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span></span>

<span data-ttu-id="ce08f-136">Sie legen die Identitätswechsel Ebene fest, indem Sie einen geeigneten RPC- \_ C- \_ IMP- \_ Level \_ xxx-Wert an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) über den *dwimplevel* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="ce08f-136">You set the impersonation level by passing an appropriate RPC\_C\_IMP\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwImpLevel* parameter.</span></span>

<span data-ttu-id="ce08f-137">Verschiedene Authentifizierungsdienste unterstützen Identitätswechsel auf delegatebene an verschiedene Blöcke.</span><span class="sxs-lookup"><span data-stu-id="ce08f-137">Different authentication services support delegate-level impersonation to different extents.</span></span> <span data-ttu-id="ce08f-138">Beispielsweise unterstützt NTLMSSP Thread übergreifende und prozessübergreifende delegatebenenidentitäts-Identitätswechsel, aber nicht Computer übergreifend.</span><span class="sxs-lookup"><span data-stu-id="ce08f-138">For instance, NTLMSSP supports cross-thread and cross-process delegate-level impersonation, but not cross-computer.</span></span> <span data-ttu-id="ce08f-139">Auf der anderen Seite unterstützt das Kerberos-Protokoll Identitätswechsel auf delegatebene über Computer Grenzen hinweg, während SChannel keinen Identitätswechsel auf der delegatebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce08f-139">On the other hand, the Kerberos protocol supports delegate-level impersonation across computer boundaries, while Schannel does not support any impersonation at the delegate level.</span></span> <span data-ttu-id="ce08f-140">Wenn Sie über einen Proxy mit Identitätswechsel verfügen und die Identitätswechsel Ebene auf Delegieren festlegen möchten, sollten Sie [**setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) mithilfe der Standard Konstanten für jeden Parameter Außer der Identitätswechsel Ebene aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ce08f-140">If you have a proxy at impersonate level and you want to set the impersonation level to delegate, you should call [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) using the default constants for every parameter except the impersonation level.</span></span> <span data-ttu-id="ce08f-141">COM wählt NTLM lokal und das Kerberos-Protokoll Remote aus (wenn das Kerberos-Protokoll funktioniert).</span><span class="sxs-lookup"><span data-stu-id="ce08f-141">COM will choose NTLM locally and the Kerberos protocol remotely (when the Kerberos protocol will work).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce08f-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce08f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce08f-143">Delegierung und Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="ce08f-143">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 