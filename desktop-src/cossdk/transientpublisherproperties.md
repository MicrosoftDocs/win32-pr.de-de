---
description: Enthält ein-Objekt für jede vorübergehende Verleger Eigenschaft für die übergeordnete transientabonnements-Auflistung. Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.
ms.assetid: 63921caa-5c22-4203-b1a3-f143928f4742
title: Transientpublisherproperties-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientPublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 707cb974dce632c6eb5f65bc38f1fff8b779e54d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342606"
---
# <a name="transientpublisherproperties-collection"></a><span data-ttu-id="96a82-104">Transientpublisherproperties-Auflistung</span><span class="sxs-lookup"><span data-stu-id="96a82-104">TransientPublisherProperties collection</span></span>

<span data-ttu-id="96a82-105">Enthält ein-Objekt für jede vorübergehende Verleger Eigenschaft für die übergeordnete [**transientabonnements**](transientsubscriptions.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="96a82-105">Contains an object for each transient publisher property for the parent [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span> <span data-ttu-id="96a82-106">Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="96a82-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="96a82-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="96a82-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="96a82-108">Member</span><span class="sxs-lookup"><span data-stu-id="96a82-108">Members</span></span>

<span data-ttu-id="96a82-109">Die **transientpublisherproperties** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="96a82-109">The **TransientPublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="96a82-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="96a82-110">Related Collections</span></span>

<span data-ttu-id="96a82-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="96a82-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="96a82-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="96a82-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="96a82-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="96a82-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="96a82-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="96a82-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="96a82-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="96a82-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="96a82-116">**Transientabonnements**</span><span class="sxs-lookup"><span data-stu-id="96a82-116">**TransientSubscriptions**</span></span>](transientsubscriptions.md)

## <a name="properties"></a><span data-ttu-id="96a82-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96a82-117">Properties</span></span>

<span data-ttu-id="96a82-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="96a82-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="96a82-119">Name</span><span class="sxs-lookup"><span data-stu-id="96a82-119">Name</span></span>](#name)
-   [<span data-ttu-id="96a82-120">Wert</span><span class="sxs-lookup"><span data-stu-id="96a82-120">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="96a82-121">Name</span><span class="sxs-lookup"><span data-stu-id="96a82-121">Name</span></span>



| <span data-ttu-id="96a82-122">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96a82-122">Entry</span></span> | <span data-ttu-id="96a82-123">Wert</span><span class="sxs-lookup"><span data-stu-id="96a82-123">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a82-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96a82-124">Description</span></span>    | <span data-ttu-id="96a82-125">Den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="96a82-125">The name of the property.</span></span> <span data-ttu-id="96a82-126">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="96a82-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="96a82-127">Access</span><span class="sxs-lookup"><span data-stu-id="96a82-127">Access</span></span>         | <span data-ttu-id="96a82-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="96a82-128">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="96a82-129">type</span><span class="sxs-lookup"><span data-stu-id="96a82-129">Type</span></span>           | <span data-ttu-id="96a82-130">String</span><span class="sxs-lookup"><span data-stu-id="96a82-130">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="96a82-131">Standard</span><span class="sxs-lookup"><span data-stu-id="96a82-131">Default</span></span>        | <span data-ttu-id="96a82-132">"Neue Eigenschaft"</span><span class="sxs-lookup"><span data-stu-id="96a82-132">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="96a82-133">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="96a82-133">Minimum system</span></span> | <span data-ttu-id="96a82-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="96a82-134">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="96a82-135">Wert</span><span class="sxs-lookup"><span data-stu-id="96a82-135">Value</span></span>



| <span data-ttu-id="96a82-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96a82-136">Entry</span></span> | <span data-ttu-id="96a82-137">Wert</span><span class="sxs-lookup"><span data-stu-id="96a82-137">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="96a82-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96a82-138">Description</span></span>    | <span data-ttu-id="96a82-139">Ein-Wert für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="96a82-139">A value for the property.</span></span> |
| <span data-ttu-id="96a82-140">Access</span><span class="sxs-lookup"><span data-stu-id="96a82-140">Access</span></span>         | <span data-ttu-id="96a82-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="96a82-141">ReadWrite</span></span>                 |
| <span data-ttu-id="96a82-142">type</span><span class="sxs-lookup"><span data-stu-id="96a82-142">Type</span></span>           | <span data-ttu-id="96a82-143">Variant</span><span class="sxs-lookup"><span data-stu-id="96a82-143">Variant</span></span>                   |
| <span data-ttu-id="96a82-144">Standard</span><span class="sxs-lookup"><span data-stu-id="96a82-144">Default</span></span>        | <span data-ttu-id="96a82-145">–</span><span class="sxs-lookup"><span data-stu-id="96a82-145">N/A</span></span>                       |
| <span data-ttu-id="96a82-146">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="96a82-146">Minimum system</span></span> | <span data-ttu-id="96a82-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="96a82-147">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="96a82-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96a82-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a82-149">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="96a82-149">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
