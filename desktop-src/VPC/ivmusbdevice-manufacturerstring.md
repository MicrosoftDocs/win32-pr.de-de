---
title: IVMUSBDevice ManufacturerString-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den Namen des USB-Geräteherstellers ab.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- ManufacturerString-Eigenschaft Virtueller PC
- ManufacturerString-Eigenschaft Virtueller PC, IVMUSBDevice-Schnittstelle
- IVMUSBDevice-Schnittstelle Virtueller PC, ManufacturerString -Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0ec725779e4ffd18d46752f4083ad53c5b77c8392b45dc414d927b1038988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973710"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a>IVMUSBDevice::ManufacturerString (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Namen des USB-Geräteherstellers ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des USB-Geräteherstellers.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                            | Bedeutung                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | Die Methode wurde erfolgreich abgeschlossen.<br/> |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl> | Der Parameter ist **NULL.**<br/>         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice ist als 63C1258C-5721-4070-B86B-A6CE2AFEC0B3 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

