---
description: WMI verfügt über mehrere Typen von Klassen- und Eigenschaftsqualifizierern. Qualifizierer können auch geänderte Varianten aufweisen.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: WMI-Qualifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf51888592949aadefec7c864dc0a24df6a4fa68f6fb34c8e3cda880da6873
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502810"
---
# <a name="wmi-qualifiers"></a>WMI-Qualifizierer

WMI verfügt über mehrere Typen von Klassen- und [*Eigenschaftsqualifizierern.*](gloss-q.md) Qualifizierer können auch [*geänderte Varianten aufweisen.*](gloss-f.md) Die folgenden Typen von Qualifizierern und Varianten werden in WMI verwendet.

Der Name jedes Qualifizierers wird mit seinem Datentyp und einem Indikator dafür angezeigt, ob der Qualifizierer auf eine Klasse, Instanz, Eigenschaft oder Methode angewendet werden kann. Für Qualifizierer wie **Zuordnung** (siehe [Metaqualifizierer)](meta-qualifiers.md)gibt es eine implizite Verwendungsregel, dass der Metaqualifizierer ebenfalls vorhanden sein muss. Die implizite Verwendungsregel für die **Aggregationsqualifizierer** ist beispielsweise, dass auch der **Zuordnungsqualifizierer** vorhanden sein muss.



| Qualifizierertyp                              | Beschreibung                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Meta](meta-qualifiers.md)                 | Verfeinern Sie die Definition von Metakonstrukten, indem Sie die tatsächliche Verwendung einer Klasse oder Eigenschaftendeklaration verdeutlichen.                          |
| [Optional](optional-qualifiers.md)         | Behandelt Situationen, die nicht für alle CIM-konformen Implementierungen üblich sind.                                                                 |
| [Qualifizierer-Varianten](qualifier-flavors.md)  | Stellt weitere Informationen zu einem Qualifizierer bereit, z. B. ob eine abgeleitete Klasse oder Instanz den ursprünglichen Wert des Qualifizierers überschreiben kann. |
| [Standard](standard-qualifiers.md)         | Unterstützt die Beschreibungen, die alle CIM-kompatiblen Implementierungen verarbeiten müssen.                                                         |
| [WMI-spezifisch](wmi-specific-qualifiers.md) | Beschreibt WMI-spezifische Qualifizierer, z. B. Leistungsindikatorklassenqualifizierer.                                                   |



 

Weitere Informationen zum Anwenden von Qualifizierern auf Ihre WMI-Klassen finden Sie unter [Hinzufügen eines Qualifizierers.](adding-a-qualifier.md) Informationen zum Untersuchen von Qualifizierern für vorhandene WMI-Klassen finden Sie im folgenden Beispielcode.

## <a name="example"></a>Beispiel

Der folgende PowerShell-Code aus dem [TechNet-Katalog](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7)beschreibt, wie Qualifizierer aus einer WMI-Klasse abgerufen werden.


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



 

 



