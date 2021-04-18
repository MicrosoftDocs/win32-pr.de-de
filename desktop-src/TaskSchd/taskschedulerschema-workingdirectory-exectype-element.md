---
title: WorkingDirectory (exectype)-Element
description: Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- WorkingDirectory-Element Taskplaner
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341039"
---
# <a name="workingdirectory-exectype-element"></a>WorkingDirectory (exectype)-Element

Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

Das **WorkingDirectory** -Element wird durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                      | Abgeleitet von                                                 | BESCHREIBUNG                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**exectype**](taskschedulerschema-exectype-complextype.md) | Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird das Arbeitsverzeichnis von der [**execaction. WorkingDirectory**](execaction-workingdirectory.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird das Arbeitsverzeichnis durch die [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Ausführungs Aktion.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





