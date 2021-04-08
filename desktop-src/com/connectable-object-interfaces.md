---
title: Verbindungs fähige Objekt Schnittstellen
description: Verbindungs fähige Objekt Schnittstellen
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856908"
---
# <a name="connectable-object-interfaces"></a><span data-ttu-id="307f7-103">Verbindungs fähige Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="307f7-103">Connectable Object Interfaces</span></span>

<span data-ttu-id="307f7-104">Die Unterstützung für Verbindungs fähige Objekte erfordert die Unterstützung für vier Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="307f7-104">Support for connectable objects requires support for four interfaces:</span></span>

-   <span data-ttu-id="307f7-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) für das Verbindungs fähigen-Objekt</span><span class="sxs-lookup"><span data-stu-id="307f7-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) on the connectable object</span></span>
-   <span data-ttu-id="307f7-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) für das Verbindungspunkt Objekt</span><span class="sxs-lookup"><span data-stu-id="307f7-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) on the connection point object</span></span>
-   <span data-ttu-id="307f7-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) für ein Enumeratorobjekt</span><span class="sxs-lookup"><span data-stu-id="307f7-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) on an enumerator object</span></span>
-   <span data-ttu-id="307f7-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) für ein Enumeratorobjekt</span><span class="sxs-lookup"><span data-stu-id="307f7-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) on an enumerator object</span></span>

<span data-ttu-id="307f7-109">Die beiden letzteren sind als standardenumeratoren für die Typen **IConnectionPoint \*** und [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata)definiert.</span><span class="sxs-lookup"><span data-stu-id="307f7-109">The latter two are defined as standard enumerators for the types **IConnectionPoint \*** and [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span></span>

<span data-ttu-id="307f7-110">Außerdem kann das Verbindungs fähigen-Objekt optional [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) und [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) unterstützen, um für einen Client ausreichend Informationen bereitzustellen, damit der Client zur Laufzeit Unterstützung für die ausgehende Schnittstelle bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="307f7-110">Additionally, the connectable object can optionally support [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) to provide enough information to a client so that the client can provide support for the outgoing interface at run time.</span></span>

<span data-ttu-id="307f7-111">Schließlich muss der Client ein Sink-Objekt bereitstellen, das die ausgehende Schnittstelle implementiert. Dies ist eine benutzerdefinierte COM-Schnittstelle, die vom Verbindungs fähigen-Objekt definiert wird.</span><span class="sxs-lookup"><span data-stu-id="307f7-111">Finally, the client must provide a sink object that implements the outgoing interface, which is a custom COM interface defined by the connectable object.</span></span>

<span data-ttu-id="307f7-112">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="307f7-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="307f7-113">Verwenden von IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="307f7-113">Using IConnectionPointContainer</span></span>](using-iconnectionpointcontainer.md)
-   [<span data-ttu-id="307f7-114">Verwenden von IConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="307f7-114">Using IConnectionPoint</span></span>](using-iconnectionpoint.md)
-   [<span data-ttu-id="307f7-115">Verwenden von IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="307f7-115">Using IProvideClassInfo</span></span>](using-iprovideclassinfo.md)

## <a name="related-topics"></a><span data-ttu-id="307f7-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="307f7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="307f7-117">Architektur von Verbindungs fähigen Objekten</span><span class="sxs-lookup"><span data-stu-id="307f7-117">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




