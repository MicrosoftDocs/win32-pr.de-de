---
title: Proxy
description: Ein Proxy befindet sich im Adressraum des aufrufenden Prozesses und fungiert als Ersatz für das Remote Objekt.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106361101"
---
# <a name="proxy"></a><span data-ttu-id="62095-103">Proxy</span><span class="sxs-lookup"><span data-stu-id="62095-103">Proxy</span></span>

<span data-ttu-id="62095-104">Ein Proxy befindet sich im Adressraum des aufrufenden Prozesses und fungiert als Ersatz für das Remote Objekt.</span><span class="sxs-lookup"><span data-stu-id="62095-104">A proxy resides in the address space of the calling process and acts as a surrogate for the remote object.</span></span> <span data-ttu-id="62095-105">Aus der Perspektive des aufrufenden Objekts ist der Proxy das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="62095-105">From the perspective of the calling object, the proxy is the object.</span></span> <span data-ttu-id="62095-106">In der Regel besteht die Rolle des Proxys darin, die Schnittstellenparameter für Aufrufe von Methoden in seinen Objekt Schnittstellen zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="62095-106">Typically, the proxy's role is to package the interface parameters for calls to methods in its object interfaces.</span></span> <span data-ttu-id="62095-107">Der Proxy verpackt die Parameter in einem Nachrichten Puffer und übergibt den Puffer an den Kanal, der den Transport zwischen Prozessen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="62095-107">The proxy packages the parameters into a message buffer and passes the buffer onto the channel, which handles the transport between processes.</span></span> <span data-ttu-id="62095-108">Der Proxy wird als Aggregat-oder zusammengesetztes Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="62095-108">The proxy is implemented as an aggregate, or composite, object.</span></span> <span data-ttu-id="62095-109">Es enthält ein vom System bereitgestelltes Manager-Element, das als Proxy Manager und eine oder mehrere Schnittstellen spezifische Komponenten bezeichnet wird, die als Schnittstellen Proxys bezeichnet werden</span><span class="sxs-lookup"><span data-stu-id="62095-109">It contains a system-provided, manager piece called the proxy manager and one or more interface-specific components called interface proxies.</span></span> <span data-ttu-id="62095-110">Die Anzahl der Schnittstellen Proxys entspricht der Anzahl von Objekt Schnittstellen, die für diesen bestimmten Client verfügbar gemacht wurden.</span><span class="sxs-lookup"><span data-stu-id="62095-110">The number of interface proxies equals the number of object interfaces that have been exposed to that particular client.</span></span> <span data-ttu-id="62095-111">Für den Client, der das Komponentenobjektmodell erfüllt, scheint der Proxy das echte Objekt zu sein.</span><span class="sxs-lookup"><span data-stu-id="62095-111">To the client complying with the component object model, the proxy appears to be the real object.</span></span>

> [!Note]  
> <span data-ttu-id="62095-112">Mit benutzerdefiniertem Marshalling kann der Proxy ähnlich implementiert werden, oder er kann direkt mit dem Objekt kommunizieren, ohne einen Stub zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="62095-112">With custom marshaling, the proxy can be implemented similarly or it can communicate directly with the object without using a stub.</span></span>

 

<span data-ttu-id="62095-113">Jeder Schnittstellen Proxy ist ein Komponenten Objekt, das den Marshallingcode für eine der Schnittstellen des-Objekts implementiert.</span><span class="sxs-lookup"><span data-stu-id="62095-113">Each interface proxy is a component object that implements the marshaling code for one of the object's interfaces.</span></span> <span data-ttu-id="62095-114">Der Proxy stellt das Objekt dar, für das es Marshallingcode bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="62095-114">The proxy represents the object for which it provides marshaling code.</span></span> <span data-ttu-id="62095-115">Jeder Proxy implementiert auch die Schnittstelle " [**iripcproxybuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) ".</span><span class="sxs-lookup"><span data-stu-id="62095-115">Each proxy also implements the [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) interface.</span></span> <span data-ttu-id="62095-116">Obwohl die vom Proxy dargestellte Objektschnittstelle öffentlich ist, ist die Implementierung von " **typcproxybuffer** " Privat und wird intern innerhalb des Proxys verwendet.</span><span class="sxs-lookup"><span data-stu-id="62095-116">Although the object interface represented by the proxy is public, the **IRpcProxyBuffer** implementation is private and is used internally within the proxy.</span></span> <span data-ttu-id="62095-117">Der Proxy-Manager verfolgt die Schnittstellen Proxys und enthält auch die öffentliche Implementierung der kontrollierten [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle für das Aggregat.</span><span class="sxs-lookup"><span data-stu-id="62095-117">The proxy manager keeps track of the interface proxies and also contains the public implementation of the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface for the aggregate.</span></span> <span data-ttu-id="62095-118">Jeder Schnittstellen Proxy kann in einer separaten dll vorhanden sein, die geladen wird, wenn die Schnittstelle, die er unterstützt, auf den Client materialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="62095-118">Each interface proxy can exist in a separate DLL that is loaded when the interface it supports is materialized to the client.</span></span>

## <a name="structure-of-the-proxy"></a><span data-ttu-id="62095-119">Struktur des Proxys</span><span class="sxs-lookup"><span data-stu-id="62095-119">Structure of the Proxy</span></span>

<span data-ttu-id="62095-120">Das folgende Diagramm zeigt die Struktur eines Proxys, der das Standardmarshalling von Parametern unterstützt, die zu zwei Schnittstellen gehören: IA1 und IA2.</span><span class="sxs-lookup"><span data-stu-id="62095-120">The following diagram shows the structure of a proxy that supports the standard marshaling of parameters belonging to two interfaces: IA1 and IA2.</span></span> <span data-ttu-id="62095-121">Jeder Schnittstellen Proxy implementiert " [**iripcproxybuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) " für die interne Kommunikation zwischen den Aggregat teilen.</span><span class="sxs-lookup"><span data-stu-id="62095-121">Each interface proxy implements [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) for internal communication between the aggregate pieces.</span></span> <span data-ttu-id="62095-122">Wenn der Proxy bereit ist, seine gemarshallten Parameter über die Prozess Grenze hinweg zu übergeben, ruft er Methoden in der Schnittstelle " [**iripcchannelbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) " auf, die vom Kanal implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="62095-122">When the proxy is ready to pass its marshaled parameters across the process boundary, it calls methods in the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface, which is implemented by the channel.</span></span> <span data-ttu-id="62095-123">Der-Kanal leitet wiederum den Aufruf an die RPC-Lauf Zeit Bibliothek weiter, sodass er sein Ziel im-Objekt erreichen kann.</span><span class="sxs-lookup"><span data-stu-id="62095-123">The channel in turn forwards the call to the RPC run-time library so that it can reach its destination in the object.</span></span>

![Diagramm, das die Struktur des Proxys anzeigt.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a><span data-ttu-id="62095-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62095-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62095-126">Kanal</span><span class="sxs-lookup"><span data-stu-id="62095-126">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="62095-127">Kommunikation zwischen Objekten</span><span class="sxs-lookup"><span data-stu-id="62095-127">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="62095-128">Marshalling von Details</span><span class="sxs-lookup"><span data-stu-id="62095-128">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="62095-129">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="62095-129">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="62095-130">Stub</span><span class="sxs-lookup"><span data-stu-id="62095-130">Stub</span></span>](stub.md)
</dt> </dl>

 

 