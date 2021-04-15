---
title: Ivmguestos Computername-Eigenschaft (vpccominterfaces. h)
description: Der Computername des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- Computername-Eigenschaft virtueller PC
- Computername-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, Computername (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b266c238809284b340095dd25390d6e5f3d2b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479005"
---
# <a name="ivmguestoscomputername-property"></a><span data-ttu-id="ed8df-106">Ivmguestos:: Computername (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ed8df-106">IVMGuestOS::ComputerName property</span></span>

<span data-ttu-id="ed8df-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed8df-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ed8df-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ed8df-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ed8df-109">Ruft den Computernamen des Gast Betriebssystems ab, das auf dem virtuellen Computer (VM) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed8df-109">Retrieves the computer name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="ed8df-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ed8df-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8df-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed8df-111">Syntax</span></span>


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a><span data-ttu-id="ed8df-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ed8df-112">Property value</span></span>

<span data-ttu-id="ed8df-113">Der Computername des Gast Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="ed8df-113">The computer name of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ed8df-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ed8df-114">Error codes</span></span>



| <span data-ttu-id="ed8df-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="ed8df-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="ed8df-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ed8df-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ed8df-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ed8df-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="ed8df-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed8df-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="ed8df-119"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ed8df-119"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="ed8df-120">Der-Parameter ist ungültig oder wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="ed8df-120">The parameter is not valid or not specified.</span></span><br/>         |
| <dl> <span data-ttu-id="ed8df-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="ed8df-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="ed8df-122">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed8df-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="ed8df-123"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="ed8df-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="ed8df-124">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="ed8df-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="ed8df-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ed8df-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="ed8df-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ed8df-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="ed8df-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed8df-127">Requirements</span></span>



| <span data-ttu-id="ed8df-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed8df-128">Requirement</span></span> | <span data-ttu-id="ed8df-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ed8df-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8df-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed8df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8df-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed8df-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed8df-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed8df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8df-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ed8df-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ed8df-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ed8df-134">End of client support</span></span><br/>    | <span data-ttu-id="ed8df-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed8df-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ed8df-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="ed8df-136">Product</span></span><br/>                  | <span data-ttu-id="ed8df-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ed8df-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ed8df-138">Header</span><span class="sxs-lookup"><span data-stu-id="ed8df-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed8df-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed8df-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ed8df-140">IID</span><span class="sxs-lookup"><span data-stu-id="ed8df-140">IID</span></span><br/>                      | <span data-ttu-id="ed8df-141">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="ed8df-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ed8df-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed8df-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8df-143">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="ed8df-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

