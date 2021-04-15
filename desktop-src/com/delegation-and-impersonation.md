---
title: Delegierung und Identitätswechsel
description: In Client-/Serverszenarien ist es üblich, dass ein Server einen anderen Server aufruft, um eine Aufgabe im Auftrag eines Clients auszuführen. Die Situation, in der ein Server die Autorität erhält, im Auftrag eines Clients zu agieren, wird als Delegierung bezeichnet.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550047"
---
# <a name="delegation-and-impersonation"></a><span data-ttu-id="922e3-104">Delegierung und Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="922e3-104">Delegation and Impersonation</span></span>

<span data-ttu-id="922e3-105">In Client-/Serverszenarien ist es üblich, dass ein Server einen anderen Server aufruft, um eine Aufgabe im Auftrag eines Clients auszuführen.</span><span class="sxs-lookup"><span data-stu-id="922e3-105">In client/server scenarios, it is common for one server to call another server to accomplish some task on a client's behalf.</span></span> <span data-ttu-id="922e3-106">Die Situation, in der ein Server die Autorität erhält, im Auftrag eines Clients zu agieren, wird als *Delegierung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="922e3-106">The situation where a server is given the authority to act on a client's behalf is called *delegation*.</span></span>

<span data-ttu-id="922e3-107">Aus Sicht der Sicherheit ergeben sich zwei Probleme im Hinblick auf die Delegierung:</span><span class="sxs-lookup"><span data-stu-id="922e3-107">From a security standpoint, two issues arise regarding delegation:</span></span>

-   <span data-ttu-id="922e3-108">Was soll der Server tun, wenn er im Auftrag des Clients agiert?</span><span class="sxs-lookup"><span data-stu-id="922e3-108">What should the server be allowed to do when acting on the client's behalf?</span></span>
-   <span data-ttu-id="922e3-109">Welche Identität wird vom Server angezeigt, wenn er andere Server im Auftrag eines Clients aufruft?</span><span class="sxs-lookup"><span data-stu-id="922e3-109">What identity is presented by the server when it calls other servers on behalf of a client?</span></span>

<span data-ttu-id="922e3-110">Um diese Probleme zu beheben, bietet com die folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="922e3-110">To deal with these issues, COM provides the following functionality.</span></span> <span data-ttu-id="922e3-111">Vom Client kann eine Identitätswechsel *Ebene* festgelegt werden, die festlegt, in welchem Umfang der Server als Client fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="922e3-111">The client can set an *impersonation level* that determines to what extent the server will be able to act as the client.</span></span> <span data-ttu-id="922e3-112">Wenn der Client dem Server genügend Berechtigungen gewährt *, kann der* Server den Client als Identitätswechsel durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="922e3-112">If the client grants enough authority to the server, the server can *impersonate* (pretend to be) the client.</span></span> <span data-ttu-id="922e3-113">Beim Annehmen der Identität des Clients erhält der Server Zugriff auf nur die Objekte oder Ressourcen, für die der Client über die Berechtigung verfügt.</span><span class="sxs-lookup"><span data-stu-id="922e3-113">When impersonating the client, the server is given access to only those objects or resources that the client has permission to use.</span></span> <span data-ttu-id="922e3-114">Der Server, der als Client fungiert, kann auch das *ausblenden aktivieren,* um seine eigene Identität zu maskieren und die Identität des Clients in Aufrufen anderer com-Komponenten zu projizieren.</span><span class="sxs-lookup"><span data-stu-id="922e3-114">The server, acting as a client, can also enable *cloaking* to mask its own identity and project the client's identity in calls to other COM components.</span></span>

![Diagramm, das zeigt, wie der Server, der als Client fungiert, das Cloaking aktivieren kann.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

<span data-ttu-id="922e3-116">Sehen Sie sich das Szenario an, das in der obigen Abbildung veranschaulicht wird. a und b sind Prozesse auf einem anderen Computer als C. verarbeiten a-Aufrufe b und b C. Client A legt die Identitätswechsel Ebene fest.</span><span class="sxs-lookup"><span data-stu-id="922e3-116">Consider the scenario illustrated by the preceding figure, where A and B are processes on a different machine from C. Process A calls B, and B calls C. Client A sets the impersonation level.</span></span> <span data-ttu-id="922e3-117">B legt die Funktionsfähigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="922e3-117">B sets the cloaking capability.</span></span> <span data-ttu-id="922e3-118">Wenn eine eine Identitätswechsel Ebene festlegt, die den Identitätswechsel zulässt, kann B die Identität eines annehmen, wenn C in einem Auftrag aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="922e3-118">If A sets an impersonation level that permits impersonation, B can impersonate A when calling C on A's behalf.</span></span> <span data-ttu-id="922e3-119">Die Identität, die für Prozess C dargestellt wird, ist entweder eine Identität oder die Identität des b, abhängig davon, ob das Cloaking durch B aktiviert wurde. Wenn das Cloaking aktiviert ist, ist die für Prozess C vorgelegte Identität die eines. Wenn das Cloaking nicht aktiviert ist, wird die Identität von B in C angezeigt.</span><span class="sxs-lookup"><span data-stu-id="922e3-119">The identity that is presented to process C will be either A's identity or B's identity, depending on whether cloaking was enabled by B. If cloaking is enabled, the identity presented to process C will be that of A. If cloaking is not enabled, B's identity will be presented to C.</span></span>

<span data-ttu-id="922e3-120">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="922e3-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="922e3-121">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="922e3-121">Impersonation</span></span>](impersonation.md)
-   [<span data-ttu-id="922e3-122">Identitätswechsel Ebenen</span><span class="sxs-lookup"><span data-stu-id="922e3-122">Impersonation Levels</span></span>](impersonation-levels.md)
-   [<span data-ttu-id="922e3-123">Cloaking</span><span class="sxs-lookup"><span data-stu-id="922e3-123">Cloaking</span></span>](cloaking.md)

 

 




