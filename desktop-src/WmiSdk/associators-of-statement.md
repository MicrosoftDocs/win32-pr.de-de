---
description: Ruft alle-Instanzen ab, die einer bestimmten Quell Instanz zugeordnet sind.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: Assoziatoren der Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347638"
---
# <a name="associators-of-statement"></a>Assoziatoren der Anweisung

Die ASSOCIATORS of-Anweisung ruft alle-Instanzen ab, die einer bestimmten Quell Instanz zugeordnet sind. Die abgerufenen Instanzen werden als Endpunkte bezeichnet. Jeder Endpunkt wird so oft zurückgegeben, wie es Zuordnungen zwischen ihm und dem Quell Objekt gibt. Nehmen wir beispielsweise an, dass die Instanzen a, B, X und Y vorhanden sind. Es sind zwei Assoziations Instanzen vorhanden: eine, die a und X verknüpft, und eine andere, die B und Y verknüpft. Die folgende Abfrage gibt den einzelnen Endpunkt X zurück:


```sql
ASSOCIATORS OF {A}
```



Wenn jedoch eine weitere Zuordnung vorhanden ist, die A und X verknüpft, gibt die obige Abfrage zwei X-Endpunkte zurück.

Die grundlegende Syntax für die assoziatoren der-Anweisung lautet:

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Beachten Sie, dass die geschweiften Klammern Teil der Syntax sind. Ein gültiger Objekt Pfad kann für objectPath verwendet werden. Die Token im Objekt Pfad dürfen keine Leerzeichen enthalten. Beispielsweise gibt die Abfrage in der folgenden Liste-Instanzen zurück, die dem angegebenen logischen Datenträger zugeordnet sind:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Wie bei der [SELECT-Anweisung](select-statement-for-data-queries.md)können auch assoziatoren der-Anweisung eine [WHERE-Klausel](where-clause.md)enthalten, aber die WHERE-Klausel für einen assoziators der-Anweisung unterscheidet sich stark von der SELECT-Klausel der-Anweisung.

Die [WHERE-Klausel](where-clause.md) der ASSOCIATORS of-Anweisung kann ein oder mehrere der folgenden vordefinierten Schlüsselwörter und ihre Werte enthalten:


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



Beachten Sie, dass die optionalen Unterklauseln nicht durch Kommas voneinander getrennt sind.

Das Schlüsselwort " **AssocClass** " gibt an, dass die zurückgegebenen Endpunkte über die angegebene Klasse oder eine der abgeleiteten Klassen mit der Quelle verknüpft werden müssen. Die Abfrage in der folgenden Liste gibt z. b. nur Endpunkte zurück, die der Quelle über die [**Win32 \_ systemdevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) -Zuordnungs Klasse oder eine der abgeleiteten Klassen zugeordnet sind:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Das **classdefsonly** -Schlüsselwort gibt an, dass die-Klausel ein Resultset von Klassen Definitions Objekten anstelle tatsächlicher Instanzen der Klassen zurückgibt. Bei diesen Objekten handelt es sich um die Definitionen von Klassen, zu denen die Endpunkt Instanzen gehören. Die Abfrage in der folgenden Liste gibt beispielsweise Definitionen für das [**Win32- \_ Verzeichnis**](/windows/desktop/CIMWin32Prov/win32-directory) und die [**Win32- \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) -Klassen zurück:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

Die Schlüsselwörter **classdefsonly** und **resultClass** schließen sich gegenseitig aus. Die gemeinsame Verwendung verursacht einen ungültigen Abfrage Fehler.

Das "Requirements **dassocqualifier** "-Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte dem Quell Objekt über eine Association-Klasse zugeordnet werden müssen, die den angegebenen Qualifizierer enthält. Dieser Filtertyp wird verwendet, um große Bereiche von Endpunkten auszuschließen, es sei denn, die Endpunkte werden dem Ziel über einen bestimmten Satz von markierten Zuordnungs Klassen zugeordnet. Die Abfrage in der folgenden Liste gibt beispielsweise Endpunkt Instanzen zurück, wenn die Association-Klasse einen Qualifizierer namens **Association** enthält.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Das "Requirements **dqualifier** "-Schlüsselwort gibt an, dass die dem Quell Objekt zugeordneten zurückgegebenen Endpunkte den angegebenen Qualifizierer einschließen müssen Das "Requirements **dqualifier** "-Schlüsselwort kann verwendet werden, um bestimmte Typen von Instanzen in das Resultset einzubeziehen. Die Abfrage in der folgenden Liste gibt beispielsweise Endpunkt Instanzen zurück, die einen Qualifizierer namens [**locale**](swbemobjectpath-locale.md)enthalten.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Das **resultClass** -Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte, die dem Quell Objekt zugeordnet sind, zu der angegebenen Klasse gehören bzw. davon abgeleitet werden müssen. Die Abfrage in der folgenden Liste gibt beispielsweise Endpunkt Instanzen zurück, die von der [**CIM- \_ Verzeichnis**](/windows/desktop/CIMWin32Prov/cim-directory) Klasse abgeleitet sind:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

Die Schlüsselwörter **classdefsonly** und **resultClass** schließen sich gegenseitig aus. Die gemeinsame Verwendung verursacht einen ungültigen Abfrage Fehler.

Das **RESULTROLE** -Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quell Objekt spielen müssen. Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweis Eigenschaft vom Typ [ref](references.md). Beispielsweise kann das **RESULTROLE** -Schlüsselwort verwendet werden, um alle Endpunkte abzurufen, die die **GroupComponent** -Eigenschaft in ihrer Zuordnung zu einem Quell Objekt aufweisen, wie die folgende Abfrage veranschaulicht.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Das **Role** -Schlüsselwort gibt an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quell Objekt beteiligt sind, in dem das Quell Objekt eine bestimmte Rolle spielt. Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweis Eigenschaft vom Typ **ref**. Beispielsweise kann das **Role** -Schlüsselwort verwendet werden, um alle Endpunkte abzurufen, die einem Quell Objekt zugeordnet sind, das die **GroupComponent** -Eigenschaft hat, wie die folgende Abfrage veranschaulicht.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Such
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Folgen
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Komplexe Abfragen können nicht "and" oder "or" verwenden, um Schlüsselwörter für assoziatoren von und [verweisen](references-of-statement.md) auf-Anweisungen zu trennen. Außerdem ist das Gleichheitszeichen der einzige gültige Operator, der in solchen Abfragen verwendet werden kann. Beispielsweise ist die folgende Abfrage gültig:

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Die folgenden Beispiele sind ungültig. Im ersten Beispiel wird nicht das Gleichheitszeichen verwendet, und das zweite Beispiel versucht fälschlicherweise, das **-** Schlüsselwort und das-Schlüsselwort zu verwenden.

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
