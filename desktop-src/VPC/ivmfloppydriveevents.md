---
title: Ivmfloppydriveevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmfloppydrive-Schnittstelle. Der Client implementiert diese Methoden zum Empfangen von Ereignissen, die von ivmfloppydrive gesendet werden.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Ivmfloppydriveevents-Schnittstelle virtueller PC
- Ivmfloppydriveevents Interface Virtual PC, beschrieben
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
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106059"
---
# <a name="ivmfloppydriveevents-interface"></a>Ivmfloppydriveevents-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die ausgehende Ereignis Schnittstelle für die [**ivmfloppydrive**](ivmfloppydrive.md) -Schnittstelle. Der Client implementiert diese Methoden zum Empfangen von Ereignissen, die von **ivmfloppydrive** gesendet werden.

## <a name="members"></a>Member

Die **ivmfloppydriveevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmfloppydriveevents** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ivmfloppydriveevents** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Onmediaeject**](ivmfloppydriveevents-onmediaeject.md)   | Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausworfen wurden.<br/>  |
| [**Onmediainsert**](ivmfloppydriveevents-onmediainsert.md) | Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmfloppydriveevents ist als a9ed3401-4e09-4177-86ec-a13bf9fa7d4e definiert.<br/>      |



 

