---
title: Ivmdvddriveevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmdvddrive-Schnittstelle.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Ivmdvddriveevents-Schnittstelle virtueller PC
- Virtueller Computer für ivmdvddriveevents Interface, beschrieben
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
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479011"
---
# <a name="ivmdvddriveevents-interface"></a>Ivmdvddriveevents-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die ausgehende Ereignis Schnittstelle für die [**ivmdvddrive**](ivmdvddrive.md) -Schnittstelle.

## <a name="members"></a>Member

Die **ivmdvddriveevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmdvddriveevents** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ivmdvddriveevents** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Onmediaeject**](ivmdvddriveevents-onmediaeject.md)   | Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausworfen wurden.<br/>  |
| [**Onmediainsert**](ivmdvddriveevents-onmediainsert.md) | Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmdvddriveevents ist als c2a7d8e9-e76c-4eb8-94f7-71a5122d249b definiert.<br/>         |



 

