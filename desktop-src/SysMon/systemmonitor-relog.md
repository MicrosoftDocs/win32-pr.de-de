---
title: SystemMonitor.Relog-Methode
description: Erfasst die Indikatordaten erneut in einer neuen Datei. Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu reduzieren.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Relog-Methode SysMon
- Relog-Methode SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , Relog-Methode
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
ms.openlocfilehash: 73025a352ba3ec2e9ed113c59a7e04f98084495da834f83bf052c697833dd13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881727"
---
# <a name="systemmonitorrelog-method"></a>SystemMonitor.Relog-Methode

Erfasst die Indikatordaten erneut in einer neuen Datei. Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu reduzieren.

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

*fileName* \[ In\]
</dt> <dd>

Dateipfad der Protokolldatei. Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben. Die Protokolldateinamenerweiterung muss entweder .blg, .tsv oder .csv sein. Wenn ein Ordner im Pfad nicht vorhanden ist, erstellt SYSMON ihn. Wenn die Datei vorhanden ist, wird die Datei überschrieben. SYSMON wendet die Standard-ACLs aus dem übergeordneten Verzeichnis an.

</dd> <dt>

*fileType* \[ In\]
</dt> <dd>

Format der in der Protokolldatei gespeicherten Indikatordaten. Sie können entweder [**SysmonFileType.sysmonFileBlg,**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) **SysmonFileType.sysmonFileCsv** oder **SysmonFileType.sysmonFileTsv** angeben.

</dd> <dt>

*Filter* \[ In\]
</dt> <dd>

Anzahl der Beispiele aus den alten Protokolldateien, die in der neuen Protokolldatei gespeichert werden sollen. Geben Sie 1 an, um jedes Beispiel aus den alten Dateien in den neuen Dateien zu speichern. Geben Sie 2 an, um eines von zwei Stichproben aus der alten Datei zu speichern. Geben Sie 3 an, um eines von drei Beispielen aus der alten Datei zu speichern. Und so weiter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode verwendet die Protokolldateien, die in der [**SystemMonitor.LogFiles-Auflistung**](systemmonitor-logfiles.md) enthalten sind, um die Indikatordaten neu zu protokollieren.

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

[**SystemMonitor.SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





