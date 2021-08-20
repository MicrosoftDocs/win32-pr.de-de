---
title: IVMVirtualNetwork HostAdapter-Eigenschaft (VPCCOMInterfaces.h)
description: Name des Adapters, mit dem das virtuelle Netzwerk verbunden ist.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- HostAdapter-Eigenschaft Virtueller PC
- HostAdapter-Eigenschaft Virtueller PC, IVMVirtualNetwork-Schnittstelle
- IVMVirtualNetwork-Schnittstelle Virtueller PC, HostAdapter-Eigenschaft
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
ms.openlocfilehash: 72db5d8349572b2bd3549c2ee54d20e994bdfe8aed6ba0fbe31875e04f6942f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122680"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>IVMVirtualNetwork::HostAdapter (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Namen des Adapters ab, mit dem das virtuelle Netzwerk verbunden ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des Hostadapters, mit dem das virtuelle Netzwerk verbunden ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                            | Bedeutung                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | Der Vorgang wurde durchgeführt.<br/>                                                                                                                              |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                 | Der Parameter ist **NULL.**<br/>                                                                                                                                 |
| <dl> <dt>VM \_ E \_ ADAPTER \_ NOT \_ FOUND</dt> <dt>0xA0040700</dt> </dl> | Der Ethernet-Hostadapter, mit dem dieses virtuelle Netzwerk verbunden war, ist nicht mehr verfügbar. Der Ethernet-Hostadapter wurde möglicherweise entfernt oder deaktiviert.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                          |



## <a name="remarks"></a>Hinweise

Der virtuelle Netzwerkadapter ermöglicht es einem virtuellen Netzwerk, mit externen Netzwerken zu sprechen. Normalerweise ist auf dem Hostcomputer ein Adapter pro Ethernet-Adapter installiert. Angenommen, ein Hostcomputer hat einen Adapter mit der Bezeichnung "10/100 ENET". Um eine virtuelle NIC mit dem Netzwerk zu verbinden, das an "10/100 ENET" angefügt ist, legen Sie die Eigenschaft **Netzwerkhostadapter** des virtuellen Netzwerks auf "10/100 ENET" fest, und verbinden Sie die virtuelle NIC mit diesem virtuellen Netzwerk.

Wenn die **HostAdapter-Eigenschaft** auf eine leere Zeichenfolge ("") festgelegt ist, ist der virtuelle NIC-Adapter mit dem Netzwerk "Internal Network" oder "Shared Networking (NAT)" verbunden. Virtuelle NICs, die an das Netzwerk "Internes Netzwerk" angefügt sind, haben keinen Zugriff auf externe Netzwerke auf dem Systemhost. Die virtuellen NICs, die an dieses virtuelle Netzwerk angefügt sind, können jedoch weiterhin miteinander kommunizieren.

Auf die vollständige Liste der Adapter kann über die [**IVMHostInfo::NetworkAdapters-Eigenschaft zugegriffen**](ivmhostinfo-networkadapters.md) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

