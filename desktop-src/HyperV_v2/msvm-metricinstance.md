---
description: Stellt eine Zuordnung von metrikwertobjekten mit ihren metrikdefinitionen dar.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360525"
---
# <a name="msvm_metricinstance-class"></a><span data-ttu-id="fb9c9-103">MSVM \_ metricinstance-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb9c9-103">Msvm\_MetricInstance class</span></span>

<span data-ttu-id="fb9c9-104">Stellt eine Zuordnung von metrikwertobjekten mit ihren metrikdefinitionen dar.</span><span class="sxs-lookup"><span data-stu-id="fb9c9-104">Represents an association of metric value objects with their metrics definitions.</span></span> <span data-ttu-id="fb9c9-105">Diese Zuordnung verknüpft eine Instanz von [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) mit der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="fb9c9-105">This association ties an instance of [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) to its [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span>

<span data-ttu-id="fb9c9-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb9c9-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb9c9-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fb9c9-108">Member</span><span class="sxs-lookup"><span data-stu-id="fb9c9-108">Members</span></span>

<span data-ttu-id="fb9c9-109">Die **MSVM \_ metricinstance** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb9c9-109">The **Msvm\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="fb9c9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb9c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb9c9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb9c9-111">Properties</span></span>

<span data-ttu-id="fb9c9-112">Die **MSVM \_ metricinstance** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb9c9-112">The **Msvm\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb9c9-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="fb9c9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb9c9-114">Datentyp: \* \* \* \* CIM \_ managedelta \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fb9c9-114">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="fb9c9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb9c9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb9c9-116">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="fb9c9-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fb9c9-117">Ein Verweis auf eine Instanz der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Klasse, die die metrikdefinitionen darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb9c9-117">A reference to an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class that represents the metrics definitions.</span></span>

</dd> <dt>

<span data-ttu-id="fb9c9-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="fb9c9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb9c9-119">Datentyp: \* \* \* \* CIM \_ managedelta \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fb9c9-119">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="fb9c9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb9c9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb9c9-121">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="fb9c9-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fb9c9-122">Ein Verweis auf eine Instanz der [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) -Klasse, die die Metriken darstellt, die vom **Vorgänger** abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="fb9c9-122">A reference to an instance of the [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) class that represents the metrics that are dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb9c9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb9c9-123">Requirements</span></span>



| <span data-ttu-id="fb9c9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb9c9-124">Requirement</span></span> | <span data-ttu-id="fb9c9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fb9c9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c9-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb9c9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9c9-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb9c9-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fb9c9-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb9c9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9c9-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb9c9-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb9c9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb9c9-130">Namespace</span></span><br/>                | <span data-ttu-id="fb9c9-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb9c9-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fb9c9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fb9c9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb9c9-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb9c9-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb9c9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fb9c9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb9c9-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb9c9-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




