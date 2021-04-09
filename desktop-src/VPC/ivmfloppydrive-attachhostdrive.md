---
title: Ivmfloppydrive AttachHostDrive-Methode (vpccominterfaces. h)
description: Fügt ein physisches Laufwerk auf dem Host an das Diskettenlaufwerk auf dem virtuellen Computer an.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- AttachHostDrive-Methode Virtual PC
- AttachHostDrive-Methode Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, AttachHostDrive-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040743"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a>Ivmfloppydrive:: AttachHostDrive-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt ein physisches Laufwerk auf dem Host an das Diskettenlaufwerk auf dem virtuellen Computer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Laufwerk *Etter* \[ in\]
</dt> <dd>

Der Laufwerk Buchstabe des physischen Disketten Laufwerks auf dem Host Computer, an das angefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                                                     |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>      | Der *DriveLetter* -Parameter ist **null**, ist kein gültiges Diskettenlaufwerk, oder der angegebene Pfad ist leer.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.<br/>                       |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmfloppydrive**](ivmfloppydrive.md)
</dt> </dl>

 

