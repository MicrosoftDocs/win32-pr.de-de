---
title: Ivmvirtualpc minimummemorypervm-Eigenschaft (vpccominterfaces. h)
description: Ruft die minimal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer (in Megabyte) ab.
ms.assetid: 3e7757cd-df45-4b30-9a38-6cfca0ee631a
keywords:
- Minimummemorypervm-Eigenschaft virtueller PC
- Minimummemorypervm-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, minimummemorypervm (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MinimumMemoryPerVM
- IVMVirtualPC.get_MinimumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e083bd788c7bc51a45b7dd556107da13196ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102787"
---
# <a name="ivmvirtualpcminimummemorypervm-property"></a><span data-ttu-id="27176-106">Ivmvirtualpc:: minimummemorypervm (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="27176-106">IVMVirtualPC::MinimumMemoryPerVM property</span></span>

<span data-ttu-id="27176-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27176-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27176-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27176-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27176-109">Ruft die minimal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer (in Megabyte) ab.</span><span class="sxs-lookup"><span data-stu-id="27176-109">Retrieves the minimum allowable quantity of physical memory per virtual machine, in megabytes.</span></span>

<span data-ttu-id="27176-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="27176-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="27176-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="27176-111">Syntax</span></span>


```C++
HRESULT get_MinimumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="27176-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="27176-112">Property value</span></span>

<span data-ttu-id="27176-113">Die minimale zulässige Menge (in Megabyte) des physischen Speichers pro virtuellem Computer.</span><span class="sxs-lookup"><span data-stu-id="27176-113">The minimum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27176-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="27176-114">Error codes</span></span>



| <span data-ttu-id="27176-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="27176-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="27176-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="27176-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27176-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27176-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="27176-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="27176-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="27176-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27176-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="27176-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="27176-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="27176-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="27176-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="27176-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="27176-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="27176-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="27176-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="27176-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="27176-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="27176-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27176-125">Requirements</span></span>



| <span data-ttu-id="27176-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27176-126">Requirement</span></span> | <span data-ttu-id="27176-127">Wert</span><span class="sxs-lookup"><span data-stu-id="27176-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27176-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27176-128">Minimum supported client</span></span><br/> | <span data-ttu-id="27176-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27176-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27176-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27176-130">Minimum supported server</span></span><br/> | <span data-ttu-id="27176-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="27176-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27176-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="27176-132">End of client support</span></span><br/>    | <span data-ttu-id="27176-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27176-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27176-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="27176-134">Product</span></span><br/>                  | <span data-ttu-id="27176-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27176-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27176-136">Header</span><span class="sxs-lookup"><span data-stu-id="27176-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="27176-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="27176-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27176-138">IID</span><span class="sxs-lookup"><span data-stu-id="27176-138">IID</span></span><br/>                      | <span data-ttu-id="27176-139">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="27176-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="27176-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27176-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27176-141">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="27176-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

