---
title: IVMVirtualNetworkCollection-Elementeigenschaft (VPCCOMInterfaces.h)
description: IVMVirtualNetwork-Objekt, das dem angegebenen Index entspricht.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Elementeigenschaft Virtueller PC
- Item-Eigenschaft Virtueller PC, IVMVirtualNetworkCollection-Schnittstelle
- IVMVirtualNetworkCollection-Schnittstelle Virtueller PC , Item-Eigenschaft
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
ms.openlocfilehash: 9133efe93ef5feeb9d8e15862a9d25ea6b14c0de08dd35faa46abc4589fcb21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592318"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a>IVMVirtualNetworkCollection::Item-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft das [**IVMVirtualNetwork-Objekt**](ivmvirtualnetwork.md) ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**IVMVirtualNetwork-Objekt.**](ivmvirtualnetwork.md)

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                                      |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der *parameter virtualNetwork* ist **NULL.**<br/>                                        |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                  |



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

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> <dt>

[**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

