---
title: LogFiles-Objekt (Isysmon.h)
description: Verwenden Sie diese Klasse, um eine Auflistung von einer oder mehreren Protokolldateien zu verwalten, die Leistungsdaten enthalten. Um dieses Objekt abzurufen, rufen Sie Systemmonitor. Logfiles auf.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- Logfiles-Objekt (Sysmon)
- Logfiles-Objekt (Sysmon), beschrieben
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
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475051"
---
# <a name="logfiles-object"></a>Logfiles-Objekt

Verwenden Sie diese Klasse, um eine Auflistung von einer oder mehreren Protokolldateien zu verwalten, die Leistungsdaten enthalten.

Um dieses Objekt abzurufen, rufen Sie [**Systemmonitor. Logfiles**](systemmonitor-logfiles.md)auf.

## <a name="members"></a>Member

Das **Logfiles** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Logfiles** -Objekt verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Eren**](systemmonitor-logfiles-add.md)       | Fügt der Auflistung eine [**logfileitem**](logfileitem.md) -Instanz hinzu.<br/>      |
| [**Aufgeh**](systemmonitor-logfiles-remove.md) | Entfernt eine [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Logfiles** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                 | BESCHREIBUNG                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Countdown**](systemmonitor-logfiles-count.md)<br/> | Ruft die Anzahl der [**logfileitem**](logfileitem.md) -Instanzen in der Auflistung ab.<br/>  |
| [**Element**](systemmonitor-logfiles-item.md)<br/>   | Ruft die angegebene [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Legen Sie [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonlogfiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)fest, damit die Leistungsindikatoren von sysmon aus einer Protokolldatei angezeigt werden. Nachdem Sie der Auflistung die Protokolldateien hinzugefügt haben, geben Sie mithilfe der [**Zähler**](counters.md) Sammlung die Indikatorendaten an, die Sie aus den Protokolldateien lesen möchten. Beachten Sie Folgendes: Wenn **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonlogfiles** festgelegt ist, werden die Protokolldateien von sysmon jedes Mal neu erstellt, wenn Sie eine Protokolldatei oder einen Indikatoren zu den jeweiligen Sammlungen hinzufügen.

**Vor Windows Vista:** Sie können der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) keine Protokolldateien hinzufügen, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonlogfiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)festgelegt ist. Legen Sie zunächst **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonnulldatasource** fest, fügen Sie die Protokolldateien und Leistungsindikatoren hinzu, und legen Sie **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonlogfiles** fest.

Die Eigenschaften [**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md) und [**Systemmonitor. logviewstoppt**](systemmonitor-logviewstop.md) geben den Bereich der Stichprobenwerte aus den zu Graphen enden Protokolldateien an. In sysmon-Diagrammen wird nur eine Ansicht der Daten aus der Protokolldatei angezeigt (in der Diagramm Ansicht wird kein Bildlauf durchführen, wie dies beim Anzeigen der aktuellen Aktivität des Computers der Fall ist). Wenn die Stichprobendaten überschreiten, was in einer einzelnen Diagramm Ansicht angezeigt werden kann, komprimiert sysmon die Stichprobendaten (jeder Diagramm Punkt steht für den Durchschnitt mehrerer Stichprobenwerte), damit alle Stichprobendaten aus den Protokolldateien im Diagramm abgeglichen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





