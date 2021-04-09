---
title: Systemmonitor. logviewstart (Eigenschaft)
description: Ruft das Startdatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Logviewstart-Eigenschaft (Sysmon)
- Logviewstart-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, logviewstart (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949746"
---
# <a name="systemmonitorlogviewstart-property"></a>Systemmonitor. logviewstart (Eigenschaft)

Ruft das Startdatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a>Eigenschaftswert

Das Startdatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.

## <a name="remarks"></a>Bemerkungen

Sysmon Ruft Werte aus den Protokolldateien ab, die in den Datumsangaben "Start" und " [**Systemmonitor. logviewend**](systemmonitor-logviewstop.md) " fallen.

Wenn Sie kein Startdatum angeben oder wenn Sie diese Eigenschaft auf einen Datumswert festlegen, der außerhalb des Bereichs der in den Protokolldateien gefundenen Datumswerte liegt, wird der Wert von sysmon in den frühesten in den Protokolldateien gefundenen Datumswert geändert.

Wenn diese Eigenschaft auf einen Datumswert festgelegt ist, der größer als [**logviewstoppt**](systemmonitor-logviewstop.md)ist, wird der Wert von sysmon in den Wert von **logviewstoppt** geändert.

Wenn Sie ein Start-und ein Enddatum angeben, sollten Sie die Datumsangaben vor dem Festlegen von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)angeben.

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

[**Systemmonitor. Logfiles**](systemmonitor-logfiles.md)
</dt> <dt>

[**Systemmonitor. logviewstoppt**](systemmonitor-logviewstop.md)
</dt> <dt>

[**Systemmonitor. logsourcestarttime**](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[**Systemmonitor. setlogviewrange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





