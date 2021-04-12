---
description: Stellt eine Zuordnung zwischen einer Instanz der CIM \_ Computersystem-Klasse dar, die das Replikat des virtuellen Computers und eine Instanz der CIM \_ Computersystem-Klasse darstellt, die das Replikat des virtuellen Computers darstellt.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Msvm_ReplicaSystemDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216242"
---
# <a name="msvm_replicasystemdependency-class"></a><span data-ttu-id="03ce7-103">MSVM \_ replicasystem-Abhängigkeits Klasse</span><span class="sxs-lookup"><span data-stu-id="03ce7-103">Msvm\_ReplicaSystemDependency class</span></span>

<span data-ttu-id="03ce7-104">Stellt eine Zuordnung zwischen einer Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse dar, die das Replikat des virtuellen Computers und eine Instanz der **CIM \_ Computersystem** -Klasse darstellt, die das Replikat des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="03ce7-104">Represents an association between an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica and an instance of the **CIM\_ComputerSystem** class that represents the test virtual machine replica.</span></span>

<span data-ttu-id="03ce7-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="03ce7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ce7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="03ce7-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="03ce7-107">Member</span><span class="sxs-lookup"><span data-stu-id="03ce7-107">Members</span></span>

<span data-ttu-id="03ce7-108">Die **MSVM- \_ replicasystemdepeng-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="03ce7-108">The **Msvm\_ReplicaSystemDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="03ce7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03ce7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03ce7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03ce7-110">Properties</span></span>

<span data-ttu-id="03ce7-111">Die **MSVM- \_ replicasystemdepeng-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="03ce7-111">The **Msvm\_ReplicaSystemDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03ce7-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="03ce7-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ce7-113">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="03ce7-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="03ce7-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03ce7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ce7-115">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="03ce7-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="03ce7-116">Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die das Replikat des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="03ce7-116">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica.</span></span> <span data-ttu-id="03ce7-117">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="03ce7-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="03ce7-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="03ce7-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ce7-119">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="03ce7-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="03ce7-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03ce7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ce7-121">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")</span><span class="sxs-lookup"><span data-stu-id="03ce7-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="03ce7-122">Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die das virtuelle Test Replikat darstellt, das von der [**MSVM \_ replicationservice. testreplicasystem**](testreplicasystem-msvm-replicationservice.md) -Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="03ce7-122">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the test virtual machine replica created by the [**Msvm\_ReplicationService.TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) method.</span></span> <span data-ttu-id="03ce7-123">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="03ce7-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03ce7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03ce7-124">Requirements</span></span>



| <span data-ttu-id="03ce7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03ce7-125">Requirement</span></span> | <span data-ttu-id="03ce7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="03ce7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ce7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03ce7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="03ce7-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03ce7-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="03ce7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03ce7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="03ce7-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03ce7-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03ce7-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="03ce7-131">Namespace</span></span><br/>                | <span data-ttu-id="03ce7-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="03ce7-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="03ce7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="03ce7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03ce7-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="03ce7-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03ce7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="03ce7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03ce7-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03ce7-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

