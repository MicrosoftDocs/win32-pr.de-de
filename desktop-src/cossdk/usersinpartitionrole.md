---
description: 'UsersInPartitionRole-Auflistung: Enthält ein Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.'
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: UsersInPartitionRole-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a4c134ebead08ef576337528a8ef75d8b8be21a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105548"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="45114-103">UsersInPartitionRole-Auflistung</span><span class="sxs-lookup"><span data-stu-id="45114-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="45114-104">Enthält ein -Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="45114-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="45114-105">Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)</span><span class="sxs-lookup"><span data-stu-id="45114-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="45114-106">Member</span><span class="sxs-lookup"><span data-stu-id="45114-106">Members</span></span>

<span data-ttu-id="45114-107">Die **UsersInPartitionRole-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="45114-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="45114-108">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="45114-108">Related Collections</span></span>

<span data-ttu-id="45114-109">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="45114-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="45114-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="45114-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="45114-111">**Propertyinfo**</span><span class="sxs-lookup"><span data-stu-id="45114-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="45114-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="45114-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="45114-113">Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="45114-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="45114-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="45114-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="45114-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45114-115">Properties</span></span>

<span data-ttu-id="45114-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="45114-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="45114-117">Benutzer</span><span class="sxs-lookup"><span data-stu-id="45114-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="45114-118">Benutzer</span><span class="sxs-lookup"><span data-stu-id="45114-118">User</span></span>



| <span data-ttu-id="45114-119">Eingabe</span><span class="sxs-lookup"><span data-stu-id="45114-119">Entry</span></span> | <span data-ttu-id="45114-120">Wert</span><span class="sxs-lookup"><span data-stu-id="45114-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45114-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45114-121">Description</span></span>    | <span data-ttu-id="45114-122">Der Benutzername.</span><span class="sxs-lookup"><span data-stu-id="45114-122">The user name.</span></span> <span data-ttu-id="45114-123">Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="45114-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="45114-124">Access</span><span class="sxs-lookup"><span data-stu-id="45114-124">Access</span></span>         | <span data-ttu-id="45114-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="45114-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="45114-126">type</span><span class="sxs-lookup"><span data-stu-id="45114-126">Type</span></span>           | <span data-ttu-id="45114-127">String</span><span class="sxs-lookup"><span data-stu-id="45114-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="45114-128">Standard</span><span class="sxs-lookup"><span data-stu-id="45114-128">Default</span></span>        | <span data-ttu-id="45114-129">"Neuer Benutzer"</span><span class="sxs-lookup"><span data-stu-id="45114-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45114-130">Mindestsystem</span><span class="sxs-lookup"><span data-stu-id="45114-130">Minimum system</span></span> | <span data-ttu-id="45114-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45114-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="45114-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="45114-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45114-133">COM+-Verwaltungssammlungen</span><span class="sxs-lookup"><span data-stu-id="45114-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
