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
# <a name="vmusbdeviceclassenum-enumeration"></a>Vmusbdebug-um-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt die USB-Geräteklasse an.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmusbtoviceclass \_ interfacedescriptor**
</dt> <dd>

Ein nicht identifiziertes Gerät.

</dd> <dt>

<span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmusbdebug \_ -Audiodatei**
</dt> <dd>

Audiogerät.

</dd> <dt>

<span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmusbdebug- \_ Kommunikation**
</dt> <dd>

Kommunikationsgerät.

</dd> <dt>

<span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmusbdebug- \_ HID**
</dt> <dd>

Versteckgerät.

</dd> <dt>

<span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmusbdebug- \_ physischer**
</dt> <dd>

Physisches Sensorgerät.

</dd> <dt>

<span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmusbdebug- \_ Bild**
</dt> <dd>

Geräte scannen oder Abbild Erstellung.

</dd> <dt>

<span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmusbdebug- \_ Drucker**
</dt> <dd>

Druckergerät.

</dd> <dt>

<span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmusbde viceclass- \_ massspeicher**
</dt> <dd>

Massen Speichergerät.

</dd> <dt>

<span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmusbdebug- \_ Hub**
</dt> <dd>

Hub-Gerät

</dd> <dt>

<span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmusbdeviceclass \_ cdcdata**
</dt> <dd>

CDC-Daten Gerät.

</dd> <dt>

<span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmusbdeviceclass \_ Smartcard**
</dt> <dd>

Smartcardgerät.

</dd> <dt>

<span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmusbdebug- \_ ContentSecurity**
</dt> <dd>

Inhalts Sicherheitsgerät.

</dd> <dt>

<span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmusbdebug- \_ Video**
</dt> <dd>

Video Gerät.

</dd> <dt>

<span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmusbdebug- \_ Personalwesen**
</dt> <dd>

Health Care-Gerät.

</dd> <dt>

<span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmusbdeviceclass \_ diagnosticdevice**
</dt> <dd>

Diagnosegerät.

</dd> <dt>

<span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmusbabviceclass \_ wirelesscontroller**
</dt> <dd>

Drahtlos Gerät.

</dd> <dt>

<span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmusbde viceclass \_ Sonstiges**
</dt> <dd>

Verschiedenes Gerät.

</dd> <dt>

<span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmusbdeviceclass \_ applicationspecific**
</dt> <dd>

Anwendungsspezifisches Gerät.

</dd> <dt>

<span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmusbdebug- \_ vendorspecific**
</dt> <dd>

Herstellerspezifisches Gerät.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmusbdevice::D eviceclass**](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

