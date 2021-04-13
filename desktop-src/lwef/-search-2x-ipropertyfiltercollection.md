---
title: Ipropertyfiltercollection-Schnittstelle (wdssharedidl. h)
description: Macht Eigenschaften der zurückgegebenen Auflistung auf der Grundlage der übermittelten Abfrage verfügbar.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Ipropertyfiltercollection-Schnittstelle ältere Windows-Umgebungs Features
- Ipropertyfiltercollection-Schnittstelle ältere Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340857"
---
# <a name="ipropertyfiltercollection-interface"></a><span data-ttu-id="d5109-105">Ipropertyfiltercollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d5109-105">IPropertyFilterCollection interface</span></span>

> [!NOTE]
> <span data-ttu-id="d5109-106">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="d5109-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d5109-107">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d5109-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d5109-108">Macht Eigenschaften der zurückgegebenen Auflistung auf der Grundlage der übermittelten Abfrage verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5109-108">Exposes properties of the returned collection based on the query submitted.</span></span>

## <a name="members"></a><span data-ttu-id="d5109-109">Member</span><span class="sxs-lookup"><span data-stu-id="d5109-109">Members</span></span>

<span data-ttu-id="d5109-110">Die **ipropertyfiltercollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d5109-110">The **IPropertyFilterCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5109-111">**Ipropertyfiltercollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d5109-111">**IPropertyFilterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="d5109-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d5109-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5109-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d5109-113">Properties</span></span>

<span data-ttu-id="d5109-114">Die **ipropertyfiltercollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d5109-114">The **IPropertyFilterCollection** interface has these properties.</span></span>



| <span data-ttu-id="d5109-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d5109-115">Property</span></span>                                                                         | <span data-ttu-id="d5109-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="d5109-116">Access type</span></span>           | <span data-ttu-id="d5109-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5109-117">Description</span></span>                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="d5109-118">**AddItem**</span><span class="sxs-lookup"><span data-stu-id="d5109-118">**AddItem**</span></span>](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | <span data-ttu-id="d5109-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d5109-119">Read-only</span></span><br/>  | <span data-ttu-id="d5109-120">Fügt der Auflistung einen neuen Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5109-120">Adds a new filter to the collection.</span></span> <br/>             |
| [<span data-ttu-id="d5109-121">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="d5109-121">**clear**</span></span>](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | <span data-ttu-id="d5109-122">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="d5109-122">Write-only</span></span><br/> | <span data-ttu-id="d5109-123">Löscht die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d5109-123">Clears the collection.</span></span> <br/>                           |
| [<span data-ttu-id="d5109-124">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="d5109-124">**Count**</span></span>](-search-2x-ipropertyfiltercollection-count.md)<br/>           | <span data-ttu-id="d5109-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d5109-125">Read-only</span></span><br/>  | <span data-ttu-id="d5109-126">Anzahl der Filter in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d5109-126">Number of filters in the collection.</span></span> <br/>             |
| [<span data-ttu-id="d5109-127">**GetITem**</span><span class="sxs-lookup"><span data-stu-id="d5109-127">**GetITem**</span></span>](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | <span data-ttu-id="d5109-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5109-128">Read/write</span></span><br/> | <span data-ttu-id="d5109-129">Gibt einen bestimmten Filter in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="d5109-129">Returns a specific filter within the collection.</span></span> <br/> |
| [<span data-ttu-id="d5109-130">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="d5109-130">**RemoveItem**</span></span>](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | <span data-ttu-id="d5109-131">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="d5109-131">Write-only</span></span><br/> | <span data-ttu-id="d5109-132">Entfernt einen bestimmten Filter für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d5109-132">Removes a specific filter to the collection.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="d5109-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5109-133">Remarks</span></span>

<span data-ttu-id="d5109-134">Diese Eigenschaften werden verwendet, um die von der Abfrage zurückgegebene Auflistung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="d5109-134">These properties are used to filter collection returned by the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5109-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5109-135">Requirements</span></span>



| <span data-ttu-id="d5109-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5109-136">Requirement</span></span> | <span data-ttu-id="d5109-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d5109-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5109-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5109-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d5109-139">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5109-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d5109-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5109-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d5109-141">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5109-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d5109-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d5109-142">Redistributable</span></span><br/>          | <span data-ttu-id="d5109-143">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d5109-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="d5109-144">Header</span><span class="sxs-lookup"><span data-stu-id="d5109-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5109-145"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5109-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

