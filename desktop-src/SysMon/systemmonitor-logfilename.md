---
title: Systemmonitor. LogFileName (Eigenschaft)
description: Ruft den Namen einer Protokolldatei ab, die als Quelle der im System Monitor angezeigten Indikatorenwerte verwendet werden soll, oder legt ihn fest.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- LogFileName-Eigenschaft (Sysmon)
- LogFileName-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", LogFileName (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391935"
---
# <a name="systemmonitorlogfilename-property"></a>Systemmonitor. LogFileName (Eigenschaft)

Ruft den Namen einer Protokolldatei ab, die als Quelle der im System Monitor angezeigten Indikatorenwerte verwendet werden soll, oder legt ihn fest.

> [!Note]  
> Diese Eigenschaft wurde von der [**Logfiles**](systemmonitor-logfiles.md) -Eigenschaft als veraltet eingestuft.

 

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property LogFileName As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad zur Protokolldatei. Sie können einen absoluten, relativen oder UNC-Pfad angeben. Der Name der Protokolldatei Erweiterung muss ". csv", ". TSV" oder ". BLG" lauten.

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp                                  | Bedingung                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | Die angegebene Datei wurde nicht gefunden. Der Err. Number-Wert ist 0xc0000bd1. |
| **System.ArgumentException**                    | Sie dürfen keine leere Zeichenfolge angeben.                                    |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt den Namen der Protokolldatei aus dem ersten Member der [**Logfiles**](systemmonitor-logfiles.md) -Auflistung zurück.

Das Festlegen dieser Eigenschaft schlägt fehl, wenn die [**Logfiles**](systemmonitor-logfiles.md) -Auflistung mindestens ein Element enthält.

Sie müssen das-Logman.exe Tool oder das MMC-Snap-in "Perfmon. msc" verwenden, um die Protokolldateien zu generieren, die Sie dieser Sammlung hinzufügen. Bei Perfmon. msc befinden sich die Leistungs Protokoll Protokolle unter **Leistungsprotokolle und-Warnungen**. Ausführliche Informationen zur Verwendung von Logman.exe oder Perfmon. msc finden Sie, indem Sie im **Hilfe-und Support Center** nach logman suchen oder die Leistung verwenden.

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

[**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





