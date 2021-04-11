---
description: Enthält ein-Objekt für jede Herausgeber Eigenschaft für die übergeordnete Index Index Auflistung.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Publisherproperties-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: bdab3e8143ea3d35d07adb5caa73639fcb568cd1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127016"
---
# <a name="publisherproperties-collection"></a><span data-ttu-id="ea6eb-103">Publisherproperties-Sammlung</span><span class="sxs-lookup"><span data-stu-id="ea6eb-103">PublisherProperties collection</span></span>

<span data-ttu-id="ea6eb-104">Enthält ein-Objekt für jede Herausgeber Eigenschaft für die [**übergeordnete Index**](subscriptionsforcomponent.md) Index Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ea6eb-104">Contains an object for each publisher property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="ea6eb-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ea6eb-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ea6eb-106">Member</span><span class="sxs-lookup"><span data-stu-id="ea6eb-106">Members</span></span>

<span data-ttu-id="ea6eb-107">Die **publisherproperties** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="ea6eb-107">The **PublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ea6eb-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="ea6eb-108">Related Collections</span></span>

<span data-ttu-id="ea6eb-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="ea6eb-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ea6eb-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ea6eb-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ea6eb-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ea6eb-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ea6eb-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="ea6eb-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ea6eb-113">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="ea6eb-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ea6eb-114">**Abonnement forcomponent**</span><span class="sxs-lookup"><span data-stu-id="ea6eb-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="ea6eb-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea6eb-115">Properties</span></span>

<span data-ttu-id="ea6eb-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ea6eb-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ea6eb-117">Name</span><span class="sxs-lookup"><span data-stu-id="ea6eb-117">Name</span></span>](#name)
-   [<span data-ttu-id="ea6eb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ea6eb-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="ea6eb-119">Name</span><span class="sxs-lookup"><span data-stu-id="ea6eb-119">Name</span></span>



| <span data-ttu-id="ea6eb-120">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ea6eb-120">Entry</span></span> | <span data-ttu-id="ea6eb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ea6eb-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6eb-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea6eb-122">Description</span></span>    | <span data-ttu-id="ea6eb-123">Den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ea6eb-123">The name of the property.</span></span> <span data-ttu-id="ea6eb-124">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ea6eb-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ea6eb-125">Access</span><span class="sxs-lookup"><span data-stu-id="ea6eb-125">Access</span></span>         | <span data-ttu-id="ea6eb-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ea6eb-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ea6eb-127">type</span><span class="sxs-lookup"><span data-stu-id="ea6eb-127">Type</span></span>           | <span data-ttu-id="ea6eb-128">String</span><span class="sxs-lookup"><span data-stu-id="ea6eb-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ea6eb-129">Standard</span><span class="sxs-lookup"><span data-stu-id="ea6eb-129">Default</span></span>        | <span data-ttu-id="ea6eb-130">"Neue Eigenschaft"</span><span class="sxs-lookup"><span data-stu-id="ea6eb-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ea6eb-131">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="ea6eb-131">Minimum system</span></span> | <span data-ttu-id="ea6eb-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ea6eb-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="ea6eb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ea6eb-133">Value</span></span>



| <span data-ttu-id="ea6eb-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ea6eb-134">Entry</span></span> | <span data-ttu-id="ea6eb-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ea6eb-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="ea6eb-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea6eb-136">Description</span></span>    | <span data-ttu-id="ea6eb-137">Ein-Wert für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ea6eb-137">A value for the property.</span></span> |
| <span data-ttu-id="ea6eb-138">Access</span><span class="sxs-lookup"><span data-stu-id="ea6eb-138">Access</span></span>         | <span data-ttu-id="ea6eb-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea6eb-139">ReadWrite</span></span>                 |
| <span data-ttu-id="ea6eb-140">type</span><span class="sxs-lookup"><span data-stu-id="ea6eb-140">Type</span></span>           | <span data-ttu-id="ea6eb-141">Variant</span><span class="sxs-lookup"><span data-stu-id="ea6eb-141">Variant</span></span>                   |
| <span data-ttu-id="ea6eb-142">Standard</span><span class="sxs-lookup"><span data-stu-id="ea6eb-142">Default</span></span>        | <span data-ttu-id="ea6eb-143">–</span><span class="sxs-lookup"><span data-stu-id="ea6eb-143">N/A</span></span>                       |
| <span data-ttu-id="ea6eb-144">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="ea6eb-144">Minimum system</span></span> | <span data-ttu-id="ea6eb-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ea6eb-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="ea6eb-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea6eb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6eb-147">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="ea6eb-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
