---
description: Die CIM \_ associatedakku-Abhängigkeit ordnet einen Akku einem logischen Gerät zu. Verwenden Sie diese Zuordnung, um einzelne Batterien zu modellieren, die eine unterbrechungsfreie Stromversorgung (USV) bilden.
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: CIM_AssociatedBattery-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214233"
---
# <a name="cim_associatedbattery-class"></a><span data-ttu-id="c371c-104">CIM \_ associatedakku-Klasse</span><span class="sxs-lookup"><span data-stu-id="c371c-104">CIM\_AssociatedBattery class</span></span>

<span data-ttu-id="c371c-105">Die **CIM \_ associatedakku** -Abhängigkeit ordnet einen Akku einem logischen Gerät zu.</span><span class="sxs-lookup"><span data-stu-id="c371c-105">The **CIM\_AssociatedBattery** dependency associates a battery with a logical device.</span></span> <span data-ttu-id="c371c-106">Verwenden Sie diese Zuordnung, um einzelne Batterien zu modellieren, die eine unterbrechungsfreie Stromversorgung (USV) bilden.</span><span class="sxs-lookup"><span data-stu-id="c371c-106">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c371c-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c371c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c371c-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c371c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c371c-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c371c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c371c-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c371c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c371c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c371c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c371c-112">Member</span><span class="sxs-lookup"><span data-stu-id="c371c-112">Members</span></span>

<span data-ttu-id="c371c-113">Die **CIM \_ associatedakku** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c371c-113">The **CIM\_AssociatedBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="c371c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c371c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c371c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c371c-115">Properties</span></span>

<span data-ttu-id="c371c-116">Die **CIM \_ associatedakku** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c371c-116">The **CIM\_AssociatedBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c371c-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="c371c-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c371c-118">Datentyp: **CIM \_ Akku**</span><span class="sxs-lookup"><span data-stu-id="c371c-118">Data type: **CIM\_Battery**</span></span>
</dt> <dt>

<span data-ttu-id="c371c-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c371c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c371c-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="c371c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c371c-121">Eine [**CIM- \_ Akku**](cim-battery.md) , in der der Akku beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c371c-121">A [**CIM\_Battery**](cim-battery.md) that describes the battery.</span></span>

</dd> <dt>

<span data-ttu-id="c371c-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="c371c-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c371c-123">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c371c-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c371c-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c371c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c371c-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="c371c-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c371c-126">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät enthält, das den Akku benötigt oder mit diesem verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c371c-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device needing or associated with the battery.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c371c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c371c-127">Remarks</span></span>

<span data-ttu-id="c371c-128">Die **CIM \_ associatedakku** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c371c-128">The **CIM\_AssociatedBattery** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c371c-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c371c-129">WMI does not implement this class.</span></span> <span data-ttu-id="c371c-130">Weitere Informationen zu Klassen, die von **CIM \_ associatedakku** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c371c-130">For more information about classes derived from **CIM\_AssociatedBattery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c371c-131">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c371c-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c371c-132">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c371c-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c371c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c371c-133">Requirements</span></span>



| <span data-ttu-id="c371c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c371c-134">Requirement</span></span> | <span data-ttu-id="c371c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c371c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c371c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c371c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c371c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c371c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c371c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c371c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c371c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c371c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c371c-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="c371c-140">Namespace</span></span><br/>                | <span data-ttu-id="c371c-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c371c-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c371c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c371c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c371c-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c371c-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c371c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c371c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c371c-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c371c-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c371c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c371c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c371c-147">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="c371c-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

