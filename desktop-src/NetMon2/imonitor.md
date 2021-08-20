---
description: Die IMonitor-Schnittstelle stellt Methoden bereit, die den Monitorvorgang steuern. Diese Methoden werden vom Monitor Control Service (MCSVC) aufgerufen.
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: IMonitor-Schnittstelle (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 16199568473315fb61e53428d01c72032f3efff6ea0591bfd72ca2475f854fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133101"
---
# <a name="imonitor-interface"></a>IMonitor-Schnittstelle

Die **IMonitor-Schnittstelle** stellt Methoden bereit, die den Monitorvorgang steuern. Diese Methoden werden vom [*Monitor Control Service*](m.md) (MCSVC) aufgerufen.

## <a name="members"></a>Member

Die **IMonitor-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMonitor** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMonitor-Schnittstelle** verfügt über diese Methoden.



| Methode                                        | Beschreibung                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**DoConfigure**](imonitor-doconfigure.md)   | Aktualisiert die Monitorkonfiguration.<br/>                                                                           |
| [**DoInitialize**](imonitor-doinitialize.md) | Initialisiert einen Monitor.<br/>                                                                                   |
| [**OnFrames**](imonitor-onframes.md)         | Gibt den Status eines Frame-Ereignisses an.<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | Gibt an, dass der Monitor erfolgreich konfiguriert wurde und die Datenerfassung beginnt.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Gibt ein NPP-Statusereignis an.<br/>                                                                           |
| [**OnStop**](imonitor-onstop.md)             | Gibt den Abschluss der Datenerfassung an.<br/>                                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

