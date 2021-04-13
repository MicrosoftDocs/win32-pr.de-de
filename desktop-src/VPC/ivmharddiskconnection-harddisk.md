---
title: Eigenschaft ' ivmharddiskconnection Harddisk ' (vpccominterfaces. h)
description: Ruft ein Festplatten Objekt ab, das dieser Verbindung entspricht.
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- Festplatten Eigenschaft Virtual PC
- Festplatten Eigenschaft Virtual PC, ivmharddiskconnection-Schnittstelle
- Ivmharddiskconnection-Schnittstelle Virtual PC, Festplatten Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9baa365606b71b693dd841471d50a475a42677d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392012"
---
# <a name="ivmharddiskconnectionharddisk-property"></a>Ivmharddiskconnection:: Harddisk-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft ein Festplatten Objekt ab, das dieser Verbindung entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**ivmharddisk**](ivmharddisk.md) -Objekt, das die Festplatte beschreibt, die dieser Verbindung zugeordnet ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                       | Bedeutung                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                    |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>            | Der-Parameter ist **null** oder ungültig.<br/>                                                                                          |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>    | Die aktuelle Konfiguration der virtuellen Maschine ist ungültig.<br/>                                                                          |
| <dl> <dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt> </dl> | Der Busstandort für diese Verbindung wurde nicht ordnungsgemäß initialisiert, oder das Gerät an diesem Speicherort ist keine gültige Festplatte.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                |



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

 

