---
title: Ivmguestos osminorversion-Eigenschaft (vpccominterfaces. h)
description: Die neben Version des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- Osminorversion-Eigenschaft virtueller PC
- Osminorversion-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, osminorversion (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c068ee6d8112561f57d0644f6bc7bc4844096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337321"
---
# <a name="ivmguestososminorversion-property"></a><span data-ttu-id="f0fc6-106">Ivmguestos:: osminorversion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f0fc6-106">IVMGuestOS::OSMinorVersion property</span></span>

<span data-ttu-id="f0fc6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0fc6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0fc6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0fc6-109">Ruft die neben Version des Gast Betriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-109">Retrieves the minor version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="f0fc6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0fc6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0fc6-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="f0fc6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f0fc6-112">Property value</span></span>

<span data-ttu-id="f0fc6-113">Die Nebenversion.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0fc6-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f0fc6-114">Error codes</span></span>



| <span data-ttu-id="f0fc6-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="f0fc6-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f0fc6-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0fc6-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f0fc6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f0fc6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="f0fc6-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="f0fc6-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f0fc6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="f0fc6-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="f0fc6-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="f0fc6-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="f0fc6-122">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="f0fc6-123"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="f0fc6-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="f0fc6-124">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="f0fc6-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f0fc6-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="f0fc6-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="f0fc6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0fc6-127">Requirements</span></span>



| <span data-ttu-id="f0fc6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0fc6-128">Requirement</span></span> | <span data-ttu-id="f0fc6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f0fc6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0fc6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0fc6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f0fc6-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0fc6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0fc6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0fc6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f0fc6-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0fc6-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0fc6-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f0fc6-134">End of client support</span></span><br/>    | <span data-ttu-id="f0fc6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0fc6-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0fc6-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="f0fc6-136">Product</span></span><br/>                  | <span data-ttu-id="f0fc6-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0fc6-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0fc6-138">Header</span><span class="sxs-lookup"><span data-stu-id="f0fc6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0fc6-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0fc6-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0fc6-140">IID</span><span class="sxs-lookup"><span data-stu-id="f0fc6-140">IID</span></span><br/>                      | <span data-ttu-id="f0fc6-141">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f0fc6-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0fc6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0fc6-143">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="f0fc6-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

