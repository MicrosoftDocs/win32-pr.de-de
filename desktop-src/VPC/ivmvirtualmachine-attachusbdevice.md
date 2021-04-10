---
title: Ivmvirtualmachine attachingbdevice-Methode (vpccominterfaces. h)
description: Fügt ein USB-Gerät an einen virtuellen Computer an.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Attachingbdevice-Methode Virtual PC
- Attachingbdevice-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, attachingbdevice-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040738"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a><span data-ttu-id="bab48-106">Ivmvirtualmachine:: attachingbdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="bab48-106">IVMVirtualMachine::AttachUSBDevice method</span></span>

<span data-ttu-id="bab48-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bab48-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bab48-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bab48-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bab48-109">Fügt ein USB-Gerät an einen virtuellen Computer (VM) an.</span><span class="sxs-lookup"><span data-stu-id="bab48-109">Attaches a USB device to a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="bab48-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab48-110">Syntax</span></span>


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="bab48-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bab48-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab48-112">*in-bdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bab48-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab48-113">Ein [**ivmusbdevice**](ivmusbdevice.md) -Zeiger, der das USB-Gerät darstellt, das mit dem Host verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="bab48-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device connected to the host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab48-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bab48-114">Return value</span></span>

<span data-ttu-id="bab48-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bab48-115">This method can return one of these values.</span></span>



| <span data-ttu-id="bab48-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bab48-116">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="bab48-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bab48-117">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bab48-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="bab48-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bab48-119">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="bab48-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="bab48-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bab48-121">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="bab48-122"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="bab48-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                        | <span data-ttu-id="bab48-123">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bab48-123">The VM is not running.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="bab48-124"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                             | <span data-ttu-id="bab48-125">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="bab48-125">The configuration is unknown.</span></span><br/>                                           |
| <dl> <span data-ttu-id="bab48-126"><dt>**VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch**</dt> nehmen <dt>0xa0040504</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-126"><dt>**VM\_E\_ADDITIONS\_NOT\_AVAIL**</dt> <dt>0xA0040504</dt></span></span> </dl>                   | <span data-ttu-id="bab48-127">Integrations Komponenten sind im Gast Betriebssystem nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bab48-127">Integration Components are not available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="bab48-128"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="bab48-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>          | <span data-ttu-id="bab48-129">Das USB-Feature ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bab48-129">The USB feature is not available.</span></span><br/>                                       |
| <dl> <span data-ttu-id="bab48-130"><dt>**VM \_ E \_ USB- \_ Connector- \_ Treiber \_ Fehler**</dt> <dt>0xa00400925</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-130"><dt>**VM\_E\_USB\_CONNECTOR\_DRIVER\_ERROR**</dt> <dt>0xA00400925</dt></span></span> </dl>          | <span data-ttu-id="bab48-131">Fehler beim USB-Connector-Treiber.</span><span class="sxs-lookup"><span data-stu-id="bab48-131">There was a USB Connector driver error.</span></span><br/>                                 |
| <dl> <span data-ttu-id="bab48-132"><dt>**VM \_ E \_ USB- \_ Anfüge Fehler \_ \_ Weitere \_ Geräte**</dt> <dt>0xa00400931</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-132"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_MORE\_DEVICES**</dt> <dt>0xA00400931</dt></span></span> </dl>     | <span data-ttu-id="bab48-133">Weitere Geräte können nicht an die VM angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bab48-133">Cannot attach more devices to the VM.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bab48-134"><dt>**VM \_ \_ \_ \_ \_ \_ Fehler beim Anfügen des USB-**</dt> Anfügens. <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bab48-134"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_GP\_ERROR**</dt> <dt>0xA00400932</dt></span></span> </dl>         | <span data-ttu-id="bab48-135">Die USB-Umleitung wird von einer Gruppenrichtlinien Einstellung verhindert.</span><span class="sxs-lookup"><span data-stu-id="bab48-135">A group policy setting is preventing the USB redirection.</span></span><br/>               |
| <dl> <span data-ttu-id="bab48-136"><dt>**VM \_ Fehler beim E \_ -USB- \_ Anfügen \_ \_ \_**</dt> mit <dt>0xa00400933</dt> .</span><span class="sxs-lookup"><span data-stu-id="bab48-136"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_ALREADY\_ASSIGNED**</dt> <dt>0xA00400933</dt></span></span> </dl> | <span data-ttu-id="bab48-137">Ein USB-Gerät wurde bereits von einem anderen Client angefügt.</span><span class="sxs-lookup"><span data-stu-id="bab48-137">A USB device has already been attached by some other client.</span></span><br/>            |
| <dl> <span data-ttu-id="bab48-138"><dt>**VM \_ E \_ USB \_ - \_ Anfüge**</dt> Fehler <dt>0xa00400926</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-138"><dt>**VM\_E\_USB\_ATTACH\_FAILED**</dt> <dt>0xA00400926</dt></span></span> </dl>                    | <span data-ttu-id="bab48-139">Der Anfüge Vorgang ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="bab48-139">The attach operation failed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="bab48-140"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-140"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="bab48-141">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bab48-141">An unexpected error has occurred.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="bab48-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bab48-142">Requirements</span></span>



| <span data-ttu-id="bab48-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bab48-143">Requirement</span></span> | <span data-ttu-id="bab48-144">Wert</span><span class="sxs-lookup"><span data-stu-id="bab48-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab48-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bab48-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bab48-146">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bab48-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bab48-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bab48-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bab48-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bab48-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bab48-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bab48-149">End of client support</span></span><br/>    | <span data-ttu-id="bab48-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bab48-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bab48-151">Produkt</span><span class="sxs-lookup"><span data-stu-id="bab48-151">Product</span></span><br/>                  | <span data-ttu-id="bab48-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bab48-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bab48-153">Header</span><span class="sxs-lookup"><span data-stu-id="bab48-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="bab48-154"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab48-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bab48-155">IID</span><span class="sxs-lookup"><span data-stu-id="bab48-155">IID</span></span><br/>                      | <span data-ttu-id="bab48-156">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="bab48-156">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bab48-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bab48-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab48-158">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="bab48-158">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

