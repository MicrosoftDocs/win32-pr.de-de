---
description: Stellt die Zuordnung zwischen zwei metrikdefinitionen oder zwei Metrikwerten dar.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Msvm_MetricCollectionDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353962"
---
# <a name="msvm_metriccollectiondependency-class"></a><span data-ttu-id="fa609-103">MSVM- \_ metriccollectiondepencklasse</span><span class="sxs-lookup"><span data-stu-id="fa609-103">Msvm\_MetricCollectionDependency class</span></span>

<span data-ttu-id="fa609-104">Stellt die Zuordnung zwischen zwei metrikdefinitionen oder zwei Metrikwerten dar.</span><span class="sxs-lookup"><span data-stu-id="fa609-104">Represents the association between two metric definitions or two metric values.</span></span>

<span data-ttu-id="fa609-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa609-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa609-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa609-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fa609-107">Member</span><span class="sxs-lookup"><span data-stu-id="fa609-107">Members</span></span>

<span data-ttu-id="fa609-108">Die **MSVM-Klasse " \_ metriccollectiondependenz** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fa609-108">The **Msvm\_MetricCollectionDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="fa609-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa609-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa609-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa609-110">Properties</span></span>

<span data-ttu-id="fa609-111">Die **MSVM \_ metriccollectiondepenc-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa609-111">The **Msvm\_MetricCollectionDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa609-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="fa609-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa609-113">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="fa609-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="fa609-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fa609-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa609-115">Ein Verweis auf eine Instanz der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse, die die unabhängige metrikdefinition oder den Metrikwert darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa609-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the independent metric definition or metric value.</span></span> <span data-ttu-id="fa609-116">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fa609-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="fa609-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="fa609-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa609-118">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="fa609-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="fa609-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fa609-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa609-120">Ein Verweis auf eine Instanz der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse, die die **metrikdefinition oder den Metrikwert** darstellt, der vom Vorgänger abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="fa609-120">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition or metric value that is dependent on the **Antecedent**.</span></span> <span data-ttu-id="fa609-121">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fa609-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa609-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa609-122">Requirements</span></span>



| <span data-ttu-id="fa609-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa609-123">Requirement</span></span> | <span data-ttu-id="fa609-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fa609-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa609-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa609-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa609-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa609-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa609-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa609-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa609-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa609-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa609-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa609-129">Namespace</span></span><br/>                | <span data-ttu-id="fa609-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa609-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa609-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fa609-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa609-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fa609-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa609-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fa609-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa609-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa609-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

