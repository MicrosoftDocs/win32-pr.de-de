---
title: Ivmvirtualnetworkcollection-Element Eigenschaft (vpccominterfaces. h)
description: Ivmvirtualnetwork-Objekt, das dem angegebenen Index entspricht.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmvirtualnetworkcollection-Schnittstelle
- Ivmvirtualnetworkcollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040700"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a>Ivmvirtualnetworkcollection:: Item (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                                      |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der *VirtualNetwork* -Parameter ist **null**.<br/>                                        |
| <dl> <dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                  |



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

[**Ivmvirtualnetwork**](ivmvirtualnetwork.md)
</dt> <dt>

[**Ivmvirtualnetworkcollection**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

