---
title: Logfiles. Add-Methode
description: Fügt der Auflistung eine Protokolldatei hinzu.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Methode hinzufügen (Sysmon)
- Add-Methode (Sysmon), Logfiles-Klasse
- Logfiles-Klasse sysmon, Methode hinzufügen
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
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103827"
---
# <a name="logfilesadd-method"></a>Logfiles. Add-Methode

Fügt der Auflistung eine Protokolldatei hinzu.

## <a name="syntax"></a>Syntax


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfadname* \[ in\]
</dt> <dd>

Der Pfad zur Protokolldatei. Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben. Der Name der Protokolldatei Erweiterung muss ". csv", ". TSV" oder ". BLG" lauten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen das-Logman.exe Tool oder das MMC-Snap-in "Perfmon. msc" verwenden, um die Protokolldateien zu generieren, die Sie dieser Sammlung hinzufügen. Bei Perfmon. msc befinden sich die Leistungs Protokoll Protokolle unter **Leistungsprotokolle und-Warnungen**. Ausführliche Informationen zur Verwendung von Logman.exe oder Perfmon. msc finden Sie, indem Sie im **Hilfe-und Support Center** nach logman suchen oder die Leistung verwenden.

**Vor Windows Vista:** Sie können der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) keine Protokolldateien hinzufügen, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonlogfiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)festgelegt ist. Legen Sie zunächst **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonnulldatasource** fest, fügen Sie die Protokolldateien und Leistungsindikatoren hinzu, und legen Sie **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonlogfiles** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**Logfileitem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





