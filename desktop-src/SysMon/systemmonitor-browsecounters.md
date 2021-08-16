---
title: SystemMonitor BrowseCounters-Methode
description: Zeigt das Dialogfeld Leistungsindikatoren hinzufügen an.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- BrowseCounters-Methode SysMon
- BrowseCounters-Methode SysMon , SystemMonitor-Schnittstelle
- SystemMonitor-Schnittstelle SysMon , BrowseCounters-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e88d493ea0e4e1a9312191533162c8eb5a94cfb4233d17d21bb7217a136d403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882926"
---
# <a name="systemmonitorbrowsecounters-method"></a>SystemMonitor::BrowseCounters-Methode

Zeigt das Dialogfeld **Leistungsindikatoren hinzufügen** an.

## <a name="syntax"></a>Syntax


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

In diesem Dialogfeld kann der Benutzer lokale oder Remoteleistungsindikatoren aus einer Liste von Leistungsobjekten auswählen. Die ausgewählten Indikatoren werden der [**Sammlung Indikatoren**](counters.md) hinzugefügt und im Diagramm oder Bericht angezeigt.

Implementieren Sie das [**OnCounterAdded-Ereignis,**](systemmonitor-oncounteradded.md) um Benachrichtigungen zu erhalten, wenn ein Zähler hinzugefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**Counters.Add**](counters-add.md)
</dt> </dl>

 

 





