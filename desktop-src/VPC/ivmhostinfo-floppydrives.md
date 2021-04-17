---
title: Ivmhostinfo floppydrives-Eigenschaft (vpccominterfaces. h)
description: Ruft die den Host Disketten zugeordneten Laufwerk Buchstaben ab.
ms.assetid: 9a8ab4b5-6ee8-463f-809b-b88cd28d9373
keywords:
- Floppydrives-Eigenschaft virtueller PC
- Floppydrives-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, floppydrives (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.FloppyDrives
- IVMHostInfo.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c31e3ece942f31fc6245c9f23a2995eb7b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392011"
---
# <a name="ivmhostinfofloppydrives-property"></a><span data-ttu-id="33e49-106">Ivmhostinfo:: floppydrives (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="33e49-106">IVMHostInfo::FloppyDrives property</span></span>

<span data-ttu-id="33e49-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="33e49-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="33e49-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="33e49-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="33e49-109">Ruft die den Host Disketten zugeordneten Laufwerk Buchstaben ab.</span><span class="sxs-lookup"><span data-stu-id="33e49-109">Retrieves the drive letters associated with host floppy drives.</span></span>

<span data-ttu-id="33e49-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="33e49-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e49-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e49-111">Syntax</span></span>


```C++
HRESULT get_FloppyDrives(
  [out, retval] VARIANT *floppyDrives
);
```



## <a name="property-value"></a><span data-ttu-id="33e49-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="33e49-112">Property value</span></span>

<span data-ttu-id="33e49-113">Ein Array von Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="33e49-113">An array of drive letters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="33e49-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="33e49-114">Error codes</span></span>



| <span data-ttu-id="33e49-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="33e49-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="33e49-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="33e49-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="33e49-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="33e49-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="33e49-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="33e49-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="33e49-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="33e49-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="33e49-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="33e49-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="33e49-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="33e49-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="33e49-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="33e49-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="33e49-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33e49-123">Requirements</span></span>



| <span data-ttu-id="33e49-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33e49-124">Requirement</span></span> | <span data-ttu-id="33e49-125">Wert</span><span class="sxs-lookup"><span data-stu-id="33e49-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e49-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33e49-126">Minimum supported client</span></span><br/> | <span data-ttu-id="33e49-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33e49-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33e49-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33e49-128">Minimum supported server</span></span><br/> | <span data-ttu-id="33e49-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="33e49-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="33e49-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="33e49-130">End of client support</span></span><br/>    | <span data-ttu-id="33e49-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33e49-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="33e49-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="33e49-132">Product</span></span><br/>                  | <span data-ttu-id="33e49-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="33e49-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="33e49-134">Header</span><span class="sxs-lookup"><span data-stu-id="33e49-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e49-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e49-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="33e49-136">IID</span><span class="sxs-lookup"><span data-stu-id="33e49-136">IID</span></span><br/>                      | <span data-ttu-id="33e49-137">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="33e49-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="33e49-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33e49-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e49-139">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="33e49-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

