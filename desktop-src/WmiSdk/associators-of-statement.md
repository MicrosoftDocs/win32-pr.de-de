---
description: Ruft alle Instanzen ab, die einer bestimmten Quellinstanz zugeordnet sind.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: ASSOCIATORS OF-Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af4b3d6455e81f87882bdd185ac7a8ef245f2d57c5d8f2c863f58d9c30c7b34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071580"
---
# <a name="associators-of-statement"></a>ASSOCIATORS OF-Anweisung

Die ASSOCIATORS OF-Anweisung ruft alle Instanzen ab, die einer bestimmten Quellinstanz zugeordnet sind. Die abgerufenen Instanzen werden als Endpunkte bezeichnet. Jeder Endpunkt wird so oft zurückgegeben, wie es Zuordnungen zwischen ihm und dem Quellobjekt gibt. Angenommen, es gibt die Instanzen A, B, X und Y. Es gibt zwei Zuordnungsinstanzen, eine, die A und X verknüpft, und eine andere, die B und Y verknüpft. Die folgende Abfrage gibt den einzelnen Endpunkt X zurück:


```sql
ASSOCIATORS OF {A}
```



Wenn jedoch eine weitere Zuordnung vorhanden ist, die A und X verknüpft, gibt die obige Abfrage zwei X-Endpunkte zurück.

Die grundlegende Syntax für die ASSOCIATORS OF-Anweisung lautet:

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Beachten Sie, dass die geschweiften Klammern Teil der Syntax sind. Jeder gültige Objektpfad kann für ObjectPath verwendet werden. Die Token innerhalb des Objektpfads dürfen keinen Leerraum enthalten. Beispielsweise gibt die Abfrage in der folgenden Liste Instanzen zurück, die dem angegebenen logischen Datenträger zugeordnet sind:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Wie bei der [SELECT-Anweisung](select-statement-for-data-queries.md)kann eine ASSOCIATORS OF-Anweisung eine [WHERE-Klausel](where-clause.md)enthalten, aber die WHERE-Klausel für eine ASSOCIATORS OF-Anweisung unterscheidet sich stark von der SELECT-AnweisungWHERE-Klausel.

Die [WHERE-Klausel](where-clause.md) der ASSOCIATORS OF-Anweisung kann eines oder mehrere der folgenden vordefinierten Schlüsselwörter und deren Werte enthalten:


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



Beachten Sie, dass die optionalen Unterclausen nicht durch Kommas getrennt sind.

Das **Schlüsselwort AssocClass** gibt an, dass die zurückgegebenen Endpunkte der Quelle über die angegebene Klasse oder eine ihrer abgeleiteten Klassen zugeordnet werden müssen. Beispielsweise gibt die Abfrage in der folgenden Liste nur Endpunkte zurück, die der Quelle über die [**Win32 \_ SystemDevices-Zuordnungsklasse**](/windows/desktop/CIMWin32Prov/win32-systemdevices) oder eine ihrer abgeleiteten Klassen zugeordnet sind:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Das **ClassDefsOnly-Schlüsselwort** gibt an, dass die -Klausel ein Resultset von Klassendefinitionsobjekten anstelle tatsächlicher Instanzen der Klassen zurückgibt. Diese Objekte sind die Definitionen von Klassen, zu denen die Endpunktinstanzen gehören. Beispielsweise gibt die Abfrage in der folgenden Liste Definitionen für die [**Klassen Win32 \_ Directory**](/windows/desktop/CIMWin32Prov/win32-directory) und [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) zurück:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

Die Schlüsselwörter **ClassDefsOnly** und **ResultClass** schließen sich gegenseitig aus. Die gemeinsame Verwendung verursacht einen ungültigen Abfragefehler.

Das **RequiredAssocQualifier-Schlüsselwort** gibt an, dass die zurückgegebenen Endpunkte dem Quellobjekt über eine Zuordnungsklasse zugeordnet werden müssen, die den angegebenen Qualifizierer enthält. Diese Art der Filterung wird verwendet, um breite Bereiche von Endpunkten zu entfernen, es sei denn, die Endpunkte werden dem Ziel über einen bestimmten Satz von markierten Zuordnungsklassen zugeordnet. Beispielsweise gibt die Abfrage in der folgenden Liste Endpunktinstanzen zurück, wenn die Zuordnungsklasse einen Qualifizierer namens **Association** enthält.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Das **RequiredQualifier-Schlüsselwort** gibt an, dass die zurückgegebenen Endpunkte, die dem Quellobjekt zugeordnet sind, den angegebenen Qualifizierer enthalten müssen. Das **RequiredQualifier-Schlüsselwort** kann verwendet werden, um bestimmte Typen von Instanzen in das Resultset aufzunehmen. Beispielsweise gibt die Abfrage in der folgenden Liste Endpunktinstanzen zurück, die einen Qualifizierer namens [**Gebietsschema**](swbemobjectpath-locale.md)enthalten.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Das **ResultClass-Schlüsselwort** gibt an, dass die zurückgegebenen Endpunkte, die dem Quellobjekt zugeordnet sind, zu der angegebenen Klasse gehören oder von dieser abgeleitet werden müssen. Beispielsweise gibt die Abfrage in der folgenden Liste Endpunktinstanzen zurück, die von der [**CIM \_ Directory-Klasse**](/windows/desktop/CIMWin32Prov/cim-directory) abgeleitet sind:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

Die Schlüsselwörter **ClassDefsOnly** und **ResultClass** schließen sich gegenseitig aus. Die gemeinsame Verwendung verursacht einen ungültigen Abfragefehler.

Das **ResultRole-Schlüsselwort** gibt an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quellobjekt spielen müssen. Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweiseigenschaft vom Typ [ref](references.md). Beispielsweise kann das **ResultRole-Schlüsselwort** verwendet werden, um alle Endpunkte abzurufen, die die **GroupComponent-Eigenschaft** in ihrer Zuordnung zu einem Quellobjekt haben, wie die folgende Abfrage veranschaulicht.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Das **Role-Schlüsselwort** gibt an, dass die zurückgegebenen Endpunkte an einer Zuordnung zum Quellobjekt beteiligt sind, bei dem das Quellobjekt eine bestimmte Rolle spielt. Die Rolle wird durch die angegebene Eigenschaft definiert, eine Verweiseigenschaft vom Typ **ref**. Beispielsweise kann das **Role-Schlüsselwort** verwendet werden, um alle Endpunkte abzurufen, die einem Quellobjekt zugeordnet sind, das über die **GroupComponent-Eigenschaft** verfügt, wie die folgende Abfrage veranschaulicht.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Abfrage:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Ergebnisse:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Komplexe Abfragen können "And" oder "Or" nicht verwenden, um Schlüsselwörter für ASSOCIATORS OF- und [REFERENCES OF-Anweisungen](references-of-statement.md) zu trennen. Darüber hinaus ist das Gleichheitszeichen der einzige gültige Operator, der in solchen Abfragen verwendet werden kann. Beispielsweise ist die folgende Abfrage gültig:

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Die nächsten Beispiele sind ungültig. Im ersten Beispiel wird nicht das Gleichheitszeichen verwendet, und im zweiten Beispiel wird fälschlicherweise versucht, das **AND-Schlüsselwort** zu verwenden.

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
