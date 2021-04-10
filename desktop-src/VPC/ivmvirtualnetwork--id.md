---
title: Ivmvirtualnetwork-_ID Methode (vpccominterfaces. h)
description: Ruft den internen Bezeichner des virtuellen Netzwerks ab.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID-Methode Virtual PC
- _ID-Methode Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, _ID-Methode
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040907"
---
# <a name="ivmvirtualnetwork_id-method"></a>Ivmvirtualnetwork:: \_ ID-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den internen Bezeichner des virtuellen Netzwerks ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualnetworkid* \[ vorgenommen\]
</dt> <dd>

Der Bezeichner des virtuellen Netzwerks. Der Bezeichner für das virtuelle Netzwerk Shared Networking (NAT) lautet 01010101010101010101010101010101.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nicht von Skriptsprachen verwendet werden.

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

 

