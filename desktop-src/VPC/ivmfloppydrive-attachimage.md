---
title: Ivmfloppydrive attachimage-Methode (vpccominterfaces. h)
description: Fügt ein Disketten Medienbild auf dem Host an das Diskettenlaufwerk der virtuellen Maschine an.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Attachimage-Methode Virtual PC
- Attachimage-Methode Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, attachimage-Methode
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
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949729"
---
# <a name="ivmfloppydriveattachimage-method"></a>Ivmfloppydrive:: attachimage-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt ein Disketten Medienbild auf dem Host an das Diskettenlaufwerk der virtuellen Maschine an.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mediaimagepath* \[ in\]
</dt> <dd>

Der vollständige Pfad zu dem Disketten Medienbild, das angefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                 | Der *mediaimagepath* -Parameter ist ungültig.<br/>                                                                                 |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Der-Parameter ist **null**.<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt> </dl>      | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.<br/>                                                               |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl> | Der durch den Parameter " *mediaimagepath* " angegebene Pfad ist zu lang. Der Pfad muss kleiner als der **Maximale \_ Pfad** (260) sein.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>    | Der *mediaimagepath* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>    | Der *mediaimagepath* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                            |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                            | Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.<br/>                                                  |
| <dl> <dt>**VM \_ E \_ - \_ Abbild Erfassung \_ fehlschlagen**</dt> <dt>0xa00400650</dt> </dl>                  | Die angegebene Bilddatei konnte nicht aufgezeichnet werden.<br/>                                                                              |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |



 

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

 

