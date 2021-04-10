---
description: Die rolesforpartition-Auflistung ist immer mit einem Objekt in der Partitions Sammlung verknüpft. Sie enthält ein-Objekt für jede Rolle, die der Partition zugewiesen ist, mit der Sie verknüpft ist.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Rolesforpartition-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126332"
---
# <a name="rolesforpartition-collection"></a><span data-ttu-id="fde92-104">Rolesforpartition-Sammlung</span><span class="sxs-lookup"><span data-stu-id="fde92-104">RolesForPartition collection</span></span>

<span data-ttu-id="fde92-105">Die **rolesforpartition** -Auflistung ist immer mit einem Objekt in der [**Partitions**](partitions.md) Sammlung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="fde92-105">The **RolesForPartition** collection is always related to an object in the [**Partitions**](partitions.md) collection.</span></span> <span data-ttu-id="fde92-106">Sie enthält ein-Objekt für jede Rolle, die der Partition zugewiesen ist, mit der Sie verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="fde92-106">It holds an object for each role assigned to the partition to which it is related.</span></span>

<span data-ttu-id="fde92-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="fde92-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fde92-108">Member</span><span class="sxs-lookup"><span data-stu-id="fde92-108">Members</span></span>

<span data-ttu-id="fde92-109">Die **rolesforpartition** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="fde92-109">The **RolesForPartition** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="fde92-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="fde92-110">Related Collections</span></span>

<span data-ttu-id="fde92-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="fde92-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="fde92-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fde92-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="fde92-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="fde92-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="fde92-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="fde92-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="fde92-115">**Usersinpartitionrole**</span><span class="sxs-lookup"><span data-stu-id="fde92-115">**UsersInPartitionRole**</span></span>](usersinpartitionrole.md)

<span data-ttu-id="fde92-116">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="fde92-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="fde92-117">**Partitionen**</span><span class="sxs-lookup"><span data-stu-id="fde92-117">**Partitions**</span></span>](partitions.md)

## <a name="properties"></a><span data-ttu-id="fde92-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fde92-118">Properties</span></span>

<span data-ttu-id="fde92-119">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fde92-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="fde92-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fde92-120">Description</span></span>](#description)
-   [<span data-ttu-id="fde92-121">Name</span><span class="sxs-lookup"><span data-stu-id="fde92-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="fde92-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fde92-122">Description</span></span>



| <span data-ttu-id="fde92-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fde92-123">Entry</span></span> | <span data-ttu-id="fde92-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fde92-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="fde92-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fde92-125">Description</span></span>    | <span data-ttu-id="fde92-126">Eine Beschreibung der Rolle.</span><span class="sxs-lookup"><span data-stu-id="fde92-126">A description of the role.</span></span> |
| <span data-ttu-id="fde92-127">Access</span><span class="sxs-lookup"><span data-stu-id="fde92-127">Access</span></span>         | <span data-ttu-id="fde92-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fde92-128">ReadOnly</span></span>                   |
| <span data-ttu-id="fde92-129">type</span><span class="sxs-lookup"><span data-stu-id="fde92-129">Type</span></span>           | <span data-ttu-id="fde92-130">String</span><span class="sxs-lookup"><span data-stu-id="fde92-130">String</span></span>                     |
| <span data-ttu-id="fde92-131">Standard</span><span class="sxs-lookup"><span data-stu-id="fde92-131">Default</span></span>        | <span data-ttu-id="fde92-132">""</span><span class="sxs-lookup"><span data-stu-id="fde92-132">""</span></span>                         |
| <span data-ttu-id="fde92-133">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="fde92-133">Minimum system</span></span> | <span data-ttu-id="fde92-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fde92-134">Windows Server 2003</span></span>        |



 

### <a name="name"></a><span data-ttu-id="fde92-135">Name</span><span class="sxs-lookup"><span data-stu-id="fde92-135">Name</span></span>



| <span data-ttu-id="fde92-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fde92-136">Entry</span></span> | <span data-ttu-id="fde92-137">Wert</span><span class="sxs-lookup"><span data-stu-id="fde92-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde92-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fde92-138">Description</span></span>    | <span data-ttu-id="fde92-139">Der Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="fde92-139">The role name.</span></span> <span data-ttu-id="fde92-140">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fde92-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fde92-141">Access</span><span class="sxs-lookup"><span data-stu-id="fde92-141">Access</span></span>         | <span data-ttu-id="fde92-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fde92-142">ReadOnly</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fde92-143">type</span><span class="sxs-lookup"><span data-stu-id="fde92-143">Type</span></span>           | <span data-ttu-id="fde92-144">String</span><span class="sxs-lookup"><span data-stu-id="fde92-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fde92-145">Standard</span><span class="sxs-lookup"><span data-stu-id="fde92-145">Default</span></span>        | <span data-ttu-id="fde92-146">""</span><span class="sxs-lookup"><span data-stu-id="fde92-146">""</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fde92-147">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="fde92-147">Minimum system</span></span> | <span data-ttu-id="fde92-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fde92-148">Windows Server 2003</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="fde92-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fde92-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde92-150">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="fde92-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
