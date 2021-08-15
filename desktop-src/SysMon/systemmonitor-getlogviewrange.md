---
title: SystemMonitor.GetLogViewRange-Methode
description: Ruft das Startdatum ab, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- GetLogViewRange-Methode SysMon
- GetLogViewRange-Methode SysMon, SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , GetLogViewRange-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3233dd57327734669631fc57b31bfb85578621991f34c1b1c414a69697b82048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882426"
---
# <a name="systemmonitorgetlogviewrange-method"></a>SystemMonitor.GetLogViewRange-Methode

Ruft das Startdatum ab, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartTime* \[ out\]
</dt> <dd>

Startdatum, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird.

</dd> <dt>

*StopTime* \[ out\]
</dt> <dd>

Enddatum, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

SYSMON ruft Indikatorwerte aus den Protokolldateien ab, die einschließlich des Start- und Beendigungsdatums liegen.

Die Verwendung dieser Methode entspricht dem Zugriff auf die Eigenschaften [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) und [**SystemMonitor.LogViewStop.**](systemmonitor-logviewstop.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





