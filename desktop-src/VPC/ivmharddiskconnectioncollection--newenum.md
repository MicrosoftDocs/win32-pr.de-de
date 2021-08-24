---
title: IVMHardDiskConnectionCollection _NewEnum-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft einen Enumerator für die Auflistung ab. | IVMHardDiskConnectionCollection _NewEnum-Eigenschaft (VPCCOMInterfaces.h)
ms.assetid: 9302f536-de25-4aac-88cf-9f4af6efcda7
keywords:
- _NewEnum-Eigenschaft Virtueller PC
- _NewEnum Eigenschaft Virtueller PC, IVMHardDiskConnectionCollection-Schnittstelle
- IVMHardDiskConnectionCollection-Schnittstelle Virtueller PC , _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection._NewEnum
- IVMHardDiskConnectionCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02c4bbd5d0d54d5116adc09c3a0a23c4594834b48b1b28d1700d41e5525b5d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510800"
---
# <a name="ivmharddiskconnectioncollection_newenum-property"></a>IVMHardDiskConnectionCollection:: \_ NewEnum-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft einen Enumerator für die Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Eigenschaftswert

Der [](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) IEnumVARIANT-Enumerator.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/> |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>    |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                          |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                               |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection ist als b9f2caf4-0aeb-4085-b105-ceddb90dbf62 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

