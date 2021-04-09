---
title: Ivmdvddrive-Schnittstelle (vpccominterfaces. h)
description: Steuert ein CD-ROM-oder DVD-ROM-Laufwerk innerhalb einer virtuellen Maschine. Ivmdvddrive kann Clients über Ereignisse über die ausgehende Schnittstelle ivmdvddriveevents benachrichtigen.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Ivmdvddrive Interface Virtual PC
- Virtueller Computer für ivmdvddrive Interface, beschrieben
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
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040744"
---
# <a name="ivmdvddrive-interface"></a>Ivmdvddrive-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Steuert ein CD-ROM-oder DVD-ROM-Laufwerk innerhalb einer virtuellen Maschine. **Ivmdvddrive** kann Clients über Ereignisse über die ausgehende Schnittstelle [**ivmdvddriveevents**](ivmdvddriveevents.md) benachrichtigen.

Sie können ein neues CD-ROM-oder DVD-ROM-Laufwerk mithilfe der [**ivmvirtualmachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) -Methode zu einem virtuellen Computer hinzufügen. Sie können ein vorhandenes CD-ROM-oder DVD-ROM-Laufwerk mithilfe der [**ivmvirtualmachine:: removedvdromdrive**](ivmvirtualmachine-removedvdromdrive.md) -Methode von einem virtuellen Computer entfernen. Sie können ein **ivmdvddrive** -Objekt aus dem [**ivmdvddrivecollection**](ivmdvddrivecollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) -Eigenschaft zurückgegeben wird.

## <a name="members"></a>Member

Die **ivmdvddrive** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmdvddrive** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmdvddrive** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmdvddrive-attachhostdrive.md)   | Fügt ein Host Laufwerk an das DVD-Laufwerk innerhalb der virtuellen Maschine an.<br/>           |
| [**Attachimage**](ivmdvddrive-attachimage.md)           | Fügt ein ISO-Abbild an das DVD-Laufwerk innerhalb des virtuellen Computers an.<br/>           |
| [**Releasehostlaufwerk**](ivmdvddrive-releasehostdrive.md) | Gibt ein erfasstes Host Laufwerk vom DVD-Laufwerk frei.<br/>                           |
| [**ReleaseImage**](ivmdvddrive-releaseimage.md)         | Gibt ein erfasstes ISO-Abbild vom DVD-Laufwerk frei.<br/>                            |
| [**Setbuslokation**](ivmdvddrive-setbuslocation.md)     | Fügt das DVD-Laufwerk an die angegebene busposition auf dem virtuellen Computer an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ivmdvddrive** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                          | Zugriffstyp          | BESCHREIBUNG                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Attachment**](ivmdvddrive-attachment.md)<br/>           | Schreibgeschützt<br/> | Der Medientyp, der mit dem DVD-Laufwerk innerhalb des virtuellen Computers verbunden ist.<br/> |
| [**Busnummer**](ivmdvddrive-busnumber.md)<br/>             | Schreibgeschützt<br/> | Die Busnummer, an die dieses Gerät angefügt wird.<br/>                        |
| [**Devicengegen ber**](ivmdvddrive-devicenumber.md)<br/>       | Schreibgeschützt<br/> | Die Gerätenummer, an die dieses Laufwerk angefügt ist.<br/>                      |
| [**Hostdriveletter**](ivmdvddrive-hostdriveletter.md)<br/> | Schreibgeschützt<br/> | Der Buchstabe des Host Laufwerks, das für dieses Gerät festgelegt ist.<br/>                       |
| [**ImageFile**](ivmdvddrive-imagefile.md)<br/>             | Schreibgeschützt<br/> | Der vollständige Pfad der Bilddatei, die für dieses Gerät festgelegt ist.<br/>                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



 

