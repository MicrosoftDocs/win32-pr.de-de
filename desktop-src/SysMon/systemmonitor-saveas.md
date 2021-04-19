---
title: Systemmonitor. SaveAs-Methode
description: Speichert die Werte der Werte in der Diagramm Ansicht in einer Protokolldatei.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs-Methode (Sysmon)
- SaveAs-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", SaveAs-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345288"
---
# <a name="systemmonitorsaveas-method"></a>Systemmonitor. SaveAs-Methode

Speichert die Werte der Werte in der Diagramm Ansicht in einer Protokolldatei.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Dateipfad der Protokolldatei. Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben. Die Namen Erweiterung der Protokolldatei muss ". TSV" oder ". htm" lauten. Wenn ein Ordner im Pfad nicht vorhanden ist, wird er von sysmon erstellt. Wenn die Datei vorhanden ist, wird die Datei überschrieben. Sysmon wendet die Standard-ACLs aus dem übergeordneten Verzeichnis an.

</dd> <dt>

*filetype* \[ in\]
</dt> <dd>

Das Format der in der Protokolldatei gespeicherten Counter-Daten. Sie können entweder [**SysmonFileType.sysmonfilehtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) oder **SysmonFileType.sysmonfiletsv** angeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nur die in der Diagramm Ansicht sichtbaren Zählerdaten werden gespeichert (Informationen zur tatsächlichen Anzahl gespeicherter Datenpunkte finden Sie unter [**Systemmonitor. datapointcount**](systemmonitor-datapointcount.md)).

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

[**Systemmonitor. relog**](systemmonitor-relog.md)
</dt> </dl>

 

 





