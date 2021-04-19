---
description: Enthält ein-Objekt für jeden Partitions Benutzer.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Partitionusers-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343001"
---
# <a name="partitionusers-collection"></a><span data-ttu-id="65ea7-103">Partitionusers-Sammlung</span><span class="sxs-lookup"><span data-stu-id="65ea7-103">PartitionUsers collection</span></span>

<span data-ttu-id="65ea7-104">Enthält ein-Objekt für jeden Partitions Benutzer.</span><span class="sxs-lookup"><span data-stu-id="65ea7-104">Contains an object for each partition user.</span></span>

<span data-ttu-id="65ea7-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="65ea7-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="65ea7-106">Member</span><span class="sxs-lookup"><span data-stu-id="65ea7-106">Members</span></span>

<span data-ttu-id="65ea7-107">Die **partitionusers** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="65ea7-107">The **PartitionUsers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="65ea7-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="65ea7-108">Related Collections</span></span>

<span data-ttu-id="65ea7-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="65ea7-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="65ea7-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="65ea7-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="65ea7-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="65ea7-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="65ea7-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="65ea7-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="65ea7-113">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="65ea7-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="65ea7-114">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="65ea7-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="65ea7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65ea7-115">Properties</span></span>

<span data-ttu-id="65ea7-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="65ea7-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="65ea7-117">AccountName</span><span class="sxs-lookup"><span data-stu-id="65ea7-117">AccountName</span></span>](#accountname)
-   [<span data-ttu-id="65ea7-118">Defaultpartitionid</span><span class="sxs-lookup"><span data-stu-id="65ea7-118">DefaultPartitionID</span></span>](#defaultpartitionid)

### <a name="accountname"></a><span data-ttu-id="65ea7-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="65ea7-119">AccountName</span></span>



| <span data-ttu-id="65ea7-120">Eingabe</span><span class="sxs-lookup"><span data-stu-id="65ea7-120">Entry</span></span> | <span data-ttu-id="65ea7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="65ea7-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ea7-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65ea7-122">Description</span></span>    | <span data-ttu-id="65ea7-123">Der Name des Partitions Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="65ea7-123">Name of the partition user's account.</span></span> <span data-ttu-id="65ea7-124">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="65ea7-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="65ea7-125">Access</span><span class="sxs-lookup"><span data-stu-id="65ea7-125">Access</span></span>         | <span data-ttu-id="65ea7-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="65ea7-126">WriteOnce</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="65ea7-127">type</span><span class="sxs-lookup"><span data-stu-id="65ea7-127">Type</span></span>           | <span data-ttu-id="65ea7-128">String</span><span class="sxs-lookup"><span data-stu-id="65ea7-128">String</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="65ea7-129">Standard</span><span class="sxs-lookup"><span data-stu-id="65ea7-129">Default</span></span>        | <span data-ttu-id="65ea7-130">"Neuer Benutzer"</span><span class="sxs-lookup"><span data-stu-id="65ea7-130">"New User"</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="65ea7-131">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="65ea7-131">Minimum system</span></span> | <span data-ttu-id="65ea7-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65ea7-132">Windows Server 2003</span></span>                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a><span data-ttu-id="65ea7-133">Defaultpartitionid</span><span class="sxs-lookup"><span data-stu-id="65ea7-133">DefaultPartitionID</span></span>



| <span data-ttu-id="65ea7-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="65ea7-134">Entry</span></span> | <span data-ttu-id="65ea7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="65ea7-135">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="65ea7-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65ea7-136">Description</span></span>    | <span data-ttu-id="65ea7-137">Der Globally Unique Identifier für die Basis Anwendungs Partition.</span><span class="sxs-lookup"><span data-stu-id="65ea7-137">The globally unique identifier for the base application partition.</span></span> |
| <span data-ttu-id="65ea7-138">Access</span><span class="sxs-lookup"><span data-stu-id="65ea7-138">Access</span></span>         | <span data-ttu-id="65ea7-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="65ea7-139">ReadWrite</span></span>                                                          |
| <span data-ttu-id="65ea7-140">type</span><span class="sxs-lookup"><span data-stu-id="65ea7-140">Type</span></span>           | <span data-ttu-id="65ea7-141">String</span><span class="sxs-lookup"><span data-stu-id="65ea7-141">String</span></span>                                                             |
| <span data-ttu-id="65ea7-142">Standard</span><span class="sxs-lookup"><span data-stu-id="65ea7-142">Default</span></span>        | <span data-ttu-id="65ea7-143">{41e90f 3E-56c1-4633-81c3-6e8bac8bdd70}</span><span class="sxs-lookup"><span data-stu-id="65ea7-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span></span>                             |
| <span data-ttu-id="65ea7-144">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="65ea7-144">Minimum system</span></span> | <span data-ttu-id="65ea7-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65ea7-145">Windows Server 2003</span></span>                                                |



 

## <a name="see-also"></a><span data-ttu-id="65ea7-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65ea7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ea7-147">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="65ea7-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
