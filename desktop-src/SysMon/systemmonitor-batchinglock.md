---
title: SystemMonitor.Batchinglock-Methode
description: Sperrt den System Monitor, um zu verhindern, dass die Stichprobenentnahme von Daten aus dem neu hinzugefügten Wert oder der neuen Protokolldatei
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Batchinglock-Methode (Sysmon)
- Batchinglock-Methode "sysmon", Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", batchinglock-Methode
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
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339159"
---
# <a name="systemmonitorbatchinglock-method"></a>SystemMonitor.Batchinglock-Methode

Sperrt den System Monitor, um zu verhindern, dass die Stichprobenentnahme von Daten aus dem neu hinzugefügten Wert oder der neuen Protokolldatei

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sperre* \[ in\]
</dt> <dd>

Legen Sie diese Einstellung auf "true" fest, um den System Monitor zu sperren, um zu verhindern, dass Daten aus dem neu hinzugefügten-oder-Protokoll Legen Sie auf false fest, um die Sperre zu entfernen.

</dd> <dt>

*batchreason* \[ in\]
</dt> <dd>

Identifiziert die Quelle der Daten, die Sie sperren. Verwenden Sie denselben Grund Wert, wenn Sie die Ressource sperren und entsperren. Mögliche Werte finden Sie in der [**sysmonbatchreason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) -Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode muss zweimal aufgerufen werden, um die Quelle zu sperren (true) und einmal, um die Quelle zu entsperren (false).

Sie können nur eine Sperre platzieren. Wenn Sie z. b. die Sperre für sysmonbatchaddfiles festlegen und dann einen zweiten Anruf mithilfe von sysmonbatchaddcounters durchführen, wird der zweite-Befehl die Sperre entfernt, die durch den ersten-Befehl platziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





