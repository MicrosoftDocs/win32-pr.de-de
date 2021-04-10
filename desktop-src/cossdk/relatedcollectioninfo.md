---
description: Ruft Informationen zu anderen Auflistungen ab, die sich auf die Auflistung beziehen, von der Sie aufgerufen wird.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Relatedcollectioninfo-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214141"
---
# <a name="relatedcollectioninfo-collection"></a><span data-ttu-id="375b1-103">Relatedcollectioninfo-Auflistung</span><span class="sxs-lookup"><span data-stu-id="375b1-103">RelatedCollectionInfo collection</span></span>

<span data-ttu-id="375b1-104">Ruft Informationen zu anderen Auflistungen ab, die sich auf die Auflistung beziehen, von der Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="375b1-104">Retrieves information about other collections related to the collection from which it is called.</span></span> <span data-ttu-id="375b1-105">Auf die **relatedcollectioninfo** -Auflistung kann von jedem [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aus zugegriffen werden, indem die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="375b1-105">The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="375b1-106">Die **relatedcollectioninfo** -Auflistung enthält ein-Objekt für jede Auflistung, auf die von der ursprünglichen Auflistung aus zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="375b1-106">The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection.</span></span> <span data-ttu-id="375b1-107">Verwandte Sammlungen Folgen der Hierarchie der Komponenten Dienste-Verwaltungs Tools.</span><span class="sxs-lookup"><span data-stu-id="375b1-107">Related collections follow the Component Services administration tool collection hierarchy.</span></span>

<span data-ttu-id="375b1-108">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="375b1-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="375b1-109">Member</span><span class="sxs-lookup"><span data-stu-id="375b1-109">Members</span></span>

<span data-ttu-id="375b1-110">Die **relatedcollectioninfo** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="375b1-110">The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="375b1-111">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="375b1-111">Related Collections</span></span>

<span data-ttu-id="375b1-112">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="375b1-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="375b1-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="375b1-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   <span data-ttu-id="375b1-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="375b1-114">**RelatedCollectionInfo**</span></span>

<span data-ttu-id="375b1-115">Sie können von jeder Sammlung aus zu dieser Sammlung navigieren.</span><span class="sxs-lookup"><span data-stu-id="375b1-115">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="375b1-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="375b1-116">Properties</span></span>

<span data-ttu-id="375b1-117">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="375b1-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="375b1-118">Name</span><span class="sxs-lookup"><span data-stu-id="375b1-118">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="375b1-119">Name</span><span class="sxs-lookup"><span data-stu-id="375b1-119">Name</span></span>



| <span data-ttu-id="375b1-120">Eingabe</span><span class="sxs-lookup"><span data-stu-id="375b1-120">Entry</span></span> | <span data-ttu-id="375b1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="375b1-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="375b1-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="375b1-122">Description</span></span>    | <span data-ttu-id="375b1-123">Der Name der verknüpften Auflistung.</span><span class="sxs-lookup"><span data-stu-id="375b1-123">The name of the related collection.</span></span> <span data-ttu-id="375b1-124">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="375b1-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="375b1-125">Access</span><span class="sxs-lookup"><span data-stu-id="375b1-125">Access</span></span>         | <span data-ttu-id="375b1-126">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="375b1-126">ReadOnly</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="375b1-127">type</span><span class="sxs-lookup"><span data-stu-id="375b1-127">Type</span></span>           | <span data-ttu-id="375b1-128">String</span><span class="sxs-lookup"><span data-stu-id="375b1-128">String</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="375b1-129">Standard</span><span class="sxs-lookup"><span data-stu-id="375b1-129">Default</span></span>        | <span data-ttu-id="375b1-130">Keine</span><span class="sxs-lookup"><span data-stu-id="375b1-130">None</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="375b1-131">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="375b1-131">Minimum system</span></span> | <span data-ttu-id="375b1-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="375b1-132">Windows 2000</span></span>                                                                                                                                                                                               |



 

## <a name="see-also"></a><span data-ttu-id="375b1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="375b1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375b1-134">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="375b1-134">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
