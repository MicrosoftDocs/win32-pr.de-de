---
title: Ivmvirtualmachine removedvdromdrive-Methode (vpccominterfaces. h)
description: Entfernt das angegebene CD-oder DVD-Laufwerk von der virtuellen Maschine.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- Removedvdromdrive-Methode Virtual PC
- Removedvdromdrive-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removedvdromdrive-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0962b388c318d5abebdbd7a021a4466e644a28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104097"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a><span data-ttu-id="fd4e6-106">Ivmvirtualmachine:: removedvdromdrive-Methode</span><span class="sxs-lookup"><span data-stu-id="fd4e6-106">IVMVirtualMachine::RemoveDVDROMDrive method</span></span>

<span data-ttu-id="fd4e6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd4e6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd4e6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd4e6-109">Entfernt das angegebene CD-oder DVD-Laufwerk von der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-109">Removes the specified CD or DVD drive from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4e6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd4e6-110">Syntax</span></span>


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="fd4e6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd4e6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd4e6-112">*dvddrive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd4e6-112">*dvdDrive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd4e6-113">Das zu entfernende Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-113">The drive to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd4e6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd4e6-114">Return value</span></span>

<span data-ttu-id="fd4e6-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-115">This method can return one of these values.</span></span>



| <span data-ttu-id="fd4e6-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="fd4e6-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="fd4e6-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd4e6-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd4e6-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd4e6-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="fd4e6-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="fd4e6-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fd4e6-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="fd4e6-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fd4e6-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="fd4e6-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="fd4e6-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="fd4e6-124"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="fd4e6-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="fd4e6-125">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="fd4e6-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="fd4e6-126"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="fd4e6-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="fd4e6-127">Das angegebene Laufwerk ist nicht mit diesem Busstandort verbunden.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="fd4e6-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd4e6-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="fd4e6-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="fd4e6-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd4e6-130">Remarks</span></span>

<span data-ttu-id="fd4e6-131">Sie können ein vorhandenes CD-oder DVD-Laufwerk nur von einem beendeten virtuellen Computer entfernen.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-131">You can only remove an existing CD or DVD drive from a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd4e6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd4e6-132">Requirements</span></span>



| <span data-ttu-id="fd4e6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd4e6-133">Requirement</span></span> | <span data-ttu-id="fd4e6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="fd4e6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd4e6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd4e6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fd4e6-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd4e6-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd4e6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd4e6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fd4e6-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd4e6-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd4e6-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fd4e6-139">End of client support</span></span><br/>    | <span data-ttu-id="fd4e6-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd4e6-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd4e6-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="fd4e6-141">Product</span></span><br/>                  | <span data-ttu-id="fd4e6-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd4e6-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd4e6-143">Header</span><span class="sxs-lookup"><span data-stu-id="fd4e6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd4e6-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd4e6-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd4e6-145">IID</span><span class="sxs-lookup"><span data-stu-id="fd4e6-145">IID</span></span><br/>                      | <span data-ttu-id="fd4e6-146">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="fd4e6-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fd4e6-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd4e6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd4e6-148">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="fd4e6-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

