---
title: Ivmtask ErrorDescription-Eigenschaft (vpccominterfaces. h)
description: Ruft die lokalisierte Fehlerbeschreibung ab, die für diese Aufgabe aufgezeichnet wurde.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- ErrorDescription-Eigenschaft virtueller PC
- ErrorDescription-Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, ErrorDescription (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5c95eac383d8e071832fdbf7843c01345278c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743097"
---
# <a name="ivmtaskerrordescription-property"></a><span data-ttu-id="19fa0-106">Ivmtask:: ErrorDescription-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="19fa0-106">IVMTask::ErrorDescription property</span></span>

<span data-ttu-id="19fa0-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19fa0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="19fa0-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="19fa0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="19fa0-109">Ruft die lokalisierte Fehlerbeschreibung ab, die für diese Aufgabe aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="19fa0-109">Retrieves the localized error description recorded for this task.</span></span>

<span data-ttu-id="19fa0-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19fa0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fa0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="19fa0-111">Syntax</span></span>


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a><span data-ttu-id="19fa0-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="19fa0-112">Property value</span></span>

<span data-ttu-id="19fa0-113">Die Fehlerbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="19fa0-113">The error description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="19fa0-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="19fa0-114">Error codes</span></span>



| <span data-ttu-id="19fa0-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="19fa0-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="19fa0-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="19fa0-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="19fa0-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="19fa0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="19fa0-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="19fa0-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="19fa0-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="19fa0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="19fa0-120">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="19fa0-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="19fa0-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="19fa0-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="19fa0-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="19fa0-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="19fa0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19fa0-123">Requirements</span></span>



| <span data-ttu-id="19fa0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19fa0-124">Requirement</span></span> | <span data-ttu-id="19fa0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="19fa0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19fa0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19fa0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="19fa0-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19fa0-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19fa0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19fa0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="19fa0-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="19fa0-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="19fa0-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="19fa0-130">End of client support</span></span><br/>    | <span data-ttu-id="19fa0-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19fa0-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="19fa0-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="19fa0-132">Product</span></span><br/>                  | <span data-ttu-id="19fa0-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="19fa0-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="19fa0-134">Header</span><span class="sxs-lookup"><span data-stu-id="19fa0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="19fa0-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="19fa0-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="19fa0-136">IID</span><span class="sxs-lookup"><span data-stu-id="19fa0-136">IID</span></span><br/>                      | <span data-ttu-id="19fa0-137">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="19fa0-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="19fa0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19fa0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19fa0-139">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="19fa0-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

