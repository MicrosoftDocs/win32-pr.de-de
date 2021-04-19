---
title: Stub
description: Der Stub besteht wie der Proxy aus einem oder mehreren Schnittstellen teilen und einem Manager.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106369916"
---
# <a name="stub"></a><span data-ttu-id="bead7-103">Stub</span><span class="sxs-lookup"><span data-stu-id="bead7-103">Stub</span></span>

<span data-ttu-id="bead7-104">Der Stub besteht wie der Proxy aus einem oder mehreren Schnittstellen teilen und einem Manager.</span><span class="sxs-lookup"><span data-stu-id="bead7-104">The stub, like the proxy, is made up of one or more interface pieces and a manager.</span></span> <span data-ttu-id="bead7-105">Jeder schnittstellenstub stellt Code bereit, um die Parameter und den Code, der eine der unterstützten Schnittstellen des Objekts aufruft, zu entmarshalling.</span><span class="sxs-lookup"><span data-stu-id="bead7-105">Each interface stub provides code to unmarshal the parameters and code that calls one of the object's supported interfaces.</span></span> <span data-ttu-id="bead7-106">Jeder Stub stellt außerdem eine Schnittstelle für die interne Kommunikation bereit.</span><span class="sxs-lookup"><span data-stu-id="bead7-106">Each stub also provides an interface for internal communication.</span></span> <span data-ttu-id="bead7-107">Der Stub-Manager verfolgt die verfügbaren Schnittstellenstubs nach.</span><span class="sxs-lookup"><span data-stu-id="bead7-107">The stub manager keeps track of the available interface stubs.</span></span>

<span data-ttu-id="bead7-108">Es gibt jedoch die folgenden Unterschiede zwischen dem Stub und dem Proxy:</span><span class="sxs-lookup"><span data-stu-id="bead7-108">There are, however, the following differences between the stub and the proxy:</span></span>

-   <span data-ttu-id="bead7-109">Der wichtigste Unterschied besteht darin, dass der Stub den Client im Adressraum des Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="bead7-109">The most important difference is that the stub represents the client in the object's address space.</span></span>
-   <span data-ttu-id="bead7-110">Der Stub wird nicht als Aggregat Objekt implementiert, weil es nicht erforderlich ist, dass der Client als einzelne Einheit angezeigt wird. jedes Element im Stub ist eine separate Komponente.</span><span class="sxs-lookup"><span data-stu-id="bead7-110">The stub is not implemented as an aggregate object because there is no requirement that the client be viewed as a single unit; each piece in the stub is a separate component.</span></span>
-   <span data-ttu-id="bead7-111">Die schnittstellenstubweisen sind privat und nicht öffentlich.</span><span class="sxs-lookup"><span data-stu-id="bead7-111">The interface stubs are private rather than public.</span></span>
-   <span data-ttu-id="bead7-112">Die schnittstellenstubvorgänge implementieren " [**unpcstubbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer)", nicht " [**unpcproxybuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer)".</span><span class="sxs-lookup"><span data-stu-id="bead7-112">The interface stubs implement [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), not [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span></span>
-   <span data-ttu-id="bead7-113">Anstatt Parameter zu verpacken, die gemarshallt werden sollen, entpackt der Stub diese, nachdem Sie gemarshallt wurden, und verpackt dann die Antwort.</span><span class="sxs-lookup"><span data-stu-id="bead7-113">Instead of packaging parameters to be marshaled, the stub unpackages them after they have been marshaled and then packages the reply.</span></span>

## <a name="structure-of-the-stub"></a><span data-ttu-id="bead7-114">Struktur des Stubs</span><span class="sxs-lookup"><span data-stu-id="bead7-114">Structure of the Stub</span></span>

<span data-ttu-id="bead7-115">Das folgende Diagramm zeigt die Struktur des Stub.</span><span class="sxs-lookup"><span data-stu-id="bead7-115">The following diagram shows the structure of the stub.</span></span> <span data-ttu-id="bead7-116">Jeder schnittstellenstub ist mit einer Schnittstelle für das Objekt verbunden.</span><span class="sxs-lookup"><span data-stu-id="bead7-116">Each interface stub is connected to an interface on the object.</span></span> <span data-ttu-id="bead7-117">Der Kanal sendet eingehende Nachrichten an den entsprechenden schnittstellenstub.</span><span class="sxs-lookup"><span data-stu-id="bead7-117">The channel dispatches incoming messages to the appropriate interface stub.</span></span> <span data-ttu-id="bead7-118">Alle Komponenten kommunizieren mit dem Kanal über " [**iripcchannelbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer)", die Schnittstelle, die Zugriff auf die RPC-Lauf Zeit Bibliothek bietet.</span><span class="sxs-lookup"><span data-stu-id="bead7-118">All the components talk to the channel through [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), the interface that provides access to the RPC run-time library.</span></span>

![Screenshot, der die Struktur des Stubs anzeigt.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a><span data-ttu-id="bead7-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bead7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bead7-121">Kanal</span><span class="sxs-lookup"><span data-stu-id="bead7-121">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="bead7-122">Kommunikation zwischen Objekten</span><span class="sxs-lookup"><span data-stu-id="bead7-122">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="bead7-123">Marshalling von Details</span><span class="sxs-lookup"><span data-stu-id="bead7-123">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="bead7-124">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="bead7-124">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="bead7-125">Proxy</span><span class="sxs-lookup"><span data-stu-id="bead7-125">Proxy</span></span>](proxy.md)
</dt> </dl>

 

 