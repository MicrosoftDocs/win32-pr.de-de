---
title: IVMFloppyDriveCollection_NewEnum eigenschaft (VPCCOMInterfaces.h)
description: Ruft einen Enumerator für die Auflistung ab. | IVMFloppyDriveCollection_NewEnum eigenschaft (VPCCOMInterfaces.h)
ms.assetid: 06de9560-cba9-4c64-907e-83e77781cafc
keywords:
- _NewEnum-Eigenschaft Virtueller PC
- _NewEnum Virtual PC, IVMFloppyDriveCollection-Schnittstelle
- IVMFloppyDriveCollection-Schnittstelle Virtueller PC, _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection._NewEnum
- IVMFloppyDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceac8ef29e659269a34687f9b32c74c7f0da2d6562343c1fc8588e07230d5b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653670"
---
# <a name="ivmfloppydrivecollection_newenum-property"></a>IVMFloppyDriveCollection:: \_ NewEnum-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft einen Enumerator für die Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Eigenschaftswert

Der [IEnumVARIANT-Enumerator.](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/> |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>    |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection ist als 8ba70a25-f698-4ee5-85ce-3cc93a925516 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)
</dt> </dl>

 

