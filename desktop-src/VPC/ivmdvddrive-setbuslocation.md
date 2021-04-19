---
title: Ivmdvddrive-setbusloationmethode (vpccominterfaces. h)
description: Fügt das DVD-Laufwerk an die angegebene busposition auf dem virtuellen Computer an.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Setbusloationmethod-Methode Virtual PC
- Setbusloationmethod-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, setbuslokation-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339331"
---
# <a name="ivmdvddrivesetbuslocation-method"></a><span data-ttu-id="6fc0b-106">Ivmdvddrive:: setbusloation-Methode</span><span class="sxs-lookup"><span data-stu-id="6fc0b-106">IVMDVDDrive::SetBusLocation method</span></span>

<span data-ttu-id="6fc0b-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6fc0b-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6fc0b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6fc0b-109">Fügt das DVD-Laufwerk an die angegebene busposition auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-109">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc0b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fc0b-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="6fc0b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fc0b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc0b-112">*Busnummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fc0b-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc0b-113">Die Busnummer, an die dieses Laufwerk angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-113">The bus number to which this drive is to be attached.</span></span> <span data-ttu-id="6fc0b-114">Beispielsweise würde diese Zahl auf einem IDE-Bus angeben, ob die primäre oder sekundäre Busnummer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-114">For example, on an IDE bus, this number would represent whether to use the primary or secondary bus number.</span></span>

</dd> <dt>

<span data-ttu-id="6fc0b-115">*devicengegen ber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fc0b-115">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc0b-116">Die Gerätenummer, an die dieses Laufwerk angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-116">The device number to which this drive is to be attached.</span></span> <span data-ttu-id="6fc0b-117">Beispielsweise würde diese Zahl auf einem IDE-Bus angeben, ob der primäre oder sekundäre Geräte Speicherort verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-117">For example, on an IDE bus, this number would represent whether to use the primary or secondary device location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc0b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fc0b-118">Return value</span></span>

<span data-ttu-id="6fc0b-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-119">This method can return one of these values.</span></span>



| <span data-ttu-id="6fc0b-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6fc0b-120">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="6fc0b-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fc0b-121">Description</span></span>                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6fc0b-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6fc0b-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="6fc0b-123">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-123">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6fc0b-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6fc0b-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="6fc0b-125">Der angegebene Busspeicherort ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-125">The bus location specified is not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="6fc0b-126"><dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="6fc0b-126"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                       | <span data-ttu-id="6fc0b-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-127">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="6fc0b-128"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="6fc0b-128"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="6fc0b-129">Der Busstandort kann nicht festgelegt werden, während der virtuelle Computer ausgeführt wird oder sich in einem gespeicherten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-129">The bus location cannot be set while the virtual machine is running or in a saved state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6fc0b-130"><dt>**\_verwendende VM-E- \_ Bus \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6fc0b-130"><dt>**VM\_E\_BUS\_LOC\_IN\_USE**</dt></span></span> </dl>                                                                      | <span data-ttu-id="6fc0b-131">Ein anderes Gerät ist bereits an den angegebenen Busstandort angefügt.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-131">Another device is already attached to the specified bus location.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="6fc0b-132"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="6fc0b-132"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="6fc0b-133">Das aktuelle Laufwerk konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-133">The current drive could not be initialized.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="6fc0b-134"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="6fc0b-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="6fc0b-135">Die Änderungen konnten nicht in die Einstellungsdatei geschrieben werden, da der virtuelle Computer für dieses Laufwerk nicht bestimmt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-135">The changes could not be written to the preferences file because the virtual machine for this drive could not be determined.</span></span><br/> |
| <dl> <span data-ttu-id="6fc0b-136"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6fc0b-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="6fc0b-137">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="6fc0b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc0b-138">Requirements</span></span>



| <span data-ttu-id="6fc0b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fc0b-139">Requirement</span></span> | <span data-ttu-id="6fc0b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6fc0b-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc0b-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fc0b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc0b-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fc0b-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6fc0b-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fc0b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc0b-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6fc0b-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6fc0b-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6fc0b-145">End of client support</span></span><br/>    | <span data-ttu-id="6fc0b-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6fc0b-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6fc0b-147">Produkt</span><span class="sxs-lookup"><span data-stu-id="6fc0b-147">Product</span></span><br/>                  | <span data-ttu-id="6fc0b-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6fc0b-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6fc0b-149">Header</span><span class="sxs-lookup"><span data-stu-id="6fc0b-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc0b-150"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc0b-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6fc0b-151">IID</span><span class="sxs-lookup"><span data-stu-id="6fc0b-151">IID</span></span><br/>                      | <span data-ttu-id="6fc0b-152">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-152">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6fc0b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc0b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc0b-154">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="6fc0b-154">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

