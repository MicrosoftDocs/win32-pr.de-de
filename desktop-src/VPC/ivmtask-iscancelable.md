---
title: Ivmtask IsCancelable-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der Task abgebrochen werden kann.
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- IsCancelable-Eigenschaft, virtueller PC
- IsCancelable-Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, IsCancelable-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd06db3fc338277d7551233b0d609ceae03f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105668"
---
# <a name="ivmtaskiscancelable-property"></a><span data-ttu-id="aaccc-106">Ivmtask:: IsCancelable-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aaccc-106">IVMTask::IsCancelable property</span></span>

<span data-ttu-id="aaccc-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aaccc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aaccc-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aaccc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aaccc-109">Bestimmt, ob der Task abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="aaccc-109">Determines whether the task can be canceled.</span></span>

<span data-ttu-id="aaccc-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="aaccc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaccc-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaccc-111">Syntax</span></span>


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## <a name="property-value"></a><span data-ttu-id="aaccc-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="aaccc-112">Property value</span></span>

<span data-ttu-id="aaccc-113">**True** , wenn die Aufgabe vor dem Abschluss abgebrochen werden kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="aaccc-113">**TRUE** if the task can be canceled before completion and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aaccc-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="aaccc-114">Error codes</span></span>



| <span data-ttu-id="aaccc-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="aaccc-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="aaccc-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="aaccc-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="aaccc-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aaccc-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="aaccc-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="aaccc-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="aaccc-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="aaccc-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="aaccc-120">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="aaccc-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="aaccc-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="aaccc-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="aaccc-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="aaccc-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="aaccc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aaccc-123">Requirements</span></span>



| <span data-ttu-id="aaccc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aaccc-124">Requirement</span></span> | <span data-ttu-id="aaccc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="aaccc-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaccc-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aaccc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aaccc-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aaccc-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aaccc-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aaccc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aaccc-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aaccc-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aaccc-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="aaccc-130">End of client support</span></span><br/>    | <span data-ttu-id="aaccc-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aaccc-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aaccc-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="aaccc-132">Product</span></span><br/>                  | <span data-ttu-id="aaccc-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aaccc-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aaccc-134">Header</span><span class="sxs-lookup"><span data-stu-id="aaccc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaccc-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaccc-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aaccc-136">IID</span><span class="sxs-lookup"><span data-stu-id="aaccc-136">IID</span></span><br/>                      | <span data-ttu-id="aaccc-137">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="aaccc-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="aaccc-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aaccc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaccc-139">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="aaccc-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

