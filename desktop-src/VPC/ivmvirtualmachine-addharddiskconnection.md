---
title: Ivmvirtualmachine AddHardDiskConnection-Methode (vpccominterfaces. h)
description: Fügt der virtuellen Maschine eine neue Festplatten Verbindung hinzu.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- AddHardDiskConnection-Methode Virtual PC
- AddHardDiskConnection-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, AddHardDiskConnection-Methode
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
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338344"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>Ivmvirtualmachine:: AddHardDiskConnection-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt der virtuellen Maschine (VM) eine neue Festplatten Verbindung hinzu.

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

*harddiskpath* \[ in\]
</dt> <dd>

Der vollständige Pfad der VHD-Datei (Virtual Hard Disk) zum Herstellen einer Verbindung.

</dd> <dt>

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

*harddiskconnection* \[ Out, retval\]
</dt> <dd>

Ein [**ivmharddiskconnection**](ivmharddiskconnection.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                                  |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                      | Der *harddiskconnection* -Parameter ist **null**.<br/>                                                                                                |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                   | Der Parameter " *harddiskpath* " ist **null** , oder der Parameter " *busnumber* " oder " *devicenenumber* " ist ungültig.<br/>                                            |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt> </dl>   | Das System kann die durch den *harddiskpath* -Parameter angegebene Datei nicht finden.<br/>                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl>   | Das System kann den durch den *harddiskpath* -Parameter angegebenen Pfad nicht finden.<br/>                                                                     |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>      | Der *harddiskpath* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").<br/>                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>      | Der *harddiskpath* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl>   | Der durch den *harddiskpath* -Parameter angegebene Pfad ist zu lang. Der Pfad muss weniger als 260 Zeichen umfassen.<br/>                                     |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                              | Die Konfiguration ist unbekannt.<br/>                                                                                                                  |
| <dl> <dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert </dl>                   | Der virtuelle Computer befindet sich in einem laufenden oder gespeicherten Zustand.<br/>                                                                                                         |
| <dl> <dt>**VM \_ E \_ Drive \_ Bus \_ loc \_ \_ verwendet**</dt> <dt>0xa00400503</dt> </dl>                | Der angegebene Busspeicherort wird verwendet.<br/>                                                                                                          |
| <dl> <dt>**VM \_ E \_ ungültige \_ HD- \_ Datei**</dt> <dt>0xa0040682</dt> </dl>                        | Die VHD ist größer als 127 GB und kann nicht mit dem IDE-Bus verbunden werden.<br/>                                                                         |
| <dl> <dt>**VM \_ E \_ nicht unterstützter \_ \_ Festplatten \_ Datenträger**</dt> <dt>0xa00400686</dt> </dl>             | Der *harddiskpath* -Parameter verweist auf eine verknüpfte VHD oder eine differenzierende VHD zu einer verknüpften VHD. Verknüpfte VHDs können nicht an virtuelle Computer angefügt werden.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt> </dl> | Die angegebene VHD ist bereits mit einem anderen Busspeicherort für diesen virtuellen Computer verbunden.<br/>                                                                    |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Sie können einem beendeten virtuellen Computer nur eine neue Festplatten Verbindung hinzufügen.

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

 

