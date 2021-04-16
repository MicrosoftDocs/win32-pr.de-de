---
title: Ivmnetworkadapter attachdevirtualnetwork-Methode (vpccominterfaces. h)
description: Fügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk an.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Attachdevirtualnetwork-Methode Virtual PC
- Attachdevirtualnetwork-Methode Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, attachdevirtualnetwork-Methode
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477187"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>Ivmnetworkadapter:: attachdevirtualnetwork-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk an.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VirtualNetwork* \[ in\]
</dt> <dd>

Das virtuelle Netzwerk, mit dem diese virtuelle NIC verbunden wird. Siehe [**ivmvirtualnetwork**](ivmvirtualnetwork.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                       | Der Vorgang wurde durchgeführt.<br/>                           |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                  | Der-Parameter ist **null**.<br/>                              |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                               | Der-Parameter enthält kein gültiges virtuelles Netzwerk.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt> </dl> | Der Zugriff auf das angeforderte virtuelle Netzwerk wurde verweigert.<br/>     |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                          | Der virtuelle Computer ist ungültig oder nicht mehr vorhanden.<br/>     |
| <dl> <dt>**VM \_ E \_ ungültige \_ virtuelle \_ Netzwerk- \_ ID**</dt> </dl>                                                                        | Der-Parameter ist kein vorhandenes virtuelles Netzwerk.<br/>       |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> </dl>                                                                                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                       |



 

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

 

