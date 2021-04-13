---
title: Systemmonitor. setlogviewrange-Methode
description: Legt das Startdatum fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Setlogviewrange-Methode (Sysmon)
- Setlogviewrange-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", setlogviewrange-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391703"
---
# <a name="systemmonitorsetlogviewrange-method"></a>Systemmonitor. setlogviewrange-Methode

Legt das Startdatum fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartTime* \[ in\]
</dt> <dd>

Das Startdatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.

</dd> <dt>

*Stoppzeit* \[ in\]
</dt> <dd>

Das Enddatum, das verwendet wird, um die Werte aus den Protokolldateien abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sysmon Ruft Werte aus den Protokolldateien ab, die in den Anfangs-und Enddatums Angaben (einschließlich) fallen.

Wenn Sie kein Startdatum angeben oder wenn Sie das Startdatum auf einen Datumswert festlegen, der außerhalb des Bereichs der in den Protokolldateien gefundenen Datumswerte liegt, wird der Wert von sysmon in den frühesten in den Protokolldateien gefundenen Datumswert geändert. Wenn der Startwert größer als der Endzeit Wert ist, ändert sysmon den Startwert so, dass er mit dem Wert des Endwerts identisch ist.

Wenn Sie keinen Endwert angeben oder den Wert für die Beendigung auf einen Datumswert festlegen, der nach dem letzten in der Protokolldatei befindlichen Datum liegt, ändert sysmon den Wert in den letzten Datumswert, der in den Protokolldateien gefunden wurde. Wenn der Wert für die Beendigung kleiner ist als der Wert für die Beendigung, ändert sysmon den Endzeit Wert, sodass er dem Wert des Startwerts entspricht.

Wenn Sie ein Start-und ein Enddatum angeben, sollten Sie die Datumsangaben vor dem Festlegen von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)angeben. Wenn Sie die Datumsangaben nach dem Festlegen von **Systemmonitor. DataSourceType** festlegen, wird nur der erste Leistungsindikatoren aus der Protokolldatei abgerufen.

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

[**Systemmonitor. getlogviewrange**](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





