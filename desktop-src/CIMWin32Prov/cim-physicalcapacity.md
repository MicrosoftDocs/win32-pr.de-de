---
description: Die CIM \_ physicalcapacity-Klasse ist eine abstrakte Klasse, die die minimalen und maximalen Anforderungen eines physischen Elements und die Fähigkeit zur Unterstützung verschiedener Hardwaretypen darstellt.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: CIM_PhysicalCapacity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958446"
---
# <a name="cim_physicalcapacity-class"></a><span data-ttu-id="6c777-103">CIM \_ physicalcapacity-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c777-103">CIM\_PhysicalCapacity class</span></span>

<span data-ttu-id="6c777-104">Die **CIM \_ physicalcapacity** -Klasse ist eine abstrakte Klasse, die die minimalen und maximalen Anforderungen eines physischen Elements und die Fähigkeit zur Unterstützung verschiedener Hardwaretypen darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c777-104">The **CIM\_PhysicalCapacity** class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="6c777-105">So können z. b. die minimalen und maximalen Arbeitsspeicher Anforderungen als eine Unterklasse von **CIM \_ physicalcapacity** modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="6c777-105">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c777-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c777-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6c777-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6c777-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6c777-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c777-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6c777-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6c777-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c777-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c777-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="6c777-111">Member</span><span class="sxs-lookup"><span data-stu-id="6c777-111">Members</span></span>

<span data-ttu-id="6c777-112">Die **CIM \_ physicalcapacity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c777-112">The **CIM\_PhysicalCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="6c777-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c777-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c777-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c777-114">Properties</span></span>

<span data-ttu-id="6c777-115">Die **CIM \_ physicalcapacity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c777-115">The **CIM\_PhysicalCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c777-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6c777-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c777-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c777-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c777-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c777-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c777-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6c777-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6c777-120">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6c777-120">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="6c777-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c777-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c777-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c777-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c777-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c777-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c777-124">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6c777-124">Textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="6c777-125">**Name**</span><span class="sxs-lookup"><span data-stu-id="6c777-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c777-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c777-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c777-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c777-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c777-128">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6c777-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6c777-129">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6c777-129">Label by which the object is known.</span></span> <span data-ttu-id="6c777-130">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6c777-130">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c777-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c777-131">Remarks</span></span>

<span data-ttu-id="6c777-132">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6c777-132">WMI does not implement this class.</span></span>

<span data-ttu-id="6c777-133">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6c777-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6c777-134">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6c777-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c777-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c777-135">Requirements</span></span>



| <span data-ttu-id="6c777-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c777-136">Requirement</span></span> | <span data-ttu-id="6c777-137">Wert</span><span class="sxs-lookup"><span data-stu-id="6c777-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c777-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c777-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6c777-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c777-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c777-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c777-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6c777-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c777-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c777-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c777-142">Namespace</span></span><br/>                | <span data-ttu-id="6c777-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6c777-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c777-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6c777-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c777-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6c777-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c777-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6c777-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c777-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c777-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

