---
title: IVMVirtualNetworkCollection _NewEnum-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft einen Enumerator für die Auflistung ab. | IVMVirtualNetworkCollection _NewEnum-Eigenschaft (VPCCOMInterfaces.h)
ms.assetid: 3ea01a88-72ec-4dc0-901f-e48092cf9251
keywords:
- _NewEnum-Eigenschaft Virtueller PC
- _NewEnum Eigenschaft Virtueller PC, IVMVirtualNetworkCollection-Schnittstelle
- IVMVirtualNetworkCollection-Schnittstelle Virtueller PC , _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection._NewEnum
- IVMVirtualNetworkCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b259f6734061db5df73f8533f3f173476699cd6177f918d1c5e4bf8b9d8518e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592557"
---
# <a name="ivmvirtualnetworkcollection_newenum-property"></a>IVMVirtualNetworkCollection:: \_ NewEnum-Eigenschaft

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
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection ist als 8ed680be-4242-4b2a-a21c-1982d8b0f675 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

