---
description: Definiert die Zuordnung zwischen einer MSVM \_ basemetricdefinition und einem CIM- \_ managedelta, um Metriken für letztere zu definieren. Der Definition der Metriken wird vom managedelement Kontext zugewiesen, weshalb die Definition vom Element abhängig ist.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Msvm_MetricDefForME-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359026"
---
# <a name="msvm_metricdefforme-class"></a><span data-ttu-id="7fbf0-104">MSVM- \_ metricdefforme-Klasse</span><span class="sxs-lookup"><span data-stu-id="7fbf0-104">Msvm\_MetricDefForME class</span></span>

<span data-ttu-id="7fbf0-105">Definiert die Zuordnung zwischen einer [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) und einem [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , um Metriken für letztere zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-105">Defines the association between an [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) and a [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to define metrics for the latter.</span></span> <span data-ttu-id="7fbf0-106">Der Definition der Metriken wird vom managedelement Kontext zugewiesen, weshalb die Definition vom Element abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-106">The metrics definition is given context by the ManagedElement, which is why the definition is dependent on the element.</span></span>

<span data-ttu-id="7fbf0-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbf0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fbf0-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="7fbf0-109">Member</span><span class="sxs-lookup"><span data-stu-id="7fbf0-109">Members</span></span>

<span data-ttu-id="7fbf0-110">Die **MSVM- \_ metricdefforme** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7fbf0-110">The **Msvm\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="7fbf0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fbf0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fbf0-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fbf0-112">Properties</span></span>

<span data-ttu-id="7fbf0-113">Die **MSVM- \_ metricdefforme** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-113">The **Msvm\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fbf0-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fbf0-115">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-115">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fbf0-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fbf0-117">Ein Verweis auf eine Instanz der [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse, die das verwaltete Element darstellt, das Metriken des Typs aufweisen kann, der von der **abhängigen** Anwendung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-117">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that can have metrics of the type defined by **Dependent** applied to it.</span></span> <span data-ttu-id="7fbf0-118">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7fbf0-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fbf0-120">Datentyp: **[ **CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-120">Data type: **[**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fbf0-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fbf0-122">Ein Verweis auf eine Instanz der [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse, die die **metrikdefinition** darstellt, auf die der Vorgänger angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-122">A reference to an instance of the [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition that the **Antecedent** can have applied to it.</span></span> <span data-ttu-id="7fbf0-123">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7fbf0-124">**Metriccollectionaktivierte**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-124">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fbf0-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fbf0-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fbf0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fbf0-127">Gibt an, ob die durch **abhängige** definierte Metrik für den **Vorgänger** erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-127">Indicates whether the metric defined by **Dependent** is being collected for the **Antecedent**.</span></span> <span data-ttu-id="7fbf0-128">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-128">This will be one of the following values.</span></span>



| <span data-ttu-id="7fbf0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7fbf0-129">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="7fbf0-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7fbf0-130">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="7fbf0-131"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf0-131"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="7fbf0-132">Die Metrik wird gesammelt.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-132">The metric is being collected.</span></span><br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="7fbf0-133"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf0-133"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="7fbf0-134">Die Metrik wird nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-134">The metric is not being collected.</span></span><br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="7fbf0-135"><dt>**Reserviert**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf0-135"><dt>**Reserved**</dt> <dt>4</dt></span></span> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <span data-ttu-id="7fbf0-136"><dt>**Partiallyaktivierte**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf0-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span></span> </dl> | <span data-ttu-id="7fbf0-137">Die Metrik wird für einige, aber nicht für alle Geräte erfasst.</span><span class="sxs-lookup"><span data-stu-id="7fbf0-137">The metric is being collected for some, but not all, devices.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fbf0-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fbf0-138">Requirements</span></span>



| <span data-ttu-id="7fbf0-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fbf0-139">Requirement</span></span> | <span data-ttu-id="7fbf0-140">Wert</span><span class="sxs-lookup"><span data-stu-id="7fbf0-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbf0-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbf0-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fbf0-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7fbf0-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fbf0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbf0-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fbf0-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fbf0-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fbf0-145">Namespace</span></span><br/>                | <span data-ttu-id="7fbf0-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7fbf0-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7fbf0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7fbf0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fbf0-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf0-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fbf0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7fbf0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fbf0-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf0-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

