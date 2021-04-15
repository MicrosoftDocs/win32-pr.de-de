---
title: Ivmtaskcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Auflistung von Task-Objekten. Zum Abrufen eines ivmtaskcollection-Objekts verwenden Sie die ivmvirtualpc Tasks-Eigenschaft.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Ivmtaskcollection-Schnittstelle virtueller PC
- Virtueller Computer der ivmtaskcollection-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392104"
---
# <a name="ivmtaskcollection-interface"></a><span data-ttu-id="a2ba5-106">Ivmtaskcollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a2ba5-106">IVMTaskCollection interface</span></span>

<span data-ttu-id="a2ba5-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2ba5-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2ba5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2ba5-109">Definiert die Auflistung von Task-Objekten.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-109">Defines the collection of task objects.</span></span> <span data-ttu-id="a2ba5-110">Verwenden Sie zum Abrufen eines **ivmtaskcollection** -Objekts die [**ivmvirtualpc:: Tasks**](ivmvirtualpc-tasks.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-110">To obtain an **IVMTaskCollection** object, use the [**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="a2ba5-111">Member</span><span class="sxs-lookup"><span data-stu-id="a2ba5-111">Members</span></span>

<span data-ttu-id="a2ba5-112">Die **ivmtaskcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-112">The **IVMTaskCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a2ba5-113">**Ivmtaskcollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a2ba5-113">**IVMTaskCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="a2ba5-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2ba5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2ba5-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2ba5-115">Properties</span></span>

<span data-ttu-id="a2ba5-116">Die **ivmtaskcollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-116">The **IVMTaskCollection** interface has these properties.</span></span>



| <span data-ttu-id="a2ba5-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a2ba5-117">Property</span></span>                                                   | <span data-ttu-id="a2ba5-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a2ba5-118">Access type</span></span>          | <span data-ttu-id="a2ba5-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2ba5-119">Description</span></span>                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="a2ba5-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="a2ba5-120">**\_NewEnum**</span></span>](ivmtaskcollection--newenum.md)<br/> | <span data-ttu-id="a2ba5-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2ba5-121">Read-only</span></span><br/> | <span data-ttu-id="a2ba5-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-122">An enumerator for the collection.</span></span><br/>                        |
| [<span data-ttu-id="a2ba5-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="a2ba5-123">**Count**</span></span>](ivmtaskcollection-count.md)<br/>        | <span data-ttu-id="a2ba5-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2ba5-124">Read-only</span></span><br/> | <span data-ttu-id="a2ba5-125">Die Anzahl der Tasks in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-125">The number of tasks in this collection.</span></span><br/>                  |
| [<span data-ttu-id="a2ba5-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2ba5-126">**Item**</span></span>](ivmtaskcollection-item.md)<br/>          | <span data-ttu-id="a2ba5-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2ba5-127">Read-only</span></span><br/> | <span data-ttu-id="a2ba5-128">Das Task-Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-128">The task object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a2ba5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2ba5-129">Requirements</span></span>



| <span data-ttu-id="a2ba5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2ba5-130">Requirement</span></span> | <span data-ttu-id="a2ba5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a2ba5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ba5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2ba5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ba5-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2ba5-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2ba5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2ba5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ba5-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a2ba5-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2ba5-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a2ba5-136">End of client support</span></span><br/>    | <span data-ttu-id="a2ba5-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2ba5-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2ba5-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="a2ba5-138">Product</span></span><br/>                  | <span data-ttu-id="a2ba5-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2ba5-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2ba5-140">Header</span><span class="sxs-lookup"><span data-stu-id="a2ba5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ba5-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ba5-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2ba5-142">IID</span><span class="sxs-lookup"><span data-stu-id="a2ba5-142">IID</span></span><br/>                      | <span data-ttu-id="a2ba5-143">IID \_ ivmtaskcollection ist definiert als 5c4387c8-0e8b-4b97-8058-84679adf 4c40</span><span class="sxs-lookup"><span data-stu-id="a2ba5-143">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a2ba5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2ba5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ba5-145">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="a2ba5-145">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="a2ba5-146">**Ivmvirtualpc:: Tasks**</span><span class="sxs-lookup"><span data-stu-id="a2ba5-146">**IVMVirtualPC::Tasks**</span></span>](ivmvirtualpc-tasks.md)
</dt> </dl>

 

