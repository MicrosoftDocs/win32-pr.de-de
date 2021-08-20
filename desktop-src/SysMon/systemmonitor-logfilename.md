---
title: SystemMonitor.LogFileName (Eigenschaft)
description: Ruft den Namen einer Protokolldatei ab, die als Quelle der im Systemmonitor angezeigten Leistungsindikatorwerte verwendet werden soll, oder legt diesen fest.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- LogFileName-Eigenschaft SysMon
- LogFileName-Eigenschaft SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , LogFileName-Eigenschaft
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
ms.openlocfilehash: 888ecf566dd30b12cde8e9105c987cf5f76afd3578ef9b8f4aee3b8d38e5710f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955538"
---
# <a name="systemmonitorlogfilename-property"></a>SystemMonitor.LogFileName (Eigenschaft)

Ruft den Namen einer Protokolldatei ab, die als Quelle der im Systemmonitor angezeigten Leistungsindikatorwerte verwendet werden soll, oder legt diesen fest.

> [!Note]  
> Diese Eigenschaft wurde durch die [**LogFiles-Eigenschaft veraltet**](systemmonitor-logfiles.md) gemacht.

 

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property LogFileName As String
```



## <a name="property-value"></a>Eigenschaftswert

Pfad zur Protokolldatei. Sie können einen absoluten, relativen oder UNC-Pfad angeben. Die Protokolldateinamenerweiterung muss entweder .csv, TSV oder BLG sein.

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp                                  | Bedingung                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System.Runtime.InteropServices.COMException** | Die angegebene Datei wurde nicht finden. Der Err.Number-Wert ist 0xC0000BD1. |
| **System.ArgumentException**                    | Sie dürfen keine leere Zeichenfolge angeben.                                    |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt den Protokolldateinamen aus dem ersten Member der [**LogFiles-Auflistung**](systemmonitor-logfiles.md) zurück.

Das Festlegen dieser Eigenschaft ist nicht mehr der Fall, wenn die [**LogFiles-Auflistung**](systemmonitor-logfiles.md) ein oder mehrere Member enthält.

Sie müssen das Logman.exe-Tool oder das MMC-Snap-In Perfmon.msc verwenden, um die Protokolldateien zu generieren, die Sie dieser Sammlung hinzufügen. Für Perfmon.msc befinden sich die Leistungsindikatorprotokolle unter **Leistungsprotokolle und -warnungen**. Weitere Informationen zur Verwendung von Logman.exe oder Perfmon.msc finden Sie unter Logman bzw. Using Performance (Leistung verwenden) im **Hilfe- und Supportcenter.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





