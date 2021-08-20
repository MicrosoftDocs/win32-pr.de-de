---
title: IVMVirtualMachine AddDVUMADrive-Methode (VPCCOMInterfaces.h)
description: Fügt dem virtuellen Computer ein neues CD- oder DVD-Laufwerk hinzu.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVFÜDrive-Methode Virtueller PC
- AddDVFÜDrive-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, AddDVUMADrive-Methode
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
ms.openlocfilehash: 63a875af50d38270b898c17f2848a4e4b33fe79a4b17d9ab7b6be58cdcfcf92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123230"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>IVMVirtualMachine::AddDVUMADrive-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Fügt dem virtuellen Computer ein neues CD- oder DVD-Laufwerk hinzu.

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

*busNumber* \[ In\]
</dt> <dd>

Der Bus, an den das Laufwerk angefügt wird.



| Wert                                                                        | Bedeutung                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Das Laufwerk wird an den ersten Bus angefügt.<br/>  |
| <dl> <dt>1</dt> </dl> | Das Laufwerk wird an den zweiten Bus angefügt.<br/> |



 

</dd> <dt>

*deviceNumber* \[ In\]
</dt> <dd>

Das Gerät, an das das Laufwerk angefügt wird.



| Wert                                                                        | Bedeutung                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Das Laufwerk wird an das erste Gerät im Bus angefügt.<br/>  |
| <dl> <dt>1</dt> </dl> | Das Laufwerk wird an das zweite Gerät im Bus angefügt.<br/> |



 

</dd> <dt>

*dvdDrive* \[ out, retval\]
</dt> <dd>

Ein [**IVMDVDDrive-Objekt.**](ivmdvddrive.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                               | Beschreibung                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | Der Vorgang wurde durchgeführt.<br/>                       |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                       | Der *dvdDrive-Parameter* ist **NULL.**<br/>               |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                    | Ein Parameter ist nicht gültig.<br/>                           |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>               | Die Konfiguration ist unbekannt.<br/>                       |
| <dl> <dt>**VM \_ E \_ \_ VM, DIE \_ AUSGEFÜHRT WIRD ODER \_ 0XA004020B**</dt> <dt></dt> </dl>    | Der virtuelle Computer befindet sich in einem ausgeführten oder gespeicherten Zustand.<br/> |
| <dl> <dt>**VM \_ E \_ DRIVE \_ BUS \_ LOC IN USE \_ \_ 0XA00400503**</dt> <dt></dt> </dl> | Der angegebene Busstandort wird verwendet.<br/>               |
| <dl> <dt>**VM \_ E \_ DRIVE \_ INVALID**</dt> <dt>0xA0040502</dt> </dl>            | Das angegebene Laufwerk ist ungültig.<br/>                   |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>               | Ein unerwarteter Fehler ist aufgetreten.<br/>                   |



 

## <a name="remarks"></a>Hinweise

Sie können einem beendeten virtuellen Computer nur ein neues CD- oder DVD-Laufwerk hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

