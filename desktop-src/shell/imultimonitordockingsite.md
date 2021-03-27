---
description: Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste in einem System mit mehreren Monitoren enthält.
title: Imultimonitordockingsite-Schnittstelle
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
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995198"
---
# <a name="imultimonitordockingsite-interface"></a>Imultimonitordockingsite-Schnittstelle

Wird vom Browser implementiert. Macht Methoden verfügbar, die verwalten, welcher Monitor die Windows-Taskleiste in einem System mit mehreren Monitoren enthält.

## <a name="members"></a>Member

Die **imultimonitordockingsite** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imultimonitordockingsite** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imultimonitordockingsite** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Getmonitor**](imultimonitordockingsite-getmonitor.md)         | Ruft den aktuellen Standard Monitor ab.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Überprüft, ob der Monitor aktiv und verfügbar ist.<br/>                              |
| [**Setmonitor**](imultimonitordockingsite-setmonitor.md)         | Ändert, welcher Monitor für angedockte Symbolleisten in einem System mit mehreren Monitoren verwendet wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie implementieren die **imultimonitordockingsite** -Schnittstelle in der Regel nicht. Der ShellBrowser implementiert diese Schnittstelle, um mehrere Monitore zu unterstützen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                   |



 

 
