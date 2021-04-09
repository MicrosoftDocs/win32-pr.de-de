---
description: Die CIM \_ linkhasconnector-Klasse ordnet Kabel und Verknüpfungen zu, die als physische Connectors verwendet werden, die die physischen Elemente verbinden. Diese Zuordnung definiert explizit die Beziehung von Connectors für CIM \_ physicallink.
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: CIM_LinkHasConnector-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daeb9d07fefc4c52c7b630dcc69099c1cae429a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861239"
---
# <a name="cim_linkhasconnector-class"></a><span data-ttu-id="c63a7-104">CIM \_ linkhasconnector-Klasse</span><span class="sxs-lookup"><span data-stu-id="c63a7-104">CIM\_LinkHasConnector class</span></span>

<span data-ttu-id="c63a7-105">Die **CIM \_ linkhasconnector** -Klasse ordnet Kabel und Verknüpfungen zu, die als physische Connectors verwendet werden, die die physischen Elemente verbinden.</span><span class="sxs-lookup"><span data-stu-id="c63a7-105">The **CIM\_LinkHasConnector** class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="c63a7-106">Diese Zuordnung definiert explizit die Beziehung von Connectors für [**CIM \_ physicallink**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="c63a7-106">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c63a7-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c63a7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c63a7-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c63a7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c63a7-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c63a7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c63a7-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c63a7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c63a7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c63a7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="c63a7-112">Member</span><span class="sxs-lookup"><span data-stu-id="c63a7-112">Members</span></span>

<span data-ttu-id="c63a7-113">Die **CIM \_ linkhasconnector** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c63a7-113">The **CIM\_LinkHasConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="c63a7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c63a7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c63a7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c63a7-115">Properties</span></span>

<span data-ttu-id="c63a7-116">Die **CIM \_ linkhasconnector** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c63a7-116">The **CIM\_LinkHasConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c63a7-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c63a7-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c63a7-118">Datentyp: **CIM \_ physicallink**</span><span class="sxs-lookup"><span data-stu-id="c63a7-118">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="c63a7-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c63a7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c63a7-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c63a7-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c63a7-121">Ein [**CIM- \_ physicallink**](cim-physicallink.md) , der den physischen Link mit einem Connector beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c63a7-121">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="c63a7-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c63a7-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c63a7-123">Datentyp: **CIM \_ physicalconnector**</span><span class="sxs-lookup"><span data-stu-id="c63a7-123">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="c63a7-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c63a7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c63a7-125">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c63a7-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c63a7-126">Ein [**CIM \_ physicalconnector**](cim-physicalconnector.md) , der den physischen Connector beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c63a7-126">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c63a7-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c63a7-127">Remarks</span></span>

<span data-ttu-id="c63a7-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c63a7-128">WMI does not implement this class.</span></span>

<span data-ttu-id="c63a7-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c63a7-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c63a7-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c63a7-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c63a7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c63a7-131">Requirements</span></span>



| <span data-ttu-id="c63a7-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c63a7-132">Requirement</span></span> | <span data-ttu-id="c63a7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c63a7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c63a7-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c63a7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c63a7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c63a7-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c63a7-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c63a7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c63a7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c63a7-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c63a7-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="c63a7-138">Namespace</span></span><br/>                | <span data-ttu-id="c63a7-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c63a7-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c63a7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c63a7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c63a7-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c63a7-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c63a7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c63a7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c63a7-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c63a7-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c63a7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c63a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c63a7-145">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="c63a7-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

