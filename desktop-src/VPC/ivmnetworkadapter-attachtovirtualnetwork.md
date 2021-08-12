---
title: IVMNetworkAdapter AttachToVirtualNetwork-Methode (VPCCOMInterfaces.h)
description: Angefügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- AttachToVirtualNetwork-Methode Virtueller PC
- AttachToVirtualNetwork-Methode Virtual PC, IVMNetworkAdapter-Schnittstelle
- IVMNetworkAdapter-Schnittstelle Virtueller PC, AttachToVirtualNetwork-Methode
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
ms.openlocfilehash: b03bf8bd0bcde6ba0353ce62e227c100a17ed1df0b2267ad54cd127c95c5836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593228"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>IVMNetworkAdapter::AttachToVirtualNetwork-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Angefügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualNetwork* \[ In\]
</dt> <dd>

Das virtuelle Netzwerk, mit dem diese virtuelle NIC verbunden wird. Siehe [**IVMVirtualNetwork**](ivmvirtualnetwork.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                       | Der Vorgang wurde durchgeführt.<br/>                           |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                  | Der Parameter ist **NULL.**<br/>                              |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                               | Der -Parameter enthält kein gültiges virtuelles Netzwerk.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0X80070005</dt> </dl> | Der Zugriff auf das angeforderte virtuelle Netzwerk wurde verweigert.<br/>     |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | Der virtuelle Computer ist ungültig oder nicht mehr vorhanden.<br/>     |
| <dl> <dt>**VM \_ E \_ UNGÜLTIGE ID DES \_ \_ VIRTUELLEN \_ NETZWERKS**</dt> </dl>                                                                        | Der -Parameter ist kein vorhandenes virtuelles Netzwerk.<br/>       |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> </dl>                                                                                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter ist als e32e4165-22b8-4dc0-8d57-850171ae207a definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

