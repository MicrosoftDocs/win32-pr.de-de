---
title: Ivmnetworkadapter-VirtualNetwork-Eigenschaft (vpccominterfaces. h)
description: Ruft das virtuelle Netzwerk ab, an das die Netzwerkschnittstelle angefügt ist.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork-Eigenschaft virtueller PC
- VirtualNetwork-Eigenschaft Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, VirtualNetwork-Eigenschaft
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
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040046"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a>Ivmnetworkadapter:: VirtualNetwork-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das virtuelle Netzwerk ab, an das die Netzwerkschnittstelle angefügt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Schnittstelle, die das virtuelle Netzwerk darstellt, an das diese virtuelle Netzwerkschnittstelle angefügt ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                  |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                            | Der-Parameter ist **null**.<br/>                                                     |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                                       | Diese Netzwerkschnittstelle ist nicht verbunden und nicht mit einem virtuellen Netzwerk verbunden.<br/> |
| <dl> <dt>VM \_ E \_ ungültige \_ virtuelle \_ Netzwerk- \_ ID</dt> <dt>0xa00400702</dt> </dl> | Diese Schnittstelle ist mit einem virtuellen Netzwerk mit einer ungültigen ID verbunden.<br/>           |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmnetworkadapter**](ivmnetworkadapter.md)
</dt> </dl>

 

