---
description: Diese Zuordnung verknüpft ein verwaltetes Element mit den Metrikwerten, die für das Element beibehalten werden.
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Msvm_MetricForME-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353960"
---
# <a name="msvm_metricforme-class"></a><span data-ttu-id="82af2-103">MSVM- \_ metricforme-Klasse</span><span class="sxs-lookup"><span data-stu-id="82af2-103">Msvm\_MetricForME class</span></span>

<span data-ttu-id="82af2-104">Diese Zuordnung verknüpft ein verwaltetes Element mit den Metrikwerten, die für das Element beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="82af2-104">This association links a managed element to the metric values being maintained for it.</span></span>

<span data-ttu-id="82af2-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82af2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82af2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="82af2-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="82af2-107">Member</span><span class="sxs-lookup"><span data-stu-id="82af2-107">Members</span></span>

<span data-ttu-id="82af2-108">Die **MSVM- \_ metricforme** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="82af2-108">The **Msvm\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="82af2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82af2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82af2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82af2-110">Properties</span></span>

<span data-ttu-id="82af2-111">Die **MSVM- \_ metricforme** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82af2-111">The **Msvm\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82af2-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="82af2-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82af2-113">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="82af2-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="82af2-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82af2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82af2-115">Ein Verweis auf eine Instanz der [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse, die das verwaltete Element darstellt, dessen Metriken durch **abhängige** beibehalten definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="82af2-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that has metrics defined by **Dependent** maintained for it.</span></span> <span data-ttu-id="82af2-116">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82af2-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="82af2-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="82af2-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82af2-118">Datentyp: \* \* \* \* CIM \_ basemetricvalue \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="82af2-118">Data type: \*\*\*\*CIM\_BaseMetricValue\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="82af2-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82af2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82af2-120">Ein Verweis auf eine Instanz der **CIM \_ basemetricvalue** -Klasse, die die Metrik darstellt, die der **Vorgänger** für Sie erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="82af2-120">A reference to an instance of the **CIM\_BaseMetricValue** class that represents the metric that the **Antecedent** has collected for it.</span></span> <span data-ttu-id="82af2-121">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82af2-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82af2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82af2-122">Requirements</span></span>



| <span data-ttu-id="82af2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82af2-123">Requirement</span></span> | <span data-ttu-id="82af2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="82af2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82af2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82af2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82af2-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82af2-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="82af2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82af2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82af2-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82af2-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82af2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="82af2-129">Namespace</span></span><br/>                | <span data-ttu-id="82af2-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="82af2-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="82af2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="82af2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82af2-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="82af2-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82af2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="82af2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82af2-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82af2-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

