---
description: Die CIM \_ packagedcomponent-Zuordnung stellt eine explizite Beziehung dar, in der eine Komponente in der Regel in einem physischen Paket (z. b. einem Chassis oder einer Karte) enthalten ist.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: CIM_PackagedComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860748"
---
# <a name="cim_packagedcomponent-class"></a><span data-ttu-id="58595-103">CIM \_ packagedcomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="58595-103">CIM\_PackagedComponent class</span></span>

<span data-ttu-id="58595-104">Die **CIM \_ packagedcomponent** -Zuordnung stellt eine explizite Beziehung dar, in der eine Komponente in der Regel in einem physischen Paket (z. b. einem Chassis oder einer Karte) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="58595-104">The **CIM\_PackagedComponent** association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

<span data-ttu-id="58595-105">**Hinweis**  Eine Komponente kann aus dem enthaltenden Paket entfernt oder noch nicht in eingefügt werden (d. h., **die** boolesche Eigenschaft für Wechsel Datenträger ist **true**).</span><span class="sxs-lookup"><span data-stu-id="58595-105">**Note**  A component may be removed from, or not yet inserted into, its containing package (that is, the **Removable** Boolean property is **TRUE**).</span></span> <span data-ttu-id="58595-106">Daher ist eine Komponente möglicherweise nicht immer einem Container zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="58595-106">Therefore, a component may not always be associated with a container.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58595-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="58595-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58595-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58595-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58595-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="58595-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="58595-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="58595-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58595-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="58595-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="58595-112">Member</span><span class="sxs-lookup"><span data-stu-id="58595-112">Members</span></span>

<span data-ttu-id="58595-113">Die **CIM \_ packagedcomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58595-113">The **CIM\_PackagedComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="58595-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58595-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58595-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58595-115">Properties</span></span>

<span data-ttu-id="58595-116">Die **CIM \_ packagedcomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58595-116">The **CIM\_PackagedComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58595-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="58595-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58595-118">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="58595-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="58595-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58595-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58595-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="58595-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="58595-121">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das physische Paket beschreibt, das Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="58595-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that contains component(s).</span></span>

</dd> <dt>

<span data-ttu-id="58595-122">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="58595-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58595-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58595-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58595-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58595-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58595-125">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="58595-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="58595-126">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="58595-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="58595-127">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58595-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="58595-128">Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="58595-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="58595-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="58595-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58595-130">Datentyp: **CIM \_ physicalcomponent**</span><span class="sxs-lookup"><span data-stu-id="58595-130">Data type: **CIM\_PhysicalComponent**</span></span>
</dt> <dt>

<span data-ttu-id="58595-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58595-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58595-132">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="58595-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="58595-133">Eine [**CIM- \_ physicalcomponent**](cim-physicalcomponent.md) , die die physische Komponente beschreibt, die im Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="58595-133">A [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) describing the physical component which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58595-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58595-134">Remarks</span></span>

<span data-ttu-id="58595-135">Die **CIM \_ packagedcomponent** -Klasse wird vom [**CIM- \_ Container**](cim-container.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58595-135">The **CIM\_PackagedComponent** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="58595-136">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="58595-136">WMI does not implement this class.</span></span>

<span data-ttu-id="58595-137">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58595-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58595-138">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="58595-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58595-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58595-139">Requirements</span></span>



| <span data-ttu-id="58595-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58595-140">Requirement</span></span> | <span data-ttu-id="58595-141">Wert</span><span class="sxs-lookup"><span data-stu-id="58595-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58595-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58595-142">Minimum supported client</span></span><br/> | <span data-ttu-id="58595-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58595-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58595-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58595-144">Minimum supported server</span></span><br/> | <span data-ttu-id="58595-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58595-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58595-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="58595-146">Namespace</span></span><br/>                | <span data-ttu-id="58595-147">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58595-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58595-148">MOF</span><span class="sxs-lookup"><span data-stu-id="58595-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58595-149"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58595-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58595-150">DLL</span><span class="sxs-lookup"><span data-stu-id="58595-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58595-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58595-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58595-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58595-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58595-153">**CIM- \_ Container**</span><span class="sxs-lookup"><span data-stu-id="58595-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

