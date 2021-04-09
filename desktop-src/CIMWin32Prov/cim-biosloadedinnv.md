---
description: Die CIM \_ biosloadedinnv-Klasse ordnet ein BIOS-Element und den nicht flüchtigen Speicher zu, in dem er geladen ist.
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: CIM_BIOSLoadedInNV-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de07e1d4b886ad14f6a7fd8dbb96c1c0f2d2079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958459"
---
# <a name="cim_biosloadedinnv-class"></a><span data-ttu-id="06324-103">CIM- \_ Klasse "biosloadedinnv"</span><span class="sxs-lookup"><span data-stu-id="06324-103">CIM\_BIOSLoadedInNV class</span></span>

<span data-ttu-id="06324-104">Die **CIM \_ biosloadedinnv** -Klasse ordnet ein BIOS-Element und den nicht flüchtigen Speicher zu, in dem er geladen ist.</span><span class="sxs-lookup"><span data-stu-id="06324-104">The **CIM\_BIOSLoadedInNV** class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06324-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="06324-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06324-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="06324-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06324-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="06324-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="06324-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="06324-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06324-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="06324-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="06324-110">Member</span><span class="sxs-lookup"><span data-stu-id="06324-110">Members</span></span>

<span data-ttu-id="06324-111">Die CIM-Klasse " **\_ biosloadedinnv** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="06324-111">The **CIM\_BIOSLoadedInNV** class has these types of members:</span></span>

-   [<span data-ttu-id="06324-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06324-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06324-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06324-113">Properties</span></span>

<span data-ttu-id="06324-114">Die CIM-Klasse " **\_ biosloadedinnv** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="06324-114">The **CIM\_BIOSLoadedInNV** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06324-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="06324-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06324-116">Datentyp: **CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="06324-116">Data type: **CIM\_NonVolatileStorage**</span></span>
</dt> <dt>

<span data-ttu-id="06324-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06324-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06324-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="06324-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="06324-119">Ein [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) , der den nicht flüchtigen Speicher beschreibt.</span><span class="sxs-lookup"><span data-stu-id="06324-119">A [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) that describes the non-volatile storage.</span></span>

</dd> <dt>

<span data-ttu-id="06324-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="06324-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06324-121">Datentyp: **CIM \_ bioselements**</span><span class="sxs-lookup"><span data-stu-id="06324-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="06324-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06324-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06324-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="06324-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="06324-124">Ein [**CIM- \_ bioselor**](cim-bioselement.md) , das das im nicht flüchtigen Block gespeicherte BIOS beschreibt.</span><span class="sxs-lookup"><span data-stu-id="06324-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS stored in the non-volatile extent.</span></span>

</dd> <dt>

<span data-ttu-id="06324-125">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="06324-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06324-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06324-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06324-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06324-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06324-128">Die Endadresse, an der sich das BIOS im nicht flüchtigen Speicher befindet.</span><span class="sxs-lookup"><span data-stu-id="06324-128">Ending address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="06324-129">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="06324-129">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="06324-130">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="06324-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06324-131">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06324-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06324-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06324-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06324-133">Die Startadresse, an der sich das BIOS im nicht flüchtigen Speicher befindet.</span><span class="sxs-lookup"><span data-stu-id="06324-133">Starting address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="06324-134">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="06324-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06324-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06324-135">Remarks</span></span>

<span data-ttu-id="06324-136">Die CIM-Klasse " **\_ biosloadedinnv** " ist von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="06324-136">The **CIM\_BIOSLoadedInNV** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="06324-137">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="06324-137">WMI does not implement this class.</span></span>

<span data-ttu-id="06324-138">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="06324-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06324-139">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="06324-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06324-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06324-140">Requirements</span></span>



| <span data-ttu-id="06324-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06324-141">Requirement</span></span> | <span data-ttu-id="06324-142">Wert</span><span class="sxs-lookup"><span data-stu-id="06324-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06324-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06324-143">Minimum supported client</span></span><br/> | <span data-ttu-id="06324-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06324-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06324-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06324-145">Minimum supported server</span></span><br/> | <span data-ttu-id="06324-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06324-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06324-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="06324-147">Namespace</span></span><br/>                | <span data-ttu-id="06324-148">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="06324-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06324-149">MOF</span><span class="sxs-lookup"><span data-stu-id="06324-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06324-150"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="06324-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06324-151">DLL</span><span class="sxs-lookup"><span data-stu-id="06324-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06324-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06324-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06324-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06324-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06324-154">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="06324-154">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

