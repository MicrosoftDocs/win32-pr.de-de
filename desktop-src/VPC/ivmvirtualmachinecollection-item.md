---
title: Ivmvirtualmachinecollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das virtuelle Maschinen Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmvirtualmachinecollection-Schnittstelle
- Ivmvirtualmachinecollection Interface Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040042"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a>Ivmvirtualmachinecollection:: Item (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das virtuelle Maschinen Objekt ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt. <br/>                                                      |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der *virtualmachine* -Parameter ist **null**. <br/>                                        |
| <dl> <dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung. <br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ ivmvirtualmachinecollection ist als 59F 31786-2a3d-4sbf-9896-d85338ca0da1 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> <dt>

[**Ivmvirtualmachinecollection**](ivmvirtualmachinecollection.md)
</dt> </dl>

 

