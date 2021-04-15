---
title: Ivmharddiskconnection busnumber-Eigenschaft (vpccominterfaces. h)
description: Ruft die Busnummer ab, an die das Laufwerks Bild angefügt wird.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- Busnumber-Eigenschaft virtueller PC
- Busnumber-Eigenschaft Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection-Schnittstelle Virtual PC, busnumber-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477991"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a>Ivmharddiskconnection:: busnumber (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Busnummer ab, an die das Laufwerks Bild angefügt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Busnummer, die dieser Verbindung entspricht.

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

 

