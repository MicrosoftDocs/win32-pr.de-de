---
title: Ivmhostinfo osmajorversion-Eigenschaft (vpccominterfaces. h)
description: Ruft die Hauptversion des Betriebssystems ab, das auf dem Host Computer ausgeführt wird.
ms.assetid: d0b62d2d-532f-45c7-8622-67176b9b4a8f
keywords:
- Osmajorversion-Eigenschaft virtueller PC
- Osmajorversion-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, osmajorversion-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMajorVersion
- IVMHostInfo.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf064744d90ede010a7e48e0e23e6a62a19eb4af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391490"
---
# <a name="ivmhostinfoosmajorversion-property"></a><span data-ttu-id="8e450-106">Ivmhostinfo:: osmajorversion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8e450-106">IVMHostInfo::OSMajorVersion property</span></span>

<span data-ttu-id="8e450-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e450-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e450-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e450-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e450-109">Ruft die Hauptversion des Betriebssystems ab, das auf dem Host Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e450-109">Retrieves the major version of the operating system running on the host machine.</span></span>

<span data-ttu-id="8e450-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8e450-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e450-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e450-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] long *osMajorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="8e450-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8e450-112">Property value</span></span>

<span data-ttu-id="8e450-113">Die Hauptversion.</span><span class="sxs-lookup"><span data-stu-id="8e450-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e450-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8e450-114">Error codes</span></span>



| <span data-ttu-id="8e450-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="8e450-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8e450-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8e450-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8e450-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e450-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8e450-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e450-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="8e450-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8e450-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8e450-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="8e450-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="8e450-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8e450-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8e450-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8e450-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8e450-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e450-123">Requirements</span></span>



| <span data-ttu-id="8e450-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e450-124">Requirement</span></span> | <span data-ttu-id="8e450-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8e450-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e450-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e450-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8e450-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e450-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e450-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e450-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8e450-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e450-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e450-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8e450-130">End of client support</span></span><br/>    | <span data-ttu-id="8e450-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e450-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e450-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="8e450-132">Product</span></span><br/>                  | <span data-ttu-id="8e450-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e450-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e450-134">Header</span><span class="sxs-lookup"><span data-stu-id="8e450-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e450-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e450-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e450-136">IID</span><span class="sxs-lookup"><span data-stu-id="8e450-136">IID</span></span><br/>                      | <span data-ttu-id="8e450-137">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="8e450-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="8e450-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e450-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e450-139">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="8e450-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

