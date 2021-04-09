---
description: Die CIM \_ collectionofsensors-Zuordnung stellt die binären Sensoren dar, die den Multistate-Sensor bilden.
ms.assetid: d9494716-bb4e-4aa2-9e3b-e865360c740f
ms.tgt_platform: multiple
title: CIM_CollectionOfSensors-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfSensors
- CIM_CollectionOfSensors.PartComponent
- CIM_CollectionOfSensors.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06f33d3b55c2c35526495d492b0f063fee9c1a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958452"
---
# <a name="cim_collectionofsensors-class"></a><span data-ttu-id="65c3e-103">CIM \_ collectionofsensors-Klasse</span><span class="sxs-lookup"><span data-stu-id="65c3e-103">CIM\_CollectionOfSensors class</span></span>

<span data-ttu-id="65c3e-104">Die **CIM \_ collectionofsensors** -Zuordnung stellt die binären Sensoren dar, die den Multistate-Sensor bilden.</span><span class="sxs-lookup"><span data-stu-id="65c3e-104">The **CIM\_CollectionOfSensors** association represents the binary sensors that make up the multistate sensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65c3e-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="65c3e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65c3e-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65c3e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65c3e-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="65c3e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="65c3e-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="65c3e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c3e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="65c3e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2ABF536-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_CollectionOfSensors : CIM_Component
{
  CIM_BinarySensor     REF PartComponent;
  CIM_MultiStateSensor REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="65c3e-110">Member</span><span class="sxs-lookup"><span data-stu-id="65c3e-110">Members</span></span>

<span data-ttu-id="65c3e-111">Die **CIM \_ collectionofsensors** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="65c3e-111">The **CIM\_CollectionOfSensors** class has these types of members:</span></span>

-   [<span data-ttu-id="65c3e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65c3e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65c3e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65c3e-113">Properties</span></span>

<span data-ttu-id="65c3e-114">Die **CIM \_ collectionofsensors** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="65c3e-114">The **CIM\_CollectionOfSensors** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65c3e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="65c3e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65c3e-116">Datentyp: **CIM \_ multistaatensor**</span><span class="sxs-lookup"><span data-stu-id="65c3e-116">Data type: **CIM\_MultiStateSensor**</span></span>
</dt> <dt>

<span data-ttu-id="65c3e-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="65c3e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65c3e-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="65c3e-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="65c3e-119">Ein [**CIM- \_ multistaatensor**](cim-multistatesensor.md) , der den Multi-State-Sensor beschreibt.</span><span class="sxs-lookup"><span data-stu-id="65c3e-119">A [**CIM\_MultiStateSensor**](cim-multistatesensor.md) that describes the multi-state sensor.</span></span>

</dd> <dt>

<span data-ttu-id="65c3e-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="65c3e-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65c3e-121">Datentyp: **CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="65c3e-121">Data type: **CIM\_BinarySensor**</span></span>
</dt> <dt>

<span data-ttu-id="65c3e-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="65c3e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65c3e-123">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="65c3e-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="65c3e-124">Ein [**CIM- \_ BinarySensor**](cim-binarysensor.md) , der einen binären Sensor beschreibt, der Teil des Multi-State-Sensors ist.</span><span class="sxs-lookup"><span data-stu-id="65c3e-124">A [**CIM\_BinarySensor**](cim-binarysensor.md) that describes a binary sensor that is part of the multi-state sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65c3e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65c3e-125">Remarks</span></span>

<span data-ttu-id="65c3e-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="65c3e-126">WMI does not implement this class.</span></span>

<span data-ttu-id="65c3e-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="65c3e-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65c3e-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="65c3e-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c3e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65c3e-129">Requirements</span></span>



| <span data-ttu-id="65c3e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65c3e-130">Requirement</span></span> | <span data-ttu-id="65c3e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="65c3e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65c3e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65c3e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="65c3e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65c3e-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65c3e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65c3e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="65c3e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65c3e-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65c3e-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="65c3e-136">Namespace</span></span><br/>                | <span data-ttu-id="65c3e-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="65c3e-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65c3e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="65c3e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65c3e-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="65c3e-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65c3e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="65c3e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65c3e-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65c3e-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c3e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65c3e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c3e-143">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="65c3e-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

