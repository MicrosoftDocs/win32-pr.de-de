---
title: Ivmtask Cancel-Methode (vpccominterfaces. h)
description: Bricht die Aufgabe ab.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Methode "Virtual PC Abbrechen"
- Cancel-Methode Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, Cancel-Methode
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341237"
---
# <a name="ivmtaskcancel-method"></a><span data-ttu-id="59027-106">Ivmtask:: Cancel-Methode</span><span class="sxs-lookup"><span data-stu-id="59027-106">IVMTask::Cancel method</span></span>

<span data-ttu-id="59027-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59027-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59027-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59027-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59027-109">Bricht die Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="59027-109">Cancels the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="59027-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="59027-110">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="59027-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="59027-111">Parameters</span></span>

<span data-ttu-id="59027-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="59027-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59027-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59027-113">Return value</span></span>

<span data-ttu-id="59027-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="59027-114">This method can return one of these values.</span></span>



| <span data-ttu-id="59027-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="59027-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="59027-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59027-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="59027-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59027-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="59027-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="59027-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="59027-119"><dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="59027-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="59027-120">Die Aufgabe kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="59027-120">The task cannot be canceled.</span></span><br/>      |
| <dl> <span data-ttu-id="59027-121"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="59027-121"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="59027-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="59027-122">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59027-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59027-123">Requirements</span></span>



| <span data-ttu-id="59027-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59027-124">Requirement</span></span> | <span data-ttu-id="59027-125">Wert</span><span class="sxs-lookup"><span data-stu-id="59027-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59027-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59027-126">Minimum supported client</span></span><br/> | <span data-ttu-id="59027-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59027-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59027-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59027-128">Minimum supported server</span></span><br/> | <span data-ttu-id="59027-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="59027-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="59027-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="59027-130">End of client support</span></span><br/>    | <span data-ttu-id="59027-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59027-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59027-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="59027-132">Product</span></span><br/>                  | <span data-ttu-id="59027-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59027-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="59027-134">Header</span><span class="sxs-lookup"><span data-stu-id="59027-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="59027-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59027-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="59027-136">IID</span><span class="sxs-lookup"><span data-stu-id="59027-136">IID</span></span><br/>                      | <span data-ttu-id="59027-137">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="59027-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="59027-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59027-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59027-139">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="59027-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

