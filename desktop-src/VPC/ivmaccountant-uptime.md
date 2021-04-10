---
title: Ivmaccountant-Betriebszeit Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der Sekunden ab, die der virtuelle Computer ausgeführt wurde.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- Betriebszeit Eigenschaft (Virtual PC)
- Betriebszeit Eigenschaft Virtual PC, ivmaccountant-Schnittstelle
- Ivmaccountant Interface Virtual PC, Betriebszeit Eigenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c496aa9c32d402dcc8e84bad5410ec7774d2a80a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103977"
---
# <a name="ivmaccountantuptime-property"></a><span data-ttu-id="f25e6-106">Ivmaccountant:: uptime (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f25e6-106">IVMAccountant::UpTime property</span></span>

<span data-ttu-id="f25e6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f25e6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f25e6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f25e6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f25e6-109">Ruft die Anzahl der Sekunden ab, die der virtuelle Computer ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f25e6-109">Retrieves the number of seconds that the virtual machine has been running.</span></span>

<span data-ttu-id="f25e6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f25e6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f25e6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f25e6-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="f25e6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f25e6-112">Property value</span></span>

<span data-ttu-id="f25e6-113">Die Anzahl der Sekunden</span><span class="sxs-lookup"><span data-stu-id="f25e6-113">The number of seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f25e6-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f25e6-114">Error codes</span></span>



| <span data-ttu-id="f25e6-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="f25e6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f25e6-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f25e6-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="f25e6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f25e6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f25e6-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f25e6-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="f25e6-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f25e6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f25e6-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f25e6-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="f25e6-121"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f25e6-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="f25e6-122">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f25e6-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="f25e6-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f25e6-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f25e6-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f25e6-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="f25e6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f25e6-125">Requirements</span></span>



| <span data-ttu-id="f25e6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f25e6-126">Requirement</span></span> | <span data-ttu-id="f25e6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f25e6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f25e6-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f25e6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f25e6-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f25e6-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f25e6-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f25e6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f25e6-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f25e6-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f25e6-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f25e6-132">End of client support</span></span><br/>    | <span data-ttu-id="f25e6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25e6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f25e6-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="f25e6-134">Product</span></span><br/>                  | <span data-ttu-id="f25e6-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f25e6-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f25e6-136">Header</span><span class="sxs-lookup"><span data-stu-id="f25e6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f25e6-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f25e6-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f25e6-138">IID</span><span class="sxs-lookup"><span data-stu-id="f25e6-138">IID</span></span><br/>                      | <span data-ttu-id="f25e6-139">IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.</span><span class="sxs-lookup"><span data-stu-id="f25e6-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="f25e6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f25e6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25e6-141">**Ivmaccountant**</span><span class="sxs-lookup"><span data-stu-id="f25e6-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

