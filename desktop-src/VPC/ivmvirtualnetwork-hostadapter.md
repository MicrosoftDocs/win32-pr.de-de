---
title: Ivmvirtualnetwork-hostanapter-Eigenschaft (vpccominterfaces. h)
description: Der Name des Adapters, mit dem das virtuelle Netzwerk verbunden ist.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Host Host Eigenschaft Virtual PC
- Host Host Eigenschaft Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, Host-apter (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040865"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>Ivmvirtualnetwork:: hostapter (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Namen des Adapters ab, mit dem das virtuelle Netzwerk verbunden ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des Host Adapters, mit dem das virtuelle Netzwerk verbunden ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                            | Bedeutung                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | Der Vorgang wurde durchgeführt.<br/>                                                                                                                              |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                 | Der-Parameter ist **null**.<br/>                                                                                                                                 |
| <dl> <dt>VM \_ E- \_ Adapter \_ nicht \_ gefunden</dt> <dt>0xa0040700</dt> </dl> | Der Host-Ethernet-Adapter, mit dem dieses virtuelle Netzwerk verbunden war, ist nicht mehr verfügbar. Der hostethernet-Adapter wurde möglicherweise entfernt oder deaktiviert.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>         | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                          |



## <a name="remarks"></a>Bemerkungen

Mit dem virtuellen Netzwerkadapter kann ein virtuelles Netzwerk mit externen Netzwerken kommunizieren. Normalerweise ist ein Adapter pro Ethernet-Adapter auf dem Host Computer installiert. Nehmen wir beispielsweise an, dass ein Host Computer über einen Adapter mit der Bezeichnung "10/100 ENET" verfügt. Wenn Sie eine virtuelle NIC mit dem Netzwerk verbinden möchten, das mit "10/100 ENET" verbunden ist, legen Sie **die Eigenschaft "** Network Host" des virtuellen Netzwerks auf "10/100 ENET" fest, und verbinden Sie die virtuelle NIC mit diesem virtuellen Netzwerk.

Wenn die **Hostadapter** -Eigenschaft auf eine leere Zeichenfolge ("") festgelegt ist, wird der virtuelle NIC-Adapter mit dem Netzwerk "Internal Network" oder "Shared Networking (NAT)" verbunden. Virtuelle NICs, die an das Netzwerk "internes Netzwerk" angefügt werden, haben keinen Zugriff auf externe Netzwerke auf dem System Host. Die virtuellen NICs, die mit diesem virtuellen Netzwerk verbunden sind, können jedoch immer noch miteinander kommunizieren.

Auf die gesamte Liste der Adapter kann über die [**ivmhostinfo:: NetworkAdapters**](ivmhostinfo-networkadapters.md) -Eigenschaft zugegriffen werden.

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

 

