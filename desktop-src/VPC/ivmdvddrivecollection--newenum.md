---
title: IVMDVDDriveCollection _NewEnum-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft einen Enumerator für die CD/DVD-Sammlung ab.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- _NewEnum-Eigenschaft Virtueller PC
- _NewEnum Eigenschaft Virtueller PC, IVMDVDDriveCollection-Schnittstelle
- IVMDVDDriveCollection-Schnittstelle Virtual PC , _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aeaca7f223d260e6a1bfcc6226088debf5650b87e397a63e2e3fe21430f85ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595744"
---
# <a name="ivmdvddrivecollection_newenum-property"></a>IVMDVDDriveCollection:: \_ NewEnum-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft einen Enumerator für die CD/DVD-Sammlung ab.

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



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>E \_ FAIL</dt> <dt>0x80004005</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection ist als bc86e297-e55f-4742-9614-ad11d3131f68 definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDriveCollection**](ivmdvddrivecollection.md)
</dt> </dl>

 

