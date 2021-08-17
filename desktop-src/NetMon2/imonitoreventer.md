---
description: Die IMonitorEventer-Schnittstelle stellt Methoden zum Übermitteln von Ereignissen sowie zum Zuordnen und Freigeben von Überwachungsressourcen bereit.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: IMonitorEventer-Schnittstelle (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2af49529a74c23e0f4d4e77e0d2608cd44d12028d93022750fbbd3af891e2e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365488"
---
# <a name="imonitoreventer-interface"></a>IMonitorEventer-Schnittstelle

Die **IMonitorEventer-Schnittstelle** stellt Methoden zum Übermitteln von Ereignissen sowie zum Zuordnen und Freigeben von Überwachungsressourcen bereit.

## <a name="members"></a>Member

Die **IMonitorEventer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMonitorEventer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMonitorEventer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**FreeEventData**](imonitoreventer-freeeventdata.md) | Gibt Speicherplatz frei, der für Überwachungsdaten reserviert ist.<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | Reserviert Speicherplatz für Überwachungsdaten.<br/>       |
| [**SendNMEvent**](imonitoreventer-sendnmevent.md)     | Sendet Ereignisse an WMI.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

