---
description: Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: PropertyInfo-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127020"
---
# <a name="propertyinfo-collection"></a><span data-ttu-id="b8156-103">PropertyInfo-Auflistung</span><span class="sxs-lookup"><span data-stu-id="b8156-103">PropertyInfo collection</span></span>

<span data-ttu-id="b8156-104">Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b8156-104">Retrieves information about the properties that a specified collection supports.</span></span> <span data-ttu-id="b8156-105">Der Zugriff auf die **PropertyInfo** -Auflistung ist von jedem [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aus möglich, indem die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8156-105">The **PropertyInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="b8156-106">Die **PropertyInfo** -Auflistung enthält ein-Objekt für jede Eigenschaft, die von der ursprünglichen Auflistung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b8156-106">The **PropertyInfo** collection contains one object for each property that is supported by the original collection.</span></span>

## <a name="members"></a><span data-ttu-id="b8156-107">Member</span><span class="sxs-lookup"><span data-stu-id="b8156-107">Members</span></span>

<span data-ttu-id="b8156-108">Die **PropertyInfo** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="b8156-108">The **PropertyInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b8156-109">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="b8156-109">Related Collections</span></span>

<span data-ttu-id="b8156-110">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="b8156-110">You can navigate from this collection to any of the following collections:</span></span>

-   <span data-ttu-id="b8156-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b8156-111">**PropertyInfo**</span></span>
-   [<span data-ttu-id="b8156-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="b8156-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b8156-113">Sie können von jeder Sammlung aus zu dieser Sammlung navigieren.</span><span class="sxs-lookup"><span data-stu-id="b8156-113">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="b8156-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8156-114">Properties</span></span>

<span data-ttu-id="b8156-115">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b8156-115">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b8156-116">Name</span><span class="sxs-lookup"><span data-stu-id="b8156-116">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="b8156-117">Name</span><span class="sxs-lookup"><span data-stu-id="b8156-117">Name</span></span>



| <span data-ttu-id="b8156-118">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b8156-118">Entry</span></span> | <span data-ttu-id="b8156-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b8156-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8156-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8156-120">Description</span></span>    | <span data-ttu-id="b8156-121">Den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b8156-121">The name of the property.</span></span> <span data-ttu-id="b8156-122">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b8156-122">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b8156-123">Access</span><span class="sxs-lookup"><span data-stu-id="b8156-123">Access</span></span>         | <span data-ttu-id="b8156-124">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b8156-124">ReadOnly</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="b8156-125">type</span><span class="sxs-lookup"><span data-stu-id="b8156-125">Type</span></span>           | <span data-ttu-id="b8156-126">String</span><span class="sxs-lookup"><span data-stu-id="b8156-126">String</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="b8156-127">Standard</span><span class="sxs-lookup"><span data-stu-id="b8156-127">Default</span></span>        | <span data-ttu-id="b8156-128">Keine</span><span class="sxs-lookup"><span data-stu-id="b8156-128">None</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="b8156-129">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="b8156-129">Minimum system</span></span> | <span data-ttu-id="b8156-130">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b8156-130">Windows 2000</span></span>                                                                                                                                                                                     |



 

## <a name="see-also"></a><span data-ttu-id="b8156-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8156-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8156-132">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="b8156-132">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
