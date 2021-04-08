---
title: Ivmtask-Ergebnis Eigenschaft (vpccominterfaces. h)
description: Ruft das Ergebnis der Aufgabe ab.
ms.assetid: 640279ef-94b8-4e8f-88f3-a97cec54c121
keywords:
- Ergebnis Eigenschaft Virtual PC
- Ergebnis Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, Ergebnis Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.Result
- IVMTask.get_Result
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4dc36d1529633a850bc10e5c89e8c07147aea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956845"
---
# <a name="ivmtaskresult-property"></a><span data-ttu-id="a31ed-106">Ivmtask:: result (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a31ed-106">IVMTask::Result property</span></span>

<span data-ttu-id="a31ed-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a31ed-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a31ed-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a31ed-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a31ed-109">Ruft das Ergebnis der Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="a31ed-109">Retrieves the result of the task.</span></span>

<span data-ttu-id="a31ed-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a31ed-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31ed-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a31ed-111">Syntax</span></span>


```C++
HRESULT get_Result(
  [out, retval] VMTaskResult *result
);
```



## <a name="property-value"></a><span data-ttu-id="a31ed-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a31ed-112">Property value</span></span>

<span data-ttu-id="a31ed-113">Das Ergebnis der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="a31ed-113">The result of the task.</span></span> <span data-ttu-id="a31ed-114">Eine Liste der Werte finden Sie unter [**vmtaskresult**](vmtaskresult.md).</span><span class="sxs-lookup"><span data-stu-id="a31ed-114">For a list of values, see [**VMTaskResult**](vmtaskresult.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="a31ed-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a31ed-115">Error codes</span></span>



| <span data-ttu-id="a31ed-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a31ed-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a31ed-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a31ed-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a31ed-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a31ed-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a31ed-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a31ed-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a31ed-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a31ed-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a31ed-121">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a31ed-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="a31ed-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a31ed-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a31ed-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a31ed-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a31ed-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a31ed-124">Requirements</span></span>



| <span data-ttu-id="a31ed-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a31ed-125">Requirement</span></span> | <span data-ttu-id="a31ed-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a31ed-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31ed-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a31ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a31ed-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a31ed-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a31ed-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a31ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a31ed-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a31ed-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a31ed-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a31ed-131">End of client support</span></span><br/>    | <span data-ttu-id="a31ed-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a31ed-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a31ed-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="a31ed-133">Product</span></span><br/>                  | <span data-ttu-id="a31ed-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a31ed-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a31ed-135">Header</span><span class="sxs-lookup"><span data-stu-id="a31ed-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a31ed-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a31ed-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a31ed-137">IID</span><span class="sxs-lookup"><span data-stu-id="a31ed-137">IID</span></span><br/>                      | <span data-ttu-id="a31ed-138">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="a31ed-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="a31ed-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a31ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31ed-140">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="a31ed-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

