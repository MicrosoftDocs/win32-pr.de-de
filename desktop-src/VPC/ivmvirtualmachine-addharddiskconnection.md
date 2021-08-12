---
title: IVMVirtualMachine AddHardDiskConnection-Methode (VPCCOMInterfaces.h)
description: Fügt dem virtuellen Computer eine neue Festplattenverbindung hinzu.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- AddHardDiskConnection-Methode Virtueller PC
- AddHardDiskConnection-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, AddHardDiskConnection-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67bbeb5cdb347327a807b19ec16c901c211cdddb72ce88a8b5b00804b195f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592758"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>IVMVirtualMachine::AddHardDiskConnection-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Fügt dem virtuellen Computer (VM) eine neue Festplattenverbindung hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hardDiskPath* \[ In\]
</dt> <dd>

Der vollständige Pfad der virtuellen Festplattendatei (VHD), mit der eine Verbindung hergestellt werden soll.

</dd> <dt>

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

*hardDiskConnection* \[ out, retval\]
</dt> <dd>

Ein [**IVMHardDiskConnection-Objekt.**](ivmharddiskconnection.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                                  |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                      | Der *hardDiskConnection-Parameter* ist **NULL.**<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                                   | Ein *hardDiskPath-Parameter* **ist NULL,** oder der *parameter busNumber* oder *deviceNumber* ist ungültig.<br/>                                            |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0X80070002</dt> </dl>   | Das System kann die durch den *hardDiskPath-Parameter angegebene Datei nicht* finden.<br/>                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0X80070003</dt> </dl>   | Das System kann den durch den *hardDiskPath-Parameter angegebenen Pfad nicht* finden.<br/>                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>      | Der *hardDiskPath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?<>/ \| ":").<br/>                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | Der *hardDiskPath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | Der durch den *hardDiskPath-Parameter angegebene Pfad* ist zu lang. Der Pfad muss kleiner als 260 Zeichen sein.<br/>                                     |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                              | Die Konfiguration ist unbekannt.<br/>                                                                                                                  |
| <dl> <dt>**VM \_ E \_ \_ VM, DIE \_ AUSGEFÜHRT WIRD ODER \_ 0XA004020B**</dt> <dt></dt> </dl>                   | Der virtuelle Computer befindet sich in einem ausgeführten oder gespeicherten Zustand.<br/>                                                                                                         |
| <dl> <dt>**VM \_ E \_ DRIVE \_ BUS \_ LOC IN USE \_ \_ 0XA00400503**</dt> <dt></dt> </dl>                | Der angegebene Busstandort wird verwendet.<br/>                                                                                                          |
| <dl> <dt>**VM \_ E \_ UNGÜLTIGE \_ \_ HD-0XA0040682**</dt> <dt></dt> </dl>                        | Die VHD ist größer als 127 GB und kann nicht mit dem IDE-Bus verbunden werden.<br/>                                                                         |
| <dl> <dt>**VM \_ E \_ NICHT UNTERSTÜTZTER \_ \_ \_ HD-DATENTRÄGERTYP**</dt> <dt>0XA00400686</dt> </dl>             | Der *hardDiskPath-Parameter* bezieht sich auf eine verknüpfte VHD oder eine sich unterscheidende VHD auf eine verknüpfte VHD. Verknüpfte VHDs können nicht an virtuelle Computer angefügt werden.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ \_ WIN32(FEHLERFREIGABEVERLETZUNG) \_**</dt> <dt>0X80070020</dt> </dl> | Die angegebene VHD ist bereits mit einem anderen Busstandort für diesen virtuellen Computer verbunden.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Sie können einer beendeten virtuellen Maschine nur eine neue Festplattenverbindung hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

