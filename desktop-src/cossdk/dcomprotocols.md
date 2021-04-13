---
description: Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen. Sie enthält ein Objekt für jedes Protokoll.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Dcomprotokolle-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483214"
---
# <a name="dcomprotocols-collection"></a><span data-ttu-id="cd178-104">Dcomprotokolle-Sammlung</span><span class="sxs-lookup"><span data-stu-id="cd178-104">DCOMProtocols collection</span></span>

<span data-ttu-id="cd178-105">Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd178-105">Contains a list of the protocols to be used by DCOM.</span></span> <span data-ttu-id="cd178-106">Sie enthält ein Objekt für jedes Protokoll.</span><span class="sxs-lookup"><span data-stu-id="cd178-106">It contains an object for each protocol.</span></span>

<span data-ttu-id="cd178-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="cd178-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="cd178-108">Member</span><span class="sxs-lookup"><span data-stu-id="cd178-108">Members</span></span>

<span data-ttu-id="cd178-109">Die **dcomprotokolle** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="cd178-109">The **DCOMProtocols** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="cd178-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="cd178-110">Related Collections</span></span>

<span data-ttu-id="cd178-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="cd178-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="cd178-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="cd178-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="cd178-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="cd178-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="cd178-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="cd178-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="cd178-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="cd178-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="cd178-116">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="cd178-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="cd178-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd178-117">Properties</span></span>

<span data-ttu-id="cd178-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cd178-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="cd178-119">Name</span><span class="sxs-lookup"><span data-stu-id="cd178-119">Name</span></span>](#name)
-   [<span data-ttu-id="cd178-120">Order</span><span class="sxs-lookup"><span data-stu-id="cd178-120">Order</span></span>](#order)
-   [<span data-ttu-id="cd178-121">Protocolcode</span><span class="sxs-lookup"><span data-stu-id="cd178-121">ProtocolCode</span></span>](#protocolcode)

### <a name="name"></a><span data-ttu-id="cd178-122">Name</span><span class="sxs-lookup"><span data-stu-id="cd178-122">Name</span></span>



| <span data-ttu-id="cd178-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd178-123">Entry</span></span> | <span data-ttu-id="cd178-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cd178-124">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd178-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd178-125">Description</span></span>    | <span data-ttu-id="cd178-126">Der Name des Protokolls.</span><span class="sxs-lookup"><span data-stu-id="cd178-126">The name of the protocol.</span></span> <span data-ttu-id="cd178-127">Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cd178-127">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="cd178-128">Access</span><span class="sxs-lookup"><span data-stu-id="cd178-128">Access</span></span>         | <span data-ttu-id="cd178-129">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cd178-129">ReadWrite</span></span>                                                                                                                                                   |
| <span data-ttu-id="cd178-130">type</span><span class="sxs-lookup"><span data-stu-id="cd178-130">Type</span></span>           | <span data-ttu-id="cd178-131">String</span><span class="sxs-lookup"><span data-stu-id="cd178-131">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="cd178-132">Standard</span><span class="sxs-lookup"><span data-stu-id="cd178-132">Default</span></span>        | <span data-ttu-id="cd178-133">"Neues Protokoll"</span><span class="sxs-lookup"><span data-stu-id="cd178-133">"New Protocol"</span></span>                                                                                                                                              |
| <span data-ttu-id="cd178-134">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="cd178-134">Minimum system</span></span> | <span data-ttu-id="cd178-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cd178-135">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="order"></a><span data-ttu-id="cd178-136">Auftrag</span><span class="sxs-lookup"><span data-stu-id="cd178-136">Order</span></span>



| <span data-ttu-id="cd178-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd178-137">Entry</span></span> | <span data-ttu-id="cd178-138">Wert</span><span class="sxs-lookup"><span data-stu-id="cd178-138">Value</span></span> |
|----------------|-----------------------------------------|
| <span data-ttu-id="cd178-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd178-139">Description</span></span>    | <span data-ttu-id="cd178-140">Die Reihenfolge, in der das Protokoll ausprobiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd178-140">The order in which to try the protocol.</span></span> |
| <span data-ttu-id="cd178-141">Access</span><span class="sxs-lookup"><span data-stu-id="cd178-141">Access</span></span>         | <span data-ttu-id="cd178-142">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cd178-142">ReadWrite</span></span>                               |
| <span data-ttu-id="cd178-143">type</span><span class="sxs-lookup"><span data-stu-id="cd178-143">Type</span></span>           | <span data-ttu-id="cd178-144">Long (0-65000)</span><span class="sxs-lookup"><span data-stu-id="cd178-144">Long (0-65000)</span></span>                          |
| <span data-ttu-id="cd178-145">Standard</span><span class="sxs-lookup"><span data-stu-id="cd178-145">Default</span></span>        | <span data-ttu-id="cd178-146">0</span><span class="sxs-lookup"><span data-stu-id="cd178-146">0</span></span>                                       |
| <span data-ttu-id="cd178-147">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="cd178-147">Minimum system</span></span> | <span data-ttu-id="cd178-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cd178-148">Windows 2000</span></span>                            |



 

### <a name="protocolcode"></a><span data-ttu-id="cd178-149">Protocolcode</span><span class="sxs-lookup"><span data-stu-id="cd178-149">ProtocolCode</span></span>



| <span data-ttu-id="cd178-150">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd178-150">Entry</span></span> | <span data-ttu-id="cd178-151">Wert</span><span class="sxs-lookup"><span data-stu-id="cd178-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd178-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd178-152">Description</span></span>    | <span data-ttu-id="cd178-153">Der Code, der die RPC-Protokoll Sequenz angibt.</span><span class="sxs-lookup"><span data-stu-id="cd178-153">The code specifying the RPC protocol sequence.</span></span> <span data-ttu-id="cd178-154">Die unterstützten Protokoll Codes umfassen Folgendes: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX.</span><span class="sxs-lookup"><span data-stu-id="cd178-154">The supported protocol codes include the following: ncacn\_ip\_tcp, ncacn\_http, ncacn\_spx.</span></span> <span data-ttu-id="cd178-155">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cd178-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="cd178-156">Access</span><span class="sxs-lookup"><span data-stu-id="cd178-156">Access</span></span>         | <span data-ttu-id="cd178-157">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cd178-157">WriteOnce</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cd178-158">type</span><span class="sxs-lookup"><span data-stu-id="cd178-158">Type</span></span>           | <span data-ttu-id="cd178-159">String</span><span class="sxs-lookup"><span data-stu-id="cd178-159">String</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cd178-160">Standard</span><span class="sxs-lookup"><span data-stu-id="cd178-160">Default</span></span>        | <span data-ttu-id="cd178-161">""</span><span class="sxs-lookup"><span data-stu-id="cd178-161">""</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cd178-162">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="cd178-162">Minimum system</span></span> | <span data-ttu-id="cd178-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cd178-163">Windows 2000</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="cd178-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd178-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd178-165">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="cd178-165">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
