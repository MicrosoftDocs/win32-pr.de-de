---
title: Ivmvirtualmachine-Maus Eigenschaft (vpccominterfaces. h)
description: Ruft das Mausgerät für den virtuellen Computer ab.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Mouseproperty Virtual PC
- Mouseproperty Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, Maus Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342665"
---
# <a name="ivmvirtualmachinemouse-property"></a><span data-ttu-id="18ba1-106">Ivmvirtualmachine:: Mouse-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="18ba1-106">IVMVirtualMachine::Mouse property</span></span>

<span data-ttu-id="18ba1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="18ba1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="18ba1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="18ba1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="18ba1-109">Ruft das Mausgerät für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="18ba1-109">Retrieves the mouse device for the virtual machine.</span></span>

<span data-ttu-id="18ba1-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="18ba1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ba1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="18ba1-111">Syntax</span></span>


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a><span data-ttu-id="18ba1-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="18ba1-112">Property value</span></span>

<span data-ttu-id="18ba1-113">Ein [**ivmmouse**](ivmmouse.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="18ba1-113">An [**IVMMouse**](ivmmouse.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18ba1-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="18ba1-114">Error codes</span></span>



| <span data-ttu-id="18ba1-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="18ba1-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="18ba1-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="18ba1-116">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="18ba1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="18ba1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="18ba1-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="18ba1-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="18ba1-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="18ba1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="18ba1-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="18ba1-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="18ba1-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="18ba1-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="18ba1-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="18ba1-122">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="18ba1-123"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="18ba1-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="18ba1-124">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18ba1-124">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="18ba1-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="18ba1-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="18ba1-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="18ba1-126">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="18ba1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18ba1-127">Requirements</span></span>



| <span data-ttu-id="18ba1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18ba1-128">Requirement</span></span> | <span data-ttu-id="18ba1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="18ba1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ba1-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18ba1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="18ba1-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18ba1-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18ba1-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18ba1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="18ba1-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="18ba1-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="18ba1-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="18ba1-134">End of client support</span></span><br/>    | <span data-ttu-id="18ba1-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="18ba1-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="18ba1-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="18ba1-136">Product</span></span><br/>                  | <span data-ttu-id="18ba1-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="18ba1-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="18ba1-138">Header</span><span class="sxs-lookup"><span data-stu-id="18ba1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ba1-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ba1-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="18ba1-140">IID</span><span class="sxs-lookup"><span data-stu-id="18ba1-140">IID</span></span><br/>                      | <span data-ttu-id="18ba1-141">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="18ba1-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="18ba1-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ba1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ba1-143">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="18ba1-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

