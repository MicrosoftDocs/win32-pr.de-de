---
title: Ivmharddiskconnection-setbusloationmethode (vpccominterfaces. h)
description: Legt den Busspeicherort fest, an den diese Festplatte angefügt ist.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Setbusloationmethod-Methode Virtual PC
- Setbusloationmethod-Methode Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection-Schnittstelle Virtual PC, setbusloationmethod
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340337"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a>Ivmharddiskconnection:: setbusloations-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Legt den Busspeicherort fest, an den diese Festplatte angefügt ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vmbusnumber* \[ in\]
</dt> <dd>

Die zu verwendende Busnummer.

</dd> <dt>

*vmdevicenumschlag* \[ in\]
</dt> <dd>

Die zu verwendende Gerätenummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                               | BESCHREIBUNG                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | Der Vorgang wurde durchgeführt.<br/>                                                                    |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                    | Der angegebene Busspeicherort ist ungültig.<br/>                                                         |
| <dl> <dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert </dl>    | Der Busstandort konnte nicht festgelegt werden, weil sich der virtuelle Computer in einem laufenden oder gespeicherten Zustand befindet.<br/>    |
| <dl> <dt>**VM \_ E \_ Drive \_ Bus \_ loc \_ \_ verwendet**</dt> <dt>0xa00400503</dt> </dl> | Der Busstandort konnte nicht festgelegt werden, da zurzeit ein anderes Gerät an diesen Speicherort angeschlossen ist.<br/> |
| <dl> <dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt> </dl>            | Das aktuelle Laufwerk ist ungültig.<br/>                                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>               | Der aktuelle virtuelle Computer ist ungültig.<br/>                                                        |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>               | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmharddiskconnection ist als aefa36a5-463a-46AE-9e6c-a1fb4e12e671 definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmharddiskconnection**](ivmharddiskconnection.md)
</dt> </dl>

 

