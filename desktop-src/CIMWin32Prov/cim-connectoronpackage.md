---
description: Die CIM \_ connectoronpackage-Klasse stellt eine Zuordnung dar, die die Einschluss Beziehung zwischen Connectors und Paketen explizit macht. Physische Pakete enthalten Connectors und andere physische Elemente.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: CIM_ConnectorOnPackage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861332"
---
# <a name="cim_connectoronpackage-class"></a><span data-ttu-id="e3174-104">CIM \_ connectoronpackage-Klasse</span><span class="sxs-lookup"><span data-stu-id="e3174-104">CIM\_ConnectorOnPackage class</span></span>

<span data-ttu-id="e3174-105">Die **CIM \_ connectoronpackage** -Klasse stellt eine Zuordnung dar, die die Einschluss Beziehung zwischen Connectors und Paketen explizit macht.</span><span class="sxs-lookup"><span data-stu-id="e3174-105">The **CIM\_ConnectorOnPackage** class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="e3174-106">Physische Pakete enthalten Connectors und andere physische Elemente.</span><span class="sxs-lookup"><span data-stu-id="e3174-106">Physical packages contain connectors as well as other physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3174-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e3174-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e3174-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e3174-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e3174-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e3174-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e3174-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e3174-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3174-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3174-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e3174-112">Member</span><span class="sxs-lookup"><span data-stu-id="e3174-112">Members</span></span>

<span data-ttu-id="e3174-113">Die **CIM \_ connectoronpackage** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e3174-113">The **CIM\_ConnectorOnPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="e3174-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3174-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3174-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3174-115">Properties</span></span>

<span data-ttu-id="e3174-116">Die **CIM \_ connectoronpackage** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3174-116">The **CIM\_ConnectorOnPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3174-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e3174-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3174-118">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="e3174-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="e3174-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3174-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3174-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e3174-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e3174-121">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das physische Paket beschreibt, das über einen Connector verfügt.</span><span class="sxs-lookup"><span data-stu-id="e3174-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="e3174-122">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="e3174-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3174-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3174-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3174-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3174-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3174-125">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="e3174-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="e3174-126">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e3174-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="e3174-127">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3174-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="e3174-128">Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e3174-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3174-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e3174-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3174-130">Datentyp: **CIM \_ physicalconnector**</span><span class="sxs-lookup"><span data-stu-id="e3174-130">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="e3174-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3174-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3174-132">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e3174-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e3174-133">Ein [**CIM \_ physicalconnector**](cim-physicalconnector.md) , der den physischen Connector beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e3174-133">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3174-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3174-134">Remarks</span></span>

<span data-ttu-id="e3174-135">Die **CIM \_ connectoronpackage** -Klasse wird vom [**CIM- \_ Container**](cim-container.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e3174-135">The **CIM\_ConnectorOnPackage** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="e3174-136">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e3174-136">WMI does not implement this class.</span></span>

<span data-ttu-id="e3174-137">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e3174-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e3174-138">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e3174-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3174-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3174-139">Requirements</span></span>



| <span data-ttu-id="e3174-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3174-140">Requirement</span></span> | <span data-ttu-id="e3174-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e3174-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3174-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3174-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e3174-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3174-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3174-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3174-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e3174-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3174-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3174-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3174-146">Namespace</span></span><br/>                | <span data-ttu-id="e3174-147">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e3174-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3174-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e3174-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3174-149"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e3174-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3174-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e3174-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3174-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3174-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3174-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3174-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3174-153">**CIM- \_ Container**</span><span class="sxs-lookup"><span data-stu-id="e3174-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

