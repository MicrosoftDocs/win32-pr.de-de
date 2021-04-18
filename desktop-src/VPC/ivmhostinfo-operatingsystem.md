---
title: Ivmhostinfo-OperatingSystem-Eigenschaft (vpccominterfaces. h)
description: Ruft das Betriebssystem ab, das auf dem Computer ausgeführt wird.
ms.assetid: 1164bb7d-cdce-4649-86d6-22e3ea7bad98
keywords:
- OperatingSystem-Eigenschaft virtueller PC
- OperatingSystem-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, OperatingSystem-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.OperatingSystem
- IVMHostInfo.get_OperatingSystem
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55af1d0cfdc2abaa01fe78c08509c2448b4d8cc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341350"
---
# <a name="ivmhostinfooperatingsystem-property"></a><span data-ttu-id="99065-106">Ivmhostinfo:: OperatingSystem-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99065-106">IVMHostInfo::OperatingSystem property</span></span>

<span data-ttu-id="99065-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="99065-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="99065-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="99065-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="99065-109">Ruft das Betriebssystem ab, das auf dem Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99065-109">Retrieves the operating system running on the machine.</span></span>

<span data-ttu-id="99065-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="99065-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="99065-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="99065-111">Syntax</span></span>


```C++
HRESULT get_OperatingSystem(
  [out, retval] BSTR *operatingSystem
);
```



## <a name="property-value"></a><span data-ttu-id="99065-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="99065-112">Property value</span></span>

<span data-ttu-id="99065-113">Der Name des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="99065-113">The name of the operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99065-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="99065-114">Error codes</span></span>



| <span data-ttu-id="99065-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="99065-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="99065-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="99065-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="99065-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="99065-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="99065-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="99065-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="99065-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="99065-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="99065-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="99065-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="99065-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="99065-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="99065-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="99065-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="99065-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99065-123">Requirements</span></span>



| <span data-ttu-id="99065-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99065-124">Requirement</span></span> | <span data-ttu-id="99065-125">Wert</span><span class="sxs-lookup"><span data-stu-id="99065-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99065-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99065-126">Minimum supported client</span></span><br/> | <span data-ttu-id="99065-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99065-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99065-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99065-128">Minimum supported server</span></span><br/> | <span data-ttu-id="99065-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="99065-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="99065-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="99065-130">End of client support</span></span><br/>    | <span data-ttu-id="99065-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99065-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="99065-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="99065-132">Product</span></span><br/>                  | <span data-ttu-id="99065-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="99065-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="99065-134">Header</span><span class="sxs-lookup"><span data-stu-id="99065-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="99065-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="99065-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="99065-136">IID</span><span class="sxs-lookup"><span data-stu-id="99065-136">IID</span></span><br/>                      | <span data-ttu-id="99065-137">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="99065-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="99065-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99065-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99065-139">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="99065-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

