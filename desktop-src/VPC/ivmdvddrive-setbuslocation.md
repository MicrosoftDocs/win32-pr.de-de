---
title: Ivmdvddrive-setbusloationmethode (vpccominterfaces. h)
description: Fügt das DVD-Laufwerk an die angegebene busposition auf dem virtuellen Computer an.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Setbusloationmethod-Methode Virtual PC
- Setbusloationmethod-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, setbuslokation-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339331"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>Ivmdvddrive:: setbusloation-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt das DVD-Laufwerk an die angegebene busposition auf dem virtuellen Computer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Busnummer* \[ in\]
</dt> <dd>

Die Busnummer, an die dieses Laufwerk angefügt werden soll. Beispielsweise würde diese Zahl auf einem IDE-Bus angeben, ob die primäre oder sekundäre Busnummer verwendet werden soll.

</dd> <dt>

*devicengegen ber* \[ in\]
</dt> <dd>

Die Gerätenummer, an die dieses Laufwerk angefügt werden soll. Beispielsweise würde diese Zahl auf einem IDE-Bus angeben, ob der primäre oder sekundäre Geräte Speicherort verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                 | Der angegebene Busspeicherort ist ungültig.<br/>                                                                                     |
| <dl> <dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen </dl>                       | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |
| <dl> <dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert </dl> | Der Busstandort kann nicht festgelegt werden, während der virtuelle Computer ausgeführt wird oder sich in einem gespeicherten Zustand befindet.<br/>                                     |
| <dl> <dt>**\_verwendende VM-E- \_ Bus \_ \_ \_**</dt> </dl>                                                                      | Ein anderes Gerät ist bereits an den angegebenen Busstandort angefügt.<br/>                                                            |
| <dl> <dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt> </dl>         | Das aktuelle Laufwerk konnte nicht initialisiert werden.<br/>                                                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>            | Die Änderungen konnten nicht in die Einstellungsdatei geschrieben werden, da der virtuelle Computer für dieses Laufwerk nicht bestimmt werden konnte.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdvddrive**](ivmdvddrive.md)
</dt> </dl>

 

