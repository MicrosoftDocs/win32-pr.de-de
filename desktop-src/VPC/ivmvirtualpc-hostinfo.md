---
title: Ivmvirtualpc-Hostinfo-Eigenschaft (vpccominterfaces. h)
description: Ruft Informationen über den physischen Computer ab.
ms.assetid: 9efefea1-e608-48db-a91a-e3808b420fc2
keywords:
- Hostinfo-Eigenschaft virtueller PC
- Hostinfo-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, Hostinfo-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.HostInfo
- IVMVirtualPC.get_HostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351da69a19fd691b037a607a57136576e3b64011
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105195"
---
# <a name="ivmvirtualpchostinfo-property"></a><span data-ttu-id="a0ba8-106">Ivmvirtualpc:: Hostinfo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a0ba8-106">IVMVirtualPC::HostInfo property</span></span>

<span data-ttu-id="a0ba8-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a0ba8-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a0ba8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a0ba8-109">Ruft Informationen über den physischen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-109">Retrieves information about the physical computer.</span></span>

<span data-ttu-id="a0ba8-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ba8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0ba8-111">Syntax</span></span>


```C++
HRESULT get_HostInfo(
  [out, retval] IVMHostInfo **hostInfo
);
```



## <a name="property-value"></a><span data-ttu-id="a0ba8-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a0ba8-112">Property value</span></span>

<span data-ttu-id="a0ba8-113">Das [**ivmhostinfo**](ivmhostinfo.md) -Objekt, das Informationen über den Host Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-113">The [**IVMHostInfo**](ivmhostinfo.md) object containing information about the host machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a0ba8-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a0ba8-114">Error codes</span></span>



| <span data-ttu-id="a0ba8-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a0ba8-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a0ba8-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a0ba8-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0ba8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a0ba8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a0ba8-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a0ba8-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a0ba8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a0ba8-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a0ba8-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a0ba8-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a0ba8-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a0ba8-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a0ba8-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a0ba8-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="a0ba8-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a0ba8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0ba8-125">Requirements</span></span>



| <span data-ttu-id="a0ba8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0ba8-126">Requirement</span></span> | <span data-ttu-id="a0ba8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ba8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ba8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0ba8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ba8-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0ba8-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0ba8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0ba8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ba8-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a0ba8-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a0ba8-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a0ba8-132">End of client support</span></span><br/>    | <span data-ttu-id="a0ba8-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0ba8-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a0ba8-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="a0ba8-134">Product</span></span><br/>                  | <span data-ttu-id="a0ba8-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a0ba8-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a0ba8-136">Header</span><span class="sxs-lookup"><span data-stu-id="a0ba8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0ba8-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0ba8-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a0ba8-138">IID</span><span class="sxs-lookup"><span data-stu-id="a0ba8-138">IID</span></span><br/>                      | <span data-ttu-id="a0ba8-139">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="a0ba8-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a0ba8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0ba8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ba8-141">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="a0ba8-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

