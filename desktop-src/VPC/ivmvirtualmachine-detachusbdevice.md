---
title: Methode ' ivmvirtualmachine Detach-bdevice ' (vpccominterfaces. h)
description: Gibt ein USB-Gerät von einem virtuellen Computer frei.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Detachus-Geräte Methode Virtual PC
- Detachder bdevice-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, detachus-Geräte Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345492"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a><span data-ttu-id="ab63b-106">Ivmvirtualmachine::D etachder bdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="ab63b-106">IVMVirtualMachine::DetachUSBDevice method</span></span>

<span data-ttu-id="ab63b-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab63b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ab63b-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ab63b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ab63b-109">Gibt ein USB-Gerät von einem virtuellen Computer frei.</span><span class="sxs-lookup"><span data-stu-id="ab63b-109">Releases a USB device from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab63b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab63b-110">Syntax</span></span>


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ab63b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab63b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab63b-112">*in-bdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab63b-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab63b-113">Ein [**ivmusbdevice**](ivmusbdevice.md) -Zeiger, der das USB-Gerät darstellt, das vom virtuellen Computer getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab63b-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device to be detached from the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab63b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab63b-114">Return value</span></span>

<span data-ttu-id="ab63b-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ab63b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ab63b-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ab63b-116">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="ab63b-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab63b-117">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ab63b-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ab63b-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="ab63b-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab63b-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="ab63b-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ab63b-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                  | <span data-ttu-id="ab63b-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ab63b-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="ab63b-122"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="ab63b-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>     | <span data-ttu-id="ab63b-123">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab63b-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="ab63b-124"><dt>**VM \_ E \_ USB \_ \_ -**</dt> Fehler beim Trennen <dt>0xa00400927</dt></span><span class="sxs-lookup"><span data-stu-id="ab63b-124"><dt>**VM\_E\_USB\_DETACH\_FAILED**</dt> <dt>0xA00400927</dt></span></span> </dl> | <span data-ttu-id="ab63b-125">Fehler beim Trennvorgang.</span><span class="sxs-lookup"><span data-stu-id="ab63b-125">The detach operation failed.</span></span><br/>        |
| <dl> <span data-ttu-id="ab63b-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ab63b-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="ab63b-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ab63b-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="ab63b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab63b-128">Requirements</span></span>



| <span data-ttu-id="ab63b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab63b-129">Requirement</span></span> | <span data-ttu-id="ab63b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ab63b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab63b-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab63b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ab63b-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab63b-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab63b-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab63b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ab63b-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ab63b-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ab63b-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ab63b-135">End of client support</span></span><br/>    | <span data-ttu-id="ab63b-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab63b-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ab63b-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="ab63b-137">Product</span></span><br/>                  | <span data-ttu-id="ab63b-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ab63b-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ab63b-139">Header</span><span class="sxs-lookup"><span data-stu-id="ab63b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab63b-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab63b-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ab63b-141">IID</span><span class="sxs-lookup"><span data-stu-id="ab63b-141">IID</span></span><br/>                      | <span data-ttu-id="ab63b-142">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="ab63b-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ab63b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab63b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab63b-144">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="ab63b-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

