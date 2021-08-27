---
title: SystemMonitor.BatchingLock-Methode
description: Sperrt den Systemmonitor, um zu verhindern, dass Leistungsindikatordaten aus der neu hinzugefügten Indikator- oder Protokolldatei stichprobeniert werden.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- BatchingLock-Methode SysMon
- BatchingLock-Methode SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , BatchingLock-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f028a3cb985a530b6e034ceabe430d2dda7b12e337af40d6510a3a8d77bd0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882936"
---
# <a name="systemmonitorbatchinglock-method"></a>SystemMonitor.BatchingLock-Methode

Sperrt den Systemmonitor, um zu verhindern, dass Leistungsindikatordaten aus der neu hinzugefügten Indikator- oder Protokolldatei stichprobeniert werden.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lock (Sperren)* \[ In\]
</dt> <dd>

Legen Sie diese Einstellung auf True fest, um den Systemmonitor zu sperren, um zu verhindern, dass Zählerdaten aus der neu hinzugefügten Indikator- oder Protokolldatei stichprobeniert werden. Legen Sie diese Einstellung auf False fest, um die Sperre zu entfernen.

</dd> <dt>

*batchReason* \[ In\]
</dt> <dd>

Identifiziert die Quelle der Daten, die Sie sperren. Verwenden Sie beim Sperren und Entsperren der Ressource denselben Grundwert. Mögliche Werte finden Sie in der [**SysmonBatchReason-Enumeration.**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sie müssen diese Methode zweimal aufrufen, einmal zum Sperren der Quelle (True) und einmal zum Entsperren der Quelle (False).

Sie können nur eine Sperre platzieren. Wenn Sie beispielsweise die Sperre für SysmonBatchAddFiles festlegen und dann einen zweiten Aufruf mit SysmonBatchAddCounters als Grund vornehmen, entfernt der zweite Aufruf die Sperre, die durch den ersten Aufruf platziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





