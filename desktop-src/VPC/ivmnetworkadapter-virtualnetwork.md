---
title: IVMNetworkAdapter VirtualNetwork-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft das virtuelle Netzwerk ab, an das die Netzwerkschnittstelle angefügt ist.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork-Eigenschaft Virtueller PC
- VirtualNetwork-Eigenschaft Virtual PC, IVMNetworkAdapter-Schnittstelle
- IVMNetworkAdapter-Schnittstelle Virtueller PC, VirtualNetwork-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1bc3a3d58553d403f5e0ca6a8decbcbd3369b48450e9ec190b2f42f83de57e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136613"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a>IVMNetworkAdapter::VirtualNetwork-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft das virtuelle Netzwerk ab, an das die Netzwerkschnittstelle angefügt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**IVMVirtualNetwork-Schnittstelle,**](ivmvirtualnetwork.md) die das virtuelle Netzwerk darstellt, an das diese virtuelle Netzwerkschnittstelle angefügt ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                  |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                            | Der Parameter ist **NULL.**<br/>                                                     |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Diese Netzwerkschnittstelle ist nicht angeschlossen und nicht mit einem virtuellen Netzwerk verbunden.<br/> |
| <dl> <dt>VM \_ E \_ \_ UNGÜLTIGE \_ ID DES \_ VIRTUELLEN</dt> <dt>NETZWERKS 0XA00400702</dt> </dl> | Diese Schnittstelle ist mit einem virtuellen Netzwerk mit einer ungültigen ID verbunden.<br/>           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter ist als e32e4165-22b8-4dc0-8d57-850171ae207a definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

