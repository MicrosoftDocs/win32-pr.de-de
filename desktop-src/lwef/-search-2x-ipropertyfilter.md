---
title: Ipropertyfilter-Schnittstelle (wdssharedidl. h)
description: Macht Eigenschaften verfügbar, die zum Filtern der Abfrage verwendet werden.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Ipropertyfilter Interface, ältere Windows-Umgebungs Features
- Ipropertyfilter Interface Legacy Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518311"
---
# <a name="ipropertyfilter-interface"></a><span data-ttu-id="475cc-105">Ipropertyfilter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="475cc-105">IPropertyFilter interface</span></span>

> [!NOTE]
> <span data-ttu-id="475cc-106">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="475cc-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="475cc-107">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="475cc-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="475cc-108">Macht Eigenschaften verfügbar, die zum Filtern der Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="475cc-108">Exposes properties used to filter the query.</span></span>

## <a name="members"></a><span data-ttu-id="475cc-109">Member</span><span class="sxs-lookup"><span data-stu-id="475cc-109">Members</span></span>

<span data-ttu-id="475cc-110">Die **ipropertyfilter** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="475cc-110">The **IPropertyFilter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="475cc-111">**Ipropertyfilter** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="475cc-111">**IPropertyFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="475cc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="475cc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="475cc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="475cc-113">Properties</span></span>

<span data-ttu-id="475cc-114">Die **ipropertyfilter** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="475cc-114">The **IPropertyFilter** interface has these properties.</span></span>



| <span data-ttu-id="475cc-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="475cc-115">Property</span></span>                                                                                      | <span data-ttu-id="475cc-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="475cc-116">Access type</span></span>           | <span data-ttu-id="475cc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="475cc-117">Description</span></span>                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="475cc-118">**Ipropertyfilter:: indexcolumn**</span><span class="sxs-lookup"><span data-stu-id="475cc-118">**IPropertyFilter::IndexColumn**</span></span>](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | <span data-ttu-id="475cc-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="475cc-119">Read/write</span></span><br/> | <span data-ttu-id="475cc-120">Der Name der indizierten Spalte der Eigenschaft, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="475cc-120">Indexed column name of the property to filter by.</span></span> <br/> |
| [<span data-ttu-id="475cc-121">**Ipropertyfilter:: logicoperator**</span><span class="sxs-lookup"><span data-stu-id="475cc-121">**IPropertyFilter::LogicOperator**</span></span>](-search-2x-ipropertyfilter-logicoperator.md)<br/> | <span data-ttu-id="475cc-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="475cc-122">Read/write</span></span><br/> | <span data-ttu-id="475cc-123">Der zum Anwenden des Filters zu verwendende Logik Operator.</span><span class="sxs-lookup"><span data-stu-id="475cc-123">Logic Operator to use when applying filter.</span></span> <br/>       |
| [<span data-ttu-id="475cc-124">**Ipropertyfilter:: nestingtiefe**</span><span class="sxs-lookup"><span data-stu-id="475cc-124">**IPropertyFilter::NestingDepth**</span></span>](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | <span data-ttu-id="475cc-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="475cc-125">Read/write</span></span><br/> | <span data-ttu-id="475cc-126">Filtert die Tiefe innerhalb eines geschachtelten Satzes von Klammern.</span><span class="sxs-lookup"><span data-stu-id="475cc-126">Filters depth within a nested set of parentheses.</span></span> <br/> |
| [<span data-ttu-id="475cc-127">**Ipropertyfilter:: Text**</span><span class="sxs-lookup"><span data-stu-id="475cc-127">**IPropertyFilter::Text**</span></span>](-search-2x-ipropertyfilter-text.md)<br/>                   | <span data-ttu-id="475cc-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="475cc-128">Read/write</span></span><br/> | <span data-ttu-id="475cc-129">Text des Filters.</span><span class="sxs-lookup"><span data-stu-id="475cc-129">Text of the filter.</span></span> <br/>                               |
| [<span data-ttu-id="475cc-130">**Ipropertyfilter:: UID**</span><span class="sxs-lookup"><span data-stu-id="475cc-130">**IPropertyFilter::UID**</span></span>](-search-2x-ipropertyfilter-uid.md)<br/>                     | <span data-ttu-id="475cc-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="475cc-131">Read/write</span></span><br/> | <span data-ttu-id="475cc-132">UID: die Eigenschaft, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="475cc-132">UID fo the property to filter by.</span></span> <br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="475cc-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="475cc-133">Remarks</span></span>

<span data-ttu-id="475cc-134">Diese Eigenschaften werden verwendet, um die Abfrage zu filtern.</span><span class="sxs-lookup"><span data-stu-id="475cc-134">These properties are used to filter the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="475cc-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="475cc-135">Requirements</span></span>



| <span data-ttu-id="475cc-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="475cc-136">Requirement</span></span> | <span data-ttu-id="475cc-137">Wert</span><span class="sxs-lookup"><span data-stu-id="475cc-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="475cc-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="475cc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="475cc-139">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="475cc-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="475cc-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="475cc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="475cc-141">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="475cc-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="475cc-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="475cc-142">Redistributable</span></span><br/>          | <span data-ttu-id="475cc-143">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="475cc-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="475cc-144">Header</span><span class="sxs-lookup"><span data-stu-id="475cc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="475cc-145"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="475cc-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

