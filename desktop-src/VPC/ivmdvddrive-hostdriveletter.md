---
title: Ivmdvddrive-hostdriveletter-Eigenschaft (vpccominterfaces. h)
description: Der Buchstabe des Host Laufwerks, das für dieses Gerät festgelegt ist.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Hostdriveletter-Eigenschaft virtueller PC
- Hostdriveletter-Eigenschaft Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, hostdriveletter (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741096"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>Ivmdvddrive:: hostdriveletter (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Buchstaben des Host Laufwerks ab, das für dieses Gerät festgelegt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Laufwerk Buchstabe.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                            | Bedeutung                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | Der Vorgang wurde durchgeführt.<br/>                             |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                 | Der-Parameter ist **null**.<br/>                                |
| <dl> <dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                         |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>         | Der virtuelle Computer wurde nicht gefunden.<br/>                   |
| <dl> <dt>VM \_ E \_ Medien \_ falscher \_ Typ</dt> <dt>0xa00400728</dt> </dl> | Die von diesem DVD-Laufwerk erfassten Medien sind kein Host Laufwerk.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>         | Ein unerwarteter Fehler ist aufgetreten.<br/>                         |



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

 

