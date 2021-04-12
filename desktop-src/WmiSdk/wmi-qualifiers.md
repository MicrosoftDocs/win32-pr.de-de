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
# <a name="wmi-qualifiers"></a><span data-ttu-id="59853-104">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="59853-104">WMI Qualifiers</span></span>

<span data-ttu-id="59853-105">WMI verfügt über mehrere Typen von Klassen-und Eigenschafts [*Qualifizierern*](gloss-q.md).</span><span class="sxs-lookup"><span data-stu-id="59853-105">WMI has several types of class and property [*qualifiers*](gloss-q.md).</span></span> <span data-ttu-id="59853-106">Qualifizierer können auch [*Änderungen ändern*](gloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="59853-106">Qualifiers can also have modifying [*flavors*](gloss-f.md).</span></span> <span data-ttu-id="59853-107">Die folgenden Typen von Qualifizierern und Varianten werden in WMI verwendet.</span><span class="sxs-lookup"><span data-stu-id="59853-107">The following types of qualifiers and flavors are used in WMI.</span></span>

<span data-ttu-id="59853-108">Der Name jedes Qualifizierers wird mit seinem Datentyp und einem Indikator darüber angezeigt, ob der Qualifizierer auf eine Klasse, eine Instanz, eine Eigenschaft oder eine Methode angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="59853-108">The name of each qualifier appears with its data type and an indicator of whether the qualifier can be applied to a class, instance, property, or method.</span></span> <span data-ttu-id="59853-109">Für Qualifizierer, wie z. b. **Association** (unter [Meta-Qualifizierer](meta-qualifiers.md)erläutert), gibt es eine implizite Verwendungs Regel, dass auch der Meta-Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="59853-109">For qualifiers such as **Association** (discussed under [Meta Qualifiers](meta-qualifiers.md)), there is an implied usage rule that the meta qualifier must also be present.</span></span> <span data-ttu-id="59853-110">Die implizite Verwendungs Regel für die **Aggregations** Qualifizierer ist beispielsweise, dass der **Association** -Qualifizierer ebenfalls vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="59853-110">For example, the implicit usage rule for the **Aggregation** qualifiers is that the **Association** qualifier must also be present.</span></span>



| <span data-ttu-id="59853-111">Qualifizierertyp</span><span class="sxs-lookup"><span data-stu-id="59853-111">Qualifier type</span></span>                              | <span data-ttu-id="59853-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59853-112">Description</span></span>                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59853-113">Analysen</span><span class="sxs-lookup"><span data-stu-id="59853-113">Meta</span></span>](meta-qualifiers.md)                 | <span data-ttu-id="59853-114">Verfeinert die Definition von Meta-Konstrukten durch die Verdeutlichung der tatsächlichen Verwendung einer Klassen-oder Eigenschaften Deklaration.</span><span class="sxs-lookup"><span data-stu-id="59853-114">Refines the definition of meta-constructs by clarifying the actual usage of a class or property declaration.</span></span>                          |
| [<span data-ttu-id="59853-115">Optional</span><span class="sxs-lookup"><span data-stu-id="59853-115">Optional</span></span>](optional-qualifiers.md)         | <span data-ttu-id="59853-116">Adress Situationen, die nicht von allen CIM-kompatiblen Implementierungen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="59853-116">Addresses situations not common to all CIM-compliant implementations.</span></span>                                                                 |
| [<span data-ttu-id="59853-117">Qualifizierervarianten</span><span class="sxs-lookup"><span data-stu-id="59853-117">Qualifier Flavors</span></span>](qualifier-flavors.md)  | <span data-ttu-id="59853-118">Bietet weitere Informationen über einen Qualifizierer, z. b. ob eine abgeleitete Klasse oder eine Instanz den ursprünglichen Wert des Qualifizierers überschreiben kann.</span><span class="sxs-lookup"><span data-stu-id="59853-118">Provides more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span> |
| [<span data-ttu-id="59853-119">Standard</span><span class="sxs-lookup"><span data-stu-id="59853-119">Standard</span></span>](standard-qualifiers.md)         | <span data-ttu-id="59853-120">Unterstützt die Beschreibungen, die von allen CIM-kompatiblen Implementierungen behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="59853-120">Supports the descriptions that all CIM-compliant implementations must handle.</span></span>                                                         |
| [<span data-ttu-id="59853-121">WMI-spezifisch</span><span class="sxs-lookup"><span data-stu-id="59853-121">WMI-specific</span></span>](wmi-specific-qualifiers.md) | <span data-ttu-id="59853-122">Beschreibt die für WMI spezifischen Qualifizierer, z. b. Qualifizierer für die Leistungs</span><span class="sxs-lookup"><span data-stu-id="59853-122">Describes qualifiers specific to WMI, such as performance counter class qualifiers.</span></span>                                                   |



 

<span data-ttu-id="59853-123">Weitere Informationen zum Anwenden von Qualifizierern auf ihre WMI-Klassen finden Sie unter [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="59853-123">For more information on applying qualifiers to your WMI classes, see [Adding a Qualifier](adding-a-qualifier.md).</span></span> <span data-ttu-id="59853-124">Weitere Informationen zum Überprüfen von Qualifizierern für vorhandene WMI-Klassen finden Sie im folgenden Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="59853-124">To see how to examine qualifiers on existing WMI classes, see the example code below.</span></span>

## <a name="example"></a><span data-ttu-id="59853-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="59853-125">Example</span></span>

<span data-ttu-id="59853-126">Der folgende PowerShell-Code, der aus der [TechNet Gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7)stammt, beschreibt das Abrufen von Qualifizierern aus einer WMI-Klasse.</span><span class="sxs-lookup"><span data-stu-id="59853-126">The following PowerShell code, taken from the [TechNet gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describes how to retrieve qualifiers from a WMI class.</span></span>


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



 

 



