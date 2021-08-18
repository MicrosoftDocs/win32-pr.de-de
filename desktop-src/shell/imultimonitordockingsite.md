---
description: Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows Taskleiste auf einem System mit mehreren Monitoren enthält.
title: IMultiMonitorDockingSite-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: a5a17e8206af8f0821833f4b2ea250606de29b6fbe74b7a29ced6c5b5dc13ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458220"
---
# <a name="imultimonitordockingsite-interface"></a>IMultiMonitorDockingSite-Schnittstelle

Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows Taskleiste auf einem System mit mehreren Monitoren enthält.

## <a name="members"></a>Member

Die **IMultiMonitorDockingSite-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMultiMonitorDockingSite** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMultiMonitorDockingSite-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | Ruft den aktuellen Standardmonitor ab.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Überprüft, ob der Monitor aktiv und verfügbar ist.<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | Ändert, welcher Monitor für angedockte Symbolleisten auf einem System mit mehreren Monitoren verwendet wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **IMultiMonitorDockingSite-Schnittstelle** wird in der Regel nicht implementiert. Der Shell-Browser implementiert diese Schnittstelle, um mehrere Monitore zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                   |



 

 
