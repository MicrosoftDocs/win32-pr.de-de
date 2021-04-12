---
title: Ivmvirtualnetworkcollection-_NewEnum-Eigenschaft (vpccominterfaces. h)
description: Ruft einen Enumerator für die Auflistung ab. | Ivmvirtualnetworkcollection-_NewEnum-Eigenschaft (vpccominterfaces. h)
ms.assetid: 3ea01a88-72ec-4dc0-901f-e48092cf9251
keywords:
- Virtual PC für _NewEnum-Eigenschaft
- _NewEnum-Eigenschaft Virtual PC, ivmvirtualnetworkcollection-Schnittstelle
- Ivmvirtualnetworkcollection Interface Virtual PC, _NewEnum-Eigenschaft
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
ms.openlocfilehash: b50a279e3f160a79f143a7516e29c0dbc3eccdf4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219390"
---
# <a name="ivmvirtualnetworkcollection_newenum-property"></a>Ivmvirtualnetworkcollection:: \_ netwenum-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft einen Enumerator für die Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Eigenschaftswert

Der [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerator.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/> |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>    |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ ivmvirtualnetworkcollection ist als 8ed680be-4242-4b2a-A21C-1982d8b0f. definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualnetworkcollection**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

