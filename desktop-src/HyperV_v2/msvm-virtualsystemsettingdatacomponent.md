---
description: Eine generische Zuordnung, die verwendet wird, um einen Teil der Beziehungen zwischen einer Instanz von CIM \_ virtualsystemsettingdata und einer oder mehreren Instanzen von CIM \_ resourcezucationsettingdata herzustellen.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Msvm_VirtualSystemSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341181"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="b2751-103">MSVM \_ virtualsystemsettingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="b2751-103">Msvm\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="b2751-104">Eine generische Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) und einer oder mehreren Instanzen von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b2751-104">A generic association used to establish 'part of' relationships between one instance of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) and one or more instances of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="b2751-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2751-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2751-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2751-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b2751-107">Member</span><span class="sxs-lookup"><span data-stu-id="b2751-107">Members</span></span>

<span data-ttu-id="b2751-108">Die **MSVM \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b2751-108">The **Msvm\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b2751-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2751-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2751-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2751-110">Properties</span></span>

<span data-ttu-id="b2751-111">Die **MSVM \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2751-111">The **Msvm\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2751-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b2751-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2751-113">Datentyp: **[ **CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b2751-113">Data type: **[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b2751-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2751-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2751-115">Qualifizierer: **außer Kraft** setzung, **Min** (1), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="b2751-115">Qualifiers: **Override**, **Min** (1), **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b2751-116">Das übergeordnete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="b2751-116">The parent element in the association.</span></span> <span data-ttu-id="b2751-117">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdatacomponent**](/previous-versions//cc150674(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b2751-117">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b2751-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b2751-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2751-119">Datentyp: **[ **CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="b2751-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="b2751-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2751-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2751-121">Das untergeordnete-Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="b2751-121">The child element in the association.</span></span> <span data-ttu-id="b2751-122">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdatacomponent**](/previous-versions//cc150674(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b2751-122">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2751-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2751-123">Remarks</span></span>

<span data-ttu-id="b2751-124">Der Zugriff auf die **MSVM \_ virtualsystemsettingdatacomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="b2751-124">Access to the **Msvm\_VirtualSystemSettingDataComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b2751-125">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b2751-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2751-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2751-126">Requirements</span></span>



| <span data-ttu-id="b2751-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2751-127">Requirement</span></span> | <span data-ttu-id="b2751-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b2751-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2751-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2751-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2751-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2751-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b2751-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2751-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2751-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2751-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2751-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2751-133">Namespace</span></span><br/>                | <span data-ttu-id="b2751-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2751-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2751-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b2751-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2751-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b2751-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2751-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b2751-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2751-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2751-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2751-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2751-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2751-140">**CIM \_ virtualsystemsettingdatacomponent**</span><span class="sxs-lookup"><span data-stu-id="b2751-140">**CIM\_VirtualSystemSettingDataComponent**</span></span>](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

<span data-ttu-id="b2751-141">[**CIM \_ virtualsystemsettingdatacomponent**](/previous-versions//cc150674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2751-141">[**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b2751-142">Klassen des virtuellen Systems</span><span class="sxs-lookup"><span data-stu-id="b2751-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

