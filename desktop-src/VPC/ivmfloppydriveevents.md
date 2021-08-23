---
title: IVMFloppyDriveEvents-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die ausgehende Ereignisschnittstelle für die IVMFloppyDrive-Schnittstelle. Der Client implementiert diese Methoden zum Empfangen von Ereignissen, die von IVMFloppyDrive gesendet werden.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- IVMFloppyDriveEvents-Schnittstelle Virtueller PC
- IVMFloppyDriveEvents-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53cd275c45e23de1bb437b4c233ff64118952afae76e7c6b9bc9366facf4fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653510"
---
# <a name="ivmfloppydriveevents-interface"></a>IVMFloppyDriveEvents-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die ausgehende Ereignisschnittstelle für die [**IVMFloppyDrive-Schnittstelle.**](ivmfloppydrive.md) Der Client implementiert diese Methoden zum Empfangen von Ereignissen, die von **IVMFloppyDrive gesendet werden.**

## <a name="members"></a>Member

Die **IVMFloppyDriveEvents-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDriveEvents** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IVMFloppyDriveEvents-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | Beschreibung                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausjiziert wurden.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents ist als a9ed3401-4e09-4177-86ec-a13bf9fa7d4e definiert.<br/>      |



 

