---
title: Ivmvirtualpc maximumfloppydrivespervm-Eigenschaft (vpccominterfaces. h)
description: Hiermit wird die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer abgerufen.
ms.assetid: f0dc351b-73de-4b6b-a953-5d5b683c4e31
keywords:
- Maximumfloppydrivespervm-Eigenschaft virtueller PC
- Maximumfloppydrivespervm-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, maximumfloppydrivespervm (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumFloppyDrivesPerVM
- IVMVirtualPC.get_MaximumFloppyDrivesPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecc0d672affce5364e1658d5198681268109a1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105639"
---
# <a name="ivmvirtualpcmaximumfloppydrivespervm-property"></a><span data-ttu-id="b069d-106">Ivmvirtualpc:: maximumfloppydrivespervm-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b069d-106">IVMVirtualPC::MaximumFloppyDrivesPerVM property</span></span>

<span data-ttu-id="b069d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b069d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b069d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b069d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b069d-109">Hiermit wird die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b069d-109">Retrieves the maximum number of floppy drives per virtual machine.</span></span>

<span data-ttu-id="b069d-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b069d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b069d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b069d-111">Syntax</span></span>


```C++
HRESULT get_MaximumFloppyDrivesPerVM(
  [out, retval] long *maxDrives
);
```



## <a name="property-value"></a><span data-ttu-id="b069d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b069d-112">Property value</span></span>

<span data-ttu-id="b069d-113">Die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer.</span><span class="sxs-lookup"><span data-stu-id="b069d-113">The maximum number of floppy drives per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b069d-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b069d-114">Error codes</span></span>



| <span data-ttu-id="b069d-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="b069d-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="b069d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b069d-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b069d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b069d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="b069d-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b069d-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b069d-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b069d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="b069d-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b069d-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b069d-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b069d-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="b069d-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b069d-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="b069d-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="b069d-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="b069d-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="b069d-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b069d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b069d-125">Requirements</span></span>



| <span data-ttu-id="b069d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b069d-126">Requirement</span></span> | <span data-ttu-id="b069d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b069d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b069d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b069d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b069d-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b069d-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b069d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b069d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b069d-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b069d-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b069d-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b069d-132">End of client support</span></span><br/>    | <span data-ttu-id="b069d-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b069d-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b069d-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="b069d-134">Product</span></span><br/>                  | <span data-ttu-id="b069d-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b069d-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b069d-136">Header</span><span class="sxs-lookup"><span data-stu-id="b069d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b069d-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b069d-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b069d-138">IID</span><span class="sxs-lookup"><span data-stu-id="b069d-138">IID</span></span><br/>                      | <span data-ttu-id="b069d-139">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="b069d-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b069d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b069d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b069d-141">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="b069d-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

