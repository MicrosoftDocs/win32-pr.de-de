---
description: Die imonitoreventer-Schnittstelle stellt Methoden zum Übermitteln von Ereignissen und zum Zuweisen und Freigeben von Monitor Ressourcen bereit.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Imonitoreventer-Schnittstelle (Netmon. h)
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
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862411"
---
# <a name="imonitoreventer-interface"></a>Imonitoreventer-Schnittstelle

Die **imonitoreventer** -Schnittstelle stellt Methoden zum Übermitteln von Ereignissen und zum Zuweisen und Freigeben von Monitor Ressourcen bereit.

## <a name="members"></a>Member

Die **imonitoreventer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imonitoreventer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imonitoreventer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**Freieventdata**](imonitoreventer-freeeventdata.md) | Gibt den zugeordneten Speicherplatz für Überwachungsdaten frei.<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | Weist Speicherplatz für Überwachungsdaten zu.<br/>       |
| [**Sendnmevent**](imonitoreventer-sendnmevent.md)     | Übermittelt Ereignisse an WMI.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

