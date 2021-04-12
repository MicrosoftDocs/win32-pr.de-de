---
title: Ivmharddiskconnection-setbusloationmethode (vpccominterfaces. h)
description: Legt den Busspeicherort fest, an den diese Festplatte angefügt ist.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Setbusloationmethod-Methode Virtual PC
- Setbusloationmethod-Methode Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection-Schnittstelle Virtual PC, setbusloationmethod
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340337"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a><span data-ttu-id="32f66-106">Ivmharddiskconnection:: setbusloations-Methode</span><span class="sxs-lookup"><span data-stu-id="32f66-106">IVMHardDiskConnection::SetBusLocation method</span></span>

<span data-ttu-id="32f66-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="32f66-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="32f66-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="32f66-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="32f66-109">Legt den Busspeicherort fest, an den diese Festplatte angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="32f66-109">Sets the bus location to which this hard disk is attached.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f66-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="32f66-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="32f66-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="32f66-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f66-112">*vmbusnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32f66-112">*vmBusNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32f66-113">Die zu verwendende Busnummer.</span><span class="sxs-lookup"><span data-stu-id="32f66-113">The bus number to be used.</span></span>

</dd> <dt>

<span data-ttu-id="32f66-114">*vmdevicenumschlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32f66-114">*vmDeviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32f66-115">Die zu verwendende Gerätenummer.</span><span class="sxs-lookup"><span data-stu-id="32f66-115">The device number to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f66-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32f66-116">Return value</span></span>

<span data-ttu-id="32f66-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="32f66-117">This method can return one of these values.</span></span>



| <span data-ttu-id="32f66-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="32f66-118">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="32f66-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32f66-119">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32f66-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="32f66-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="32f66-121">The operation was successful.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="32f66-122"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="32f66-123">Der angegebene Busspeicherort ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="32f66-123">The bus location specified is not valid.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="32f66-124"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="32f66-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="32f66-125">Der Busstandort konnte nicht festgelegt werden, weil sich der virtuelle Computer in einem laufenden oder gespeicherten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="32f66-125">The bus location could not be set because the virtual machine is in a running or saved state.</span></span><br/>    |
| <dl> <span data-ttu-id="32f66-126"><dt>**VM \_ E \_ Drive \_ Bus \_ loc \_ \_ verwendet**</dt> <dt>0xa00400503</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-126"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="32f66-127">Der Busstandort konnte nicht festgelegt werden, da zurzeit ein anderes Gerät an diesen Speicherort angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="32f66-127">The bus location could not be set because another device is currently attached to this location.</span></span><br/> |
| <dl> <span data-ttu-id="32f66-128"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="32f66-129">Das aktuelle Laufwerk ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="32f66-129">The current drive is not valid.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="32f66-130"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="32f66-131">Der aktuelle virtuelle Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="32f66-131">The current virtual machine is not valid.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="32f66-132"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="32f66-133">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="32f66-133">An unexpected error has occurred.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="32f66-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32f66-134">Requirements</span></span>



| <span data-ttu-id="32f66-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32f66-135">Requirement</span></span> | <span data-ttu-id="32f66-136">Wert</span><span class="sxs-lookup"><span data-stu-id="32f66-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f66-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32f66-137">Minimum supported client</span></span><br/> | <span data-ttu-id="32f66-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32f66-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32f66-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32f66-139">Minimum supported server</span></span><br/> | <span data-ttu-id="32f66-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="32f66-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="32f66-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="32f66-141">End of client support</span></span><br/>    | <span data-ttu-id="32f66-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32f66-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="32f66-143">Produkt</span><span class="sxs-lookup"><span data-stu-id="32f66-143">Product</span></span><br/>                  | <span data-ttu-id="32f66-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="32f66-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="32f66-145">Header</span><span class="sxs-lookup"><span data-stu-id="32f66-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f66-146"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="32f66-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="32f66-147">IID</span><span class="sxs-lookup"><span data-stu-id="32f66-147">IID</span></span><br/>                      | <span data-ttu-id="32f66-148">IID \_ ivmharddiskconnection ist als aefa36a5-463a-46AE-9e6c-a1fb4e12e671 definiert.</span><span class="sxs-lookup"><span data-stu-id="32f66-148">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="32f66-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32f66-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f66-150">**Ivmharddiskconnection**</span><span class="sxs-lookup"><span data-stu-id="32f66-150">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

