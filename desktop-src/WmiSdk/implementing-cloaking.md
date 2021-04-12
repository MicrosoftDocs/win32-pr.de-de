---
description: Das Cloaking ist eine Erweiterung des Identitäts Wechsels, die eine bessere Kontrolle über die Identität eines Clients über einen Proxy durch com ermöglicht. Wie viele Arten von WMI-Sicherheit legen Sie den Cloaking über die CoSetProxyBlanket-und die CoInitializeSecurity-Schnittstelle fest.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementieren von Cloaking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217125"
---
# <a name="implementing-cloaking"></a><span data-ttu-id="12a58-104">Implementieren von Cloaking</span><span class="sxs-lookup"><span data-stu-id="12a58-104">Implementing Cloaking</span></span>

<span data-ttu-id="12a58-105">Das Cloaking ist eine Erweiterung des Identitäts Wechsels, die eine bessere Kontrolle über die Identität eines Clients über einen Proxy durch com ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="12a58-105">Cloaking is an extension to impersonation that allows for better control over how COM impersonates a client over a proxy.</span></span> <span data-ttu-id="12a58-106">Wie viele Arten von WMI-Sicherheit legen Sie den Cloaking über die [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) -und die [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="12a58-106">Like many forms of WMI security, you set cloaking through the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interfaces.</span></span>

<span data-ttu-id="12a58-107">COM bietet die folgenden Arten von Verstopfungen:</span><span class="sxs-lookup"><span data-stu-id="12a58-107">COM provides the following forms of cloaking:</span></span>

-   <span data-ttu-id="12a58-108">statischen</span><span class="sxs-lookup"><span data-stu-id="12a58-108">Static</span></span>

    <span data-ttu-id="12a58-109">COM legt die Tokenidentität durch den Thread oder das Prozess Token beim ersten Proxy des Proxys fest.</span><span class="sxs-lookup"><span data-stu-id="12a58-109">COM establishes the token identity by the thread or process token on the first call to the proxy.</span></span> <span data-ttu-id="12a58-110">Wenn Sie statisches Cloaking mit [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)verwenden, legen Sie die Identität des Proxys für die Lebensdauer des Proxys fest.</span><span class="sxs-lookup"><span data-stu-id="12a58-110">If you use static cloaking with [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), you set the identity of the proxy for the life of the proxy.</span></span>

-   <span data-ttu-id="12a58-111">Dynamisch</span><span class="sxs-lookup"><span data-stu-id="12a58-111">Dynamic</span></span>

    <span data-ttu-id="12a58-112">COM stellt die Tokenidentität aus dem Thread-oder Prozess Token bei jedem Proxy Vorgang wieder her.</span><span class="sxs-lookup"><span data-stu-id="12a58-112">COM reestablishes the token identity from the thread or process token on each call to the proxy.</span></span> <span data-ttu-id="12a58-113">Da com die Identität bei jedem-Rückruf überprüft, ermöglicht dynamisches Cloaking eine präzisere Steuerung der Client Identität.</span><span class="sxs-lookup"><span data-stu-id="12a58-113">Because COM checks the identity on each call, dynamic cloaking allows for finer control over the client identity.</span></span> <span data-ttu-id="12a58-114">Das dynamische Cloaking ist jedoch weniger effizient als das statische Cloaking.</span><span class="sxs-lookup"><span data-stu-id="12a58-114">However, dynamic cloaking is less efficient than static cloaking.</span></span>

<span data-ttu-id="12a58-115">Wenn Sie das Cloaking in Verbindung mit der Delegierungs Ebene des Identitäts Wechsels festgelegt haben, kann ein Server die Identität eines Clients über mehrere Server hinweg weitergeben, auch wenn es sich um Remote Server handelt.</span><span class="sxs-lookup"><span data-stu-id="12a58-115">When you set cloaking in conjunction with the delegation level of impersonation, a server can propagate the identity of a client across servers, even if the servers are remote.</span></span> <span data-ttu-id="12a58-116">Wenn Sie das Cloaking nicht aktivieren, führt com einen beliebigen Rückruf von einem lokalen Server an einen Remote Server im Kontext des eigentlichen Server Prozesses aus.</span><span class="sxs-lookup"><span data-stu-id="12a58-116">If you do not enable cloaking, COM makes any call from a local server to a remote server under the context of the actual server process.</span></span>

<span data-ttu-id="12a58-117">Durch das Cloaking kann WMI die Identität eines Clients annehmen, um sowohl auf lokale als auch auf Remote Netzwerkressourcen über mehrere Computer Grenzen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="12a58-117">Cloaking lets WMI impersonate a client to access both local and remote network resources across multiple computer boundaries.</span></span> <span data-ttu-id="12a58-118">WMI kann die Identität des Clients an lokale Server und Remote Server übergeben, z. b. an andere Remote Instanzen von WMI.</span><span class="sxs-lookup"><span data-stu-id="12a58-118">WMI can pass the identity of the client to local and remote servers, such as other remote instances of WMI.</span></span> <span data-ttu-id="12a58-119">Diese Remote Server können dann Vorgänge im ursprünglichen Client Kontext ausführen.</span><span class="sxs-lookup"><span data-stu-id="12a58-119">Those remote servers can then perform operations under the initial client context.</span></span>

<span data-ttu-id="12a58-120">Im folgenden Verfahren wird beschrieben, wie Sie die Verwendung von Cloaking und Delegierungen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="12a58-120">The following procedure describes how to use cloaking and delegation together.</span></span>

<span data-ttu-id="12a58-121">**So verwenden Sie das Cloaking und die Delegierung**</span><span class="sxs-lookup"><span data-stu-id="12a58-121">**To use cloaking and delegation together**</span></span>

1.  <span data-ttu-id="12a58-122">Legen Sie den Authentifizierungsdienst auf Kerberos fest.</span><span class="sxs-lookup"><span data-stu-id="12a58-122">Set the authentication service to Kerberos.</span></span>

    <span data-ttu-id="12a58-123">Kerberos ist der einzige Authentifizierungsdienst, der Remote Lecks und Delegierungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12a58-123">Kerberos is the only authentication service that supports remote cloaking and delegation.</span></span> <span data-ttu-id="12a58-124">Dies bedeutet, dass die über-und Delegierung nur auf Remote Servern verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="12a58-124">This means that cloaking and delegation can only be used on remote servers.</span></span>

2.  <span data-ttu-id="12a58-125">Markieren Sie das Server Anmelde Konto in den Active Directory Services als "Trusted for Delegation".</span><span class="sxs-lookup"><span data-stu-id="12a58-125">Mark the server login account as "Trusted for Delegation" in the Active Directory services.</span></span>
3.  <span data-ttu-id="12a58-126">Markieren Sie das Client Anmelde Konto in Active Directory Services als "Konto ist vertraulich und kann nicht delegiert werden".</span><span class="sxs-lookup"><span data-stu-id="12a58-126">Mark the client login account as "Account is sensitive and cannot be delegated" in Active Directory services.</span></span>

<span data-ttu-id="12a58-127">Beispielsweise kann ein Ansichts Anbieter, der Objekte aus mehreren WMI-Instanzen auf mehreren Computern zurückgeben kann, von Delegierung und Cloaking profitieren.</span><span class="sxs-lookup"><span data-stu-id="12a58-127">For example, a call to the View Provider, which may return objects from multiple instances of WMI on multiple computers, can benefit from delegation and cloaking.</span></span>

 

 
