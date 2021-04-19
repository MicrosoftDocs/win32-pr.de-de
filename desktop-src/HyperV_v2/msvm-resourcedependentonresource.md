---
description: Legt fest, dass eine CIM \_ resourceallocationsettingdata-Instanz, die eine Ressourcen Zuordnung darstellt, von einer anderen Ressourcenzuweisung abhängt.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Msvm_ResourceDependentOnResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353559"
---
# <a name="msvm_resourcedependentonresource-class"></a><span data-ttu-id="3c568-103">MSVM \_ resourcedependentonresource-Klasse</span><span class="sxs-lookup"><span data-stu-id="3c568-103">Msvm\_ResourceDependentOnResource class</span></span>

<span data-ttu-id="3c568-104">Legt fest, dass eine [**CIM \_ resourceallocationsettingdata**](cim-resourceallocationsettingdata.md) -Instanz, die eine Ressourcen Zuordnung darstellt, von einer anderen Ressourcenzuweisung abhängt.</span><span class="sxs-lookup"><span data-stu-id="3c568-104">Establishes that a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance representing a resource allocation depends on another resource allocation.</span></span>

<span data-ttu-id="3c568-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c568-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c568-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c568-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3c568-107">Member</span><span class="sxs-lookup"><span data-stu-id="3c568-107">Members</span></span>

<span data-ttu-id="3c568-108">Die **MSVM \_ resourcedependentonresource** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3c568-108">The **Msvm\_ResourceDependentOnResource** class has these types of members:</span></span>

-   [<span data-ttu-id="3c568-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c568-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c568-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c568-110">Properties</span></span>

<span data-ttu-id="3c568-111">Die **MSVM \_ resourcedependentonresource** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c568-111">The **Msvm\_ResourceDependentOnResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c568-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="3c568-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c568-113">Datentyp: **CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="3c568-113">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="3c568-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c568-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c568-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="3c568-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3c568-116">Ein [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) , das die unabhängige Ressource in dieser Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3c568-116">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the independent resource in this association.</span></span>

</dd> <dt>

<span data-ttu-id="3c568-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="3c568-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c568-118">Datentyp: **CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="3c568-118">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="3c568-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c568-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c568-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="3c568-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3c568-121">Ein [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) , das die Ressource darstellt, die vom Vorgänger abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="3c568-121">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the resource that is dependent on the Antecedent.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c568-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c568-122">Requirements</span></span>



| <span data-ttu-id="3c568-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c568-123">Requirement</span></span> | <span data-ttu-id="3c568-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3c568-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c568-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c568-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3c568-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c568-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3c568-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c568-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3c568-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c568-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3c568-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c568-129">Namespace</span></span><br/>                | <span data-ttu-id="3c568-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3c568-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3c568-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3c568-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c568-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3c568-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c568-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3c568-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c568-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c568-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c568-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c568-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c568-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="3c568-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

