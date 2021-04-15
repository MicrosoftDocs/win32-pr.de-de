---
title: Ivmvirtualmachine Network Adapters-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von NICs ab, die an den virtuellen Computer angefügt sind.
ms.assetid: 3877edf7-92b8-43c9-8229-a198a07079a4
keywords:
- NetworkAdapters-Eigenschaft virtueller PC
- NetworkAdapters-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Network Adapters (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.NetworkAdapters
- IVMVirtualMachine.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ce6e1fa22eca40c037eebb48803fe182810c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391981"
---
# <a name="ivmvirtualmachinenetworkadapters-property"></a>Ivmvirtualmachine:: NetworkAdapters (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft eine Aufzähl Bare Auflistung von NICs ab, die an den virtuellen Computer angefügt sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkAdapterCollection
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md) -Objekt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

