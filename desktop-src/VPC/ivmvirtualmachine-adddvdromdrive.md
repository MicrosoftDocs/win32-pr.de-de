---
title: Ivmvirtualmachine AddDVDROMDrive-Methode (vpccominterfaces. h)
description: Fügt ein neues CD-oder DVD-Laufwerk zum virtuellen Computer hinzu.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVDROMDrive-Methode Virtual PC
- AddDVDROMDrive-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, AddDVDROMDrive-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338548"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a><span data-ttu-id="cfb55-106">Ivmvirtualmachine:: AddDVDROMDrive-Methode</span><span class="sxs-lookup"><span data-stu-id="cfb55-106">IVMVirtualMachine::AddDVDROMDrive method</span></span>

<span data-ttu-id="cfb55-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfb55-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cfb55-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cfb55-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cfb55-109">Fügt ein neues CD-oder DVD-Laufwerk zum virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="cfb55-109">Adds a new CD or DVD drive to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb55-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb55-110">Syntax</span></span>


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="cfb55-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfb55-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb55-112">*Busnummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfb55-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb55-113">Der Bus, an den das Laufwerk angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cfb55-113">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="cfb55-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb55-114">Value</span></span>                                                                        | <span data-ttu-id="cfb55-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cfb55-115">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="cfb55-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="cfb55-117">Das Laufwerk wird an den ersten Bus angefügt.</span><span class="sxs-lookup"><span data-stu-id="cfb55-117">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="cfb55-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="cfb55-119">Das Laufwerk wird an den zweiten Bus angefügt.</span><span class="sxs-lookup"><span data-stu-id="cfb55-119">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cfb55-120">*devicengegen ber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfb55-120">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb55-121">Das Gerät, an das das Laufwerk angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cfb55-121">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="cfb55-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb55-122">Value</span></span>                                                                        | <span data-ttu-id="cfb55-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cfb55-123">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfb55-124"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-124"><dt>0</dt></span></span> </dl> | <span data-ttu-id="cfb55-125">Das Laufwerk wird an das erste Gerät auf dem Bus angefügt.</span><span class="sxs-lookup"><span data-stu-id="cfb55-125">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="cfb55-126"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-126"><dt>1</dt></span></span> </dl> | <span data-ttu-id="cfb55-127">Das Laufwerk wird mit dem zweiten Gerät auf dem Bus verbunden.</span><span class="sxs-lookup"><span data-stu-id="cfb55-127">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cfb55-128">*dvddrive* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cfb55-128">*dvdDrive* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb55-129">Ein [**ivmdvddrive**](ivmdvddrive.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cfb55-129">An [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb55-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfb55-130">Return value</span></span>

<span data-ttu-id="cfb55-131">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cfb55-131">This method can return one of these values.</span></span>



| <span data-ttu-id="cfb55-132">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="cfb55-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="cfb55-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfb55-133">Description</span></span>                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="cfb55-134"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-134"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="cfb55-135">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfb55-135">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="cfb55-136"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-136"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                       | <span data-ttu-id="cfb55-137">Der Parameter " *dvddrive* " ist **null**.</span><span class="sxs-lookup"><span data-stu-id="cfb55-137">The *dvdDrive* parameter is **NULL**.</span></span><br/>               |
| <dl> <span data-ttu-id="cfb55-138"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-138"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="cfb55-139">Ein Parameter ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="cfb55-139">A parameter is not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="cfb55-140"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-140"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="cfb55-141">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="cfb55-141">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="cfb55-142"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="cfb55-142"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="cfb55-143">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="cfb55-143">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="cfb55-144"><dt>**VM \_ E \_ Drive \_ Bus \_ loc \_ \_ verwendet**</dt> <dt>0xa00400503</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-144"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="cfb55-145">Der angegebene Busspeicherort wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="cfb55-145">The specified bus location is in use.</span></span><br/>               |
| <dl> <span data-ttu-id="cfb55-146"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-146"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="cfb55-147">Das angegebene Laufwerk ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cfb55-147">The drive specified is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="cfb55-148"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-148"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="cfb55-149">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cfb55-149">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="cfb55-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb55-150">Remarks</span></span>

<span data-ttu-id="cfb55-151">Sie können einem beendeten virtuellen Computer nur ein neues CD-oder DVD-Laufwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cfb55-151">You can only add a new CD or DVD drive to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb55-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfb55-152">Requirements</span></span>



| <span data-ttu-id="cfb55-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfb55-153">Requirement</span></span> | <span data-ttu-id="cfb55-154">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb55-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb55-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfb55-155">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb55-156">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfb55-156">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cfb55-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfb55-157">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb55-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cfb55-158">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cfb55-159">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cfb55-159">End of client support</span></span><br/>    | <span data-ttu-id="cfb55-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cfb55-160">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cfb55-161">Produkt</span><span class="sxs-lookup"><span data-stu-id="cfb55-161">Product</span></span><br/>                  | <span data-ttu-id="cfb55-162">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cfb55-162">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cfb55-163">Header</span><span class="sxs-lookup"><span data-stu-id="cfb55-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb55-164"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb55-164"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cfb55-165">IID</span><span class="sxs-lookup"><span data-stu-id="cfb55-165">IID</span></span><br/>                      | <span data-ttu-id="cfb55-166">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="cfb55-166">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cfb55-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfb55-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb55-168">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="cfb55-168">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

