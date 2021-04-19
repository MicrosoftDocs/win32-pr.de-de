---
description: Server-Side Anforderungen für den Identitätswechsel
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side Anforderungen für den Identitätswechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342763"
---
# <a name="server-side-requirements-for-impersonation"></a><span data-ttu-id="8c5dc-103">Server-Side Anforderungen für den Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="8c5dc-103">Server-Side Requirements for Impersonation</span></span>

<span data-ttu-id="8c5dc-104">Der Server führt den Identitätswechsel Programm gesteuert aus.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-104">The server performs impersonation programmatically.</span></span> <span data-ttu-id="8c5dc-105">Die Sicherheits Anmelde Informationen des Clients werden mithilfe von " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" explizit angenommen.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-105">It explicitly assumes the client's security credentials by using [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="8c5dc-106">Wenn der Client die ausreichende Berechtigung für den Server erteilt hat, besteht die Auswirkung, dass die Sicherheits Anmelde Informationen des Clients anstelle des Prozess Tokens durch das Thread Token des Servers ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-106">When the client has granted the server sufficient authority, this has the effect of substituting the client's security credentials with the server thread token, in place of the process token.</span></span>

<span data-ttu-id="8c5dc-107">Wenn dies der Fall ist, kann der Server z. b. das Client Token für den Zugriff auf Ressourcen verwenden, die mit einer Sicherheits Beschreibung geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-107">When this has been done, the server can, for example, use the client token to access resources guarded with a security descriptor.</span></span> <span data-ttu-id="8c5dc-108">Oder es können Aufrufe unter der Client Identität durchführen, wenn das Cloaking aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-108">Or it can make calls under the client identity, if cloaking is enabled.</span></span>

<span data-ttu-id="8c5dc-109">Der Server kann das Cloaking Programm gesteuert explizit festlegen, oder er kann sich auf eine administrative Einstellung verlassen.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-109">The server can explicitly set cloaking programmatically, or it can rely on an administrative setting.</span></span> <span data-ttu-id="8c5dc-110">Standardmäßig sind com+-Anwendungen für die Verwendung von dynamischem Cloaking konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-110">By default, COM+ applications are configured to use dynamic cloaking.</span></span> <span data-ttu-id="8c5dc-111">Weitere Details finden Sie unter [Cloaking](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="8c5dc-111">For more detail, see [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="8c5dc-112">Wenn der Server die Delegierung im Namen des Clients implementiert – unter Verwendung der Client Identität über das Netzwerk – muss die Server Prozess Identität im Active Directory Dienst als "vertrauenswürdig für die Delegierung" gekennzeichnet werden. Andernfalls tritt bei der Delegierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-112">If the server is implementing delegation on behalf of the client—using the client identity over network—the server process identity must be marked as "Trusted for delegation" in the Active Directory Service; otherwise, delegation will fail.</span></span>

<span data-ttu-id="8c5dc-113">Wenn die Client Identität nicht mehr verwendet wird, kann der Server mithilfe von [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)auf das eigene Prozess Token zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-113">When it has finished using the client's identity, the server can revert to its own process token using [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="8c5dc-114">Ausführliche Informationen zum Implementieren des Identitäts Wechsels und der Delegierung finden Sie unter [Delegierung und](/windows/desktop/com/delegation-and-impersonation)Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-114">For details on implementing impersonation and delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c5dc-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c5dc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c5dc-116">Client Identitätswechsel und Delegierung</span><span class="sxs-lookup"><span data-stu-id="8c5dc-116">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="8c5dc-117">Client seitige Anforderungen für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="8c5dc-117">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="8c5dc-118">Cloaking</span><span class="sxs-lookup"><span data-stu-id="8c5dc-118">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

 
