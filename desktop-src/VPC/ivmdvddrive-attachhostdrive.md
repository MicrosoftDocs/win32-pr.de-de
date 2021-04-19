---
title: Ivmdvddrive AttachHostDrive-Methode (vpccominterfaces. h)
description: Fügt ein Host Laufwerk an das DVD-Laufwerk innerhalb der virtuellen Maschine an.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- AttachHostDrive-Methode Virtual PC
- AttachHostDrive-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, AttachHostDrive-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342876"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>Ivmdvddrive:: AttachHostDrive-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt ein Host Laufwerk an das DVD-Laufwerk innerhalb der virtuellen Maschine an.

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

Der Buchstabe des Host Laufwerks, das angefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                             |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>         | Es wurde kein Laufwerk Buchstabe angegeben, oder der angegebene Laufwerk Buchstabe ist ungültig.<br/>                                                                                                  |
| <dl> <dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen </dl>               | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                         |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>    | Der virtuelle Computer wurde nicht gefunden.<br/>                                                                                                                                   |
| <dl> <dt>**VM \_ E- \_ Laufwerk \_ in \_ Verwendung**</dt> von <dt>0xa0040727</dt> </dl> | Ein Host-DVD-Laufwerk oder ISO-Abbild ist bereits an dieses Laufwerk innerhalb des virtuellen Computers angefügt, oder das angegebene Host Laufwerk wird bereits in einer anderen virtuellen Maschine verwendet.<br/> |
| <dl> <dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt> </dl> | Der Busort dieses Laufwerks ist ungültig, oder das Laufwerk scheint kein gültiges DVD-Laufwerk zu sein.<br/>                                                                         |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                         |



 

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

 

