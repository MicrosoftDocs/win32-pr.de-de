---
title: IVMFloppyDrive AttachImage-Methode (VPCCOMInterfaces.h)
description: Angefügt ein Diskettenmedienimage auf dem Host an das Diskettenlaufwerk des virtuellen Computers.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- 'AttachImage-Methode : Virtueller PC'
- AttachImage-Methode Virtual PC, IVMFloppyDrive-Schnittstelle
- IVMFloppyDrive-Schnittstelle Virtueller PC, AttachImage-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21af305d0e7441fc931765795bb4e5d0785a211af6806ee80fd679d6f487b218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595714"
---
# <a name="ivmfloppydriveattachimage-method"></a>IVMFloppyDrive::AttachImage-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Angefügt ein Diskettenmedienimage auf dem Host an das Diskettenlaufwerk des virtuellen Computers.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mediaImagePath* \[ In\]
</dt> <dd>

Der vollständige Pfad zum Diskettenmedienbild, das angefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                                 | Der *mediaImagePath-Parameter* ist ungültig.<br/>                                                                                 |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                    | Der Parameter ist **NULL.**<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | Zum Abschließen dieser Anforderung ist nicht genügend Arbeitsspeicher verfügbar.<br/>                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der durch den *mediaImagePath-Parameter angegebene Pfad* ist zu lang. Der Pfad muss kleiner als **MAX \_ PATH** -Zeichen (260) sein.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *mediaImagePath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Der *mediaImagePath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                            |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.<br/>                                                  |
| <dl> <dt>**VM \_ E \_ IMAGE CAPTURE FAIL \_ \_ 0XA00400650**</dt> <dt></dt> </dl>                  | Die angegebene Bilddatei konnte nicht erfasst werden.<br/>                                                                              |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive ist als 661abee6-112a-4ed9-fsf-3c874969f10e definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

