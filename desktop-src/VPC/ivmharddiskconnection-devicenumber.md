---
title: Ivmharddiskconnection devicenenumber-Eigenschaft (vpccominterfaces. h)
description: Ruft die Gerätenummer ab, an die das Laufwerks Image angefügt wird.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- Devicenenber-Eigenschaft virtueller PC
- Devicenenber-Eigenschaft Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection Interface Virtual PC, devicenumschlag-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105807"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a>Ivmharddiskconnection::D-Eigenschaft ' evicenenber '

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Gerätenummer ab, an die das Laufwerks Image angefügt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Gerätenummer, die dieser Verbindung entspricht.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                       | Bedeutung                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | Der Vorgang wurde durchgeführt.<br/>                                           |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>            | Der-Parameter ist **null** oder ungültig.<br/>                                 |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>    | Die aktuelle Konfiguration der virtuellen Maschine ist ungültig.<br/>                 |
| <dl> <dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt> </dl> | Der Busstandort für diese Verbindung wurde nicht ordnungsgemäß initialisiert.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                       |



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

 

