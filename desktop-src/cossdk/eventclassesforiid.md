---
description: Ruft Informationen zu Ereignis Klassen ab.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Eventclassesforiid-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126589"
---
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="0c360-103">Eventclassesforiid-Sammlung</span><span class="sxs-lookup"><span data-stu-id="0c360-103">EventClassesForIID collection</span></span>

<span data-ttu-id="0c360-104">Ruft Informationen zu Ereignis Klassen ab.</span><span class="sxs-lookup"><span data-stu-id="0c360-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="0c360-105">Die Verbindung zwischen Verleger und Abonnent wird von einem [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) -Objekt verwaltet, bei dem es sich um eine COM+-Komponente handelt, die die Schnittstellen und Methoden enthält, die von einem Verleger zum Auslösen von Ereignissen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c360-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="0c360-106">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c360-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="0c360-107">Member</span><span class="sxs-lookup"><span data-stu-id="0c360-107">Members</span></span>

<span data-ttu-id="0c360-108">Die **eventclassesforiid** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="0c360-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="0c360-109">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="0c360-109">Related Collections</span></span>

<span data-ttu-id="0c360-110">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="0c360-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="0c360-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="0c360-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="0c360-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0c360-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="0c360-113">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="0c360-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="0c360-114">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="0c360-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="0c360-115">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="0c360-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="0c360-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c360-116">Properties</span></span>

<span data-ttu-id="0c360-117">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0c360-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="0c360-118">Anwendung</span><span class="sxs-lookup"><span data-stu-id="0c360-118">Application</span></span>](#application)
-   [<span data-ttu-id="0c360-119">Bitness</span><span class="sxs-lookup"><span data-stu-id="0c360-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="0c360-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="0c360-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="0c360-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c360-121">Description</span></span>](#description)
-   [<span data-ttu-id="0c360-122">Isprivatecomponent</span><span class="sxs-lookup"><span data-stu-id="0c360-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="0c360-123">ProgID</span><span class="sxs-lookup"><span data-stu-id="0c360-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="0c360-124">Application</span><span class="sxs-lookup"><span data-stu-id="0c360-124">Application</span></span>



| <span data-ttu-id="0c360-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c360-125">Entry</span></span> | <span data-ttu-id="0c360-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0c360-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="0c360-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c360-127">Description</span></span>    | <span data-ttu-id="0c360-128">Die GUID für die Anwendung, die die Ereignisklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="0c360-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="0c360-129">Access</span><span class="sxs-lookup"><span data-stu-id="0c360-129">Access</span></span>         | <span data-ttu-id="0c360-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c360-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="0c360-131">type</span><span class="sxs-lookup"><span data-stu-id="0c360-131">Type</span></span>           | <span data-ttu-id="0c360-132">String</span><span class="sxs-lookup"><span data-stu-id="0c360-132">String</span></span>                                                   |
| <span data-ttu-id="0c360-133">Standard</span><span class="sxs-lookup"><span data-stu-id="0c360-133">Default</span></span>        | <span data-ttu-id="0c360-134">–</span><span class="sxs-lookup"><span data-stu-id="0c360-134">N/A</span></span>                                                      |
| <span data-ttu-id="0c360-135">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="0c360-135">Minimum system</span></span> | <span data-ttu-id="0c360-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c360-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="0c360-137">Bitness</span><span class="sxs-lookup"><span data-stu-id="0c360-137">Bitness</span></span>



| <span data-ttu-id="0c360-138">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c360-138">Entry</span></span> | <span data-ttu-id="0c360-139">Wert</span><span class="sxs-lookup"><span data-stu-id="0c360-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c360-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c360-140">Description</span></span>    | <span data-ttu-id="0c360-141">Stellt den binären bikretivität der Ereignisklasse dar.</span><span class="sxs-lookup"><span data-stu-id="0c360-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="0c360-142">Auf Systemen, die 64-Bit-Windows verwenden, unterscheidet diese Eigenschaft zwischen 64-Bit-Komponenten und 32-Bit-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0c360-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="0c360-143">Access</span><span class="sxs-lookup"><span data-stu-id="0c360-143">Access</span></span>         | <span data-ttu-id="0c360-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c360-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="0c360-145">type</span><span class="sxs-lookup"><span data-stu-id="0c360-145">Type</span></span>           | <span data-ttu-id="0c360-146">Lange mögliche Werte: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="0c360-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="0c360-147">Standard</span><span class="sxs-lookup"><span data-stu-id="0c360-147">Default</span></span>        | <span data-ttu-id="0c360-148">–</span><span class="sxs-lookup"><span data-stu-id="0c360-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="0c360-149">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="0c360-149">Minimum system</span></span> | <span data-ttu-id="0c360-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c360-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="0c360-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="0c360-151">CLSID</span></span>



| <span data-ttu-id="0c360-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c360-152">Entry</span></span> | <span data-ttu-id="0c360-153">Wert</span><span class="sxs-lookup"><span data-stu-id="0c360-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c360-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c360-154">Description</span></span>    | <span data-ttu-id="0c360-155">Die GUID für die Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="0c360-155">The GUID for the event class.</span></span> <span data-ttu-id="0c360-156">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0c360-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0c360-157">Access</span><span class="sxs-lookup"><span data-stu-id="0c360-157">Access</span></span>         | <span data-ttu-id="0c360-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c360-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="0c360-159">type</span><span class="sxs-lookup"><span data-stu-id="0c360-159">Type</span></span>           | <span data-ttu-id="0c360-160">String</span><span class="sxs-lookup"><span data-stu-id="0c360-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="0c360-161">Standard</span><span class="sxs-lookup"><span data-stu-id="0c360-161">Default</span></span>        | <span data-ttu-id="0c360-162">–</span><span class="sxs-lookup"><span data-stu-id="0c360-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="0c360-163">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="0c360-163">Minimum system</span></span> | <span data-ttu-id="0c360-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c360-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="0c360-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c360-165">Description</span></span>



| <span data-ttu-id="0c360-166">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c360-166">Entry</span></span> | <span data-ttu-id="0c360-167">Wert</span><span class="sxs-lookup"><span data-stu-id="0c360-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="0c360-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c360-168">Description</span></span>    | <span data-ttu-id="0c360-169">Beschreibt die-Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="0c360-169">Describes the event class.</span></span> |
| <span data-ttu-id="0c360-170">Access</span><span class="sxs-lookup"><span data-stu-id="0c360-170">Access</span></span>         | <span data-ttu-id="0c360-171">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c360-171">ReadOnly</span></span>                   |
| <span data-ttu-id="0c360-172">type</span><span class="sxs-lookup"><span data-stu-id="0c360-172">Type</span></span>           | <span data-ttu-id="0c360-173">String</span><span class="sxs-lookup"><span data-stu-id="0c360-173">String</span></span>                     |
| <span data-ttu-id="0c360-174">Standard</span><span class="sxs-lookup"><span data-stu-id="0c360-174">Default</span></span>        | <span data-ttu-id="0c360-175">""</span><span class="sxs-lookup"><span data-stu-id="0c360-175">""</span></span>                         |
| <span data-ttu-id="0c360-176">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="0c360-176">Minimum system</span></span> | <span data-ttu-id="0c360-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c360-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="0c360-178">Isprivatecomponent</span><span class="sxs-lookup"><span data-stu-id="0c360-178">IsPrivateComponent</span></span>



| <span data-ttu-id="0c360-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c360-179">Entry</span></span> | <span data-ttu-id="0c360-180">Wert</span><span class="sxs-lookup"><span data-stu-id="0c360-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="0c360-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c360-181">Description</span></span>    | <span data-ttu-id="0c360-182">Gibt an, ob die Ereignis Klassen Komponente privat ist.</span><span class="sxs-lookup"><span data-stu-id="0c360-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="0c360-183">Access</span><span class="sxs-lookup"><span data-stu-id="0c360-183">Access</span></span>         | <span data-ttu-id="0c360-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c360-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="0c360-185">type</span><span class="sxs-lookup"><span data-stu-id="0c360-185">Type</span></span>           | <span data-ttu-id="0c360-186">Bool</span><span class="sxs-lookup"><span data-stu-id="0c360-186">Bool</span></span>                                                    |
| <span data-ttu-id="0c360-187">Standard</span><span class="sxs-lookup"><span data-stu-id="0c360-187">Default</span></span>        | <span data-ttu-id="0c360-188">Falsch</span><span class="sxs-lookup"><span data-stu-id="0c360-188">False</span></span>                                                   |
| <span data-ttu-id="0c360-189">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="0c360-189">Minimum system</span></span> | <span data-ttu-id="0c360-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c360-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="0c360-191">ProgID</span><span class="sxs-lookup"><span data-stu-id="0c360-191">ProgID</span></span>



| <span data-ttu-id="0c360-192">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c360-192">Entry</span></span> | <span data-ttu-id="0c360-193">Wert</span><span class="sxs-lookup"><span data-stu-id="0c360-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c360-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c360-194">Description</span></span>    | <span data-ttu-id="0c360-195">Ein Anzeige Name, der zum Identifizieren der Ereignisklasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c360-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="0c360-196">Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0c360-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0c360-197">Access</span><span class="sxs-lookup"><span data-stu-id="0c360-197">Access</span></span>         | <span data-ttu-id="0c360-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c360-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="0c360-199">type</span><span class="sxs-lookup"><span data-stu-id="0c360-199">Type</span></span>           | <span data-ttu-id="0c360-200">String</span><span class="sxs-lookup"><span data-stu-id="0c360-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="0c360-201">Standard</span><span class="sxs-lookup"><span data-stu-id="0c360-201">Default</span></span>        | <span data-ttu-id="0c360-202">""</span><span class="sxs-lookup"><span data-stu-id="0c360-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="0c360-203">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="0c360-203">Minimum system</span></span> | <span data-ttu-id="0c360-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c360-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="0c360-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c360-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c360-206">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="0c360-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
