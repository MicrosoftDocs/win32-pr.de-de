---
title: Vmusbdeviceclassenum-Enumeration (vpccominterfaces. h)
description: Gibt die USB-Geräteklasse an.
ms.assetid: 3f5044ea-f7a4-4524-bfb8-55db22732f81
keywords:
- Virtueller PC für vmusbdebug-Enumeration
topic_type:
- apiref
api_name:
- VMUSBDeviceClassEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70335ae083ac2a80717ae64cc8c76f0aff9e791b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104901"
---
# <a name="vmusbdeviceclassenum-enumeration"></a><span data-ttu-id="d2765-104">Vmusbdebug-um-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d2765-104">VMUSBDeviceClassEnum enumeration</span></span>

<span data-ttu-id="d2765-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2765-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d2765-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d2765-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d2765-107">Gibt die USB-Geräteklasse an.</span><span class="sxs-lookup"><span data-stu-id="d2765-107">Specifies the USB device class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2765-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2765-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUSBDeviceClass_InterfaceDescriptor  = 0x00,
  vmUSBDeviceClass_Audio                = 0x01,
  vmUSBDeviceClass_Communication        = 0x02,
  vmUSBDeviceClass_HID                  = 0x03,
  vmUSBDeviceClass_Physical             = 0x05,
  vmUSBDeviceClass_Image                = 0x06,
  vmUSBDeviceClass_Printer              = 0x07,
  vmUSBDeviceClass_MassStorage          = 0x08,
  vmUSBDeviceClass_Hub                  = 0x09,
  vmUSBDeviceClass_CDCData              = 0x0A,
  vmUSBDeviceClass_SmartCard            = 0x0B,
  vmUSBDeviceClass_ContentSecurity      = 0x0D,
  vmUSBDeviceClass_Video                = 0x0E,
  vmUSBDeviceClass_PersonalHealthcare   = 0x0F,
  vmUSBDeviceClass_DiagnosticDevice     = 0xDC,
  vmUSBDeviceClass_WirelessController   = 0xE0,
  vmUSBDeviceClass_Miscellaneous        = 0xEF,
  vmUSBDeviceClass_ApplicationSpecific  = 0xFE,
  vmUSBDeviceClass_VendorSpecific       = 0xFF
} VMUSBDeviceClassEnum;
```



## <a name="constants"></a><span data-ttu-id="d2765-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d2765-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d2765-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmusbtoviceclass \_ interfacedescriptor**</span><span class="sxs-lookup"><span data-stu-id="d2765-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass\_InterfaceDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-111">Ein nicht identifiziertes Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-111">An unidentified device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmusbdebug \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="d2765-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass\_Audio**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-113">Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-113">Audio device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmusbdebug- \_ Kommunikation**</span><span class="sxs-lookup"><span data-stu-id="d2765-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmUSBDeviceClass\_Communication**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-115">Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-115">Communication device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmusbdebug- \_ HID**</span><span class="sxs-lookup"><span data-stu-id="d2765-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass\_HID**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-117">Versteckgerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-117">HID device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmusbdebug- \_ physischer**</span><span class="sxs-lookup"><span data-stu-id="d2765-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass\_Physical**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-119">Physisches Sensorgerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-119">Physical sensory device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmusbdebug- \_ Bild**</span><span class="sxs-lookup"><span data-stu-id="d2765-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmUSBDeviceClass\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-121">Geräte scannen oder Abbild Erstellung.</span><span class="sxs-lookup"><span data-stu-id="d2765-121">Scanning or imaging device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmusbdebug- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="d2765-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmUSBDeviceClass\_Printer**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-123">Druckergerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-123">Printer device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmusbde viceclass- \_ massspeicher**</span><span class="sxs-lookup"><span data-stu-id="d2765-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass\_MassStorage**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-125">Massen Speichergerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-125">Mass storage device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmusbdebug- \_ Hub**</span><span class="sxs-lookup"><span data-stu-id="d2765-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmUSBDeviceClass\_Hub**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-127">Hub-Gerät</span><span class="sxs-lookup"><span data-stu-id="d2765-127">Hub device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmusbdeviceclass \_ cdcdata**</span><span class="sxs-lookup"><span data-stu-id="d2765-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass\_CDCData**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-129">CDC-Daten Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-129">CDC data device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmusbdeviceclass \_ Smartcard**</span><span class="sxs-lookup"><span data-stu-id="d2765-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmUSBDeviceClass\_SmartCard**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-131">Smartcardgerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-131">Smart card device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmusbdebug- \_ ContentSecurity**</span><span class="sxs-lookup"><span data-stu-id="d2765-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass\_ContentSecurity**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-133">Inhalts Sicherheitsgerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-133">Content security device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmusbdebug- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="d2765-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmUSBDeviceClass\_Video**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-135">Video Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-135">Video device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmusbdebug- \_ Personalwesen**</span><span class="sxs-lookup"><span data-stu-id="d2765-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass\_PersonalHealthcare**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-137">Health Care-Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-137">Health care device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmusbdeviceclass \_ diagnosticdevice**</span><span class="sxs-lookup"><span data-stu-id="d2765-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass\_DiagnosticDevice**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-139">Diagnosegerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-139">Diagnostic device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmusbabviceclass \_ wirelesscontroller**</span><span class="sxs-lookup"><span data-stu-id="d2765-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass\_WirelessController**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-141">Drahtlos Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-141">Wireless device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmusbde viceclass \_ Sonstiges**</span><span class="sxs-lookup"><span data-stu-id="d2765-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass\_Miscellaneous**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-143">Verschiedenes Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-143">Miscellaneous device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmusbdeviceclass \_ applicationspecific**</span><span class="sxs-lookup"><span data-stu-id="d2765-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass\_ApplicationSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-145">Anwendungsspezifisches Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-145">Application-specific device.</span></span>

</dd> <dt>

<span data-ttu-id="d2765-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmusbdebug- \_ vendorspecific**</span><span class="sxs-lookup"><span data-stu-id="d2765-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass\_VendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="d2765-147">Herstellerspezifisches Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2765-147">Vendor-specific device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2765-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2765-148">Requirements</span></span>



| <span data-ttu-id="d2765-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2765-149">Requirement</span></span> | <span data-ttu-id="d2765-150">Wert</span><span class="sxs-lookup"><span data-stu-id="d2765-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2765-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2765-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d2765-152">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2765-152">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2765-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2765-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d2765-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d2765-154">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d2765-155">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d2765-155">End of client support</span></span><br/>    | <span data-ttu-id="d2765-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2765-156">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d2765-157">Produkt</span><span class="sxs-lookup"><span data-stu-id="d2765-157">Product</span></span><br/>                  | <span data-ttu-id="d2765-158">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d2765-158">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d2765-159">Header</span><span class="sxs-lookup"><span data-stu-id="d2765-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2765-160"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2765-160"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2765-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2765-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2765-162">**Ivmusbdevice::D eviceclass**</span><span class="sxs-lookup"><span data-stu-id="d2765-162">**IVMUSBDevice::DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

