---
title: Ivmguestos CanShutdown-Eigenschaft (vpccominterfaces. h)
description: Gibt an, ob das Gast Betriebssystem ordnungsgemäß heruntergefahren werden kann.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- Virtuelle PC für CanShutdown-Eigenschaft
- CanShutdown-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, CanShutdown (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f76e652b7a172da6f5a438f72b09443a13dcce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341247"
---
# <a name="ivmguestoscanshutdown-property"></a><span data-ttu-id="c4742-106">Ivmguestos:: CanShutdown (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c4742-106">IVMGuestOS::CanShutdown property</span></span>

<span data-ttu-id="c4742-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4742-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c4742-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c4742-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c4742-109">Gibt an, ob das Gast Betriebssystem ordnungsgemäß heruntergefahren werden kann (erfordert Integrations Komponenten).</span><span class="sxs-lookup"><span data-stu-id="c4742-109">Indicates whether the guest operating system can be cleanly shut down (requires Integration Components).</span></span>

<span data-ttu-id="c4742-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c4742-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4742-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4742-111">Syntax</span></span>


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a><span data-ttu-id="c4742-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c4742-112">Property value</span></span>

<span data-ttu-id="c4742-113">**Variant \_ "True** ", wenn das Betriebssystem den Vorgang zum Herunterfahren unterstützt, andernfalls " **\_ false** "</span><span class="sxs-lookup"><span data-stu-id="c4742-113">**VARIANT\_TRUE** if the operating system supports the shutdown operation and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4742-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c4742-114">Error codes</span></span>



| <span data-ttu-id="c4742-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c4742-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c4742-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4742-116">Meaning</span></span>                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c4742-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c4742-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c4742-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4742-118">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="c4742-119"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c4742-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="c4742-120">Der virtuelle Computer ist nicht eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="c4742-120">The virtual machine is not turned on.</span></span><br/>   |
| <dl> <span data-ttu-id="c4742-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c4742-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c4742-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c4742-122">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="c4742-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c4742-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c4742-124">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c4742-124">The virtual machine could not be found.</span></span><br/> |
| <dl> <span data-ttu-id="c4742-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c4742-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c4742-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c4742-126">An unexpected error has occurred.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="c4742-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4742-127">Requirements</span></span>



| <span data-ttu-id="c4742-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4742-128">Requirement</span></span> | <span data-ttu-id="c4742-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c4742-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4742-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4742-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c4742-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4742-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4742-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4742-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c4742-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c4742-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c4742-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c4742-134">End of client support</span></span><br/>    | <span data-ttu-id="c4742-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c4742-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c4742-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="c4742-136">Product</span></span><br/>                  | <span data-ttu-id="c4742-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c4742-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c4742-138">Header</span><span class="sxs-lookup"><span data-stu-id="c4742-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4742-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4742-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c4742-140">IID</span><span class="sxs-lookup"><span data-stu-id="c4742-140">IID</span></span><br/>                      | <span data-ttu-id="c4742-141">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="c4742-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c4742-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4742-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4742-143">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="c4742-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

