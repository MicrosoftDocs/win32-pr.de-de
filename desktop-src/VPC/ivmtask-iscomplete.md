---
title: Ivmtask IsComplete-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob die Aufgabe abgeschlossen wurde.
ms.assetid: 181fa220-4de2-4ab3-950b-fffc4fe4de64
keywords:
- IsComplete-Eigenschaft virtueller PC
- IsComplete-Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, IsComplete-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.IsComplete
- IVMTask.get_IsComplete
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbf046b4a16ef4e907f1fec0126d08815ca2955
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956592"
---
# <a name="ivmtaskiscomplete-property"></a><span data-ttu-id="69e70-106">Ivmtask:: IsComplete-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="69e70-106">IVMTask::IsComplete property</span></span>

<span data-ttu-id="69e70-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="69e70-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="69e70-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="69e70-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="69e70-109">Bestimmt, ob die Aufgabe abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="69e70-109">Determines whether the task has completed.</span></span>

<span data-ttu-id="69e70-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="69e70-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e70-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="69e70-111">Syntax</span></span>


```C++
HRESULT get_IsComplete(
  [out, retval] VARIANT_BOOL *isComplete
);
```



## <a name="property-value"></a><span data-ttu-id="69e70-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="69e70-112">Property value</span></span>

<span data-ttu-id="69e70-113">**True** , wenn die Aufgabe abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="69e70-113">**TRUE** if the task has completed and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69e70-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="69e70-114">Error codes</span></span>



| <span data-ttu-id="69e70-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="69e70-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="69e70-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="69e70-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="69e70-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="69e70-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="69e70-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="69e70-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="69e70-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="69e70-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="69e70-120">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="69e70-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="69e70-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="69e70-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="69e70-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="69e70-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="69e70-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69e70-123">Requirements</span></span>



| <span data-ttu-id="69e70-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69e70-124">Requirement</span></span> | <span data-ttu-id="69e70-125">Wert</span><span class="sxs-lookup"><span data-stu-id="69e70-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e70-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69e70-126">Minimum supported client</span></span><br/> | <span data-ttu-id="69e70-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69e70-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69e70-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69e70-128">Minimum supported server</span></span><br/> | <span data-ttu-id="69e70-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="69e70-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="69e70-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="69e70-130">End of client support</span></span><br/>    | <span data-ttu-id="69e70-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69e70-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="69e70-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="69e70-132">Product</span></span><br/>                  | <span data-ttu-id="69e70-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="69e70-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="69e70-134">Header</span><span class="sxs-lookup"><span data-stu-id="69e70-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e70-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="69e70-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="69e70-136">IID</span><span class="sxs-lookup"><span data-stu-id="69e70-136">IID</span></span><br/>                      | <span data-ttu-id="69e70-137">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="69e70-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="69e70-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69e70-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e70-139">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="69e70-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

