---
title: IVMNetworkAdapterCollection_NewEnum eigenschaft (VPCCOMInterfaces.h)
description: Ruft einen Enumerator für die Auflistung ab. | IVMNetworkAdapterCollection _NewEnum -Eigenschaft (VPCCOMInterfaces.h)
ms.assetid: 9b970fc6-f8a3-4a16-9d59-789a59a99b68
keywords:
- _NewEnum-Eigenschaft Virtueller PC
- _NewEnum Virtual PC, IVMNetworkAdapterCollection-Schnittstelle
- IVMNetworkAdapterCollection-Schnittstelle Virtueller PC , _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection._NewEnum
- IVMNetworkAdapterCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05924b793d281cc190eed434c70efa37f1a930e905751973a6b0285920e1aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007090"
---
# <a name="ivmnetworkadaptercollection_newenum-property"></a>IVMNetworkAdapterCollection:: \_ NewEnum-Eigenschaft

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
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection ist definiert als solleneafe9-ebcd-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

