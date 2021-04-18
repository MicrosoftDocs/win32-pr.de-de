---
description: Eine SNMP-Auflistung wird einer CIM-Klasse zugeordnet, und die Elemente einer Auflistung werden den Eigenschaften einer CIM-Klasse zugeordnet. Alle generierten CIM-Klassendefinitionen müssen von der snmpobjecttype-Klasse abgeleitet werden.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: SNMP-Sammlungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347318"
---
# <a name="snmp-collections"></a><span data-ttu-id="82f5e-104">SNMP-Sammlungen</span><span class="sxs-lookup"><span data-stu-id="82f5e-104">SNMP Collections</span></span>

<span data-ttu-id="82f5e-105">Eine SNMP-Auflistung wird einer CIM-Klasse zugeordnet, und die Elemente einer Auflistung werden den Eigenschaften einer CIM-Klasse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="82f5e-105">An SNMP collection maps to a CIM class and the elements of a collection map to the properties of a CIM class.</span></span> <span data-ttu-id="82f5e-106">Alle generierten CIM-Klassendefinitionen müssen von der **snmpobjecttype** -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="82f5e-106">All generated CIM class definitions must be derived from the **SnmpObjectType** class.</span></span>

> [!Note]  
> <span data-ttu-id="82f5e-107">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="82f5e-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="82f5e-108">Die folgenden Klassendefinitionen übergeordnet alle generierten Klassendefinitionen:</span><span class="sxs-lookup"><span data-stu-id="82f5e-108">The following class definitions parent all generated class definitions:</span></span>

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a><span data-ttu-id="82f5e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82f5e-109">Remarks</span></span>

<span data-ttu-id="82f5e-110">Die folgenden Regeln gelten für die Zuordnung von SNMP-Auflistungen zu CIM-Klassen.</span><span class="sxs-lookup"><span data-stu-id="82f5e-110">The following rules apply when mapping SNMP collections to CIM classes.</span></span> <span data-ttu-id="82f5e-111">Sofern nicht anders angegeben, gelten diese Regeln sowohl für skalare als auch für Tabellen Auflistungen:</span><span class="sxs-lookup"><span data-stu-id="82f5e-111">Unless otherwise specified, these rules apply to both scalar and table collections:</span></span>

-   <span data-ttu-id="82f5e-112">Der Zustellungs Prozess generiert CIM-Klassennamen durch Verkettung von "SNMP \_ ", des MIB-Modul Identitäts namens, " \_ " und des Objekt Deskriptors der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="82f5e-112">The mapping process generates CIM class names by concatenating "SNMP\_", the MIB module identity name, "\_", and the collection's object descriptor.</span></span>

    <span data-ttu-id="82f5e-113">Beispiel: das **System** wird in das **SNMP- \_ RFC1213 \_ MIB- \_ System** übersetzt, während **iftable** in **SNMP \_ RFC1213 \_ MIB \_ iftable** übersetzt.</span><span class="sxs-lookup"><span data-stu-id="82f5e-113">For example: **system** translates to **SNMP\_RFC1213\_MIB\_system**, while **ifTable** translates to **SNMP\_RFC1213\_MIB\_ifTable**.</span></span>

-   <span data-ttu-id="82f5e-114">In allen Fällen werden Bindestriche (-) in SNMP-MIB-Bezeichnerzeichen unterstrichen ( \_ ) in CIM-Klassennamen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="82f5e-114">In all cases, hyphens (-) in SNMP MIB identifiers map to underscores (\_) in CIM class names.</span></span>
-   <span data-ttu-id="82f5e-115">Namenskonflikte können auftreten, wenn die Groß-/Kleinschreibung des CIM-namens nicht beachtet wird</span><span class="sxs-lookup"><span data-stu-id="82f5e-115">Naming conflicts can occur due to CIM name case-insensitivity.</span></span> <span data-ttu-id="82f5e-116">Wenn ein Benennungs Konflikt auftritt, wählt der Anbieter eine der in Konflikt stehenden Gruppendefinitionen aus und ignoriert die restlichen Definitionen.</span><span class="sxs-lookup"><span data-stu-id="82f5e-116">If a naming conflict occurs, the provider chooses one of the conflicting group definitions and ignores the remaining definitions.</span></span>
-   <span data-ttu-id="82f5e-117">Der Identitäts Name des MIB-Moduls, das die Auflistung enthält, wird dem klassenqualifizierermodulnamen des CIM-Klasse zugeordnet. **\_**</span><span class="sxs-lookup"><span data-stu-id="82f5e-117">The identity name of the MIB module that contains the collection maps to the CIM class qualifier **Module\_Name**.</span></span>
-   <span data-ttu-id="82f5e-118">Der Objekt Bezeichner der fabricollection wird der CIM-Klassen- **qualifizierergruppe \_ objectID** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="82f5e-118">The object identifier of the fabricated collection maps to the CIM class qualifier **Group\_Objectid**.</span></span>
-   <span data-ttu-id="82f5e-119">Die Importliste des MIB-Moduls (aus der Definition des **Modul-Identity-** Makros abgerufen) wird den **\_ Importen** des CIM-klassenqualifizierungsmoduls zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="82f5e-119">The MIB module imports list (obtained from the **MODULE-IDENTITY** macro definition) maps to the CIM class qualifier **module\_imports**.</span></span> <span data-ttu-id="82f5e-120">Dieser Qualifizierer enthält eine durch Trennzeichen getrennte Liste von Modulnamen.</span><span class="sxs-lookup"><span data-stu-id="82f5e-120">This qualifier contains a comma-separated list of module names.</span></span>

 

 



