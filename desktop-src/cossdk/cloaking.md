---
description: Es gibt zwei Faktoren bei der Ermittlung des Verhaltens des Identitäts Wechsels der Zertifizierungsstelle, die der Client dem Server explizit über eine Identitätswechsel Ebene zuweist, und die Fähigkeit der Server, seine eigene Identität zu maskieren, wenn Aufrufe im Auftrag des Clients durchgeführt werden.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Cloaking (Komponenten Dienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748081"
---
# <a name="cloaking-component-services"></a><span data-ttu-id="1144c-103">Cloaking (Komponenten Dienste)</span><span class="sxs-lookup"><span data-stu-id="1144c-103">Cloaking (Component Services)</span></span>

<span data-ttu-id="1144c-104">Beim Festlegen des Verhaltens des Identitäts Wechsels gibt es zwei Komponenten: die Autorität, die der Client dem Server explizit über eine Identitätswechsel Ebene zuweist, und die Fähigkeit des Servers, seine eigene Identität zu maskieren, wenn Aufrufe im Auftrag des Clients durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1144c-104">There are two ingredients in determining the behavior of impersonation: the authority the client explicitly grants the server through an impersonation level and the server's ability to mask its own identity when making calls on the client's behalf.</span></span> <span data-ttu-id="1144c-105">Diese letztere Funktion wird als " *Cloaking*" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1144c-105">This latter capability is known as *cloaking*.</span></span> <span data-ttu-id="1144c-106">Das Cloaking muss mit der Sicherheitsidentität durchzuführen sein, unter der der Server Aufrufe ausführt.</span><span class="sxs-lookup"><span data-stu-id="1144c-106">Cloaking has to do with the security identity under which the server makes calls.</span></span>

<span data-ttu-id="1144c-107">Wenn der Server die Identität des Clients annimmt, hat er direkten Zugriff auf die Sicherheits Anmelde Informationen des Clients.</span><span class="sxs-lookup"><span data-stu-id="1144c-107">When the server impersonates the client, it has direct access to the client's security credentials.</span></span> <span data-ttu-id="1144c-108">In einem sehr lokalen Sinne übernimmt der Server Thread die Identität des Clients.</span><span class="sxs-lookup"><span data-stu-id="1144c-108">In a very local sense, the server thread takes on the identity of the client.</span></span> <span data-ttu-id="1144c-109">Wenn der Server jedoch Aufrufe außerhalb des Prozesses durchführt, wird die Client Identität nicht notwendigerweise als Identität, unter der der Aufruf erfolgt, projiziert.</span><span class="sxs-lookup"><span data-stu-id="1144c-109">But when the server makes calls outside of its process, the client identity will not necessarily be projected as the identity under which the call is made.</span></span>

<span data-ttu-id="1144c-110">Wenn das Cloaking aktiviert ist, können Aufrufe von dem Server, der die Identität des Clients annimmt, unter der Identität des Clients vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="1144c-110">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="1144c-111">Wenn das Cloaking deaktiviert ist, werden Aufrufe durch den Server unter der Identität des Servers vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1144c-111">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

<span data-ttu-id="1144c-112">Darüber hinaus gibt es zwei Arten von Verstopfungen, *statischem* und *dynamischem* Cloaking, die wie folgt beschrieben werden können:</span><span class="sxs-lookup"><span data-stu-id="1144c-112">Moreover, there are two forms of cloaking, *static cloaking* and *dynamic cloaking*, which can be described as follows:</span></span>

-   <span data-ttu-id="1144c-113">Identitätswechsel mit statischem Cloaking.</span><span class="sxs-lookup"><span data-stu-id="1144c-113">Impersonation with static cloaking.</span></span> <span data-ttu-id="1144c-114">Die ursprüngliche Client Identität (die als Server Thread Token implementiert wurde) kann bei einem Aufruf mithilfe von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)einmal an einen Downstreamserver präsentiert werden, wobei die ursprüngliche Client Identität einmal auf dem Proxy festgelegt wird, und dass das Thread Token bei nachfolgenden Methoden aufrufen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1144c-114">The original client identity (realized as the server thread token) can be presented once to a downstream server on a call using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), setting the original client identity once on the proxy, and that thread token will be used on subsequent method calls.</span></span>
-   <span data-ttu-id="1144c-115">Identitätswechsel mit dynamischem Cloaking.</span><span class="sxs-lookup"><span data-stu-id="1144c-115">Impersonation with dynamic cloaking.</span></span> <span data-ttu-id="1144c-116">Die ursprüngliche Client Identität wird bei jedem Methodenaufrufe des Downstreamservers als Server Thread Token erkannt.</span><span class="sxs-lookup"><span data-stu-id="1144c-116">The original client identity is discovered as the server thread token on each method call to the downstream server.</span></span> <span data-ttu-id="1144c-117">Tatsächlich kann die Identität, die angezeigt wird, dynamisch bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="1144c-117">In effect, the identity that is presented can be determined dynamically.</span></span> <span data-ttu-id="1144c-118">Der Aufwand, der dazu erforderlich ist, kann deutlich teurer werden.</span><span class="sxs-lookup"><span data-stu-id="1144c-118">The overhead required to do this can be considerably more expensive.</span></span>

<span data-ttu-id="1144c-119">Für COM+-Anwendungen ist die Standardkonfiguration für die Funktion für dynamisches durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="1144c-119">For COM+ applications, the default configuration is for dynamic cloaking capability.</span></span> <span data-ttu-id="1144c-120">Dies kann Programm gesteuert und administrativ geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1144c-120">This can be changed programmatically and administratively.</span></span> <span data-ttu-id="1144c-121">Während das dynamische Cloaking einen Leistungs Aufwand verursachen kann, bietet es die Flexibilität, die normalerweise für Umstände erforderlich ist, die die Verwendung von Identitätswechsel an erster Stelle erfordern.</span><span class="sxs-lookup"><span data-stu-id="1144c-121">While dynamic cloaking can have performance overhead, it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

<span data-ttu-id="1144c-122">Weitere Details zu den Zusammenhang und genauen Beschreibungen möglicher Verhalten finden Sie unter " [Cloaking](/windows/desktop/com/cloaking) " in der com-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="1144c-122">For more detail regarding cloaking and precise descriptions of possible behaviors, see [Cloaking](/windows/desktop/com/cloaking) in the COM documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1144c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1144c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1144c-124">Client Identitätswechsel und Delegierung</span><span class="sxs-lookup"><span data-stu-id="1144c-124">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="1144c-125">Client seitige Anforderungen für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="1144c-125">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="1144c-126">Server seitige Anforderungen für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="1144c-126">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
