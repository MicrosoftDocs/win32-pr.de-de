---
title: Systemmonitor. relog-Methode
description: Protokolliert die Daten des Zählers erneut in einer neuen Datei. Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu verringern.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Relog-Methode (Sysmon)
- Relog-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", Methode "relog"
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103418"
---
# <a name="systemmonitorrelog-method"></a>Systemmonitor. relog-Methode

Protokolliert die Daten des Zählers erneut in einer neuen Datei. Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu verringern.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Dateipfad der Protokolldatei. Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben. Die Namen Erweiterung der Protokolldatei muss entweder ". BLG", ". TSV" oder ". csv" lauten. Wenn ein Ordner im Pfad nicht vorhanden ist, wird er von sysmon erstellt. Wenn die Datei vorhanden ist, wird die Datei überschrieben. Sysmon wendet die Standard-ACLs aus dem übergeordneten Verzeichnis an.

</dd> <dt>

*filetype* \[ in\]
</dt> <dd>

Das Format der in der Protokolldatei gespeicherten Counter-Daten. Sie können entweder [**SysmonFileType.sysmonfileblg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonfilecsv** oder **SysmonFileType.sysmonfiletsv** angeben.

</dd> <dt>

*Filter* \[ in\]
</dt> <dd>

Anzahl der Abtastungen aus den alten Protokolldateien, die in der neuen Protokolldatei gespeichert werden sollen. Geben Sie 1 an, um jedes Beispiel aus den alten Dateien in den neuen Dateien zu speichern. Geben Sie 2 an, um eine von allen zwei Beispielen aus der alten Datei zu speichern. Geben Sie 3 an, um eine von allen drei Beispielen aus der alten Datei zu speichern. Und so weiter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode verwendet die Protokolldateien, die in der [**System Monitor. Logfiles**](systemmonitor-logfiles.md) -Auflistung enthalten sind, um die zählungdaten erneut zu protokollieren.

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

[**Systemmonitor. SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





