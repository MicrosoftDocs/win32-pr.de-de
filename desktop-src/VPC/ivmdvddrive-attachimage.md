---
title: Ivmdvddrive attachimage-Methode (vpccominterfaces. h)
description: Fügt ein ISO-Abbild an das DVD-Laufwerk innerhalb des virtuellen Computers an.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Attachimage-Methode Virtual PC
- Attachimage-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, attachimage-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392158"
---
# <a name="ivmdvddriveattachimage-method"></a>Ivmdvddrive:: attachimage-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt ein ISO-Abbild an das DVD-Laufwerk innerhalb des virtuellen Computers (VM) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ImagePath* \[ in\]
</dt> <dd>

Der vollständige Pfad zu dem ISO-Abbild, das angefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | Der Vorgang wurde durchgeführt.<br/>                                                                     |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>         | Der *ImagePath* -Parameter ist ein Verzeichnis.<br/>                                                         |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>            | Der *ImagePath* -Parameter ist **null**.<br/>                                                            |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>    | Die VM wurde nicht gefunden.<br/>                                                                        |
| <dl> <dt>**VM \_ E- \_ Laufwerk \_ in \_ Verwendung**</dt> von <dt>0xa0040727</dt> </dl> | Ein Host-DVD-Laufwerk oder ein ISO-Abbild ist bereits an dieses Laufwerk angefügt.<br/>                                  |
| <dl> <dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt> </dl> | Der Busort dieses Laufwerks ist ungültig, oder das Laufwerk scheint kein gültiges DVD-Laufwerk zu sein.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                 |



 

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

 

