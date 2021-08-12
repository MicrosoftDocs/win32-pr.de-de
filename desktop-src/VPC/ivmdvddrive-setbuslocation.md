---
title: IVMDVDDrive SetBusLocation-Methode (VPCCOMInterfaces.h)
description: Fügt das DVD-Laufwerk an den angegebenen Busspeicherort auf dem virtuellen Computer an.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- SetBusLocation-Methode Virtueller PC
- SetBusLocation-Methode Virtueller PC, IVMDVDDrive-Schnittstelle
- IVMDVDDrive-Schnittstelle Virtueller PC, SetBusLocation-Methode
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
ms.openlocfilehash: 593a42c21d1ed688185a7fe7123e972998859c010775a2cf4efd5f3bbbbaa98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595843"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>IVMDVDDrive::SetBusLocation-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Fügt das DVD-Laufwerk an den angegebenen Busspeicherort auf dem virtuellen Computer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*busNumber* \[ In\]
</dt> <dd>

Die Busnummer, an die dieses Laufwerk angefügt werden soll. Bei einem IDE-Bus würde diese Zahl beispielsweise darstellen, ob die primäre oder sekundäre Busnummer verwendet werden soll.

</dd> <dt>

*deviceNumber* \[ In\]
</dt> <dd>

Die Gerätenummer, an die dieses Laufwerk angefügt werden soll. In einem IDE-Bus würde diese Zahl beispielsweise darstellen, ob der primäre oder sekundäre Gerätestandort verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                 | Der angegebene Busstandort ist ungültig.<br/>                                                                                     |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>                       | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |
| <dl> <dt>**VM \_ E \_ VM MIT ODER \_ \_ \_ GESPEICHERTER**</dt> <dt>0XA004020B</dt> </dl> | Der Busspeicherort kann nicht festgelegt werden, während der virtuelle Computer ausgeführt wird oder sich in einem gespeicherten Zustand befindet.<br/>                                     |
| <dl> <dt>**VM \_ E \_ BUS \_ LOC \_ IN \_ USE**</dt> </dl>                                                                      | Ein anderes Gerät ist bereits an den angegebenen Busstandort angefügt.<br/>                                                            |
| <dl> <dt>**VM \_ \_ \_ E DRIVE INVALID**</dt> <dt>0xA0040502</dt> </dl>         | Das aktuelle Laufwerk konnte nicht initialisiert werden.<br/>                                                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | Die Änderungen konnten nicht in die Einstellungsdatei geschrieben werden, da der virtuelle Computer für dieses Laufwerk nicht bestimmt werden konnte.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

