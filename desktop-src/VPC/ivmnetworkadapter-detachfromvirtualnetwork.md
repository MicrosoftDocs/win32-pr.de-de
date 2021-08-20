---
title: IVMNetworkAdapter DetachFromVirtualNetwork-Methode (VPCCOMInterfaces.h)
description: Trennt die Netzwerkschnittstelle vom virtuellen Netzwerk.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- DetachFromVirtualNetwork-Methode Virtueller PC
- DetachFromVirtualNetwork-Methode Virtual PC, IVMNetworkAdapter-Schnittstelle
- IVMNetworkAdapter-Schnittstelle Virtueller PC, DetachFromVirtualNetwork-Methode
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb97c0b2bad30cb05302b67b1b5d0569b13b4c007b79163f1ce63750b512179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938471"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a>IVMNetworkAdapter::D etachFromVirtualNetwork-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Trennt die Netzwerkschnittstelle vom virtuellen Netzwerk.

## <a name="syntax"></a>Syntax


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | Beschreibung                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter ist als e32e4165-22b8-4dc0-8d57-850171ae207a definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

