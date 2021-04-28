---
description: 'UsersInRole-Auflistung: Enthält ein Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.'
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: UsersInRole-Sammlung
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
ms.openlocfilehash: 1b73c495a1af1dec9114e5a59274e457c1d09694
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105538"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="e56b6-103">UsersInRole-Sammlung</span><span class="sxs-lookup"><span data-stu-id="e56b6-103">UsersInRole collection</span></span>

<span data-ttu-id="e56b6-104">Enthält ein -Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e56b6-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="e56b6-105">Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)</span><span class="sxs-lookup"><span data-stu-id="e56b6-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="e56b6-106">Member</span><span class="sxs-lookup"><span data-stu-id="e56b6-106">Members</span></span>

<span data-ttu-id="e56b6-107">Die **UsersInRole-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="e56b6-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="e56b6-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="e56b6-108">Related Collections</span></span>

<span data-ttu-id="e56b6-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="e56b6-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="e56b6-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e56b6-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="e56b6-111">**Propertyinfo**</span><span class="sxs-lookup"><span data-stu-id="e56b6-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="e56b6-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e56b6-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="e56b6-113">Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="e56b6-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="e56b6-114">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="e56b6-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="e56b6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e56b6-115">Properties</span></span>

<span data-ttu-id="e56b6-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e56b6-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="e56b6-117">Benutzer</span><span class="sxs-lookup"><span data-stu-id="e56b6-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="e56b6-118">Benutzer</span><span class="sxs-lookup"><span data-stu-id="e56b6-118">User</span></span>



| <span data-ttu-id="e56b6-119">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e56b6-119">Entry</span></span> | <span data-ttu-id="e56b6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e56b6-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e56b6-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e56b6-121">Description</span></span>    | <span data-ttu-id="e56b6-122">Der Benutzername.</span><span class="sxs-lookup"><span data-stu-id="e56b6-122">The user name.</span></span> <span data-ttu-id="e56b6-123">Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e56b6-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e56b6-124">Access</span><span class="sxs-lookup"><span data-stu-id="e56b6-124">Access</span></span>         | <span data-ttu-id="e56b6-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e56b6-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="e56b6-126">type</span><span class="sxs-lookup"><span data-stu-id="e56b6-126">Type</span></span>           | <span data-ttu-id="e56b6-127">String</span><span class="sxs-lookup"><span data-stu-id="e56b6-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="e56b6-128">Standard</span><span class="sxs-lookup"><span data-stu-id="e56b6-128">Default</span></span>        | <span data-ttu-id="e56b6-129">"Neuer Benutzer"</span><span class="sxs-lookup"><span data-stu-id="e56b6-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="e56b6-130">Mindestsystem</span><span class="sxs-lookup"><span data-stu-id="e56b6-130">Minimum system</span></span> | <span data-ttu-id="e56b6-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e56b6-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="e56b6-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e56b6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56b6-133">COM+-Verwaltungssammlungen</span><span class="sxs-lookup"><span data-stu-id="e56b6-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
