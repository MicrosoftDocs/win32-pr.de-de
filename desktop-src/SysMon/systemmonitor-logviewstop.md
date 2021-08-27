---
title: SystemMonitor.LogViewStop-Eigenschaft
description: Ruft das Enddatum ab, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird, oder legt dieses fest.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- LogViewStop-Eigenschaft SysMon
- LogViewStop-Eigenschaft SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , LogViewStop-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c30305f99e0d9bf66dd0f00dccc7674073e0f7058bca4284411c9d24426b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882074"
---
# <a name="systemmonitorlogviewstop-property"></a>SystemMonitor.LogViewStop-Eigenschaft

Ruft das Enddatum ab, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird, oder legt dieses fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Eigenschaftswert

Enddatum, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird.

## <a name="remarks"></a>Hinweise

SYSMON ruft Leistungsindikatorwerte aus den Protokolldateien ab, die in [**systemMonitor.LogViewStart**](systemmonitor-logviewstart.md) enthalten sind, sowie einschließlich Beendigungstermine.

Wenn Sie keinen Stoppwert angeben oder diese Eigenschaft auf einen Datumswert festlegen, der nach dem letzten in der Protokolldatei enthaltenen Datum liegt, ändert SYSMON den Wert in den letzten Datumswert in den Protokolldateien.

Wenn diese Eigenschaft auf einen Datumswert festgelegt ist, der kleiner als [**LogViewStart**](systemmonitor-logviewstart.md)ist, ändert SYSMON den Wert in den Wert von **LogViewStart.**

Sie müssen das Startdatum festlegen, bevor Sie das Enddatum festlegen. Andernfalls werden beide Werte auf Date.MinValue festgelegt, und wenn Sie die Datumsangaben nach dem Festlegen von [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md)festlegen, wird nur der erste Indikatorwert aus der Protokolldatei abgerufen.

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

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor.LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





