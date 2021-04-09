---
title: Systemmonitor. logviewstoppt (Eigenschaft)
description: Ruft das Enddatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Logviewstoppt-Eigenschaft (Sysmon)
- Logviewstoppt-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", logviewstopps (Eigenschaft)
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
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956428"
---
# <a name="systemmonitorlogviewstop-property"></a>Systemmonitor. logviewstoppt (Eigenschaft)

Ruft das Enddatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Eigenschaftswert

Das Enddatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.

## <a name="remarks"></a>Bemerkungen

Sysmon Ruft Werte aus den Protokolldateien ab, die in den Dateien " [**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md) " und "End Date" (einschließlich) fallen.

Wenn Sie keinen Endwert angeben oder wenn Sie diese Eigenschaft auf einen Datumswert festlegen, der nach dem letzten in der Protokolldatei enthaltenen Datum liegt, ändert sysmon den Wert in den letzten Datumswert, der in den Protokolldateien gefunden wurde.

Wenn diese Eigenschaft auf einen Datumswert festgelegt ist, der kleiner als [**logviewstart**](systemmonitor-logviewstart.md)ist, wird der Wert von sysmon in den **logviewstart**-Wert geändert.

Sie müssen das Startdatum festlegen, bevor Sie das Enddatum festlegen. Andernfalls werden beide Werte auf Date. MinValue festgelegt. Wenn Sie die Datumsangaben nach dem Festlegen von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)festlegen, wird nur der erste Leistungsindikatoren aus der Protokolldatei abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> <dt>

[**Systemmonitor. getlogviewrange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**Systemmonitor. logsourcestoptime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**Systemmonitor. setlogviewrange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





