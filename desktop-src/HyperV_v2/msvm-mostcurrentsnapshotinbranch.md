---
description: Ordnet eine Instanz der MSVM \_ Computersystem-oder MSVM \_ plannedcomputersystem-Klasse zu, die ein virtuelles System darstellt, mit einer Instanz der MSVM \_ virtualsystemsettingdata-Klasse, die die Momentaufnahme des virtuellen Systems darstellt, die die aktuellste Momentaufnahme in einer Verzweigung abhängiger Momentaufnahmen ist.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Msvm_MostCurrentSnapshotInBranch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352731"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="8b74b-103">MSVM- \_ Klasse "mustcurrentsnapshotinbranch"</span><span class="sxs-lookup"><span data-stu-id="8b74b-103">Msvm\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="8b74b-104">Ordnet eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -oder [**MSVM \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Klasse zu, die ein virtuelles System darstellt, mit einer Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die Momentaufnahme des virtuellen Systems darstellt, die die aktuellste Momentaufnahme in einer Verzweigung abhängiger Momentaufnahmen ist.</span><span class="sxs-lookup"><span data-stu-id="8b74b-104">Associates an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing a virtual system, with an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class representing the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span>

<span data-ttu-id="8b74b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b74b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b74b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b74b-106">Syntax</span></span>

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8b74b-107">Member</span><span class="sxs-lookup"><span data-stu-id="8b74b-107">Members</span></span>

<span data-ttu-id="8b74b-108">Die **MSVM-Klasse " \_ mustcurrentsnapshotinbranch** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b74b-108">The **Msvm\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="8b74b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b74b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b74b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b74b-110">Properties</span></span>

<span data-ttu-id="8b74b-111">Die **MSVM-Klasse " \_ mustcurrentsnapshotinbranch** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b74b-111">The **Msvm\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b74b-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="8b74b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b74b-113">Datentyp: **[ **CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="8b74b-113">Data type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>
</dt> <dt>

<span data-ttu-id="8b74b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b74b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b74b-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8b74b-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8b74b-116">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -oder [**MSVM \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Klasse, die das virtuelle System darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b74b-116">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing the virtual system.</span></span> <span data-ttu-id="8b74b-117">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b74b-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="8b74b-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="8b74b-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b74b-119">Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="8b74b-119">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8b74b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b74b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b74b-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8b74b-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8b74b-122">Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die Momentaufnahme des virtuellen Systems darstellt, die die aktuellste Momentaufnahme in einer Verzweigung abhängiger Momentaufnahmen ist.</span><span class="sxs-lookup"><span data-stu-id="8b74b-122">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span> <span data-ttu-id="8b74b-123">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b74b-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b74b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b74b-124">Requirements</span></span>



| <span data-ttu-id="8b74b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b74b-125">Requirement</span></span> | <span data-ttu-id="8b74b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8b74b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b74b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b74b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8b74b-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b74b-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b74b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b74b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8b74b-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b74b-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b74b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b74b-131">Namespace</span></span><br/>                | <span data-ttu-id="8b74b-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b74b-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b74b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8b74b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b74b-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b74b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8b74b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b74b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b74b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

