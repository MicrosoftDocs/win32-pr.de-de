---
title: Ivmhostinfo-Speicher Eigenschaft (vpccominterfaces. h)
description: Ruft die Gesamtmenge an physischem Arbeitsspeicher auf dem Host Computer (in Megabyte) ab.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Arbeitsspeicher Eigenschaft (Virtual PC)
- Arbeitsspeicher Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, Memory-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f634bfe3bf81dcb13c9f09d8f19a5a82aa6902
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343054"
---
# <a name="ivmhostinfomemory-property"></a><span data-ttu-id="21904-106">Ivmhostinfo:: memory (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="21904-106">IVMHostInfo::Memory property</span></span>

<span data-ttu-id="21904-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21904-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="21904-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="21904-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="21904-109">Ruft die Gesamtmenge an physischem Arbeitsspeicher auf dem Host Computer (in Megabyte) ab.</span><span class="sxs-lookup"><span data-stu-id="21904-109">Retrieves the total amount of physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="21904-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21904-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21904-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="21904-111">Syntax</span></span>


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="21904-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="21904-112">Property value</span></span>

<span data-ttu-id="21904-113">Die Gesamtmenge des physischen Speichers in Megabyte.</span><span class="sxs-lookup"><span data-stu-id="21904-113">The total amount of physical memory, in megabytes.</span></span> <span data-ttu-id="21904-114">Dieser Wert ist eine **Variante** vom Typ VT \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="21904-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="21904-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="21904-115">Error codes</span></span>



| <span data-ttu-id="21904-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="21904-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="21904-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21904-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="21904-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="21904-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="21904-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="21904-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="21904-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="21904-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="21904-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="21904-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="21904-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="21904-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="21904-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="21904-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="21904-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21904-124">Requirements</span></span>



| <span data-ttu-id="21904-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21904-125">Requirement</span></span> | <span data-ttu-id="21904-126">Wert</span><span class="sxs-lookup"><span data-stu-id="21904-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="21904-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21904-127">Minimum supported client</span></span><br/> | <span data-ttu-id="21904-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21904-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21904-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21904-129">Minimum supported server</span></span><br/> | <span data-ttu-id="21904-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="21904-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="21904-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="21904-131">End of client support</span></span><br/>    | <span data-ttu-id="21904-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21904-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="21904-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="21904-133">Product</span></span><br/>                  | <span data-ttu-id="21904-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="21904-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="21904-135">Header</span><span class="sxs-lookup"><span data-stu-id="21904-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="21904-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="21904-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="21904-137">IID</span><span class="sxs-lookup"><span data-stu-id="21904-137">IID</span></span><br/>                      | <span data-ttu-id="21904-138">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="21904-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="21904-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21904-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21904-140">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="21904-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

