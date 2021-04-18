---
description: Enthält die Auflistungen der obersten Ebene im-Katalog.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Stamm Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340109"
---
# <a name="root-collection"></a><span data-ttu-id="bc305-103">Stamm Sammlung</span><span class="sxs-lookup"><span data-stu-id="bc305-103">Root collection</span></span>

<span data-ttu-id="bc305-104">Enthält die Auflistungen der obersten Ebene im-Katalog.</span><span class="sxs-lookup"><span data-stu-id="bc305-104">Contains the top-level collections in the catalog.</span></span> <span data-ttu-id="bc305-105">Sie enthält keine [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekte oder unterstützt keine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc305-105">It does not contain any [**COMAdminCatalogObject**](comadmincatalogobject.md) objects or support any properties.</span></span>

<span data-ttu-id="bc305-106">Die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts wird **von der Stamm** Auflistung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc305-106">The **Root** collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="bc305-107">Sie können nicht von einer Auflistung **aus zur Stamm Sammlung navigieren** .</span><span class="sxs-lookup"><span data-stu-id="bc305-107">You cannot navigate to the **Root** collection from any collection.</span></span>

## <a name="members"></a><span data-ttu-id="bc305-108">Member</span><span class="sxs-lookup"><span data-stu-id="bc305-108">Members</span></span>

<span data-ttu-id="bc305-109">Die **Stamm** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="bc305-109">The **Root** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="bc305-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="bc305-110">Related Collections</span></span>

<span data-ttu-id="bc305-111">Im folgenden finden Sie die Auflistungen der obersten Ebene im-Katalog:</span><span class="sxs-lookup"><span data-stu-id="bc305-111">The following are the top-level collections in the catalog:</span></span>

-   [<span data-ttu-id="bc305-112">**ApplicationCluster**</span><span class="sxs-lookup"><span data-stu-id="bc305-112">**ApplicationCluster**</span></span>](applicationcluster.md)
-   [<span data-ttu-id="bc305-113">**ApplicationInstance**</span><span class="sxs-lookup"><span data-stu-id="bc305-113">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="bc305-114">**Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="bc305-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="bc305-115">**Computer Liste**</span><span class="sxs-lookup"><span data-stu-id="bc305-115">**ComputerList**</span></span>](computerlist.md)
-   [<span data-ttu-id="bc305-116">**Dcomprotokolle**</span><span class="sxs-lookup"><span data-stu-id="bc305-116">**DCOMProtocols**</span></span>](dcomprotocols.md)
-   [<span data-ttu-id="bc305-117">**Eventclassesforiid**</span><span class="sxs-lookup"><span data-stu-id="bc305-117">**EventClassesForIID**</span></span>](eventclassesforiid.md)
-   [<span data-ttu-id="bc305-118">**Filesforimport**</span><span class="sxs-lookup"><span data-stu-id="bc305-118">**FilesForImport**</span></span>](filesforimport.md)
-   [<span data-ttu-id="bc305-119">**Inprocservers**</span><span class="sxs-lookup"><span data-stu-id="bc305-119">**InprocServers**</span></span>](inprocservers.md)
-   [<span data-ttu-id="bc305-120">**Legacyserver**</span><span class="sxs-lookup"><span data-stu-id="bc305-120">**LegacyServers**</span></span>](legacyservers.md)
-   [<span data-ttu-id="bc305-121">**LocalComputer**</span><span class="sxs-lookup"><span data-stu-id="bc305-121">**LocalComputer**</span></span>](localcomputer.md)
-   [<span data-ttu-id="bc305-122">**Partitionen**</span><span class="sxs-lookup"><span data-stu-id="bc305-122">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="bc305-123">**Partitionusers**</span><span class="sxs-lookup"><span data-stu-id="bc305-123">**PartitionUsers**</span></span>](partitionusers.md)
-   [<span data-ttu-id="bc305-124">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="bc305-124">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="bc305-125">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="bc305-125">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="bc305-126">**Transientabonnements**</span><span class="sxs-lookup"><span data-stu-id="bc305-126">**TransientSubscriptions**</span></span>](transientsubscriptions.md)
-   [<span data-ttu-id="bc305-127">**Wowinprocservers**</span><span class="sxs-lookup"><span data-stu-id="bc305-127">**WOWInprocServers**</span></span>](wowinprocservers.md)
-   [<span data-ttu-id="bc305-128">**Wowlegacyservers**</span><span class="sxs-lookup"><span data-stu-id="bc305-128">**WOWLegacyServers**</span></span>](wowlegacyservers.md)

## <a name="see-also"></a><span data-ttu-id="bc305-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc305-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc305-130">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="bc305-130">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
