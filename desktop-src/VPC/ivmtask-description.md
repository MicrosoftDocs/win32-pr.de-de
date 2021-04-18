---
title: Ivmtask Description-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Beschreibung der Aufgabe ab.
ms.assetid: f1d5c7a2-b29e-4a8d-9cbd-263c168ec658
keywords:
- Description-Eigenschaft virtueller PC
- Description-Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, Description-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.Description
- IVMTask.get_Description
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62123174a61aa9b1c58ec36be69774e10e75de59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344501"
---
# <a name="ivmtaskdescription-property"></a><span data-ttu-id="73c06-106">Ivmtask::D escription (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73c06-106">IVMTask::Description property</span></span>

<span data-ttu-id="73c06-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73c06-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73c06-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="73c06-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73c06-109">Ruft eine Beschreibung der Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="73c06-109">Retrieves a description of the task.</span></span>

<span data-ttu-id="73c06-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="73c06-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c06-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="73c06-111">Syntax</span></span>


```C++
HRESULT get_Description(
  [out, retval] BSTR *description
);
```



## <a name="property-value"></a><span data-ttu-id="73c06-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="73c06-112">Property value</span></span>

<span data-ttu-id="73c06-113">Die Beschreibung der Aufgabe, die von Virtual PC festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="73c06-113">The description of the task, as set by Virtual PC.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73c06-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="73c06-114">Error codes</span></span>



| <span data-ttu-id="73c06-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="73c06-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="73c06-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="73c06-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="73c06-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="73c06-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="73c06-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="73c06-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="73c06-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="73c06-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="73c06-120">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="73c06-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="73c06-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="73c06-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="73c06-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="73c06-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="73c06-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73c06-123">Requirements</span></span>



| <span data-ttu-id="73c06-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73c06-124">Requirement</span></span> | <span data-ttu-id="73c06-125">Wert</span><span class="sxs-lookup"><span data-stu-id="73c06-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c06-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73c06-126">Minimum supported client</span></span><br/> | <span data-ttu-id="73c06-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73c06-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73c06-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73c06-128">Minimum supported server</span></span><br/> | <span data-ttu-id="73c06-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="73c06-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73c06-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="73c06-130">End of client support</span></span><br/>    | <span data-ttu-id="73c06-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73c06-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73c06-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="73c06-132">Product</span></span><br/>                  | <span data-ttu-id="73c06-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73c06-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73c06-134">Header</span><span class="sxs-lookup"><span data-stu-id="73c06-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="73c06-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c06-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73c06-136">IID</span><span class="sxs-lookup"><span data-stu-id="73c06-136">IID</span></span><br/>                      | <span data-ttu-id="73c06-137">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="73c06-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="73c06-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73c06-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c06-139">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="73c06-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

