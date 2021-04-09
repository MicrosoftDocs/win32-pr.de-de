---
title: Ivmvirtualnetwork-Namenseigenschaft (vpccominterfaces. h)
description: Eindeutiger Name der virtuellen Netzwerk Instanz.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Name-Eigenschaft virtueller PC
- Name-Eigenschaft Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957019"
---
# <a name="ivmvirtualnetworkname-property"></a>Ivmvirtualnetwork:: Name-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den eindeutigen Namen der virtuellen Netzwerk Instanz ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a>Eigenschaftswert

Den Namen des virtuellen Netzwerks.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                                |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>                                                   |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Es ist ein unerwarteter Fehler aufgetreten, oder die virtuelle Netzwerk Instanz ist unbekannt.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei Namen von virtuellen Netzwerken wird die Groß-/Kleinschreibung nicht beachtet, z. b. "mynetwork" und "mynetwork" beziehen sich auf dasselbe virtuelle Netzwerk.

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

 

