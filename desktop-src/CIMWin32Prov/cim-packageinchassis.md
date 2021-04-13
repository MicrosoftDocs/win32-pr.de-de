---
description: Die CIM \_ packageinchassis-Zuordnung stellt die Beziehung dar, in der ein Chassis Andere Pakete enthalten kann, z. b. anderes Chassis und Karten.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: CIM_PackageInChassis-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483358"
---
# <a name="cim_packageinchassis-class"></a><span data-ttu-id="f5896-103">CIM \_ packageingechassis-Klasse</span><span class="sxs-lookup"><span data-stu-id="f5896-103">CIM\_PackageInChassis class</span></span>

<span data-ttu-id="f5896-104">Die **CIM \_ packageinchassis** -Zuordnung stellt die Beziehung dar, in der ein Chassis Andere Pakete enthalten kann, z. b. anderes Chassis und Karten.</span><span class="sxs-lookup"><span data-stu-id="f5896-104">The **CIM\_PackageInChassis** association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5896-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f5896-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5896-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5896-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5896-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f5896-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f5896-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f5896-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5896-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5896-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="f5896-110">Member</span><span class="sxs-lookup"><span data-stu-id="f5896-110">Members</span></span>

<span data-ttu-id="f5896-111">Die **CIM \_ packageinchassis** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f5896-111">The **CIM\_PackageInChassis** class has these types of members:</span></span>

-   [<span data-ttu-id="f5896-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5896-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5896-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5896-113">Properties</span></span>

<span data-ttu-id="f5896-114">Die **CIM \_ packageingechassis** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f5896-114">The **CIM\_PackageInChassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5896-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f5896-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5896-116">Datentyp: **CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="f5896-116">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="f5896-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f5896-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5896-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f5896-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f5896-119">Ein [**CIM- \_ Chassis**](cim-chassis.md) , das das Chassis beschreibt, das andere physische Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="f5896-119">A [**CIM\_Chassis**](cim-chassis.md) describing the chassis that contains other physical packages.</span></span>

</dd> <dt>

<span data-ttu-id="f5896-120">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="f5896-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5896-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f5896-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5896-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f5896-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5896-123">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5896-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="f5896-124">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f5896-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="f5896-125">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5896-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="f5896-126">Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f5896-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5896-127">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f5896-127">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5896-128">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="f5896-128">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="f5896-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f5896-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5896-130">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f5896-130">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f5896-131">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das physische Paket beschreibt, das im Gehäuse enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f5896-131">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package which is contained in the chassis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5896-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5896-132">Remarks</span></span>

<span data-ttu-id="f5896-133">Die **CIM \_ packageingechassis** -Klasse wird vom [**CIM- \_ Container**](cim-container.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f5896-133">The **CIM\_PackageInChassis** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="f5896-134">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f5896-134">WMI does not implement this class.</span></span>

<span data-ttu-id="f5896-135">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f5896-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f5896-136">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f5896-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5896-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5896-137">Requirements</span></span>



| <span data-ttu-id="f5896-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5896-138">Requirement</span></span> | <span data-ttu-id="f5896-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f5896-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5896-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5896-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f5896-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5896-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5896-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5896-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f5896-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5896-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5896-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5896-144">Namespace</span></span><br/>                | <span data-ttu-id="f5896-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f5896-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5896-146">MOF</span><span class="sxs-lookup"><span data-stu-id="f5896-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5896-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f5896-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5896-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f5896-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5896-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5896-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5896-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5896-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5896-151">**CIM- \_ Container**</span><span class="sxs-lookup"><span data-stu-id="f5896-151">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

