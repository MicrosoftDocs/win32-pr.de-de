---
description: Die CIM- \_ softwareelementchecks-Zuordnungs Klasse verknüpft ein Softwareelement mit Bedingungs-oder Standortinformationen, die für eine Funktion erforderlich sind.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: CIM_SoftwareElementChecks-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860840"
---
# <a name="cim_softwareelementchecks-class"></a><span data-ttu-id="7c7a6-103">CIM \_ softwareelementchecks-Klasse</span><span class="sxs-lookup"><span data-stu-id="7c7a6-103">CIM\_SoftwareElementChecks class</span></span>

<span data-ttu-id="7c7a6-104">Die **CIM- \_ softwareelementchecks** -Zuordnungs Klasse verknüpft ein Softwareelement mit Bedingungs-oder Standortinformationen, die für eine Funktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-104">The **CIM\_SoftwareElementChecks** association class relates a software element with condition or location information that a feature may require.</span></span>

<span data-ttu-id="7c7a6-105">Da Software Elemente in einem Zustand, der sofort ausgeführt werden kann, nicht in einen anderen Zustand übergehen können, ist der Wert der **Phase** -Eigenschaft auf den Zustand für [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Objekte im Zustand "bereit bis ausgeführt" beschränkt.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-105">Because software elements in a ready-to-run state cannot transition into another state, the value of the **Phase** property is restricted to in-state for [**CIM\_SoftwareElement**](cim-softwareelement.md) objects in a ready-to-run state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c7a6-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7c7a6-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7c7a6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7c7a6-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7c7a6-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7a6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c7a6-110">Syntax</span></span>

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a><span data-ttu-id="7c7a6-111">Member</span><span class="sxs-lookup"><span data-stu-id="7c7a6-111">Members</span></span>

<span data-ttu-id="7c7a6-112">Die **CIM- \_ softwareelementchecks** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7c7a6-112">The **CIM\_SoftwareElementChecks** class has these types of members:</span></span>

-   [<span data-ttu-id="7c7a6-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c7a6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c7a6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c7a6-114">Properties</span></span>

<span data-ttu-id="7c7a6-115">Die **CIM- \_ softwareelementchecks** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-115">The **CIM\_SoftwareElementChecks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c7a6-116">**Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-116">**Check**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c7a6-117">Datentyp: **CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-117">Data type: **CIM\_Check**</span></span>
</dt> <dt>

<span data-ttu-id="7c7a6-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c7a6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c7a6-119">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7c7a6-119">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7c7a6-120">Verweis auf die Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-120">Reference to the check.</span></span>

</dd> <dt>

<span data-ttu-id="7c7a6-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c7a6-122">Datentyp: **CIM \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="7c7a6-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c7a6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c7a6-124">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7c7a6-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7c7a6-125">Verweis auf das-Element.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-125">Reference to the element.</span></span>

</dd> <dt>

<span data-ttu-id="7c7a6-126">**Phase**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-126">**Phase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c7a6-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c7a6-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c7a6-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c7a6-129">Gibt an, ob es sich bei der referenzierten Prüfung um eine Zustands Überprüfung oder eine Überprüfung des nächsten Zustands handelt.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-129">Indicates whether the referenced check is an in-state check or a next-state check.</span></span>

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

<span data-ttu-id="7c7a6-130">**In-State** (0)</span><span class="sxs-lookup"><span data-stu-id="7c7a6-130">**In-State** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

<span data-ttu-id="7c7a6-131">**Nächster Zustand** (1)</span><span class="sxs-lookup"><span data-stu-id="7c7a6-131">**Next-State** (1)</span></span>


<span data-ttu-id="7c7a6-132"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7c7a6-132"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7c7a6-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c7a6-133">Remarks</span></span>

<span data-ttu-id="7c7a6-134">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-134">WMI does not implement this class.</span></span> <span data-ttu-id="7c7a6-135">Informationen zu WMI-Klassen, die von **CIM \_ Softwareelement Checks** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c7a6-135">For WMI classes derived from **CIM\_SoftwareElementChecks**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7c7a6-136">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7c7a6-137">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c7a6-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c7a6-138">Requirements</span></span>



| <span data-ttu-id="7c7a6-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c7a6-139">Requirement</span></span> | <span data-ttu-id="7c7a6-140">Wert</span><span class="sxs-lookup"><span data-stu-id="7c7a6-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c7a6-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c7a6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7c7a6-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c7a6-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c7a6-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c7a6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7c7a6-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c7a6-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c7a6-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c7a6-145">Namespace</span></span><br/>                | <span data-ttu-id="7c7a6-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7c7a6-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c7a6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7c7a6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c7a6-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7c7a6-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c7a6-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7c7a6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c7a6-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c7a6-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

