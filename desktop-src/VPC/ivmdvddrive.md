---
title: IVMDVDDrive-Schnittstelle (VPCCOMInterfaces.h)
description: Steuert ein CD-ROM- oder DVD-ROM-Laufwerk auf einem virtuellen Computer. IVMDVDDrive kann Clients mithilfe der ausgehenden SCHNITTSTELLE IVMDVDDriveEvents über Ereignisse benachrichtigen.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- IVMDVDDrive-Schnittstelle Virtueller PC
- IVMDVDDrive-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc1f611b46dcde6c4a17c1a44252501bd89df9f4ccb120f6535553afc7ef7eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938869"
---
# <a name="ivmdvddrive-interface"></a>IVMDVDDrive-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Steuert ein CD-ROM- oder DVD-ROM-Laufwerk auf einem virtuellen Computer. **IVMDVDDrive** kann Clients mithilfe der ausgehenden [**SCHNITTSTELLE IVMDVDDriveEvents**](ivmdvddriveevents.md) über Ereignisse benachrichtigen.

Sie können einem virtuellen Computer ein neues CD-ROM- oder DVD-ROM-Laufwerk hinzufügen, indem Sie die [**IVMVirtualMachine::AddDVAFFINDrive-Methode**](ivmvirtualmachine-adddvdromdrive.md) verwenden. Sie können ein vorhandenes CD-ROM- oder DVD-ROM-Laufwerk mithilfe der [**IVMVirtualMachine::RemoveDVAFFINDrive-Methode**](ivmvirtualmachine-removedvdromdrive.md) von einem virtuellen Computer entfernen. Sie können ein **IVMDVDDrive-Objekt** aus dem [**IVMDVDDriveCollection-Objekt**](ivmdvddrivecollection.md) abrufen, das von der [**IVMVirtualMachine::D VCHINDrives-Eigenschaft**](ivmvirtualmachine-dvdromdrives.md) zurückgegeben wird.

## <a name="members"></a>Member

Die **IVMDVDDrive-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDrive** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMDVDDrive-Schnittstelle** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmdvddrive-attachhostdrive.md)   | Fügt ein Hostlaufwerk an das DVD-Laufwerk innerhalb des virtuellen Computers an.<br/>           |
| [**AttachImage**](ivmdvddrive-attachimage.md)           | Fügt ein ISO-Image an das DVD-Laufwerk innerhalb des virtuellen Computers an.<br/>           |
| [**ReleaseHostDrive**](ivmdvddrive-releasehostdrive.md) | Gibt ein aufgezeichnetes Hostlaufwerk vom DVD-Laufwerk frei.<br/>                           |
| [**ReleaseImage**](ivmdvddrive-releaseimage.md)         | Gibt ein aufgezeichnetes ISO-Image vom DVD-Laufwerk frei.<br/>                            |
| [**SetBusLocation**](ivmdvddrive-setbuslocation.md)     | Fügt das DVD-Laufwerk an den angegebenen Busspeicherort auf dem virtuellen Computer an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IVMDVDDrive-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                          | Zugriffstyp          | Beschreibung                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Anhang**](ivmdvddrive-attachment.md)<br/>           | Schreibgeschützt<br/> | Der Typ des Mediums, das an das DVD-Laufwerk innerhalb des virtuellen Computers angefügt ist.<br/> |
| [**BusNumber**](ivmdvddrive-busnumber.md)<br/>             | Schreibgeschützt<br/> | Die Busnummer, an die dieses Gerät angefügt ist.<br/>                        |
| [**DeviceNumber**](ivmdvddrive-devicenumber.md)<br/>       | Schreibgeschützt<br/> | Die Gerätenummer, an die dieses Laufwerk angefügt ist.<br/>                      |
| [**HostDriveLetter**](ivmdvddrive-hostdriveletter.md)<br/> | Schreibgeschützt<br/> | Der Buchstabe des Für dieses Gerät festgelegten Hostlaufwerks.<br/>                       |
| [**ImageFile**](ivmdvddrive-imagefile.md)<br/>             | Schreibgeschützt<br/> | Der vollständige Pfad des Imagedateisatzes für dieses Gerät.<br/>                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



 

