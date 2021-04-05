---
title: Ivmtask-ID-Eigenschaft (vpccominterfaces. h)
description: Ruft einen eindeutigen Bezeichner für diese Aufgabe ab.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- ID-Eigenschaft virtueller PC
- ID-Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, ID-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859180"
---
# <a name="ivmtaskid-property"></a><span data-ttu-id="c0256-106">Ivmtask:: ID (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c0256-106">IVMTask::ID property</span></span>

<span data-ttu-id="c0256-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0256-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c0256-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c0256-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c0256-109">Ruft einen eindeutigen Bezeichner für diese Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="c0256-109">Retrieves a unique identifier for this task.</span></span>

<span data-ttu-id="c0256-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c0256-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0256-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0256-111">Syntax</span></span>


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a><span data-ttu-id="c0256-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c0256-112">Property value</span></span>

<span data-ttu-id="c0256-113">Der eindeutige Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c0256-113">The unique identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0256-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c0256-114">Error codes</span></span>



| <span data-ttu-id="c0256-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c0256-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c0256-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c0256-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c0256-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c0256-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c0256-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0256-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c0256-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c0256-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c0256-120">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c0256-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="c0256-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c0256-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c0256-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c0256-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c0256-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0256-123">Requirements</span></span>



| <span data-ttu-id="c0256-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0256-124">Requirement</span></span> | <span data-ttu-id="c0256-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c0256-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0256-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0256-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c0256-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0256-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0256-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0256-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c0256-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0256-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c0256-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c0256-130">End of client support</span></span><br/>    | <span data-ttu-id="c0256-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0256-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c0256-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="c0256-132">Product</span></span><br/>                  | <span data-ttu-id="c0256-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0256-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c0256-134">Header</span><span class="sxs-lookup"><span data-stu-id="c0256-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0256-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0256-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c0256-136">IID</span><span class="sxs-lookup"><span data-stu-id="c0256-136">IID</span></span><br/>                      | <span data-ttu-id="c0256-137">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="c0256-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="c0256-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0256-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0256-139">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="c0256-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

