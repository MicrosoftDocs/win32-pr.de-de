---
description: Die Imonitor-Schnittstelle stellt Methoden bereit, die den Monitor Vorgang steuern. Diese Methoden werden vom Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) aufgerufen.
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Imonitor-Schnittstelle (Netmon. h)
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
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863271"
---
# <a name="imonitor-interface"></a>Imonitor-Schnittstelle

Die **Imonitor** -Schnittstelle stellt Methoden bereit, die den Monitor Vorgang steuern. Diese Methoden werden vom [*Überwachungs Steuerungs Dienst (Monitor Control Service*](m.md) , mcsvc) aufgerufen.

## <a name="members"></a>Member

Die **Imonitor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imonitor** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Imonitor** -Schnittstelle verfügt über diese Methoden.



| Methode                                        | BESCHREIBUNG                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Doconfigure**](imonitor-doconfigure.md)   | Update Monitor Konfiguration.<br/>                                                                           |
| [**Doinitialize**](imonitor-doinitialize.md) | Initialisiert einen Monitor.<br/>                                                                                   |
| [**Onframes**](imonitor-onframes.md)         | Gibt den Status eines Frame Ereignisses an.<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | Gibt an, dass der Monitor erfolgreich konfiguriert wurde und dass die Datenerfassung im Begriff ist.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Gibt ein NPP-Status Ereignis an.<br/>                                                                           |
| [**OnStop**](imonitor-onstop.md)             | Gibt den Abschluss der Datenerfassung an.<br/>                                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

