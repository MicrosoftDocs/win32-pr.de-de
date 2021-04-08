---
title: Ivmguestos-CSDVersion-Eigenschaft (vpccominterfaces. h)
description: Die CSDVersion des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- CSDVersion-Eigenschaft virtueller PC
- CSDVersion-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, CSDVersion-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d82b3939f581edf328902f7fd0a26e1916abe1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957124"
---
# <a name="ivmguestoscsdversion-property"></a><span data-ttu-id="59857-106">Ivmguestos:: CSDVersion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="59857-106">IVMGuestOS::CSDVersion property</span></span>

<span data-ttu-id="59857-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59857-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59857-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59857-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59857-109">Ruft die CSDVersion des Gast Betriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59857-109">Retrieves the CSDVersion of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="59857-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="59857-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59857-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="59857-111">Syntax</span></span>


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a><span data-ttu-id="59857-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="59857-112">Property value</span></span>

<span data-ttu-id="59857-113">Eine mit NULL endenden Zeichenfolge, z. b. "Service Pack 3", die das neueste Service Pack angibt, das auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="59857-113">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="59857-114">Wenn kein Service Pack installiert wurde, ist die Zeichenfolge leer.</span><span class="sxs-lookup"><span data-stu-id="59857-114">If no Service Pack has been installed, the string is empty.</span></span>

## <a name="error-codes"></a><span data-ttu-id="59857-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="59857-115">Error codes</span></span>



| <span data-ttu-id="59857-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="59857-116">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="59857-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="59857-117">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="59857-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59857-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="59857-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="59857-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="59857-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="59857-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="59857-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="59857-121">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="59857-122"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="59857-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="59857-123">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59857-123">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="59857-124"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="59857-124"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="59857-125">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="59857-125">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="59857-126"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="59857-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="59857-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="59857-127">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="59857-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59857-128">Requirements</span></span>



| <span data-ttu-id="59857-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59857-129">Requirement</span></span> | <span data-ttu-id="59857-130">Wert</span><span class="sxs-lookup"><span data-stu-id="59857-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59857-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59857-131">Minimum supported client</span></span><br/> | <span data-ttu-id="59857-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59857-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59857-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59857-133">Minimum supported server</span></span><br/> | <span data-ttu-id="59857-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="59857-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="59857-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="59857-135">End of client support</span></span><br/>    | <span data-ttu-id="59857-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59857-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59857-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="59857-137">Product</span></span><br/>                  | <span data-ttu-id="59857-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59857-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="59857-139">Header</span><span class="sxs-lookup"><span data-stu-id="59857-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="59857-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59857-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="59857-141">IID</span><span class="sxs-lookup"><span data-stu-id="59857-141">IID</span></span><br/>                      | <span data-ttu-id="59857-142">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="59857-142">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="59857-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59857-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59857-144">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="59857-144">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

