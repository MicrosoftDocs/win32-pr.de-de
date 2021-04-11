---
description: Die CIM \_ packagetempsensor-Zuordnung stellt die Beziehung dar, in der ein Temperatursensor häufig in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Umgebung des Pakets zu überwachen.
ms.assetid: 79f2c4d1-5e1a-4c5f-9ef4-0c8bc3926a13
ms.tgt_platform: multiple
title: CIM_PackageTempSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageTempSensor
- CIM_PackageTempSensor.Dependent
- CIM_PackageTempSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28c3fa3ba569a2bf3101d62734bb9e4d5372fcf0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126933"
---
# <a name="cim_packagetempsensor-class"></a><span data-ttu-id="9905b-103">CIM \_ packagetempsensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="9905b-103">CIM\_PackageTempSensor class</span></span>

<span data-ttu-id="9905b-104">Die **CIM \_ packagetempsensor** -Zuordnung stellt die Beziehung dar, in der ein Temperatursensor häufig in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Umgebung des Pakets zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="9905b-104">The **CIM\_PackageTempSensor** association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9905b-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9905b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9905b-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9905b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9905b-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9905b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9905b-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9905b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9905b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9905b-109">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B8F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageTempSensor : CIM_Dependency
{
  CIM_PhysicalPackage   REF Dependent;
  CIM_TemperatureSensor REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9905b-110">Member</span><span class="sxs-lookup"><span data-stu-id="9905b-110">Members</span></span>

<span data-ttu-id="9905b-111">Die **CIM \_ packagetempsensor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9905b-111">The **CIM\_PackageTempSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="9905b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9905b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9905b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9905b-113">Properties</span></span>

<span data-ttu-id="9905b-114">Die **CIM \_ packagetempsensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9905b-114">The **CIM\_PackageTempSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9905b-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="9905b-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9905b-116">Datentyp: **CIM- \_ Temperatursensor**</span><span class="sxs-lookup"><span data-stu-id="9905b-116">Data type: **CIM\_TemperatureSensor**</span></span>
</dt> <dt>

<span data-ttu-id="9905b-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9905b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9905b-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="9905b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9905b-119">Ein [**CIM \_**](cim-temperaturesensor.md) -Temperatursensor, der den Temperatursensor für das Paket beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9905b-119">A [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) describing the temperature sensor for the package.</span></span>

</dd> <dt>

<span data-ttu-id="9905b-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="9905b-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9905b-121">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="9905b-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="9905b-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9905b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9905b-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="9905b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9905b-124">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das physische Paket beschreibt, dessen Umgebung überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="9905b-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose environment is monitored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9905b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9905b-125">Remarks</span></span>

<span data-ttu-id="9905b-126">**CIM \_ Packagetempsensor** wird von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9905b-126">**CIM\_PackageTempSensor** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9905b-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9905b-127">WMI does not implement this class.</span></span>

<span data-ttu-id="9905b-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9905b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9905b-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9905b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9905b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9905b-130">Requirements</span></span>



| <span data-ttu-id="9905b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9905b-131">Requirement</span></span> | <span data-ttu-id="9905b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9905b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9905b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9905b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9905b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9905b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9905b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9905b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9905b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9905b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9905b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="9905b-137">Namespace</span></span><br/>                | <span data-ttu-id="9905b-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9905b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9905b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9905b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9905b-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9905b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9905b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9905b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9905b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9905b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9905b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9905b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9905b-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="9905b-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

