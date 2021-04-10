---
description: Die CIM-Zuordnungs Slots-Zuordnung \_ beschreibt das Layout von Slots auf einem hostboard oder einer Adapterkarte.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: CIM_AdjacentSlots-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127221"
---
# <a name="cim_adjacentslots-class"></a><span data-ttu-id="1d0b7-103">CIM-Klasse "- \_ Klasse"</span><span class="sxs-lookup"><span data-stu-id="1d0b7-103">CIM\_AdjacentSlots class</span></span>

<span data-ttu-id="1d0b7-104">Die **CIM \_** -Zuordnungs Slots-Zuordnung beschreibt das Layout von Slots auf einem hostboard oder einer Adapterkarte.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-104">The **CIM\_AdjacentSlots** association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="1d0b7-105">Informationen, wie z. b. der Abstand zwischen den Slots und ob Sie "Shared" sind (wenn eine aufgefüllt wird, der andere Slot kann nicht verwendet werden), werden als Zuordnungs Eigenschaften übermittelt.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-105">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d0b7-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d0b7-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1d0b7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d0b7-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1d0b7-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0b7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d0b7-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a><span data-ttu-id="1d0b7-111">Member</span><span class="sxs-lookup"><span data-stu-id="1d0b7-111">Members</span></span>

<span data-ttu-id="1d0b7-112">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1d0b7-112">The **CIM\_AdjacentSlots** class has these types of members:</span></span>

-   [<span data-ttu-id="1d0b7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d0b7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d0b7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d0b7-114">Properties</span></span>

<span data-ttu-id="1d0b7-115">Die **CIM \_** -Klasse "-Klasse" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-115">The **CIM\_AdjacentSlots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d0b7-116">**Distancebetweenslots**</span><span class="sxs-lookup"><span data-stu-id="1d0b7-116">**DistanceBetweenSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0b7-117">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="1d0b7-117">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="1d0b7-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d0b7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d0b7-119">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="1d0b7-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="1d0b7-120">Abstand in Zoll zwischen angrenzenden Slots.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-120">Distance, in inches, between adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="1d0b7-121">**Sharedslots**</span><span class="sxs-lookup"><span data-stu-id="1d0b7-121">**SharedSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0b7-122">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1d0b7-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d0b7-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d0b7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0b7-124">**True** gibt an, dass einer der Slots durch eine Adapterkarte aufgefüllt wird. der andere Slot muss leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-124">If **TRUE**, one of the slots is populated by an adapter card; the other slot must be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="1d0b7-125">**Slota**</span><span class="sxs-lookup"><span data-stu-id="1d0b7-125">**SlotA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0b7-126">Datentyp: **CIM- \_ Slot**</span><span class="sxs-lookup"><span data-stu-id="1d0b7-126">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="1d0b7-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d0b7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0b7-128">Verweis auf einen der angrenzenden Slots.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-128">Reference to one of the adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="1d0b7-129">**Slotb**</span><span class="sxs-lookup"><span data-stu-id="1d0b7-129">**SlotB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0b7-130">Datentyp: **CIM- \_ Slot**</span><span class="sxs-lookup"><span data-stu-id="1d0b7-130">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="1d0b7-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d0b7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0b7-132">Verweis auf den "anderen" angrenzenden Slot.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-132">Reference to the "other" adjacent slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d0b7-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d0b7-133">Remarks</span></span>

<span data-ttu-id="1d0b7-134">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-134">WMI does not implement this class.</span></span>

<span data-ttu-id="1d0b7-135">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d0b7-136">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1d0b7-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0b7-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d0b7-137">Requirements</span></span>



| <span data-ttu-id="1d0b7-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d0b7-138">Requirement</span></span> | <span data-ttu-id="1d0b7-139">Wert</span><span class="sxs-lookup"><span data-stu-id="1d0b7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0b7-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d0b7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0b7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d0b7-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d0b7-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d0b7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0b7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d0b7-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d0b7-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d0b7-144">Namespace</span></span><br/>                | <span data-ttu-id="1d0b7-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1d0b7-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d0b7-146">MOF</span><span class="sxs-lookup"><span data-stu-id="1d0b7-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d0b7-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1d0b7-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d0b7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1d0b7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d0b7-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d0b7-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d0b7-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d0b7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0b7-151">CIM-Klassen</span><span class="sxs-lookup"><span data-stu-id="1d0b7-151">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

