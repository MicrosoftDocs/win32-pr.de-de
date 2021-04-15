---
title: Ivmhostinfo memorytotalstring-Eigenschaft (vpccominterfaces. h)
description: Ruft die Gesamtmenge an physischem Arbeitsspeicher auf dem Host Computer (in Megabyte) als Zeichenfolge ab.
ms.assetid: 732c62e5-2776-4551-909f-7ddab74e067d
keywords:
- Memorytotalstring-Eigenschaft virtueller PC
- Memorytotalstring-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, memorytotalstring (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryTotalString
- IVMHostInfo.get_MemoryTotalString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e6c16a4215aba141ff1803d340c63dc9faa868
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391986"
---
# <a name="ivmhostinfomemorytotalstring-property"></a><span data-ttu-id="bfae0-106">Ivmhostinfo:: memorytotalstring (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bfae0-106">IVMHostInfo::MemoryTotalString property</span></span>

<span data-ttu-id="bfae0-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bfae0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bfae0-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bfae0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bfae0-109">Ruft die Gesamtmenge an physischem Arbeitsspeicher auf dem Host Computer (in Megabyte) als Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="bfae0-109">Retrieves the total amount of physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="bfae0-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bfae0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfae0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfae0-111">Syntax</span></span>


```C++
HRESULT get_MemoryTotalString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="bfae0-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bfae0-112">Property value</span></span>

<span data-ttu-id="bfae0-113">Die Gesamtmenge des physischen Speichers in Megabyte.</span><span class="sxs-lookup"><span data-stu-id="bfae0-113">The total amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bfae0-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bfae0-114">Error codes</span></span>



| <span data-ttu-id="bfae0-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="bfae0-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bfae0-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bfae0-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bfae0-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bfae0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bfae0-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfae0-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="bfae0-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bfae0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bfae0-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bfae0-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="bfae0-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bfae0-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bfae0-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bfae0-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bfae0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfae0-123">Requirements</span></span>



| <span data-ttu-id="bfae0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfae0-124">Requirement</span></span> | <span data-ttu-id="bfae0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bfae0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfae0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfae0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bfae0-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfae0-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfae0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfae0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bfae0-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bfae0-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bfae0-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bfae0-130">End of client support</span></span><br/>    | <span data-ttu-id="bfae0-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bfae0-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bfae0-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="bfae0-132">Product</span></span><br/>                  | <span data-ttu-id="bfae0-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bfae0-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bfae0-134">Header</span><span class="sxs-lookup"><span data-stu-id="bfae0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfae0-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfae0-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bfae0-136">IID</span><span class="sxs-lookup"><span data-stu-id="bfae0-136">IID</span></span><br/>                      | <span data-ttu-id="bfae0-137">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="bfae0-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="bfae0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfae0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfae0-139">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="bfae0-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

