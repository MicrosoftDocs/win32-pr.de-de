---
title: Ivmvirtualnetwork Network Adapters-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von NICs ab, die an das virtuelle Netzwerk angefügt sind.
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- NetworkAdapters-Eigenschaft virtueller PC
- NetworkAdapters-Eigenschaft Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, Netzwerkadaptern (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba86f649744eeb34139c65de9aa4523ddc74d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339594"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a>Ivmvirtualnetwork:: NetworkAdapters (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft eine Aufzähl Bare Auflistung von NICs ab, die an das virtuelle Netzwerk angefügt sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine neue [**ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md) , die die virtuellen NICs enthält, die mit diesem virtuellen Netzwerk verbunden sind.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualnetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualnetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

