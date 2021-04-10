---
description: Stellt eine Zuordnung zwischen einer Instanz von MSVM \_ Computersystem dar, die den virtuellen Computer und eine Instanz von MSVM \_ replicationrelationship darstellt, die eine Replikations Beziehung des virtuellen Computers darstellt.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958744"
---
# <a name="msvm_systemreplicationrelationship-class"></a><span data-ttu-id="89519-103">MSVM \_ systemreplicationrelationship-Klasse</span><span class="sxs-lookup"><span data-stu-id="89519-103">Msvm\_SystemReplicationRelationship class</span></span>

<span data-ttu-id="89519-104">Stellt eine Zuordnung zwischen einer Instanz von [**MSVM \_ Computersystem**](msvm-computersystem.md) dar, die den virtuellen Computer und eine Instanz von [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) darstellt, die eine Replikations Beziehung des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="89519-104">Represents an association between an instance of [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the virtual machine and an instance of [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) that represents a replication relationship of the virtual machine.</span></span> <span data-ttu-id="89519-105">Diese Klasse wird von der [**CIM- \_ Abhängigkeits**](/windows/desktop/CIMWin32Prov/cim-dependency) Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="89519-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="89519-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="89519-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89519-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89519-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="89519-108">Member</span><span class="sxs-lookup"><span data-stu-id="89519-108">Members</span></span>

<span data-ttu-id="89519-109">Die **MSVM \_ systemreplicationrelationship** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="89519-109">The **Msvm\_SystemReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="89519-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89519-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89519-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89519-111">Properties</span></span>

<span data-ttu-id="89519-112">Die **MSVM \_ systemreplicationrelationship** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89519-112">The **Msvm\_SystemReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89519-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="89519-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89519-114">Datentyp: **MSVM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="89519-114">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="89519-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89519-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89519-116">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="89519-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="89519-117">Verweis auf die Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="89519-117">Reference to the instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="89519-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="89519-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89519-119">Datentyp: **MSVM \_ replicationrelationship**</span><span class="sxs-lookup"><span data-stu-id="89519-119">Data type: **Msvm\_ReplicationRelationship**</span></span>
</dt> <dt>

<span data-ttu-id="89519-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89519-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89519-121">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")</span><span class="sxs-lookup"><span data-stu-id="89519-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="89519-122">Verweis auf die Instanz der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, die die Replikations Beziehung eines virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="89519-122">Reference to the instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that represents the replication relationship of a virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89519-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89519-123">Requirements</span></span>



| <span data-ttu-id="89519-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89519-124">Requirement</span></span> | <span data-ttu-id="89519-125">Wert</span><span class="sxs-lookup"><span data-stu-id="89519-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89519-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89519-126">Minimum supported client</span></span><br/> | <span data-ttu-id="89519-127">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="89519-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="89519-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89519-128">Minimum supported server</span></span><br/> | <span data-ttu-id="89519-129">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89519-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="89519-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="89519-130">Namespace</span></span><br/>                | <span data-ttu-id="89519-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="89519-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="89519-132">MOF</span><span class="sxs-lookup"><span data-stu-id="89519-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89519-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="89519-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89519-134">DLL</span><span class="sxs-lookup"><span data-stu-id="89519-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89519-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89519-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="89519-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89519-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89519-137">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="89519-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="89519-138">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="89519-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

