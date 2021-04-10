---
description: Enthält ein-Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Usersinrole-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5bf36937d08efd377b48ef251ffb7219c05504f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214202"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="c6b3c-103">Usersinrole-Auflistung</span><span class="sxs-lookup"><span data-stu-id="c6b3c-103">UsersInRole collection</span></span>

<span data-ttu-id="c6b3c-104">Enthält ein-Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c6b3c-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="c6b3c-105">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c6b3c-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="c6b3c-106">Member</span><span class="sxs-lookup"><span data-stu-id="c6b3c-106">Members</span></span>

<span data-ttu-id="c6b3c-107">Die **usersinrole** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="c6b3c-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="c6b3c-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="c6b3c-108">Related Collections</span></span>

<span data-ttu-id="c6b3c-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="c6b3c-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="c6b3c-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c6b3c-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="c6b3c-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="c6b3c-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="c6b3c-112">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="c6b3c-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="c6b3c-113">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="c6b3c-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="c6b3c-114">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="c6b3c-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="c6b3c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6b3c-115">Properties</span></span>

<span data-ttu-id="c6b3c-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c6b3c-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="c6b3c-117">Benutzer</span><span class="sxs-lookup"><span data-stu-id="c6b3c-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="c6b3c-118">Benutzer</span><span class="sxs-lookup"><span data-stu-id="c6b3c-118">User</span></span>



| <span data-ttu-id="c6b3c-119">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c6b3c-119">Entry</span></span> | <span data-ttu-id="c6b3c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c6b3c-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b3c-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6b3c-121">Description</span></span>    | <span data-ttu-id="c6b3c-122">Der Benutzername.</span><span class="sxs-lookup"><span data-stu-id="c6b3c-122">The user name.</span></span> <span data-ttu-id="c6b3c-123">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c6b3c-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="c6b3c-124">Access</span><span class="sxs-lookup"><span data-stu-id="c6b3c-124">Access</span></span>         | <span data-ttu-id="c6b3c-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="c6b3c-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="c6b3c-126">type</span><span class="sxs-lookup"><span data-stu-id="c6b3c-126">Type</span></span>           | <span data-ttu-id="c6b3c-127">String</span><span class="sxs-lookup"><span data-stu-id="c6b3c-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="c6b3c-128">Standard</span><span class="sxs-lookup"><span data-stu-id="c6b3c-128">Default</span></span>        | <span data-ttu-id="c6b3c-129">"Neuer Benutzer"</span><span class="sxs-lookup"><span data-stu-id="c6b3c-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="c6b3c-130">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="c6b3c-130">Minimum system</span></span> | <span data-ttu-id="c6b3c-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c6b3c-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="c6b3c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6b3c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b3c-133">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="c6b3c-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
