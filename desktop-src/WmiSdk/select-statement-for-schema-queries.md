---
description: Schema Daten Abfragen verwenden die SELECT-Anweisung mit einer ähnlichen Syntax wie bei Daten Abfragen.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: SELECT-Anweisung für Schema Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217954"
---
# <a name="select-statement-for-schema-queries"></a>SELECT-Anweisung für Schema Abfragen

Schema Daten Abfragen verwenden die SELECT-Anweisung mit einer ähnlichen Syntax wie bei [Daten Abfragen](select-statement-for-data-queries.md). Der Unterschied besteht in der Verwendung einer speziellen Klasse mit dem Namen "Meta \_ Class", die die Abfrage als Schema Abfrage bezeichnet.

Im folgenden Beispiel werden alle Klassendefinitionen angefordert, die sich innerhalb des aktuellen Namespace befinden.


```sql
SELECT * FROM meta_class
```



Schema Abfragen unterstützen nur " \* ". Um den Gültigkeitsbereich der zurückgegebenen Definitionen einzuschränken, kann ein Anbieter eine WHERE-Klausel hinzufügen, die eine bestimmte Klasse angibt.

Im folgenden Beispiel wird gezeigt, wie eine WHERE-Klausel hinzugefügt wird, um eine bestimmte Klasse anzugeben.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



Die spezielle Eigenschaft, die **\_ \_ als bezeichnet wird, identifiziert die** Zielklasse für eine Schema Abfrage. Beachten Sie, dass der ISA-Operator mit der **\_ \_ this** -Eigenschaft verwendet werden muss, um Definitionen für die Unterklassen der Zielklasse anzufordern. Die vorherige Abfrage gibt die Definition für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse und Definitionen für alle zugehörigen Unterklassen zurück.

Im folgenden Beispiel wird gezeigt, wie eine Klassendefinition für eine einzelne Klasse mithilfe der- **\_ \_ Klassen** System Eigenschaft angefordert wird.


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Diese Abfrage entspricht dem Aufrufen der [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode oder der [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode, wobei der Objekt Pfad Parameter auf "Win32 \_ LogicalDisk" festgelegt ist.

Das folgende VBScript-Codebeispiel ruft alle untergeordneten Klassen einer WMI-Klasse der obersten Ebene ab. Die \_ \_ WMI-System Eigenschaft der Dynastie enthält den Namen der Klasse der obersten Ebene, von der eine Klasse abgeleitet wird, mit der Sie alle Klassen in einem Namespace abrufen können, die von einer Klasse der obersten Ebene abgeleitet werden, einschließlich dieser Klasse.


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



Das folgende VBScript Ruft eine unmittelbare untergeordnete Klasse für eine WMI-Klasse ab.


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



Das folgende VBScript Ruft die Klassen der obersten Ebene ab. Für alle Klassen der obersten Ebene in einem WMI-Namespace \_ \_ ist die System Eigenschaft "Superclass" NULL. Daher ist es möglich, die Klassen der obersten Ebene abzurufen, indem Sie nach einer NULL-Superclass suchen.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
