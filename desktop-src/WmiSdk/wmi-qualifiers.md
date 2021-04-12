---
description: WMI verfügt über mehrere Typen von Klassen-und Eigenschafts Qualifizierern. Qualifizierer können auch Änderungen ändern.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: WMI Qualifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215305"
---
# <a name="wmi-qualifiers"></a>WMI Qualifizierer

WMI verfügt über mehrere Typen von Klassen-und Eigenschafts [*Qualifizierern*](gloss-q.md). Qualifizierer können auch [*Änderungen ändern*](gloss-f.md). Die folgenden Typen von Qualifizierern und Varianten werden in WMI verwendet.

Der Name jedes Qualifizierers wird mit seinem Datentyp und einem Indikator darüber angezeigt, ob der Qualifizierer auf eine Klasse, eine Instanz, eine Eigenschaft oder eine Methode angewendet werden kann. Für Qualifizierer, wie z. b. **Association** (unter [Meta-Qualifizierer](meta-qualifiers.md)erläutert), gibt es eine implizite Verwendungs Regel, dass auch der Meta-Qualifizierer Die implizite Verwendungs Regel für die **Aggregations** Qualifizierer ist beispielsweise, dass der **Association** -Qualifizierer ebenfalls vorhanden sein muss.



| Qualifizierertyp                              | BESCHREIBUNG                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Analysen](meta-qualifiers.md)                 | Verfeinert die Definition von Meta-Konstrukten durch die Verdeutlichung der tatsächlichen Verwendung einer Klassen-oder Eigenschaften Deklaration.                          |
| [Optional](optional-qualifiers.md)         | Adress Situationen, die nicht von allen CIM-kompatiblen Implementierungen gemeinsam sind.                                                                 |
| [Qualifizierervarianten](qualifier-flavors.md)  | Bietet weitere Informationen über einen Qualifizierer, z. b. ob eine abgeleitete Klasse oder eine Instanz den ursprünglichen Wert des Qualifizierers überschreiben kann. |
| [Standard](standard-qualifiers.md)         | Unterstützt die Beschreibungen, die von allen CIM-kompatiblen Implementierungen behandelt werden müssen.                                                         |
| [WMI-spezifisch](wmi-specific-qualifiers.md) | Beschreibt die für WMI spezifischen Qualifizierer, z. b. Qualifizierer für die Leistungs                                                   |



 

Weitere Informationen zum Anwenden von Qualifizierern auf ihre WMI-Klassen finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md). Weitere Informationen zum Überprüfen von Qualifizierern für vorhandene WMI-Klassen finden Sie im folgenden Beispielcode.

## <a name="example"></a>Beispiel

Der folgende PowerShell-Code, der aus der [TechNet Gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7)stammt, beschreibt das Abrufen von Qualifizierern aus einer WMI-Klasse.


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 



