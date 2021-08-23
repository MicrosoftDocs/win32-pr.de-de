---
title: IVMDVDDrive ReleaseHostDrive-Methode (VPCCOMInterfaces.h)
description: Gibt ein aufgezeichnetes Hostlaufwerk vom DVD-Laufwerk frei.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- ReleaseHostDrive-Methode Virtueller PC
- ReleaseHostDrive-Methode Virtueller PC, IVMDVDDrive-Schnittstelle
- IVMDVDDrive-Schnittstelle Virtueller PC, ReleaseHostDrive-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865b9aa54304d8ddacacf048825d6c9767347f341d31524cbd4dd60d7060ae4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136803"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>IVMDVDDrive::ReleaseHostDrive-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt ein aufgezeichnetes Hostlaufwerk vom DVD-Laufwerk frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                         | Beschreibung                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                               | Der Vorgang wurde durchgeführt.<br/>                                      |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                  |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>         | Der virtuelle Computer wurde nicht gefunden.<br/>                            |
| <dl> <dt>**VM \_ E \_ MEDIA \_ WRONG \_ TYPE**</dt> <dt>0xA00400728</dt> </dl> | Das derzeit erfasste Medium ist kein Hostdatenträgerlaufwerk.<br/>             |
| <dl> <dt>**VM \_ E \_ LAUFWERK \_ UNGÜLTIGE**</dt> <dt>0xA0040502</dt> </dl>      | Das Laufwerk konnte aufgrund eines ungültigen Busspeicherorts nicht initialisiert werden.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>         | Ein unerwarteter Fehler ist aufgetreten.<br/>                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

