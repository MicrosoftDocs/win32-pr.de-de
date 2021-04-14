---
title: Iresulttype-Schnittstelle (wdssharedidl. h)
description: Macht Eigenschaftentyp Informationen verfügbar.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Features
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476128"
---
# <a name="iresulttype-interface"></a><span data-ttu-id="f8421-105">Iresulttype-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f8421-105">IResultType interface</span></span>

> [!NOTE]
> <span data-ttu-id="f8421-106">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="f8421-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f8421-107">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="f8421-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="f8421-108">Macht Eigenschaftentyp Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8421-108">Exposes property type information.</span></span>

## <a name="members"></a><span data-ttu-id="f8421-109">Member</span><span class="sxs-lookup"><span data-stu-id="f8421-109">Members</span></span>

<span data-ttu-id="f8421-110">Die **iresulttype** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f8421-110">The **IResultType** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f8421-111">**Iresulttype** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f8421-111">**IResultType** also has these types of members:</span></span>

-   [<span data-ttu-id="f8421-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8421-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8421-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8421-113">Properties</span></span>

<span data-ttu-id="f8421-114">Die **iresulttype** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f8421-114">The **IResultType** interface has these properties.</span></span>



| <span data-ttu-id="f8421-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f8421-115">Property</span></span>                                                                 | <span data-ttu-id="f8421-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f8421-116">Access type</span></span>           | <span data-ttu-id="f8421-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8421-117">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8421-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="f8421-118">**DisplayName**</span></span>](-search-2x-iresulttype-displayname.md)<br/>     | <span data-ttu-id="f8421-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8421-119">Read-only</span></span><br/>  | <span data-ttu-id="f8421-120">Lokalisierter Anzeige Name des Typs:</span><span class="sxs-lookup"><span data-stu-id="f8421-120">Localized display name of the type:</span></span><br/>                                        |
| [<span data-ttu-id="f8421-121">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="f8421-121">**GetProperty**</span></span>](-search-2x-iresulttype-getproperty.md)<br/>     | <span data-ttu-id="f8421-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f8421-122">Read/write</span></span><br/> | <span data-ttu-id="f8421-123">Diese Eigenschaft enthält angegebene Eigenschafts Informationen.</span><span class="sxs-lookup"><span data-stu-id="f8421-123">This property contains specified property information.</span></span> <br/>                    |
| [<span data-ttu-id="f8421-124">**Preceivedtype**</span><span class="sxs-lookup"><span data-stu-id="f8421-124">**PreceivedType**</span></span>](-search-2x-iresulttype-preceivedtype.md)<br/> | <span data-ttu-id="f8421-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8421-125">Read-only</span></span><br/>  | <span data-ttu-id="f8421-126">Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f8421-126">This property contains the string used to identify the type in the index.</span></span> <br/> |
| [<span data-ttu-id="f8421-127">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="f8421-127">**PropertyCount**</span></span>](-search-2x-iresulttype-propertycount.md)<br/> | <span data-ttu-id="f8421-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8421-128">Read-only</span></span><br/>  | <span data-ttu-id="f8421-129">Diese Eigenschaft enthält die Anzahl der Eigenschaften, die vom-Typ verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="f8421-129">This property contains the number of properties exposed by the type.</span></span> <br/>      |
| [<span data-ttu-id="f8421-130">**UID**</span><span class="sxs-lookup"><span data-stu-id="f8421-130">**UID**</span></span>](-search-2x-iresulttype-uid.md)<br/>                     | <span data-ttu-id="f8421-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8421-131">Read-only</span></span><br/>  | <span data-ttu-id="f8421-132">Diese Eigenschaft enthält den eindeutigen Bezeichner für den Typ.</span><span class="sxs-lookup"><span data-stu-id="f8421-132">This property contains the unique identifier for the type.</span></span> <br/>                |



 

## <a name="remarks"></a><span data-ttu-id="f8421-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8421-133">Remarks</span></span>

<span data-ttu-id="f8421-134">Diese Methoden machen die Typen der zurückgegebenen Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8421-134">These methods expose the types of information returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8421-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8421-135">Requirements</span></span>



| <span data-ttu-id="f8421-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8421-136">Requirement</span></span> | <span data-ttu-id="f8421-137">Wert</span><span class="sxs-lookup"><span data-stu-id="f8421-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8421-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8421-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f8421-139">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8421-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f8421-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8421-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f8421-141">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8421-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f8421-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f8421-142">Redistributable</span></span><br/>          | <span data-ttu-id="f8421-143">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="f8421-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="f8421-144">Header</span><span class="sxs-lookup"><span data-stu-id="f8421-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8421-145"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8421-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

