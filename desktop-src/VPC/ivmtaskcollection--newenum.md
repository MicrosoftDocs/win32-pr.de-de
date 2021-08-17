---
title: IVMTaskCollection_NewEnum eigenschaft (VPCCOMInterfaces.h)
description: Ruft einen Enumerator für die Auflistung ab. | IVMTaskCollection_NewEnum eigenschaft (VPCCOMInterfaces.h)
ms.assetid: 15c36bdb-5d26-4f67-aa7e-73b9bde2aa22
keywords:
- _NewEnum-Eigenschaft Virtueller PC
- _NewEnum Virtual PC, IVMTaskCollection-Schnittstelle
- IVMTaskCollection-Schnittstelle Virtual PC , _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTaskCollection._NewEnum
- IVMTaskCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba76d1bf2bab1803521b66e150e049c871a4901f4ca64c739d7ed86542cb2b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752630"
---
# <a name="ivmtaskcollection_newenum-property"></a>IVMTaskCollection:: \_ NewEnum-Eigenschaft

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
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection ist als 5c4387c8-0e8b-4b97-8058-84679adf4c40 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMTaskCollection**](ivmtaskcollection.md)
</dt> </dl>

 

