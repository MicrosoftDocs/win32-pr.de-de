---
title: Ivmguestos OSVersion-Eigenschaft (vpccominterfaces. h)
description: Die Version des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: ef189c14-dc87-4d77-9567-345f49483b13
keywords:
- OSVersion-Eigenschaft virtueller PC
- OSVersion-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, OSVersion (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.OSVersion
- IVMGuestOS.get_OSVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338ae98c1830bae208f14aa522f716ac47899731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858866"
---
# <a name="ivmguestososversion-property"></a><span data-ttu-id="3a031-106">Ivmguestos:: OSVersion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3a031-106">IVMGuestOS::OSVersion property</span></span>

<span data-ttu-id="3a031-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a031-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a031-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a031-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a031-109">Hiermit wird die Version des Gast Betriebssystems abgerufen, das auf dem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a031-109">Retrieves the version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="3a031-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3a031-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a031-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a031-111">Syntax</span></span>


```C++
HRESULT get_OSVersion(
  [out, retval] BSTR *OSVersion
);
```



## <a name="property-value"></a><span data-ttu-id="3a031-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3a031-112">Property value</span></span>

<span data-ttu-id="3a031-113">Die Version.</span><span class="sxs-lookup"><span data-stu-id="3a031-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a031-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3a031-114">Error codes</span></span>



| <span data-ttu-id="3a031-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="3a031-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="3a031-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3a031-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3a031-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a031-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="3a031-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a031-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="3a031-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3a031-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="3a031-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="3a031-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="3a031-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="3a031-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="3a031-122">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a031-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="3a031-123"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="3a031-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="3a031-124">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="3a031-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="3a031-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3a031-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="3a031-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3a031-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="3a031-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a031-127">Requirements</span></span>



| <span data-ttu-id="3a031-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a031-128">Requirement</span></span> | <span data-ttu-id="3a031-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3a031-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a031-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a031-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a031-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a031-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a031-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a031-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a031-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3a031-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3a031-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3a031-134">End of client support</span></span><br/>    | <span data-ttu-id="3a031-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a031-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3a031-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="3a031-136">Product</span></span><br/>                  | <span data-ttu-id="3a031-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a031-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3a031-138">Header</span><span class="sxs-lookup"><span data-stu-id="3a031-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a031-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a031-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3a031-140">IID</span><span class="sxs-lookup"><span data-stu-id="3a031-140">IID</span></span><br/>                      | <span data-ttu-id="3a031-141">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="3a031-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3a031-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a031-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a031-143">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="3a031-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

