---
title: LogFiles.Add-Methode
description: Fügt der Auflistung eine Protokolldatei hinzu.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Hinzufügen der SysMon-Methode
- Hinzufügen der SysMon- und LogFiles-Methode
- LogFiles-Klasse SysMon , Add-Methode
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af01c5c7a1bbe16826457d7e1f8700df01876827c522a36db41f6c3843101d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882335"
---
# <a name="logfilesadd-method"></a>LogFiles.Add-Methode

Fügt der Auflistung eine Protokolldatei hinzu.

## <a name="syntax"></a>Syntax


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pathname* \[ In\]
</dt> <dd>

Pfad zur Protokolldatei. Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben. Die Protokolldateinamenerweiterung muss entweder .csv, TSV oder BLG sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen das Logman.exe-Tool oder das MMC-Snap-In Perfmon.msc verwenden, um die Protokolldateien zu generieren, die Sie dieser Sammlung hinzufügen. Für Perfmon.msc befinden sich die Leistungsindikatorprotokolle unter **Leistungsprotokolle und -warnungen**. Ausführliche Informationen zur Verwendung von Logman.exe oder Perfmon.msc finden Sie im **Hilfe- und Supportcenter** nach Logman bzw. Using Performance.

**Vor Windows Vista:** Sie können der [**Protokolldateisammlung**](systemmonitor-logfiles.md) keine Protokolldateien hinzufügen, wenn der Wert von [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)festgelegt ist. Legen Sie zunächst **SystemMonitor.DataSourceType** auf **DataSourceTypeConstants.sysmonNullDataSource** fest, fügen Sie Ihre Protokolldateien und Leistungsindikatoren hinzu, und legen Sie dann **SystemMonitor.DataSourceType** auf **DataSourceTypeConstants.sysmonLogFiles** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





