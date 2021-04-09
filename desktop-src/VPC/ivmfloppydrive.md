---
title: Ivmfloppydrive-Schnittstelle (vpccominterfaces. h)
description: Steuert ein Diskettenlaufwerk innerhalb eines virtuellen Computers.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Ivmfloppydrive Interface Virtual PC
- Virtueller Computer für ivmfloppydrive Interface, beschrieben
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
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957021"
---
# <a name="ivmfloppydrive-interface"></a>Ivmfloppydrive-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Steuert ein Diskettenlaufwerk innerhalb eines virtuellen Computers. **Ivmfloppydrive** kann Clients über Ereignisse über die ausgehende Schnittstelle [**ivmfloppydriveevents**](ivmfloppydriveevents.md) benachrichtigen. Sie können ein **ivmfloppydrive** -Objekt aus dem [**ivmfloppydrivecollection**](ivmfloppydrivecollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine:: floppydrives**](ivmvirtualmachine-floppydrives.md) -Eigenschaft zurückgegeben wird.

## <a name="members"></a>Member

Die **ivmfloppydrive** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmfloppydrive** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmfloppydrive** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Fügt ein physisches Laufwerk auf dem Host an das Diskettenlaufwerk auf dem virtuellen Computer an.<br/> |
| [**Attachimage**](ivmfloppydrive-attachimage.md)           | Fügt ein Disketten Medienbild auf dem Host an das Diskettenlaufwerk an.<br/>                    |
| [**Releasehostlaufwerk**](ivmfloppydrive-releasehostdrive.md) | Gibt ein physisches Laufwerk auf dem Host vom Diskettenlaufwerk frei.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Gibt ein Disketten Medienbild auf dem Host vom Diskettenlaufwerk aus.<br/>                  |



 

### <a name="properties"></a>Eigenschaften

Die **ivmfloppydrive** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | BESCHREIBUNG                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**Attachment**](ivmfloppydrive-attachment.md)<br/>           | Schreibgeschützt<br/> | Der Medientyp, der mit dem Diskettenlaufwerk innerhalb des virtuellen Computers verbunden ist.<br/>     |
| [**Drivenreiber**](ivmfloppydrive-drivenumber.md)<br/>         | Schreibgeschützt<br/> | Der null basierte Index des Controllers, an den dieses Diskettenlaufwerk angefügt ist.<br/> |
| [**Hostdriveletter**](ivmfloppydrive-hostdriveletter.md)<br/> | Schreibgeschützt<br/> | Der Buchstabe des Host Laufwerks, an das das Diskettenlaufwerk angefügt ist.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Schreibgeschützt<br/> | Der vollständige Pfad der Bilddatei, an die das Diskettenlaufwerk angefügt ist.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.<br/>             |



 

