---
description: Enthält ein-Objekt für jede Rolle, die der-Schnittstelle zugewiesen ist, mit der die Auflistung verknüpft ist. Die Rollen müssen bereits auf Anwendungsebene zugewiesen sein.
ms.assetid: f5c1dc9a-13da-4504-a244-4ce8058240b8
title: Rolesforinterface-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60c52e3cb48adc0ed52ef10bd9e0a73e716fabfc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344946"
---
# <a name="rolesforinterface-collection"></a><span data-ttu-id="8c3e3-104">Rolesforinterface-Auflistung</span><span class="sxs-lookup"><span data-stu-id="8c3e3-104">RolesForInterface collection</span></span>

<span data-ttu-id="8c3e3-105">Enthält ein-Objekt für jede Rolle, die der-Schnittstelle zugewiesen ist, mit der die Auflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="8c3e3-105">Contains an object for each role assigned to the interface to which the collection is related.</span></span> <span data-ttu-id="8c3e3-106">Die Rollen müssen bereits auf Anwendungsebene zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="8c3e3-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="8c3e3-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8c3e3-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="8c3e3-108">Member</span><span class="sxs-lookup"><span data-stu-id="8c3e3-108">Members</span></span>

<span data-ttu-id="8c3e3-109">Die **rolesforinterface** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="8c3e3-109">The **RolesForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8c3e3-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="8c3e3-110">Related Collections</span></span>

<span data-ttu-id="8c3e3-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="8c3e3-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="8c3e3-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8c3e3-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="8c3e3-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8c3e3-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8c3e3-114">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="8c3e3-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="8c3e3-115">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="8c3e3-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="8c3e3-116">**Interfakesforcomponent**</span><span class="sxs-lookup"><span data-stu-id="8c3e3-116">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="8c3e3-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c3e3-117">Properties</span></span>

<span data-ttu-id="8c3e3-118">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8c3e3-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="8c3e3-119">Name</span><span class="sxs-lookup"><span data-stu-id="8c3e3-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="8c3e3-120">Name</span><span class="sxs-lookup"><span data-stu-id="8c3e3-120">Name</span></span>



| <span data-ttu-id="8c3e3-121">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8c3e3-121">Entry</span></span> | <span data-ttu-id="8c3e3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8c3e3-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3e3-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c3e3-123">Description</span></span>    | <span data-ttu-id="8c3e3-124">Der Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="8c3e3-124">The role name.</span></span> <span data-ttu-id="8c3e3-125">Muss bereits eine Rolle sein, die der Anwendung zugewiesen ist (in der Rollen Auflistung angezeigt).</span><span class="sxs-lookup"><span data-stu-id="8c3e3-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="8c3e3-126">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c3e3-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8c3e3-127">Access</span><span class="sxs-lookup"><span data-stu-id="8c3e3-127">Access</span></span>         | <span data-ttu-id="8c3e3-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="8c3e3-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8c3e3-129">type</span><span class="sxs-lookup"><span data-stu-id="8c3e3-129">Type</span></span>           | <span data-ttu-id="8c3e3-130">String</span><span class="sxs-lookup"><span data-stu-id="8c3e3-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8c3e3-131">Standard</span><span class="sxs-lookup"><span data-stu-id="8c3e3-131">Default</span></span>        | <span data-ttu-id="8c3e3-132">"Neue Rolle"</span><span class="sxs-lookup"><span data-stu-id="8c3e3-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8c3e3-133">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="8c3e3-133">Minimum system</span></span> | <span data-ttu-id="8c3e3-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8c3e3-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="8c3e3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c3e3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3e3-136">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="8c3e3-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
