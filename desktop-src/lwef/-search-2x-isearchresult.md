---
title: Isearchresult-Schnittstelle (wdssharedidl. h)
description: Macht Informationen und Eigenschaften für das Resultset verfügbar.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- Isearchresult Interface, ältere Windows-Umgebungs Features
- Isearchresult Interface, ältere Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742312"
---
# <a name="isearchresult-interface"></a><span data-ttu-id="5a0af-105">Isearchresult-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5a0af-105">ISearchResult interface</span></span>

> [!NOTE]
> <span data-ttu-id="5a0af-106">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="5a0af-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5a0af-107">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="5a0af-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="5a0af-108">Macht Informationen und Eigenschaften für das Resultset verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a0af-108">Exposes information and properties regarding the result set.</span></span>

## <a name="members"></a><span data-ttu-id="5a0af-109">Member</span><span class="sxs-lookup"><span data-stu-id="5a0af-109">Members</span></span>

<span data-ttu-id="5a0af-110">Die **isearchresult** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5a0af-110">The **ISearchResult** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5a0af-111">**Isearchresult** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5a0af-111">**ISearchResult** also has these types of members:</span></span>

-   [<span data-ttu-id="5a0af-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a0af-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a0af-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a0af-113">Methods</span></span>

<span data-ttu-id="5a0af-114">Die **isearchresult** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5a0af-114">The **ISearchResult** interface has these methods.</span></span>



| <span data-ttu-id="5a0af-115">Methode</span><span class="sxs-lookup"><span data-stu-id="5a0af-115">Method</span></span>                                                            | <span data-ttu-id="5a0af-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a0af-116">Description</span></span>                 |
|:------------------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="5a0af-117">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="5a0af-117">**Availability**</span></span>](-search-2x-isearchresult-availability.md)     | <span data-ttu-id="5a0af-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-118">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-119">**DoVerb**</span><span class="sxs-lookup"><span data-stu-id="5a0af-119">**DoVerb**</span></span>](-search-2x-isearchresult-doverb.md)                 | <span data-ttu-id="5a0af-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-120">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-121">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="5a0af-121">**GetIcon**</span></span>](-search-2x-isearchresult-geticon.md)               | <span data-ttu-id="5a0af-122">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-122">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-123">**GetThumbnail**</span><span class="sxs-lookup"><span data-stu-id="5a0af-123">**GetThumbnail**</span></span>](-search-2x-isearchresult-getthumbnail.md)     | <span data-ttu-id="5a0af-124">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-124">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-125">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="5a0af-125">**GetValue**</span></span>](-search-2x-isearchresult-getvalue.md)             | <span data-ttu-id="5a0af-126">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-126">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-127">**Getverb**</span><span class="sxs-lookup"><span data-stu-id="5a0af-127">**GetVerb**</span></span>](-search-2x-isearchresult-getverb.md)               | <span data-ttu-id="5a0af-128">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-128">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-129">**Iconcount**</span><span class="sxs-lookup"><span data-stu-id="5a0af-129">**IconCount**</span></span>](-search-2x-isearchresult-iconcount.md)           | <span data-ttu-id="5a0af-130">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-130">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-131">**Sin**</span><span class="sxs-lookup"><span data-stu-id="5a0af-131">**Index**</span></span>](-search-2x-isearchresult-index.md)                   | <span data-ttu-id="5a0af-132">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-132">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-133">**LoadState**</span><span class="sxs-lookup"><span data-stu-id="5a0af-133">**LoadState**</span></span>](-search-2x-isearchresult-loadstate.md)           | <span data-ttu-id="5a0af-134">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-134">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-135">**Vorschau**</span><span class="sxs-lookup"><span data-stu-id="5a0af-135">**Previewer**</span></span>](-search-2x-isearchresult-previewer.md)           | <span data-ttu-id="5a0af-136">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-136">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-137">**PutValue**</span><span class="sxs-lookup"><span data-stu-id="5a0af-137">**PutValue**</span></span>](-search-2x-isearchresult-putvalue.md)             | <span data-ttu-id="5a0af-138">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-138">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-139">**Thumbnailstate**</span><span class="sxs-lookup"><span data-stu-id="5a0af-139">**ThumbnailState**</span></span>](-search-2x-isearchresult-thumbnailstate.md) | <span data-ttu-id="5a0af-140">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-140">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-141">**type**</span><span class="sxs-lookup"><span data-stu-id="5a0af-141">**Type**</span></span>](-search-2x-isearchresult-type.md)                     | <span data-ttu-id="5a0af-142">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-142">Not implemented.</span></span><br/> |
| [<span data-ttu-id="5a0af-143">**Verbcount**</span><span class="sxs-lookup"><span data-stu-id="5a0af-143">**VerbCount**</span></span>](-search-2x-isearchresult-verbcount.md)           | <span data-ttu-id="5a0af-144">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0af-144">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a0af-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a0af-145">Remarks</span></span>

<span data-ttu-id="5a0af-146">Diese Methoden machen Eigenschaften und Aktionen verfügbar, die für das Resultset gelten.</span><span class="sxs-lookup"><span data-stu-id="5a0af-146">These methods expose properties and actions applicable to the result set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0af-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a0af-147">Requirements</span></span>



| <span data-ttu-id="5a0af-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a0af-148">Requirement</span></span> | <span data-ttu-id="5a0af-149">Wert</span><span class="sxs-lookup"><span data-stu-id="5a0af-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0af-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a0af-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5a0af-151">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a0af-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5a0af-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a0af-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5a0af-153">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a0af-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5a0af-154">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5a0af-154">Redistributable</span></span><br/>          | <span data-ttu-id="5a0af-155">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="5a0af-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="5a0af-156">Header</span><span class="sxs-lookup"><span data-stu-id="5a0af-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a0af-157"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a0af-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

