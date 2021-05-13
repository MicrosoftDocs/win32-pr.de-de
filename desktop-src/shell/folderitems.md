---
description: Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.
title: FolderItems-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840651"
---
# <a name="folderitems-object"></a><span data-ttu-id="42897-104">FolderItems-Objekt</span><span class="sxs-lookup"><span data-stu-id="42897-104">FolderItems object</span></span>

<span data-ttu-id="42897-105">Stellt die Auflistung von Elementen in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="42897-105">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="42897-106">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.</span><span class="sxs-lookup"><span data-stu-id="42897-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="42897-107">Member</span><span class="sxs-lookup"><span data-stu-id="42897-107">Members</span></span>

<span data-ttu-id="42897-108">Das **FolderItems-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="42897-108">The **FolderItems** object has these types of members:</span></span>

-   [<span data-ttu-id="42897-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="42897-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="42897-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42897-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42897-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="42897-111">Methods</span></span>

<span data-ttu-id="42897-112">Das **FolderItems-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="42897-112">The **FolderItems** object has these methods.</span></span>



| <span data-ttu-id="42897-113">Methode</span><span class="sxs-lookup"><span data-stu-id="42897-113">Method</span></span>                                    | <span data-ttu-id="42897-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42897-114">Description</span></span>                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42897-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="42897-115">**\_NewEnum**</span></span>](folderitems--newenum.md) | <span data-ttu-id="42897-116">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="42897-116">Not implemented.</span></span><br/>                                                                              |
| [<span data-ttu-id="42897-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="42897-117">**Item**</span></span>](folderitems-item.md)          | <span data-ttu-id="42897-118">Ruft das [**FolderItem-Objekt**](folderitem.md) für ein angegebenes Element in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="42897-118">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="42897-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42897-119">Properties</span></span>

<span data-ttu-id="42897-120">Das **FolderItems-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42897-120">The **FolderItems** object has these properties.</span></span>



| <span data-ttu-id="42897-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="42897-121">Property</span></span>                                                  | <span data-ttu-id="42897-122">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="42897-122">Access type</span></span>          | <span data-ttu-id="42897-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42897-123">Description</span></span>                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42897-124">**Application**</span><span class="sxs-lookup"><span data-stu-id="42897-124">**Application**</span></span>](folderitems-application.md)<br/> | <span data-ttu-id="42897-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42897-125">Read-only</span></span><br/> | <span data-ttu-id="42897-126">Enthält das [**Application-Objekt**](folderitems-application.md) der Ordnerelementeauflistung.</span><span class="sxs-lookup"><span data-stu-id="42897-126">Contains the [**Application**](folderitems-application.md) object of the folder items collection.</span></span><br/> |
| [<span data-ttu-id="42897-127">**Count**</span><span class="sxs-lookup"><span data-stu-id="42897-127">**Count**</span></span>](folderitems-count.md)<br/>             | <span data-ttu-id="42897-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42897-128">Read-only</span></span><br/> | <span data-ttu-id="42897-129">Enthält die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="42897-129">Contains the number of items in the collection.</span></span><br/>                                                    |
| [<span data-ttu-id="42897-130">**Parent**</span><span class="sxs-lookup"><span data-stu-id="42897-130">**Parent**</span></span>](folderitems-parent.md)<br/>           | <span data-ttu-id="42897-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42897-131">Read-only</span></span><br/> | <span data-ttu-id="42897-132">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="42897-132">Not implemented.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="42897-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42897-133">Requirements</span></span>



| <span data-ttu-id="42897-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42897-134">Requirement</span></span> | <span data-ttu-id="42897-135">Wert</span><span class="sxs-lookup"><span data-stu-id="42897-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42897-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42897-136">Minimum supported client</span></span><br/> | <span data-ttu-id="42897-137">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42897-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42897-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42897-138">Minimum supported server</span></span><br/> | <span data-ttu-id="42897-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42897-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42897-140">Header</span><span class="sxs-lookup"><span data-stu-id="42897-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="42897-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="42897-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="42897-142">Idl</span><span class="sxs-lookup"><span data-stu-id="42897-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42897-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="42897-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="42897-144">DLL</span><span class="sxs-lookup"><span data-stu-id="42897-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42897-145"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="42897-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




