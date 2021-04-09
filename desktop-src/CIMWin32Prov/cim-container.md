---
description: Die CIM \_ -Container Klasse stellt eine Zuordnung zwischen einem enthaltenen und einem enthaltenden physischen Element dar. Ein enthaltende Objekt muss ein physisches Paket sein.
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: CIM_Container-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70aca54c80a954deed88d1ec740f0057753bf5e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958447"
---
# <a name="cim_container-class"></a><span data-ttu-id="813ab-104">CIM- \_ Container Klasse</span><span class="sxs-lookup"><span data-stu-id="813ab-104">CIM\_Container class</span></span>

<span data-ttu-id="813ab-105">Die **CIM- \_ Container** Klasse stellt eine Zuordnung zwischen einem enthaltenen und einem enthaltenden physischen Element dar.</span><span class="sxs-lookup"><span data-stu-id="813ab-105">The **CIM\_Container** class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="813ab-106">Ein enthaltende Objekt muss ein physisches Paket sein.</span><span class="sxs-lookup"><span data-stu-id="813ab-106">A containing object must be a physical package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="813ab-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="813ab-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="813ab-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="813ab-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="813ab-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="813ab-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="813ab-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="813ab-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="813ab-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="813ab-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a><span data-ttu-id="813ab-112">Member</span><span class="sxs-lookup"><span data-stu-id="813ab-112">Members</span></span>

<span data-ttu-id="813ab-113">Die **CIM- \_ Container** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="813ab-113">The **CIM\_Container** class has these types of members:</span></span>

-   [<span data-ttu-id="813ab-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="813ab-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="813ab-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="813ab-115">Properties</span></span>

<span data-ttu-id="813ab-116">Die **CIM- \_ Container** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="813ab-116">The **CIM\_Container** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="813ab-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="813ab-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="813ab-118">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="813ab-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="813ab-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="813ab-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="813ab-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="813ab-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="813ab-121">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das physische Paket darstellt, das andere physische Elemente enthält, einschließlich anderer Pakete.</span><span class="sxs-lookup"><span data-stu-id="813ab-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that represents the physical package that contains other physical elements, including other packages.</span></span>

</dd> <dt>

<span data-ttu-id="813ab-122">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="813ab-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="813ab-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="813ab-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="813ab-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="813ab-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="813ab-125">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="813ab-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="813ab-126">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="813ab-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="813ab-127">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="813ab-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="813ab-128">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="813ab-128">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="813ab-129">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="813ab-129">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="813ab-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="813ab-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="813ab-131">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="813ab-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="813ab-132">Ein [**CIM \_ PhysicalElement**](cim-physicalelement.md) , das das physische Element beschreibt, das im Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="813ab-132">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="813ab-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="813ab-133">Remarks</span></span>

<span data-ttu-id="813ab-134">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="813ab-134">WMI does not implement this class.</span></span> <span data-ttu-id="813ab-135">Weitere Informationen zu Klassen, die vom **CIM- \_ Container** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="813ab-135">For more information about classes derived from **CIM\_Container**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="813ab-136">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="813ab-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="813ab-137">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="813ab-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="813ab-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="813ab-138">Requirements</span></span>



| <span data-ttu-id="813ab-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="813ab-139">Requirement</span></span> | <span data-ttu-id="813ab-140">Wert</span><span class="sxs-lookup"><span data-stu-id="813ab-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="813ab-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="813ab-141">Minimum supported client</span></span><br/> | <span data-ttu-id="813ab-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="813ab-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="813ab-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="813ab-143">Minimum supported server</span></span><br/> | <span data-ttu-id="813ab-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="813ab-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="813ab-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="813ab-145">Namespace</span></span><br/>                | <span data-ttu-id="813ab-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="813ab-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="813ab-147">MOF</span><span class="sxs-lookup"><span data-stu-id="813ab-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="813ab-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="813ab-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="813ab-149">DLL</span><span class="sxs-lookup"><span data-stu-id="813ab-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="813ab-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="813ab-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="813ab-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="813ab-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="813ab-152">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="813ab-152">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

