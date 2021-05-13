---
description: Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste auf einem System mit mehreren Monitoren enthält.
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
ms.openlocfilehash: 5ea3461d00c16f7384d7396e2f03946d517c460f
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841891"
---
# <a name="imultimonitordockingsite-interface"></a>IMultiMonitorDockingSite-Schnittstelle

Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste auf einem System mit mehreren Monitoren enthält.

## <a name="members"></a>Member

Die **IMultiMonitorDockingSite-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMultiMonitorDockingSite** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMultiMonitorDockingSite-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | Ruft den aktuellen Standardmonitor ab.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Überprüft, ob der Monitor aktiv und verfügbar ist.<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | Änderungen, die für angedockte Symbolleisten auf einem System mit mehreren Monitoren verwendet werden.<br/> |



 

## <a name="remarks"></a>Hinweise

In der Regel implementieren Sie die **IMultiMonitorDockingSite-Schnittstelle** nicht. Der Shell-Browser implementiert diese Schnittstelle, um mehrere Monitore zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                   |



 

 
