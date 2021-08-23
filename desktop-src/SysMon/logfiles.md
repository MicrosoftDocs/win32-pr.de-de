---
title: LogFiles-Objekt (Isysmon.h)
description: Verwenden Sie diese Klasse, um eine Sammlung von Protokolldateien zu verwalten, die Leistungsindikatordaten enthalten. Um dieses Objekt abzurufen, rufen Sie SystemMonitor.LogFiles auf.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- LogFiles-Objekt SysMon
- LogFiles-Objekt SysMon , beschrieben
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a0890acdf656c807ae3bcb275012bd56a4711a114547f750f04fd8d875fc68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883148"
---
# <a name="logfiles-object"></a>LogFiles-Objekt

Verwenden Sie diese Klasse, um eine Sammlung von Protokolldateien zu verwalten, die Leistungsindikatordaten enthalten.

Um dieses Objekt abzurufen, rufen Sie [**SystemMonitor.LogFiles auf.**](systemmonitor-logfiles.md)

## <a name="members"></a>Member

Das **LogFiles-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **LogFiles-Objekt** verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Hinzufügen**](systemmonitor-logfiles-add.md)       | Fügt der [**Auflistung eine LogFileItem-Instanz**](logfileitem.md) hinzu.<br/>      |
| [**Entfernen**](systemmonitor-logfiles-remove.md) | Entfernt eine [**LogFileItem-Instanz**](logfileitem.md) aus der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **LogFiles-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                 | BESCHREIBUNG                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Anzahl**](systemmonitor-logfiles-count.md)<br/> | Ruft die Anzahl der [**LogFileItem-Instanzen**](logfileitem.md) in der Auflistung ab.<br/>  |
| [**Element**](systemmonitor-logfiles-item.md)<br/>   | Ruft die angegebene [**LogFileItem-Instanz**](logfileitem.md) aus der Auflistung ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Damit SYSMON Leistungsindikatoren aus einer Protokolldatei anzeigen kann, legen Sie [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonLogFiles fest.**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants) Nachdem Sie die Protokolldateien zur Sammlung hinzugefügt haben, geben Sie mithilfe der [**Counters-Auflistung**](counters.md) die Leistungsindikatordaten an, die Sie aus den Protokolldateien lesen möchten. Wenn **SystemMonitor.DataSourceType** auf **DataSourceTypeConstants.sysmonLogFiles** festgelegt ist, werden die Protokolldateien von SYSMON bei jedem Hinzufügen einer Protokolldatei oder eines Leistungsindikators zu den jeweiligen Sammlungen erneutsammpelt.

**Vor der Windows Vista:** Sie können der Protokolldateisammlung keine Protokolldateien hinzufügen, wenn der Wert von [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) aufDataSourceTypeConstants.sys [**MonLogFiles festgelegt ist.**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants) [](systemmonitor-logfiles.md) Legen Sie **zuerst SystemMonitor.DataSourceType** auf **DataSourceTypeConstants.sysmonNullDataSource** fest, fügen Sie Ihre Protokolldateien und Leistungsindikatoren hinzu, und legen Sie **dann SystemMonitor.DataSourceType** auf **DataSourceTypeConstants.sysmonLogFiles fest.**

Die [**Eigenschaften SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) und [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) geben den Bereich der Stichprobenwerte aus den Protokolldateien für das Diagramm an. SYSMON erstellt nur einen Diagrammwert von Daten aus der Protokolldatei (die Diagrammansicht führt keinen Bildlauf durch, wie es beim Diagramm der aktuellen Aktivität des Computers der Fall ist). Wenn die Stichprobendaten das überschreiten, was in einer einzelnen Diagrammansicht angezeigt werden kann, komprimiert SYSMON die Stichprobendaten (jeder Diagrammpunkt stellt den Durchschnitt mehrerer stichprobenisierter Werte dar), um alle Stichprobendaten aus den Protokolldateien im Diagramm zu erfüllen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





