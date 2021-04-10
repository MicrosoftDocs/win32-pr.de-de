---
title: Moniker
description: Ein Moniker in com ist nicht nur eine Möglichkeit zum Identifizieren eines Objekts \ 8212; ein Moniker wird auch als Objekt implementiert.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036395"
---
# <a name="monikers"></a><span data-ttu-id="e9ce9-103">Moniker</span><span class="sxs-lookup"><span data-stu-id="e9ce9-103">Monikers</span></span>

<span data-ttu-id="e9ce9-104">Ein Moniker in com ist nicht nur eine Möglichkeit, ein Objekt zu identifizieren – ein Moniker wird auch als Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-104">A moniker in COM is not only a way to identify an object—a moniker is also implemented as an object.</span></span> <span data-ttu-id="e9ce9-105">Dieses Objekt stellt Dienste bereit, mit denen eine Komponente einen Zeiger auf das vom Moniker identifizierte Objekt abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-105">This object provides services allowing a component to obtain a pointer to the object identified by the moniker.</span></span> <span data-ttu-id="e9ce9-106">Dieser Vorgang wird als *Bindung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-106">This process is referred to as *binding*.</span></span>

<span data-ttu-id="e9ce9-107">Moniker sind Objekte, die die [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle implementieren und im Allgemeinen in DLLs als Komponenten Objekte implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-107">Monikers are objects that implement the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface and are generally implemented in DLLs as component objects.</span></span> <span data-ttu-id="e9ce9-108">Es gibt zwei Möglichkeiten, die Verwendung von Monikern anzuzeigen: als monikerclient, eine Komponente, die einen Moniker verwendet, um einen Zeiger auf ein anderes Objekt zu erhalten. und als monikeranbieter eine Komponente, die Moniker bereitstellt, die ihre Objekte an monikerclients identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-108">There are two ways of viewing the use of monikers: as a moniker client, a component that uses a moniker to get a pointer to another object; and as a moniker provider, a component that supplies monikers identifying its objects to moniker clients.</span></span>

<span data-ttu-id="e9ce9-109">OLE verwendet Moniker, um Verbindungen mit Objekten herzustellen und Sie zu aktivieren, unabhängig davon, ob Sie sich auf demselben Computer oder über ein Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-109">OLE uses monikers to connect to and activate objects, whether they are in the same machine or across a network.</span></span> <span data-ttu-id="e9ce9-110">Eine sehr wichtige Verwendung ist für Netzwerkverbindungen.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-110">A very important use is for network connections.</span></span> <span data-ttu-id="e9ce9-111">Sie werden auch zum identifizieren, verbinden und Ausführen von OLE-Verbund Dokumenten Verknüpfungs Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-111">They are also used to identify, connect to, and run OLE compound document link objects.</span></span> <span data-ttu-id="e9ce9-112">In diesem Fall fungiert die Link Quelle als monikeranbieter, und der Container, der das Link Objekt enthält, fungiert als monikerclient.</span><span class="sxs-lookup"><span data-stu-id="e9ce9-112">In this case, the link source acts as the moniker provider and the container holding the link object acts as the moniker client.</span></span>

<span data-ttu-id="e9ce9-113">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e9ce9-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e9ce9-114">Monikerclients</span><span class="sxs-lookup"><span data-stu-id="e9ce9-114">Moniker Clients</span></span>](moniker-clients.md)
-   [<span data-ttu-id="e9ce9-115">Monikeranbieter</span><span class="sxs-lookup"><span data-stu-id="e9ce9-115">Moniker Providers</span></span>](moniker-providers.md)
-   [<span data-ttu-id="e9ce9-116">OLE-Monikerimplementierungen</span><span class="sxs-lookup"><span data-stu-id="e9ce9-116">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)

## <a name="related-topics"></a><span data-ttu-id="e9ce9-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9ce9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ce9-118">Das Component Object Model</span><span class="sxs-lookup"><span data-stu-id="e9ce9-118">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 




