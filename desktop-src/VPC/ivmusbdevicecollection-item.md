---
title: Ivmusbdevicecollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das USB-Geräte Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmusbdebug ecollection-Schnittstelle
- Ivmusbdebug-Schnittstelle virtueller PC, Element Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477046"
---
# <a name="ivmusbdevicecollectionitem-property"></a>Ivmusbdebug:: Item-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das USB-Geräte Objekt ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**ivmusbdevice**](ivmusbdevice.md) -Objekt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt. <br/>                                                      |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der *Parameter* "" ist **null**. <br/>                                             |
| <dl> <dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung. <br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmusbdevicecollection ist als 4f-cd6a5--ID definiert. d1c-9s4d-e90abb8b3749<br/>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmusbdevice**](ivmusbdevice.md)
</dt> <dt>

[**Ivmusbde vicecollection**](ivmusbdevicecollection.md)
</dt> </dl>

 

