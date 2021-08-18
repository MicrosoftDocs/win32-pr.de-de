---
title: IVMFloppyDrive-Schnittstelle (VPCCOMInterfaces.h)
description: Steuert ein Diskettenlaufwerk innerhalb eines virtuellen Computers.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- IVMFloppyDrive-Schnittstelle Virtueller PC
- IVMFloppyDrive-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63db224861b547b9485b03080ce3ffb3f5c118ef0de71597db79aa0888a1528d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594806"
---
# <a name="ivmfloppydrive-interface"></a>IVMFloppyDrive-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Steuert ein Diskettenlaufwerk innerhalb eines virtuellen Computers. **IVMFloppyDrive kann** Clients über Ereignisse mithilfe der ausgehenden [**IVMFloppyDriveEvents-Schnittstelle**](ivmfloppydriveevents.md) benachrichtigen. Sie können ein **IVMFloppyDrive-Objekt** aus dem [**IVMFloppyDriveCollection-Objekt**](ivmfloppydrivecollection.md) abrufen, das von der [**IVMVirtualMachine::FloppyDrives-Eigenschaft zurückgegeben**](ivmvirtualmachine-floppydrives.md) wird.

## <a name="members"></a>Member

Die **IVMFloppyDrive-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDrive** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMFloppyDrive-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Anfügen eines physischen Laufwerks auf dem Host an das Diskettenlaufwerk auf dem virtuellen Computer.<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | Angefügt ein Diskettenmedienbild auf dem Host an das Diskettenlaufwerk.<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | Gibt ein physisches Laufwerk auf dem Host vom Diskettenlaufwerk frei.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Gibt ein Diskettenmedienimage auf dem Host vom Diskettenlaufwerk frei.<br/>                  |



 

### <a name="properties"></a>Eigenschaften

Die **IVMFloppyDrive-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | BESCHREIBUNG                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**Anhang**](ivmfloppydrive-attachment.md)<br/>           | Schreibgeschützt<br/> | Der Medientyp, der an das Diskettenlaufwerk auf dem virtuellen Computer angefügt ist.<br/>     |
| [**DriveNumber**](ivmfloppydrive-drivenumber.md)<br/>         | Schreibgeschützt<br/> | Der nullbasierte Index des Controllers, an den dieses Diskettenlaufwerk angefügt ist.<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | Schreibgeschützt<br/> | Der Buchstabe des Hostlaufwerks, an das das Diskettenlaufwerk angefügt ist.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Schreibgeschützt<br/> | Der vollständige Pfad der Imagedatei, an die das Diskettenlaufwerk angefügt ist.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive ist als 661abee6-112a-4ed9-fsf-3c874969f10e definiert.<br/>             |



 

