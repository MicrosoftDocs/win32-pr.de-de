---
title: Ivmguestos ishosttimesyncenabled-Eigenschaft (vpccominterfaces. h)
description: Gibt an, ob die Integrations Komponenten auf diesem virtuellen Computer die Uhr des Gasts mit der hostuhr synchronisieren sollen.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- Ishosttimesyncenabled-Eigenschaft virtueller PC
- Ishosttimesyncenabled-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, ishosttimesyncenabled (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337933"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a><span data-ttu-id="7c6ef-106">Ivmguestos:: ishosttimesyncenabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c6ef-106">IVMGuestOS::IsHostTimeSyncEnabled property</span></span>

<span data-ttu-id="7c6ef-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7c6ef-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7c6ef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7c6ef-109">Gibt an, ob die Integrations Komponenten auf diesem virtuellen Computer (VM) die gastuhr mit der hostuhr synchronisieren sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-109">Indicates whether the Integration Components in this virtual machine (VM) should synchronize the guest's clock with the host's clock.</span></span>

<span data-ttu-id="7c6ef-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6ef-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c6ef-111">Syntax</span></span>


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="7c6ef-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7c6ef-112">Property value</span></span>

<span data-ttu-id="7c6ef-113">Verwenden Sie **Variant \_ true** , wenn die Integrations Komponenten auf diesem virtuellen Computer die Uhr des Gasts mit der hostuhr synchronisieren sollen, und andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="7c6ef-113">Use **VARIANT\_TRUE** if the integration components in this VM should synchronize the guest's clock with the host's clock and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c6ef-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7c6ef-114">Error codes</span></span>



| <span data-ttu-id="7c6ef-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7c6ef-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7c6ef-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c6ef-116">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="7c6ef-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c6ef-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7c6ef-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-118">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="7c6ef-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7c6ef-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7c6ef-120">Der *isaktivierte* Parameter ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-120">The *isEnabled* parameter is not specified.</span></span><br/> |
| <dl> <span data-ttu-id="7c6ef-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="7c6ef-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7c6ef-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-122">The configuration is unknown.</span></span><br/>               |
| <dl> <span data-ttu-id="7c6ef-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7c6ef-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7c6ef-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-124">An unexpected error has occurred.</span></span><br/>           |



## <a name="remarks"></a><span data-ttu-id="7c6ef-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c6ef-125">Remarks</span></span>

<span data-ttu-id="7c6ef-126">Diese Einstellung kann nicht geändert werden, solange der virtuelle Computer aktiv ist (d. h., wird ausgeführt oder befindet sich im gespeicherten Zustand).</span><span class="sxs-lookup"><span data-stu-id="7c6ef-126">You cannot change this setting while the virtual machine is active (that is, running or in saved state).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6ef-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c6ef-127">Requirements</span></span>



| <span data-ttu-id="7c6ef-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c6ef-128">Requirement</span></span> | <span data-ttu-id="7c6ef-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7c6ef-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6ef-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c6ef-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6ef-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c6ef-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c6ef-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c6ef-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6ef-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7c6ef-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7c6ef-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7c6ef-134">End of client support</span></span><br/>    | <span data-ttu-id="7c6ef-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c6ef-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7c6ef-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="7c6ef-136">Product</span></span><br/>                  | <span data-ttu-id="7c6ef-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7c6ef-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7c6ef-138">Header</span><span class="sxs-lookup"><span data-stu-id="7c6ef-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c6ef-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c6ef-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7c6ef-140">IID</span><span class="sxs-lookup"><span data-stu-id="7c6ef-140">IID</span></span><br/>                      | <span data-ttu-id="7c6ef-141">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="7c6ef-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7c6ef-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c6ef-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6ef-143">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="7c6ef-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

