---
title: Ivmvirtualpc-Betriebszeit Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der Sekunden ab, die die Windows Virtual PC-Anwendung ausgeführt wurde.
ms.assetid: 3007a961-2e8c-4674-aab6-4424d0d73eca
keywords:
- Betriebszeit Eigenschaft (Virtual PC)
- Betriebszeit Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, Betriebszeit Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.UpTime
- IVMVirtualPC.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab07128380a097677e0ad8acca5208e5cef11da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743440"
---
# <a name="ivmvirtualpcuptime-property"></a><span data-ttu-id="9edc9-106">Ivmvirtualpc:: uptime (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9edc9-106">IVMVirtualPC::UpTime property</span></span>

<span data-ttu-id="9edc9-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9edc9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9edc9-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9edc9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9edc9-109">Ruft die Anzahl der Sekunden ab, die die Windows Virtual PC-Anwendung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9edc9-109">Retrieves the number of seconds the Windows Virtual PC application has been running.</span></span>

<span data-ttu-id="9edc9-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9edc9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9edc9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9edc9-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="9edc9-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9edc9-112">Property value</span></span>

<span data-ttu-id="9edc9-113">Die Anzahl der Sekunden, die die Windows Virtual PC-Anwendung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9edc9-113">The number of seconds that the Windows Virtual PC application has been running.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9edc9-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9edc9-114">Error codes</span></span>



| <span data-ttu-id="9edc9-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="9edc9-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="9edc9-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9edc9-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9edc9-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9edc9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="9edc9-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9edc9-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9edc9-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9edc9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="9edc9-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="9edc9-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="9edc9-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9edc9-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="9edc9-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9edc9-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="9edc9-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="9edc9-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="9edc9-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="9edc9-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9edc9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9edc9-125">Requirements</span></span>



| <span data-ttu-id="9edc9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9edc9-126">Requirement</span></span> | <span data-ttu-id="9edc9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9edc9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9edc9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9edc9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9edc9-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9edc9-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9edc9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9edc9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9edc9-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9edc9-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9edc9-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9edc9-132">End of client support</span></span><br/>    | <span data-ttu-id="9edc9-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9edc9-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9edc9-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="9edc9-134">Product</span></span><br/>                  | <span data-ttu-id="9edc9-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9edc9-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9edc9-136">Header</span><span class="sxs-lookup"><span data-stu-id="9edc9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9edc9-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9edc9-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9edc9-138">IID</span><span class="sxs-lookup"><span data-stu-id="9edc9-138">IID</span></span><br/>                      | <span data-ttu-id="9edc9-139">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="9edc9-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9edc9-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9edc9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9edc9-141">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="9edc9-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

