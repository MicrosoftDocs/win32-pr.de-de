---
description: Der SNMP-Anbieter verwendet bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen die folgenden CIM-Klassen Qualifizierer.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: CIM-Klassen Qualifizierer für MIB-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217747"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a><span data-ttu-id="4c5dc-103">CIM-Klassen Qualifizierer für MIB-Objekte</span><span class="sxs-lookup"><span data-stu-id="4c5dc-103">CIM Class Qualifiers for MIB Objects</span></span>

<span data-ttu-id="4c5dc-104">Der SNMP-Anbieter verwendet bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen die folgenden CIM-Klassen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-104">The SNMP Provider uses the following CIM class qualifiers when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="4c5dc-105">Ein obligatorischer Qualifizierer muss vorhanden sein, damit der SNMP-Anbieter ein Gruppen Objekt vollständig auflösen muss.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-105">A mandatory qualifier must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="4c5dc-106">Wenn Sie keinen obligatorischen Qualifizierer definieren, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-106">Failure to define a mandatory qualifier returns an error.</span></span> <span data-ttu-id="4c5dc-107">Wenn Sie einen ungültigen qualifiziererwert angeben, wird auch ein Fehler</span><span class="sxs-lookup"><span data-stu-id="4c5dc-107">Specifying an illegal qualifier value also returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="4c5dc-108">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4c5dc-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 



| <span data-ttu-id="4c5dc-109">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="4c5dc-109">Qualifier</span></span>           | <span data-ttu-id="4c5dc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c5dc-110">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5dc-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4c5dc-111">**Description**</span></span>     | <span data-ttu-id="4c5dc-112">**Zeichenfolge** Optionale</span><span class="sxs-lookup"><span data-stu-id="4c5dc-112">**string** Optional</span></span><br/> <span data-ttu-id="4c5dc-113">Die Beschreibung der Klasse.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-113">Description of the class.</span></span><br/>                                                                      |
| <span data-ttu-id="4c5dc-114">**Group \_ objectID**</span><span class="sxs-lookup"><span data-stu-id="4c5dc-114">**Group\_Objectid**</span></span> | <span data-ttu-id="4c5dc-115">**Zeichenfolge** Obligatorisch, wenn die Klasse für den SNMP-Klassen Anbieter vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-115">**string** Mandatory, if the class is for the SNMP class provider.</span></span><br/> <span data-ttu-id="4c5dc-116">Der Objekt Bezeichner der fabricollection.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-116">Object identifier of the fabricated collection.</span></span><br/> |
| <span data-ttu-id="4c5dc-117">**Modul \_ Importe**</span><span class="sxs-lookup"><span data-stu-id="4c5dc-117">**Module\_Imports**</span></span> | <span data-ttu-id="4c5dc-118">**Zeichenfolge** Optionale</span><span class="sxs-lookup"><span data-stu-id="4c5dc-118">**string** Optional</span></span><br/> <span data-ttu-id="4c5dc-119">Durch Trennzeichen getrennte Liste von MIB-Modulnamen, die zum Auflösen von Importen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-119">Comma-separated list of MIB module names used to resolve imports.</span></span><br/>                              |
| <span data-ttu-id="4c5dc-120">**\_Modulname**</span><span class="sxs-lookup"><span data-stu-id="4c5dc-120">**Module\_Name**</span></span>    | <span data-ttu-id="4c5dc-121">**Zeichenfolge** Optionale</span><span class="sxs-lookup"><span data-stu-id="4c5dc-121">**string** Optional</span></span><br/> <span data-ttu-id="4c5dc-122">Der Identitäts Name eines MIB-Moduls.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-122">Identity name of a MIB module.</span></span><br/>                                                                 |
| <span data-ttu-id="4c5dc-123">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="4c5dc-123">**Reference**</span></span>       | <span data-ttu-id="4c5dc-124">**Zeichenfolge** Optionale</span><span class="sxs-lookup"><span data-stu-id="4c5dc-124">**string** Optional</span></span><br/> <span data-ttu-id="4c5dc-125">Verweist auf ein anderes Dokument, das weitere Informationen zur-Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-125">Refers to another document that contains more information about the class.</span></span><br/>                     |
| <span data-ttu-id="4c5dc-126">**Singleton**</span><span class="sxs-lookup"><span data-stu-id="4c5dc-126">**Singleton**</span></span>       | <span data-ttu-id="4c5dc-127">**Bool** Obligatorisch für Klassen, die aus skalaren Auflistungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-127">**Bool** Mandatory for classes mapped from scalar collections.</span></span><br/> <span data-ttu-id="4c5dc-128">Gibt eine Klasse an, die nur eine Instanz aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="4c5dc-128">Indicates a class that can only have one instance.</span></span><br/>  |



 

 

 




