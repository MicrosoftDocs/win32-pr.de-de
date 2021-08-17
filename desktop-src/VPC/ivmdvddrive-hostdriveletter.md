---
title: IVMDVDDrive HostDriveLetter-Eigenschaft (VPCCOMInterfaces.h)
description: Der Buchstabe des für dieses Gerät festgelegten Hostlaufwerks.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- HostDriveLetter-Eigenschaft Virtueller PC
- HostDriveLetter-Eigenschaft Virtueller PC, IVMDVDDrive-Schnittstelle
- IVMDVDDrive-Schnittstelle Virtueller PC, HostDriveLetter-Eigenschaft
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
ms.openlocfilehash: 1eb9105ec970331a755881d7f5b1425cf43c58f5267f5970042ce64b458070a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056868"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>IVMDVDDrive::HostDriveLetter (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Buchstaben des Für dieses Gerät festgelegten Hostlaufwerks ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Laufwerkbuchstaben.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                            | Bedeutung                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | Der Vorgang wurde durchgeführt.<br/>                             |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                 | Der Parameter ist **NULL.**<br/>                                |
| <dl> <dt>E \_ FEHLER</dt> <dt>0x80004005</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                         |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>         | Der virtuelle Computer wurde nicht gefunden.<br/>                   |
| <dl> <dt>VM \_ E \_ MEDIA WRONG TYPE \_ \_ 0XA00400728</dt> <dt></dt> </dl> | Das von diesem DVD-Laufwerk erfasste Medium ist kein Hostlaufwerk.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Ein unerwarteter Fehler ist aufgetreten.<br/>                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

