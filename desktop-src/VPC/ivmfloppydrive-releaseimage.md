---
title: Ivmfloppydrive ReleaseImage-Methode (vpccominterfaces. h)
description: Gibt ein Disketten Medienbild auf dem Host vom Diskettenlaufwerk aus.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- ReleaseImage-Methode Virtual PC
- ReleaseImage-Methode Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, ReleaseImage-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece899bbb615fc2d54a3cbdc86193e743168ef23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739768"
---
# <a name="ivmfloppydrivereleaseimage-method"></a>Ivmfloppydrive:: ReleaseImage-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt ein Disketten Medienbild auf dem Host vom Diskettenlaufwerk aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                          | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | Der Vorgang wurde durchgeführt.<br/>                                               |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>          | Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.<br/> |
| <dl> <dt>**VM \_ E \_ Medien \_ falscher \_ Typ**</dt> <dt>0xa00400728</dt> </dl>  | Das an dieses Diskettenlaufwerk angefügte Medium ist kein Disketten Image.<br/>         |
| <dl> <dt>**VM \_ E \_ kein \_ Medium \_ erfasst**</dt> <dt>0xa00400652</dt> </dl> | An dieses Diskettenlaufwerk sind keine Medien angefügt.<br/>                            |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                           |



 

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

 

