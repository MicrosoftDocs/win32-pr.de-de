---
title: IVMDVDDriveEvents-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die ausgehende Ereignisschnittstelle für die IVMDVDDrive-Schnittstelle.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- IVMDVDDriveEvents-Schnittstelle Virtueller PC
- IVMDVDDriveEvents-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb34bf77b6692c90977262ac7e2177019169e3195ee44415a0693102e6d15ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136793"
---
# <a name="ivmdvddriveevents-interface"></a>IVMDVDDriveEvents-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die ausgehende Ereignisschnittstelle für die [**IVMDVDDrive-Schnittstelle.**](ivmdvddrive.md)

## <a name="members"></a>Member

Die **IVMDVDDriveEvents-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDriveEvents** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IVMDVDDriveEvents-Schnittstelle** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausjiziert wurden.<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents ist als c2a7d8e9-e76c-4eb8-94f7-71a5122d249b definiert.<br/>         |



 

