---
title: Exec (aktiongroup)-Element
description: Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Exec-Element Taskplaner
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106364296"
---
# <a name="exec-actiongroup-element"></a>Exec (aktiongroup)-Element

Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

Das **exec** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                         | Abgeleitet von                                                       | BESCHREIBUNG                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md) | [**Aktions sType**](taskschedulerschema-actionstype-complextype.md) | Enthält die Aktionen, die vom Task ausgeführt werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | type       | BESCHREIBUNG                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumente**](taskschedulerschema-arguments-exectype-element.md)               | **string** | Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind.<br/>                               |
| [**Get-Help**](taskschedulerschema-command-exectype-element.md)                   | **string** | Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | Zeichenfolge     | Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.<br/> |



## <a name="attributes"></a>Attributes



| Name | type       | BESCHREIBUNG                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **string** | Der Bezeichner der Aktion, die von der Aufgabe ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Die oben aufgeführten untergeordneten Elemente werden durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.

Bei der Skript Entwicklung wird eine Ausführungs Aktion vom [**execaction**](execaction.md) -Objekt definiert.

Bei der C++-Entwicklung wird eine Ausführungs Aktion von der [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) -Schnittstelle definiert.

Wenn Umgebungsvariablen in den Elementen [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md)oder [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) verwendet werden, werden die Werte der Umgebungsvariablen zwischengespeichert und verwendet, wenn die Taskeng.exe (Task-Engine) gestartet wird. Änderungen an den Umgebungsvariablen, die nach dem Start der Task-Engine auftreten, werden von der Task-Engine nicht verwendet.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Ereignis Auslösers verwendet, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





