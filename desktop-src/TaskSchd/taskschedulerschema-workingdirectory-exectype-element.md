---
title: WorkingDirectory-Element (execType)
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
ms.openlocfilehash: 5a91908d5cd774f19f32a182934688dc899179d1abba967b7871a646efcfe042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513740"
---
# <a name="workingdirectory-exectype-element"></a>WorkingDirectory-Element (execType)

Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

Das **WorkingDirectory-Element** wird durch den komplexen [**execType-Typ**](taskschedulerschema-exectype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                      | Abgeleitet von                                                 | Beschreibung                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Gibt eine Aktion an, die einen Befehlszeilenvorgang ausführt.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird das Arbeitsverzeichnis durch die [**ExecAction.WorkingDirectory-Eigenschaft**](execaction-workingdirectory.md) angegeben.

Für die C++-Entwicklung wird das Arbeitsverzeichnis durch die [**IExecAction::WorkingDirectory-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Ausführungsaktion.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





