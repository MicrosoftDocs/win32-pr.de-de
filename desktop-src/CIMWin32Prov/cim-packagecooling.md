---
description: Die CIM \_ packagecooling-Zuordnung stellt die Beziehung dar, in der ein Kühlgerät in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Kühlung des Pakets zu unterstützen.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: CIM_PackageCooling-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f88cd3f07983870bed8fd2d740f3bf9051019b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523739"
---
# <a name="cim_packagecooling-class"></a><span data-ttu-id="aa9b8-103">CIM \_ packagecooling-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa9b8-103">CIM\_PackageCooling class</span></span>

<span data-ttu-id="aa9b8-104">Die **CIM \_ packagecooling** -Zuordnung stellt die Beziehung dar, in der ein Kühlgerät in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Kühlung des Pakets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-104">The **CIM\_PackageCooling** association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa9b8-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aa9b8-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aa9b8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aa9b8-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aa9b8-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9b8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa9b8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="aa9b8-110">Member</span><span class="sxs-lookup"><span data-stu-id="aa9b8-110">Members</span></span>

<span data-ttu-id="aa9b8-111">Die **CIM \_ packagecooling** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aa9b8-111">The **CIM\_PackageCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="aa9b8-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa9b8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa9b8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa9b8-113">Properties</span></span>

<span data-ttu-id="aa9b8-114">Die **CIM \_ packagecooling** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-114">The **CIM\_PackageCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa9b8-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="aa9b8-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9b8-116">Datentyp: **CIM \_ coolingdevice**</span><span class="sxs-lookup"><span data-stu-id="aa9b8-116">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="aa9b8-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9b8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9b8-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="aa9b8-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="aa9b8-119">Ein [**CIM \_ coolingdevice**](cim-coolingdevice.md) , das das Kühlgerät für das Paket beschreibt.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-119">A [**CIM\_CoolingDevice**](cim-coolingdevice.md) that describes the cooling device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b8-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="aa9b8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9b8-121">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="aa9b8-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="aa9b8-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9b8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9b8-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="aa9b8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="aa9b8-124">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das physische Paket beschreibt, dessen Umgebung gekühlt wird.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package whose environment is cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa9b8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa9b8-125">Remarks</span></span>

<span data-ttu-id="aa9b8-126">**CIM \_ Packagecooling** ist von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-126">**CIM\_PackageCooling** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="aa9b8-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-127">WMI does not implement this class.</span></span>

<span data-ttu-id="aa9b8-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aa9b8-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9b8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa9b8-130">Requirements</span></span>



| <span data-ttu-id="aa9b8-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa9b8-131">Requirement</span></span> | <span data-ttu-id="aa9b8-132">Wert</span><span class="sxs-lookup"><span data-stu-id="aa9b8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9b8-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa9b8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9b8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa9b8-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa9b8-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa9b8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9b8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa9b8-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa9b8-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa9b8-137">Namespace</span></span><br/>                | <span data-ttu-id="aa9b8-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aa9b8-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa9b8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="aa9b8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa9b8-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa9b8-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa9b8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="aa9b8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa9b8-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa9b8-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9b8-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa9b8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9b8-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="aa9b8-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

