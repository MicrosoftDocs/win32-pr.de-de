---
description: Die Rollen Sammlung bezieht sich immer auf ein Objekt in der Anwendungs Auflistung. Sie enthält ein-Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der Sie verknüpft ist.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Rollen Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214262"
---
# <a name="roles-collection"></a><span data-ttu-id="1e296-104">Rollen Sammlung</span><span class="sxs-lookup"><span data-stu-id="1e296-104">Roles collection</span></span>

<span data-ttu-id="1e296-105">Die **Rollen** Sammlung bezieht sich immer auf ein Objekt in der [**Anwendungs**](applications.md) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1e296-105">The **Roles** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="1e296-106">Sie enthält ein-Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der Sie verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="1e296-106">It holds an object for each role assigned to the application to which it is related.</span></span>

<span data-ttu-id="1e296-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e296-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="1e296-108">Member</span><span class="sxs-lookup"><span data-stu-id="1e296-108">Members</span></span>

<span data-ttu-id="1e296-109">Die **Rollen** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="1e296-109">The **Roles** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="1e296-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="1e296-110">Related Collections</span></span>

<span data-ttu-id="1e296-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="1e296-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="1e296-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1e296-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="1e296-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1e296-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="1e296-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="1e296-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="1e296-115">**Usersinrole**</span><span class="sxs-lookup"><span data-stu-id="1e296-115">**UsersInRole**</span></span>](usersinrole.md)

<span data-ttu-id="1e296-116">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="1e296-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="1e296-117">**Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="1e296-117">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="1e296-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e296-118">Properties</span></span>

<span data-ttu-id="1e296-119">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1e296-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="1e296-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e296-120">Description</span></span>](#description)
-   [<span data-ttu-id="1e296-121">Name</span><span class="sxs-lookup"><span data-stu-id="1e296-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="1e296-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e296-122">Description</span></span>



| <span data-ttu-id="1e296-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1e296-123">Entry</span></span> | <span data-ttu-id="1e296-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1e296-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="1e296-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e296-125">Description</span></span>    | <span data-ttu-id="1e296-126">Eine Beschreibung der Rolle.</span><span class="sxs-lookup"><span data-stu-id="1e296-126">A description of the role.</span></span> |
| <span data-ttu-id="1e296-127">Access</span><span class="sxs-lookup"><span data-stu-id="1e296-127">Access</span></span>         | <span data-ttu-id="1e296-128">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1e296-128">ReadWrite</span></span>                  |
| <span data-ttu-id="1e296-129">type</span><span class="sxs-lookup"><span data-stu-id="1e296-129">Type</span></span>           | <span data-ttu-id="1e296-130">String</span><span class="sxs-lookup"><span data-stu-id="1e296-130">String</span></span>                     |
| <span data-ttu-id="1e296-131">Standard</span><span class="sxs-lookup"><span data-stu-id="1e296-131">Default</span></span>        | <span data-ttu-id="1e296-132">""</span><span class="sxs-lookup"><span data-stu-id="1e296-132">""</span></span>                         |
| <span data-ttu-id="1e296-133">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="1e296-133">Minimum system</span></span> | <span data-ttu-id="1e296-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1e296-134">Windows 2000</span></span>               |



 

### <a name="name"></a><span data-ttu-id="1e296-135">Name</span><span class="sxs-lookup"><span data-stu-id="1e296-135">Name</span></span>



| <span data-ttu-id="1e296-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1e296-136">Entry</span></span> | <span data-ttu-id="1e296-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1e296-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e296-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e296-138">Description</span></span>    | <span data-ttu-id="1e296-139">Der Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="1e296-139">The role name.</span></span> <span data-ttu-id="1e296-140">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1e296-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1e296-141">Access</span><span class="sxs-lookup"><span data-stu-id="1e296-141">Access</span></span>         | <span data-ttu-id="1e296-142">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="1e296-142">WriteOnce</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1e296-143">type</span><span class="sxs-lookup"><span data-stu-id="1e296-143">Type</span></span>           | <span data-ttu-id="1e296-144">String</span><span class="sxs-lookup"><span data-stu-id="1e296-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1e296-145">Standard</span><span class="sxs-lookup"><span data-stu-id="1e296-145">Default</span></span>        | <span data-ttu-id="1e296-146">"Neue Rolle"</span><span class="sxs-lookup"><span data-stu-id="1e296-146">"New Role"</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1e296-147">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="1e296-147">Minimum system</span></span> | <span data-ttu-id="1e296-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1e296-148">Windows 2000</span></span>                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="1e296-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e296-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e296-150">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="1e296-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
