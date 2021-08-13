---
title: IVMFloppyDrive ReleaseHostDrive-Methode (VPCCOMInterfaces.h)
description: Gibt ein physisches Laufwerk auf dem Host vom Diskettenlaufwerk frei.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- ReleaseHostDrive-Methode Virtueller PC
- ReleaseHostDrive-Methode Virtueller PC, IVMFloppyDrive-Schnittstelle
- IVMFloppyDrive-Schnittstelle Virtueller PC, ReleaseHostDrive-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44202754528483f88ab045b848e83a6a41a318b1e1ffed6122c2a2ac971237c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594846"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a>IVMFloppyDrive::ReleaseHostDrive-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt ein physisches Laufwerk auf dem Host vom Diskettenlaufwerk frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                          | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | Der Vorgang wurde durchgeführt.<br/>                                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>          | Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.<br/> |
| <dl> <dt>**VM \_ E \_ MEDIA \_ WRONG \_ TYPE**</dt> <dt>0xA00400728</dt> </dl>  | Das an dieses Diskettenlaufwerk angefügte Medium ist kein physisches Diskettenlaufwerk.<br/>     |
| <dl> <dt>**VM \_ E \_ NO \_ MEDIA \_ CAPTURED**</dt> <dt>0xA00400652</dt> </dl> | An dieses Diskettenlaufwerk sind keine Medien angefügt.<br/>                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive ist als 661abee6-112a-4ed9-wadf-3c874969f10e definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

