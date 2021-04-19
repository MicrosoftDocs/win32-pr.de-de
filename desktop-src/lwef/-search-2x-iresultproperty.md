---
title: Iresultproperty-Schnittstelle (wdssharedidl. h)
description: Macht Ergebnis Eigenschaften verfügbar.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Iresultproperty-Schnittstelle ältere Windows-Umgebungs Features
- Iresultproperty-Schnittstelle ältere Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345313"
---
# <a name="iresultproperty-interface"></a><span data-ttu-id="d8062-105">Iresultproperty-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d8062-105">IResultProperty interface</span></span>

> [!NOTE]
> <span data-ttu-id="d8062-106">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="d8062-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d8062-107">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d8062-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d8062-108">Macht Ergebnis Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d8062-108">Exposes result properties.</span></span>

## <a name="members"></a><span data-ttu-id="d8062-109">Member</span><span class="sxs-lookup"><span data-stu-id="d8062-109">Members</span></span>

<span data-ttu-id="d8062-110">Die **iresultproperty** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d8062-110">The **IResultProperty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d8062-111">**Iresultproperty** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8062-111">**IResultProperty** also has these types of members:</span></span>

-   [<span data-ttu-id="d8062-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8062-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d8062-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8062-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d8062-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="d8062-114">Methods</span></span>

<span data-ttu-id="d8062-115">Die **iresultproperty** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d8062-115">The **IResultProperty** interface has these methods.</span></span>



| <span data-ttu-id="d8062-116">Methode</span><span class="sxs-lookup"><span data-stu-id="d8062-116">Method</span></span>                                                    | <span data-ttu-id="d8062-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8062-117">Description</span></span>                 |
|:----------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="d8062-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="d8062-118">**GoBack**</span></span>](-search-2x-iresultproperty-goback.md)       | <span data-ttu-id="d8062-119">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8062-119">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d8062-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="d8062-120">**GoForward**</span></span>](-search-2x-iresultproperty-goforward.md) | <span data-ttu-id="d8062-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8062-121">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d8062-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8062-122">Properties</span></span>

<span data-ttu-id="d8062-123">Die **iresultproperty** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8062-123">The **IResultProperty** interface has these properties.</span></span>



| <span data-ttu-id="d8062-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d8062-124">Property</span></span>                                                                   | <span data-ttu-id="d8062-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="d8062-125">Access type</span></span>          | <span data-ttu-id="d8062-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8062-126">Description</span></span>                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [<span data-ttu-id="d8062-127">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d8062-127">**DataType**</span></span>](-search-2x-iresultproperty-datatype.md)<br/>         | <span data-ttu-id="d8062-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8062-128">Read-only</span></span><br/> | <span data-ttu-id="d8062-129">Ein Properties-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="d8062-129">A properties data type.</span></span> <br/>                   |
| [<span data-ttu-id="d8062-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d8062-130">**DisplayName**</span></span>](-search-2x-iresultproperty-displayname.md)<br/>   | <span data-ttu-id="d8062-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8062-131">Read-only</span></span><br/> | <span data-ttu-id="d8062-132">Lokalisierter Anzeige Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d8062-132">Localized display name of the property.</span></span> <br/>   |
| [<span data-ttu-id="d8062-133">**DisplayState**</span><span class="sxs-lookup"><span data-stu-id="d8062-133">**DisplayState**</span></span>](-search-2x-iresultproperty-displaystate.md)<br/> | <span data-ttu-id="d8062-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8062-134">Read-only</span></span><br/> | <span data-ttu-id="d8062-135">Die Fähigkeit der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d8062-135">Visability of the property.</span></span> <br/>               |
| [<span data-ttu-id="d8062-136">**Deuteten**</span><span class="sxs-lookup"><span data-stu-id="d8062-136">**Hint**</span></span>](-search-2x-iresultproperty-hint.md)<br/>                 | <span data-ttu-id="d8062-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8062-137">Read-only</span></span><br/> | <span data-ttu-id="d8062-138">Spezieller Wert, der für das Abrufen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8062-138">Special value used to aid data retrieval.</span></span> <br/> |
| [<span data-ttu-id="d8062-139">**Indexcolumn**</span><span class="sxs-lookup"><span data-stu-id="d8062-139">**IndexColumn**</span></span>](-search-2x-iresultproperty-indexcolumn.md)<br/>   | <span data-ttu-id="d8062-140">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8062-140">Read-only</span></span><br/> | <span data-ttu-id="d8062-141">Eigenschaften Spaltenname im Index.</span><span class="sxs-lookup"><span data-stu-id="d8062-141">Properties column name in the index.</span></span> <br/>      |
| [<span data-ttu-id="d8062-142">**UID**</span><span class="sxs-lookup"><span data-stu-id="d8062-142">**UID**</span></span>](-search-2x-iresultproperty-uid.md)<br/>                   | <span data-ttu-id="d8062-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8062-143">Read-only</span></span><br/> | <span data-ttu-id="d8062-144">Eindeutiger Bezeichner für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d8062-144">Unique identifier for the property.</span></span> <br/>       |



 

## <a name="remarks"></a><span data-ttu-id="d8062-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8062-145">Remarks</span></span>

<span data-ttu-id="d8062-146">Dies sind die Rückgabe Eigenschaften von Elementen.</span><span class="sxs-lookup"><span data-stu-id="d8062-146">These are the items return properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8062-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8062-147">Requirements</span></span>



| <span data-ttu-id="d8062-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8062-148">Requirement</span></span> | <span data-ttu-id="d8062-149">Wert</span><span class="sxs-lookup"><span data-stu-id="d8062-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8062-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8062-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d8062-151">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8062-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d8062-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8062-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d8062-153">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8062-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8062-154">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d8062-154">Redistributable</span></span><br/>          | <span data-ttu-id="d8062-155">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d8062-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="d8062-156">Header</span><span class="sxs-lookup"><span data-stu-id="d8062-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8062-157"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8062-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

