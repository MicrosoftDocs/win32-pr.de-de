---
description: Stellt eine Zuordnung zwischen einem virtuellen System und der aktuellen Momentaufnahme des Systems dar. Diese Zuordnung kann nur vorhanden sein, wenn das virtuelle System mithilfe einer Momentaufnahme erstellt wurde oder eine Momentaufnahme aus dem virtuellen System erstellt wurde.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: CIM_MostCurrentSnapshotInBranch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348313"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="97f44-104">CIM- \_ Klasse "mustcurrentsnapshotinbranch"</span><span class="sxs-lookup"><span data-stu-id="97f44-104">CIM\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="97f44-105">Stellt eine Zuordnung zwischen einem virtuellen System und der aktuellen Momentaufnahme des Systems dar.</span><span class="sxs-lookup"><span data-stu-id="97f44-105">Represents an association between a virtual system and the most current snapshot of the system.</span></span> <span data-ttu-id="97f44-106">Diese Zuordnung kann nur vorhanden sein, wenn das virtuelle System mithilfe einer Momentaufnahme erstellt wurde oder eine Momentaufnahme aus dem virtuellen System erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="97f44-106">This association can only exist if the virtual system was create using a snapshot or if a snapshot was created from the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f44-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97f44-107">Syntax</span></span>

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="97f44-108">Member</span><span class="sxs-lookup"><span data-stu-id="97f44-108">Members</span></span>

<span data-ttu-id="97f44-109">Die CIM-Klasse " **\_ mustcurrentsnapshotinbranch** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="97f44-109">The **CIM\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="97f44-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97f44-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97f44-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97f44-111">Properties</span></span>

<span data-ttu-id="97f44-112">Die CIM-Klasse " **\_ mustcurrentsnapshotinbranch** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="97f44-112">The **CIM\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97f44-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="97f44-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f44-114">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="97f44-114">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="97f44-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="97f44-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f44-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="97f44-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="97f44-117">Ein Verweis auf die Instanz des [**CIM- \_ Computer Systems**](cim-computersystem.md) , das das virtuelle System darstellt.</span><span class="sxs-lookup"><span data-stu-id="97f44-117">A reference to the instance of [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="97f44-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="97f44-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f44-119">Datentyp: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="97f44-119">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="97f44-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="97f44-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f44-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="97f44-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="97f44-122">Ein Verweis auf die Instanz von [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) , die die Momentaufnahme des virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="97f44-122">A reference to the instance of [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that represents the virtual system snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97f44-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97f44-123">Requirements</span></span>



| <span data-ttu-id="97f44-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97f44-124">Requirement</span></span> | <span data-ttu-id="97f44-125">Wert</span><span class="sxs-lookup"><span data-stu-id="97f44-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97f44-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97f44-126">Minimum supported client</span></span><br/> | <span data-ttu-id="97f44-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="97f44-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="97f44-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97f44-128">Minimum supported server</span></span><br/> | <span data-ttu-id="97f44-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97f44-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="97f44-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="97f44-130">Namespace</span></span><br/>                | <span data-ttu-id="97f44-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="97f44-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="97f44-132">MOF</span><span class="sxs-lookup"><span data-stu-id="97f44-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97f44-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="97f44-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97f44-134">DLL</span><span class="sxs-lookup"><span data-stu-id="97f44-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97f44-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97f44-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="97f44-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97f44-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f44-137">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="97f44-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

