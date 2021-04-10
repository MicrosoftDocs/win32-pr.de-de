---
title: Ivmvirtualpcevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmvirtualpc-Schnittstelle.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Ivmvirtualpcevents Interface Virtual PC
- Virtueller Computer für ivmvirtualpcevents Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040849"
---
# <a name="ivmvirtualpcevents-interface"></a>Ivmvirtualpcevents-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die ausgehende Ereignis Schnittstelle für die [**ivmvirtualpc**](ivmvirtualpc.md) -Schnittstelle. Der Client implementiert diese Methoden, um von [**ivmvirtualpc**](ivmvirtualpc.md)gesendete Ereignisse zu empfangen.

## <a name="members"></a>Member

Die **ivmvirtualpcevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmvirtualpcevents** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ivmvirtualpcevents** -Schnittstelle verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Oneventprotokolliert**](ivmvirtualpcevents-oneventlogged.md)     | Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.<br/>      |
| [**Onvmstatechange**](ivmvirtualpcevents-onvmstatechange.md) | Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmvirtualpcevents ist als efed1ef1-3c09-41f7-a9c2-7e29fa286c9d definiert.<br/>        |



 

