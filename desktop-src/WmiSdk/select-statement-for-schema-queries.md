---
description: Schemadatenabfragen verwenden die SELECT-Anweisung mit einer Syntax ähnlich der für Datenabfragen.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: SELECT-Anweisung für Schemaabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd08cffa3fccc9a8cc2bf50452dcefcc1b7bfc0a62e512069b2db098bc6d13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315674"
---
# <a name="select-statement-for-schema-queries"></a>SELECT-Anweisung für Schemaabfragen

Schemadatenabfragen verwenden die SELECT-Anweisung mit einer Syntax ähnlich der für [Datenabfragen.](select-statement-for-data-queries.md) Der Unterschied besteht in der Verwendung einer speziellen Klasse namens "meta class", die die Abfrage \_ als Schemaabfrage identifiziert.

Im folgenden Beispiel werden alle Klassendefinitionen innerhalb des aktuellen Namespaces anforderungen.


```sql
SELECT * FROM meta_class
```



Schemaabfragen unterstützen nur " \* ". Ein Anbieter kann eine WHERE-Klausel hinzufügen, die eine bestimmte Klasse angibt, um den Gültigkeitsbereich der zurückgegebenen Definitionen zu spezifizieren.

Das folgende Beispiel zeigt, wie eine WHERE-Klausel hinzugefügt wird, um eine bestimmte Klasse anzugeben.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



Die spezielle Eigenschaft namens **\_ \_ identifiziert** die Zielklasse für eine Schemaabfrage. Beachten Sie, dass der ISA-Operator mit dieser Eigenschaft verwendet werden muss, um Definitionen für die Unterklassen der Zielklasse an fordern zu können. **\_ \_** Die vorherige Abfrage gibt die Definition für die [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) und Definitionen für alle ihre Unterklassen zurück.

Das folgende Beispiel zeigt, wie sie eine Klassendefinition für eine einzelne Klasse mithilfe der **\_ \_ Class-Systemeigenschaft** anfordern.


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Diese Abfrage entspricht dem Aufrufen der [**IWbemServices::GetObject-**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices::GetObjectAsync-Methode,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) bei der der Objektpfadparameter auf "Win32 \_ LogicalDisk" festgelegt ist.

Im folgenden VBScript-Codebeispiel werden alle untergeordneten Klassen einer WMI-Klasse der obersten Ebene abgerufen. Die \_ WMI-Systemeigenschaft Desi- enthält den Namen der Klasse der obersten Ebene, von der eine Klasse abgeleitet wird, mit der Sie alle Klassen in einem Namespace abrufen können, der von einer Klasse der obersten Ebene abgeleitet wurde, einschließlich dieser \_ Klasse.


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



Das folgende VBScript ruft eine unmittelbar untergeordnete Klasse für eine WMI-Klasse ab.


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



Das folgende VBScript ruft Klassen der obersten Ebene ab. Für alle Klassen der obersten Ebene in einem WMI-Namespace ist die \_ \_ Superclass-Systemeigenschaft NULL. Daher ist es möglich, die Klassen der obersten Ebene abzurufen, indem Sie nach einer NULL-Übergeordneten Klasse suchen.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
