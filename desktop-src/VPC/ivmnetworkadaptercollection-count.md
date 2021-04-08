---
title: Ivmnetworkadaptercollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der Netzwerkschnittstellen in dieser Auflistung ab.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmnetworkadaptercollection-Schnittstelle
- Ivmnetworkadaptercollection-Schnittstelle Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102806"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a>Ivmnetworkadaptercollection:: count (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Anzahl der Netzwerkschnittstellen in dieser Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der Netzwerkschnittstellen.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ ivmnetworkadaptercollection ist als ebaeafe9-EBCD-47cf-866e-ad87d735e479 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

