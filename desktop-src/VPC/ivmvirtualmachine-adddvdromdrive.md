---
title: Ivmvirtualmachine AddDVDROMDrive-Methode (vpccominterfaces. h)
description: Fügt ein neues CD-oder DVD-Laufwerk zum virtuellen Computer hinzu.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVDROMDrive-Methode Virtual PC
- AddDVDROMDrive-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, AddDVDROMDrive-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338548"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>Ivmvirtualmachine:: AddDVDROMDrive-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt ein neues CD-oder DVD-Laufwerk zum virtuellen Computer hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Busnummer* \[ in\]
</dt> <dd>

Der Bus, an den das Laufwerk angefügt wird.



| Wert                                                                        | Bedeutung                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Das Laufwerk wird an den ersten Bus angefügt.<br/>  |
| <dl> <dt>1</dt> </dl> | Das Laufwerk wird an den zweiten Bus angefügt.<br/> |



 

</dd> <dt>

*devicengegen ber* \[ in\]
</dt> <dd>

Das Gerät, an das das Laufwerk angefügt wird.



| Wert                                                                        | Bedeutung                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Das Laufwerk wird an das erste Gerät auf dem Bus angefügt.<br/>  |
| <dl> <dt>1</dt> </dl> | Das Laufwerk wird mit dem zweiten Gerät auf dem Bus verbunden.<br/> |



 

</dd> <dt>

*dvddrive* \[ Out, retval\]
</dt> <dd>

Ein [**ivmdvddrive**](ivmdvddrive.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                               | BESCHREIBUNG                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | Der Vorgang wurde durchgeführt.<br/>                       |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                       | Der Parameter " *dvddrive* " ist **null**.<br/>               |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                    | Ein Parameter ist nicht gültig.<br/>                           |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>               | Die Konfiguration ist unbekannt.<br/>                       |
| <dl> <dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert </dl>    | Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".<br/> |
| <dl> <dt>**VM \_ E \_ Drive \_ Bus \_ loc \_ \_ verwendet**</dt> <dt>0xa00400503</dt> </dl> | Der angegebene Busspeicherort wird verwendet.<br/>               |
| <dl> <dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt> </dl>            | Das angegebene Laufwerk ist ungültig.<br/>                   |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>               | Ein unerwarteter Fehler ist aufgetreten.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Sie können einem beendeten virtuellen Computer nur ein neues CD-oder DVD-Laufwerk hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

