---
description: WMI definiert eine Reihe von Systemeigenschaften, die neben klassenspezifischen Eigenschaften allen Klassen und Instanzen von Klassen zugeordnet sind.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: CIM-System Eigenschaften für MIB-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362279"
---
# <a name="cim-system-properties-for-mib-objects"></a><span data-ttu-id="8a65a-103">CIM-System Eigenschaften für MIB-Objekte</span><span class="sxs-lookup"><span data-stu-id="8a65a-103">CIM System Properties for MIB Objects</span></span>

<span data-ttu-id="8a65a-104">WMI definiert eine Reihe von Systemeigenschaften, die neben klassenspezifischen Eigenschaften allen Klassen und Instanzen von Klassen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8a65a-104">WMI defines a set of system properties that are associated with all classes and instances of classes in addition to class-specific properties.</span></span>

> [!Note]  
> <span data-ttu-id="8a65a-105">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8a65a-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="8a65a-106">Der SNMP-Anbieter verwendet die folgenden CIM-Systemeigenschaften bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8a65a-106">The SNMP Provider uses the following CIM system properties when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="8a65a-107">Erforderliche Eigenschaften müssen vorhanden sein, damit der SNMP-Anbieter ein Gruppen Objekt vollständig auflösen muss.</span><span class="sxs-lookup"><span data-stu-id="8a65a-107">Mandatory properties must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="8a65a-108">Wenn Sie eine obligatorische Eigenschaft nicht definieren, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a65a-108">Failure to define a mandatory property returns an error.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8a65a-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8a65a-109">Property</span></span></th>
<th><span data-ttu-id="8a65a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a65a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a65a-111"><strong>__CLASS</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-111"><strong>__CLASS</strong></span></span></td>
<td><span data-ttu-id="8a65a-112"><strong>Zeichenfolge</strong> Verpflich</span><span class="sxs-lookup"><span data-stu-id="8a65a-112"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8a65a-113">Für-Instanzen die Klasse, zu der das Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="8a65a-113">For instances, the class to which the object belongs.</span></span> <span data-ttu-id="8a65a-114">Bei Klassen ist dies der Klassenname.</span><span class="sxs-lookup"><span data-stu-id="8a65a-114">For classes, this is the class name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a65a-115"><strong>__DYNASTY</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-115"><strong>__DYNASTY</strong></span></span></td>
<td><span data-ttu-id="8a65a-116"><strong>Zeichenfolge</strong> Optionale</span><span class="sxs-lookup"><span data-stu-id="8a65a-116"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="8a65a-117">Der Name der Klasse, bei der es sich um die ultimative Basisklasse für das aktuelle Objekt handelt (nicht um seine unmittelbare übergeordnete Klasse).</span><span class="sxs-lookup"><span data-stu-id="8a65a-117">Name of the class that is the ultimate base class for the current object (not its immediate parent class).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a65a-118"><strong>__GENUS</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-118"><strong>__GENUS</strong></span></span></td>
<td><span data-ttu-id="8a65a-119"><strong>UInt32</strong> Verpflich</span><span class="sxs-lookup"><span data-stu-id="8a65a-119"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="8a65a-120">Typ des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8a65a-120">Type of object.</span></span> <span data-ttu-id="8a65a-121">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="8a65a-121">Values are:</span></span><br/> <dl> <span data-ttu-id="8a65a-122">1 = Klasse</span><span class="sxs-lookup"><span data-stu-id="8a65a-122">1 = class</span></span><br />
<span data-ttu-id="8a65a-123">2 = Instanz</span><span class="sxs-lookup"><span data-stu-id="8a65a-123">2 = instance</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a65a-124"><strong>__NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-124"><strong>__NAMESPACE</strong></span></span></td>
<td><span data-ttu-id="8a65a-125"><strong>Zeichenfolge</strong> Verpflich</span><span class="sxs-lookup"><span data-stu-id="8a65a-125"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8a65a-126">Der Namespace, in dem sich das Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="8a65a-126">Namespace where the object is located.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a65a-127"><strong>__PATH</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-127"><strong>__PATH</strong></span></span></td>
<td><span data-ttu-id="8a65a-128"><strong>Zeichenfolge</strong> Verpflich</span><span class="sxs-lookup"><span data-stu-id="8a65a-128"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8a65a-129">Absoluter Pfad zum Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a65a-129">Absolute path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a65a-130"><strong>__PROPERTYCOUNT</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-130"><strong>__PROPERTYCOUNT</strong></span></span></td>
<td><span data-ttu-id="8a65a-131"><strong>UInt32</strong> Verpflich</span><span class="sxs-lookup"><span data-stu-id="8a65a-131"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="8a65a-132">Anzahl der nicht-Systemeigenschaften, die für das Objekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8a65a-132">Number of non-system properties defined for the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a65a-133"><strong>__RELPATH</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-133"><strong>__RELPATH</strong></span></span></td>
<td><span data-ttu-id="8a65a-134"><strong>Zeichenfolge</strong> Verpflich</span><span class="sxs-lookup"><span data-stu-id="8a65a-134"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8a65a-135">Relativer Pfad zum Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a65a-135">Relative path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a65a-136"><strong>__SERVER</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-136"><strong>__SERVER</strong></span></span></td>
<td><span data-ttu-id="8a65a-137"><strong>Zeichenfolge</strong> Verpflich</span><span class="sxs-lookup"><span data-stu-id="8a65a-137"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8a65a-138">Server, der das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8a65a-138">Server supplying the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a65a-139"><strong>__SUPERCLASS</strong></span><span class="sxs-lookup"><span data-stu-id="8a65a-139"><strong>__SUPERCLASS</strong></span></span></td>
<td><span data-ttu-id="8a65a-140"><strong>Zeichenfolge</strong> Optionale</span><span class="sxs-lookup"><span data-stu-id="8a65a-140"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="8a65a-141">Unmittelbar übergeordnete Klasse des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8a65a-141">Immediate parent class of the object.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




