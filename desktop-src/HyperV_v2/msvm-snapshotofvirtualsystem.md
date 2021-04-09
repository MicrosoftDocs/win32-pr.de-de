---
description: Ordnet einem virtuellen System eine Momentaufnahme zu, die vom virtuellen System erfasst wurde.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Msvm_SnapshotOfVirtualSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959277"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a><span data-ttu-id="3fbda-103">MSVM \_ snapshodessystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="3fbda-103">Msvm\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="3fbda-104">Ordnet einem virtuellen System eine Momentaufnahme zu, die vom virtuellen System erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="3fbda-104">Associates a virtual system with a snapshot that was captured from the virtual system.</span></span>

<span data-ttu-id="3fbda-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3fbda-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fbda-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fbda-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3fbda-107">Member</span><span class="sxs-lookup"><span data-stu-id="3fbda-107">Members</span></span>

<span data-ttu-id="3fbda-108">Die **MSVM \_ snapshotofvirtualsystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3fbda-108">The **Msvm\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="3fbda-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3fbda-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fbda-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3fbda-110">Properties</span></span>

<span data-ttu-id="3fbda-111">Die **MSVM \_ snapshodessystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3fbda-111">The **Msvm\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fbda-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="3fbda-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fbda-113">Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="3fbda-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3fbda-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3fbda-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fbda-115">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das virtuelle System darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fbda-115">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system.</span></span> <span data-ttu-id="3fbda-116">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3fbda-116">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="3fbda-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="3fbda-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fbda-118">Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="3fbda-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3fbda-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3fbda-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fbda-120">Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die Momentaufnahme darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fbda-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the snapshot.</span></span> <span data-ttu-id="3fbda-121">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3fbda-121">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3fbda-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fbda-122">Requirements</span></span>



| <span data-ttu-id="3fbda-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fbda-123">Requirement</span></span> | <span data-ttu-id="3fbda-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3fbda-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbda-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fbda-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3fbda-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fbda-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3fbda-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fbda-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3fbda-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fbda-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fbda-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fbda-129">Namespace</span></span><br/>                | <span data-ttu-id="3fbda-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3fbda-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fbda-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3fbda-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fbda-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3fbda-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fbda-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3fbda-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fbda-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fbda-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fbda-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fbda-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbda-136">**CIM \_ snapshoto-virtualsystem**</span><span class="sxs-lookup"><span data-stu-id="3fbda-136">**CIM\_SnapshotOfVirtualSystem**</span></span>](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[<span data-ttu-id="3fbda-137">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="3fbda-137">**CreateSnapshot**</span></span>](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

