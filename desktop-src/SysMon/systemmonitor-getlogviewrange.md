---
title: Systemmonitor. getlogviewrange-Methode
description: Ruft das Startdatum ab, das zum Abrufen von Counter-Werten aus den Protokolldateien verwendet wird.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Getlogviewrange-Methode (Sysmon)
- Getlogviewrange-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", getlogviewrange-Methode
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
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517798"
---
# <a name="systemmonitorgetlogviewrange-method"></a>Systemmonitor. getlogviewrange-Methode

Ruft das Startdatum ab, das zum Abrufen von Counter-Werten aus den Protokolldateien verwendet wird.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartTime* \[ vorgenommen\]
</dt> <dd>

Das Startdatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.

</dd> <dt>

*Stoppzeit* \[ vorgenommen\]
</dt> <dd>

Das Enddatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sysmon Ruft Werte aus den Protokolldateien ab, die in den Anfangs-und Enddatums Angaben (einschließlich) fallen.

Die Verwendung dieser Methode ist mit dem Zugriff auf die Eigenschaften [**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md) und [**Systemmonitor. logviewstoppt**](systemmonitor-logviewstop.md) identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> <dt>

[**Systemmonitor. setlogviewrange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





