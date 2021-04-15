---
title: Ivmguestos osname-Eigenschaft (vpccominterfaces. h)
description: Der Name des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- Osname-Eigenschaft virtueller PC
- Osname-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, osname-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672c7b2c852bcbb1ec39b61889b03738e3a2df23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476554"
---
# <a name="ivmguestososname-property"></a><span data-ttu-id="bdfcd-106">Ivmguestos:: osname (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bdfcd-106">IVMGuestOS::OSName property</span></span>

<span data-ttu-id="bdfcd-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bdfcd-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bdfcd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bdfcd-109">Ruft den Namen des Gast Betriebssystems ab, das auf dem virtuellen Computer (VM) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-109">Retrieves the name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="bdfcd-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdfcd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdfcd-111">Syntax</span></span>


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a><span data-ttu-id="bdfcd-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bdfcd-112">Property value</span></span>

<span data-ttu-id="bdfcd-113">Der vollständige Name (einschließlich des Sammlungs namens) des Gast Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-113">The full name (including suite name) of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bdfcd-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bdfcd-114">Error codes</span></span>



| <span data-ttu-id="bdfcd-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="bdfcd-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="bdfcd-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bdfcd-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bdfcd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bdfcd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="bdfcd-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="bdfcd-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bdfcd-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="bdfcd-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="bdfcd-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="bdfcd-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="bdfcd-122">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="bdfcd-123"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="bdfcd-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="bdfcd-124">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="bdfcd-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bdfcd-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="bdfcd-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="bdfcd-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdfcd-127">Remarks</span></span>

<span data-ttu-id="bdfcd-128">Der virtuelle Computer muss ausgeführt werden (d. h. vollständig gestartet und nicht heruntergefahren werden), und Integrations Komponenten müssen installiert werden, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-128">The VM must be running (that is, fully booted and not shutting down) and integration components must be installed when this method is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdfcd-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdfcd-129">Requirements</span></span>



| <span data-ttu-id="bdfcd-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdfcd-130">Requirement</span></span> | <span data-ttu-id="bdfcd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bdfcd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfcd-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdfcd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bdfcd-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdfcd-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bdfcd-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdfcd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bdfcd-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bdfcd-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bdfcd-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bdfcd-136">End of client support</span></span><br/>    | <span data-ttu-id="bdfcd-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bdfcd-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bdfcd-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="bdfcd-138">Product</span></span><br/>                  | <span data-ttu-id="bdfcd-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bdfcd-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bdfcd-140">Header</span><span class="sxs-lookup"><span data-stu-id="bdfcd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdfcd-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdfcd-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bdfcd-142">IID</span><span class="sxs-lookup"><span data-stu-id="bdfcd-142">IID</span></span><br/>                      | <span data-ttu-id="bdfcd-143">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="bdfcd-143">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="bdfcd-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdfcd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdfcd-145">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="bdfcd-145">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

