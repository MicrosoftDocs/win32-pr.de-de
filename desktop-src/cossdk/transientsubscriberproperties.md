---
description: Enthält ein-Objekt für jede Abonnenten Eigenschaft für die übergeordnete transientabonnements-Auflistung. Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.
ms.assetid: b4f003b0-db9d-45f1-a57d-3e4d321289ca
title: Transientabonberproperties-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 17f89638efe232f2cdf06e1206f74a0df44601b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343997"
---
# <a name="transientsubscriberproperties-collection"></a><span data-ttu-id="d20e6-104">Transientabonberproperties-Auflistung</span><span class="sxs-lookup"><span data-stu-id="d20e6-104">TransientSubscriberProperties collection</span></span>

<span data-ttu-id="d20e6-105">Enthält ein-Objekt für jede Abonnenten Eigenschaft für die übergeordnete [**transientabonnements**](transientsubscriptions.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d20e6-105">Contains an object for each subscriber property for the parent [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span> <span data-ttu-id="d20e6-106">Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="d20e6-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="d20e6-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d20e6-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="d20e6-108">Member</span><span class="sxs-lookup"><span data-stu-id="d20e6-108">Members</span></span>

<span data-ttu-id="d20e6-109">Die **transientabonberproperties** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="d20e6-109">The **TransientSubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="d20e6-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="d20e6-110">Related Collections</span></span>

<span data-ttu-id="d20e6-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="d20e6-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="d20e6-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="d20e6-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="d20e6-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="d20e6-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="d20e6-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="d20e6-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="d20e6-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="d20e6-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="d20e6-116">**Transientabonnements**</span><span class="sxs-lookup"><span data-stu-id="d20e6-116">**TransientSubscriptions**</span></span>](transientsubscriptions.md)

## <a name="properties"></a><span data-ttu-id="d20e6-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d20e6-117">Properties</span></span>

<span data-ttu-id="d20e6-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d20e6-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="d20e6-119">Name</span><span class="sxs-lookup"><span data-stu-id="d20e6-119">Name</span></span>](#name)
-   [<span data-ttu-id="d20e6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d20e6-120">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="d20e6-121">Name</span><span class="sxs-lookup"><span data-stu-id="d20e6-121">Name</span></span>



| <span data-ttu-id="d20e6-122">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d20e6-122">Entry</span></span> | <span data-ttu-id="d20e6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d20e6-123">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d20e6-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d20e6-124">Description</span></span>    | <span data-ttu-id="d20e6-125">Den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d20e6-125">The name of the property.</span></span> <span data-ttu-id="d20e6-126">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d20e6-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d20e6-127">Access</span><span class="sxs-lookup"><span data-stu-id="d20e6-127">Access</span></span>         | <span data-ttu-id="d20e6-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d20e6-128">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d20e6-129">type</span><span class="sxs-lookup"><span data-stu-id="d20e6-129">Type</span></span>           | <span data-ttu-id="d20e6-130">String</span><span class="sxs-lookup"><span data-stu-id="d20e6-130">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d20e6-131">Standard</span><span class="sxs-lookup"><span data-stu-id="d20e6-131">Default</span></span>        | <span data-ttu-id="d20e6-132">"Neue Eigenschaft"</span><span class="sxs-lookup"><span data-stu-id="d20e6-132">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d20e6-133">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d20e6-133">Minimum system</span></span> | <span data-ttu-id="d20e6-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d20e6-134">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="d20e6-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d20e6-135">Value</span></span>



| <span data-ttu-id="d20e6-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d20e6-136">Entry</span></span> | <span data-ttu-id="d20e6-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d20e6-137">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="d20e6-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d20e6-138">Description</span></span>    | <span data-ttu-id="d20e6-139">Ein-Wert für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d20e6-139">A value for the property.</span></span> |
| <span data-ttu-id="d20e6-140">Access</span><span class="sxs-lookup"><span data-stu-id="d20e6-140">Access</span></span>         | <span data-ttu-id="d20e6-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d20e6-141">ReadWrite</span></span>                 |
| <span data-ttu-id="d20e6-142">type</span><span class="sxs-lookup"><span data-stu-id="d20e6-142">Type</span></span>           | <span data-ttu-id="d20e6-143">Variant</span><span class="sxs-lookup"><span data-stu-id="d20e6-143">Variant</span></span>                   |
| <span data-ttu-id="d20e6-144">Standard</span><span class="sxs-lookup"><span data-stu-id="d20e6-144">Default</span></span>        | <span data-ttu-id="d20e6-145">–</span><span class="sxs-lookup"><span data-stu-id="d20e6-145">N/A</span></span>                       |
| <span data-ttu-id="d20e6-146">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="d20e6-146">Minimum system</span></span> | <span data-ttu-id="d20e6-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d20e6-147">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="d20e6-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d20e6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d20e6-149">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="d20e6-149">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
