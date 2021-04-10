---
title: Ivmusbdevice-Eigenschaft "attacheddevm" (vpccominterfaces. h)
description: Ruft den Namen des virtuellen Computers ab, an den das USB-Gerät angefügt ist.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- Eigenschaften von "AttachedTo VM" für Virtual PC
- Eigenschaft "AttachedTo VM" Virtual PC, ivmusbdevice Interface
- Ivmusbdevice Interface Virtual PC, Eigenschaft "AttachedTo VM"
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040676"
---
# <a name="ivmusbdeviceattachedtovm-property"></a>Ivmusbdevice:: AttachedTo VM (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Namen des virtuellen Computers ab, an den das USB-Gerät angefügt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des virtuellen Computers (VM).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                           | Bedeutung                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                              | Das Gerät ist an den virtuellen Computer angefügt, und der Name wird zurückgegeben.<br/> |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                           | Das Gerät ist an den Host angefügt.<br/>                         |
| <dl> <dt>VM \_ E \_ USB \_ externe \_ VM</dt> <dt>0xa00400929</dt> </dl> | Das Gerät ist an einen virtuellen Computer in einer anderen Benutzersitzung angefügt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                | Der-Parameter ist **null**.<br/>                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmusbdevice**](ivmusbdevice.md)
</dt> </dl>

 

