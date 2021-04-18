---
description: Enthält eine Liste der in-Process-Server, die beim System registriert sind. Sie enthält ein-Objekt für jede Komponente, die als Prozess interner Server registriert ist.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Sammlung "inprocservers"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345428"
---
# <a name="inprocservers-collection"></a><span data-ttu-id="10397-104">Sammlung "inprocservers"</span><span class="sxs-lookup"><span data-stu-id="10397-104">InprocServers collection</span></span>

<span data-ttu-id="10397-105">Enthält eine Liste der in-Process-Server, die beim System registriert sind.</span><span class="sxs-lookup"><span data-stu-id="10397-105">Contains a list of the in-process servers registered with the system.</span></span> <span data-ttu-id="10397-106">Sie enthält ein-Objekt für jede Komponente, die als Prozess interner Server registriert ist.</span><span class="sxs-lookup"><span data-stu-id="10397-106">It contains an object for each component that is registered as an in-process server.</span></span>

<span data-ttu-id="10397-107">Diese Auflistung unterstützt die [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts, jedoch nicht die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -Methode.</span><span class="sxs-lookup"><span data-stu-id="10397-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="10397-108">Verwenden Sie Methoden für das [**comadmincatalog**](comadmincatalog.md) -Objekt, um Komponenten in einer Anwendung zu installieren oder zu importieren.</span><span class="sxs-lookup"><span data-stu-id="10397-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="10397-109">Member</span><span class="sxs-lookup"><span data-stu-id="10397-109">Members</span></span>

<span data-ttu-id="10397-110">Die **inprocservers** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="10397-110">The **InprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="10397-111">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="10397-111">Related Collections</span></span>

<span data-ttu-id="10397-112">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="10397-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="10397-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="10397-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="10397-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="10397-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="10397-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="10397-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="10397-116">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="10397-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="10397-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10397-117">Properties</span></span>

<span data-ttu-id="10397-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="10397-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="10397-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="10397-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="10397-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="10397-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="10397-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="10397-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="10397-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="10397-122">CLSID</span></span>



| <span data-ttu-id="10397-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="10397-123">Entry</span></span> | <span data-ttu-id="10397-124">Wert</span><span class="sxs-lookup"><span data-stu-id="10397-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10397-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10397-125">Description</span></span>    | <span data-ttu-id="10397-126">Eine GUID für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="10397-126">A GUID for the component.</span></span> <span data-ttu-id="10397-127">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10397-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="10397-128">Access</span><span class="sxs-lookup"><span data-stu-id="10397-128">Access</span></span>         | <span data-ttu-id="10397-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="10397-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="10397-130">type</span><span class="sxs-lookup"><span data-stu-id="10397-130">Type</span></span>           | <span data-ttu-id="10397-131">String</span><span class="sxs-lookup"><span data-stu-id="10397-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="10397-132">Standard</span><span class="sxs-lookup"><span data-stu-id="10397-132">Default</span></span>        | <span data-ttu-id="10397-133">–</span><span class="sxs-lookup"><span data-stu-id="10397-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="10397-134">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="10397-134">Minimum system</span></span> | <span data-ttu-id="10397-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="10397-135">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="inprocserver32"></a><span data-ttu-id="10397-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="10397-136">InprocServer32</span></span>



| <span data-ttu-id="10397-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="10397-137">Entry</span></span> | <span data-ttu-id="10397-138">Wert</span><span class="sxs-lookup"><span data-stu-id="10397-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="10397-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10397-139">Description</span></span>    | <span data-ttu-id="10397-140">Der Dateipfad für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="10397-140">The file path for the component.</span></span> |
| <span data-ttu-id="10397-141">Access</span><span class="sxs-lookup"><span data-stu-id="10397-141">Access</span></span>         | <span data-ttu-id="10397-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="10397-142">ReadOnly</span></span>                         |
| <span data-ttu-id="10397-143">type</span><span class="sxs-lookup"><span data-stu-id="10397-143">Type</span></span>           | <span data-ttu-id="10397-144">String</span><span class="sxs-lookup"><span data-stu-id="10397-144">String</span></span>                           |
| <span data-ttu-id="10397-145">Standard</span><span class="sxs-lookup"><span data-stu-id="10397-145">Default</span></span>        | <span data-ttu-id="10397-146">–</span><span class="sxs-lookup"><span data-stu-id="10397-146">N/A</span></span>                              |
| <span data-ttu-id="10397-147">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="10397-147">Minimum system</span></span> | <span data-ttu-id="10397-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="10397-148">Windows 2000</span></span>                     |



 

### <a name="progid"></a><span data-ttu-id="10397-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="10397-149">ProgID</span></span>



| <span data-ttu-id="10397-150">Eingabe</span><span class="sxs-lookup"><span data-stu-id="10397-150">Entry</span></span> | <span data-ttu-id="10397-151">Wert</span><span class="sxs-lookup"><span data-stu-id="10397-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10397-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10397-152">Description</span></span>    | <span data-ttu-id="10397-153">Ein Name, der die Komponente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="10397-153">A name identifying the component.</span></span> <span data-ttu-id="10397-154">Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10397-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="10397-155">Access</span><span class="sxs-lookup"><span data-stu-id="10397-155">Access</span></span>         | <span data-ttu-id="10397-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="10397-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="10397-157">type</span><span class="sxs-lookup"><span data-stu-id="10397-157">Type</span></span>           | <span data-ttu-id="10397-158">String</span><span class="sxs-lookup"><span data-stu-id="10397-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="10397-159">Standard</span><span class="sxs-lookup"><span data-stu-id="10397-159">Default</span></span>        | <span data-ttu-id="10397-160">–</span><span class="sxs-lookup"><span data-stu-id="10397-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="10397-161">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="10397-161">Minimum system</span></span> | <span data-ttu-id="10397-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="10397-162">Windows 2000</span></span>                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="10397-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10397-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10397-164">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="10397-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
