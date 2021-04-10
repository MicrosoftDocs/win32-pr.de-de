---
description: Die CIM \_ chassisinrack-Zuordnung stellt die &\# 0034 dar, die&\# 0034;-Beziehung zwischen einem Gestell und einem darin enthaltenen Chassis enthält.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: CIM_ChassisInRack-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127113"
---
# <a name="cim_chassisinrack-class"></a><span data-ttu-id="58807-103">CIM \_ chassisinrack-Klasse</span><span class="sxs-lookup"><span data-stu-id="58807-103">CIM\_ChassisInRack class</span></span>

<span data-ttu-id="58807-104">Die **CIM \_ chassisinrack** -Zuordnung stellt die "enthaltende" Beziehung zwischen einem Gestell und einem darin enthaltenen Chassis dar.</span><span class="sxs-lookup"><span data-stu-id="58807-104">The **CIM\_ChassisInRack** association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58807-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="58807-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58807-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58807-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58807-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="58807-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="58807-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="58807-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58807-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="58807-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a><span data-ttu-id="58807-110">Member</span><span class="sxs-lookup"><span data-stu-id="58807-110">Members</span></span>

<span data-ttu-id="58807-111">Die **CIM \_ chassisinrack** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58807-111">The **CIM\_ChassisInRack** class has these types of members:</span></span>

-   [<span data-ttu-id="58807-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58807-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58807-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58807-113">Properties</span></span>

<span data-ttu-id="58807-114">Die **CIM \_ chassisinrack** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58807-114">The **CIM\_ChassisInRack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58807-115">**Bottomu**</span><span class="sxs-lookup"><span data-stu-id="58807-115">**BottomU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58807-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58807-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58807-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58807-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58807-118">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="58807-118">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="58807-119">Eine ganze Zahl, die das niedrigste oder untere "U" angibt, in dem das Chassis eingebunden ist.</span><span class="sxs-lookup"><span data-stu-id="58807-119">Integer that indicates the lowest or bottom "U" in which the chassis is mounted.</span></span> <span data-ttu-id="58807-120">Ein "U" ist eine Standard Maßeinheit für die Höhe eines Rasters oder einer Regal baren Komponente und ist gleich 1,75 Zoll oder 4,445 Zentimeter.</span><span class="sxs-lookup"><span data-stu-id="58807-120">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="58807-121">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="58807-121">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58807-122">Datentyp: **CIM \_ Rack**</span><span class="sxs-lookup"><span data-stu-id="58807-122">Data type: **CIM\_Rack**</span></span>
</dt> <dt>

<span data-ttu-id="58807-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58807-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58807-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="58807-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="58807-125">Ein [**CIM- \_ Rack**](cim-rack.md) , das das Gestell beschreibt, das das Chassis enthält.</span><span class="sxs-lookup"><span data-stu-id="58807-125">A [**CIM\_Rack**](cim-rack.md) that describes the rack that contains the chassis.</span></span>

</dd> <dt>

<span data-ttu-id="58807-126">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="58807-126">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58807-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58807-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58807-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58807-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58807-129">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="58807-129">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="58807-130">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="58807-130">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="58807-131">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58807-131">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="58807-132">Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="58807-132">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="58807-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="58807-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58807-134">Datentyp: **CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="58807-134">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="58807-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58807-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58807-136">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="58807-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="58807-137">Ein [**CIM- \_ Chassis**](cim-chassis.md) , das das Chassis beschreibt, das in das Gestell eingebunden ist.</span><span class="sxs-lookup"><span data-stu-id="58807-137">A [**CIM\_Chassis**](cim-chassis.md) that describes the chassis which is mounted in the rack.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58807-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58807-138">Remarks</span></span>

<span data-ttu-id="58807-139">Die **CIM \_ chassisinrack** -Klasse wird vom [**CIM- \_ Container**](cim-container.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58807-139">The **CIM\_ChassisInRack** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="58807-140">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="58807-140">WMI does not implement this class.</span></span>

<span data-ttu-id="58807-141">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58807-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58807-142">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="58807-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58807-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58807-143">Requirements</span></span>



| <span data-ttu-id="58807-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58807-144">Requirement</span></span> | <span data-ttu-id="58807-145">Wert</span><span class="sxs-lookup"><span data-stu-id="58807-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58807-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58807-146">Minimum supported client</span></span><br/> | <span data-ttu-id="58807-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58807-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58807-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58807-148">Minimum supported server</span></span><br/> | <span data-ttu-id="58807-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58807-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58807-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="58807-150">Namespace</span></span><br/>                | <span data-ttu-id="58807-151">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58807-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58807-152">MOF</span><span class="sxs-lookup"><span data-stu-id="58807-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58807-153"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58807-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58807-154">DLL</span><span class="sxs-lookup"><span data-stu-id="58807-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58807-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58807-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58807-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58807-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58807-157">**CIM- \_ Container**</span><span class="sxs-lookup"><span data-stu-id="58807-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

