---
description: Client-Side Anforderungen für den Identitätswechsel
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side Anforderungen für den Identitätswechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342409"
---
# <a name="client-side-requirements-for-impersonation"></a><span data-ttu-id="4633e-103">Client-Side Anforderungen für den Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="4633e-103">Client-Side Requirements for Impersonation</span></span>

<span data-ttu-id="4633e-104">Die folgenden beiden Einstellungen können relativ zum Identitätswechsel auf der Clientseite angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="4633e-104">The following two settings can be specified relative to impersonation on the client side:</span></span>

-   <span data-ttu-id="4633e-105">Die Identitätswechsel Ebene, die angibt, dass der Client die Identität des Servers verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4633e-105">Impersonation level, which indicates the client's willingness to have the server use its identity.</span></span>
-   <span data-ttu-id="4633e-106">Eine Einstellung im Active Directory Dienst, über die das Client Konto als "Konto ist vertraulich und nicht delegiert werden" gekennzeichnet werden kann, wodurch die Delegierung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="4633e-106">A setting in the Active Directory Service through which the client account can be marked "Account is sensitive and cannot be delegated," which will disable delegation.</span></span>

<span data-ttu-id="4633e-107">Die Identitätswechsel Ebene kann auf verschiedene Weise festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4633e-107">The impersonation level can be set in a variety of ways.</span></span> <span data-ttu-id="4633e-108">Wenn der Client keine Identitätswechsel Ebene angibt, wird der Computer weite Standard von com verwendet.</span><span class="sxs-lookup"><span data-stu-id="4633e-108">If the client does not indicate an impersonation level, the machine-wide default will be used by COM.</span></span> <span data-ttu-id="4633e-109">Der Computer weite Standard kann entweder mithilfe des Verwaltungs Programms Komponenten Dienste oder Dcomcnfg.exe festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4633e-109">The machine-wide default can be set using either the Component Services administrative tool or Dcomcnfg.exe.</span></span> <span data-ttu-id="4633e-110">Der Client kann auch eine bevorzugte Identitätswechsel Ebene mit Dcomcnfg.exe angeben.</span><span class="sxs-lookup"><span data-stu-id="4633e-110">The client can also indicate a preferred impersonation level administratively with Dcomcnfg.exe.</span></span>

<span data-ttu-id="4633e-111">Der Client kann die Identitätswechsel Ebene Programm gesteuert angeben. dabei wird entweder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)– Äquivalent zu [**IClientSecurity:: setblanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket)verwendet, das so oft wie erforderlich aufgerufen werden kann – oder [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), das einmal pro Prozess aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4633e-111">The client can indicate the impersonation level programmatically, using either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)—equivalent to [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), which can be called as often as necessary—or [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), which can be called once per process.</span></span>

<span data-ttu-id="4633e-112">Wenn der Client einen Identitätswechsel auf delegatebene anzeigt – die breiteste Stelle, die er dem Server gewähren kann – muss der Client unter einer Identität ausgeführt werden, die im Active Directory-Dienst ordnungsgemäß konfiguriert ist, damit die Identität delegiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4633e-112">If the client indicates delegate-level impersonation—the broadest authority it can grant to the server—the client should be running under an identity that is properly configured in the Active Directory Service to enable its identity to be delegated.</span></span>

<span data-ttu-id="4633e-113">Weitere Details zu Identitätswechsel Ebenen und den Anforderungen für die Delegierung finden Sie unter [Delegierung und](/windows/desktop/com/delegation-and-impersonation)Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="4633e-113">For more detail regarding impersonation levels and the requirements for delegation to work, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

<span data-ttu-id="4633e-114">Com+-Anwendungen können natürlich immer als Clients fungieren.</span><span class="sxs-lookup"><span data-stu-id="4633e-114">COM+ applications can always act as clients, of course.</span></span> <span data-ttu-id="4633e-115">Wenn die COM+-Anwendung eine andere Anwendung oder Ressource aufruft, wird eine Identitätswechsel Ebene ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="4633e-115">When the COM+ application makes a call to another application or resource, it expresses an impersonation level.</span></span> <span data-ttu-id="4633e-116">Für com+-Server Anwendungen können Sie eine Ebene für den Identitätswechsel administrativ festlegen.</span><span class="sxs-lookup"><span data-stu-id="4633e-116">For COM+ server applications, you can set an impersonation level administratively.</span></span> <span data-ttu-id="4633e-117">COM+-Bibliotheksanwendungen können Ihre eigene Identitätswechsel Ebene nicht festlegen. Sie verwenden stattdessen die des Host Prozesses.</span><span class="sxs-lookup"><span data-stu-id="4633e-117">COM+ library applications cannot set their own impersonation level; they use that of the host process instead.</span></span> <span data-ttu-id="4633e-118">Informationen zum Festlegen des Identitäts Wechsels für eine COM+-Anwendung finden Sie unter [Festlegen einer](setting-an-impersonation-level.md)Identitätswechsel Ebene.</span><span class="sxs-lookup"><span data-stu-id="4633e-118">To learn how to set impersonation for a COM+ application, see [Setting an Impersonation Level](setting-an-impersonation-level.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4633e-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4633e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4633e-120">Client Identitätswechsel und Delegierung</span><span class="sxs-lookup"><span data-stu-id="4633e-120">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="4633e-121">Cloaking</span><span class="sxs-lookup"><span data-stu-id="4633e-121">Cloaking</span></span>](cloaking.md)
</dt> <dt>

[<span data-ttu-id="4633e-122">Server seitige Anforderungen für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="4633e-122">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
