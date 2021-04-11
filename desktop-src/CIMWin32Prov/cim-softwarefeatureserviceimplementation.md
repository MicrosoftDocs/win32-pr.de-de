---
description: Die CIM \_ softwarefeatureserviceimplementation-Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung in Software dar.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureServiceImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126014"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a><span data-ttu-id="fe846-103">CIM \_ softwarefeatureserviceimplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="fe846-103">CIM\_SoftwareFeatureServiceImplementation class</span></span>

<span data-ttu-id="fe846-104">Die **CIM \_ softwarefeatureserviceimplementation** -Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung in Software dar.</span><span class="sxs-lookup"><span data-stu-id="fe846-104">The **CIM\_SoftwareFeatureServiceImplementation** class represents an association between a service and how it is implemented in software.</span></span> <span data-ttu-id="fe846-105">Ein Dienst kann von mehreren Softwarefunktionen bereitgestellt werden, die miteinander zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe846-105">A service can be provided by more than one software feature, operating in conjunction with one another.</span></span> <span data-ttu-id="fe846-106">Darüber hinaus kann ein Software Feature mehr als einen Dienst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fe846-106">Additionally, a software feature can provide more than one service.</span></span> <span data-ttu-id="fe846-107">Wenn mehrere Software Features einem einzelnen Dienst zugeordnet sind, wird davon ausgegangen, dass die Elemente zusammenarbeiten, um den Dienst bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fe846-107">When multiple software features are associated with a single service, it is assumed that the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="fe846-108">Wenn verschiedene Implementierungen eines Dienstanbieter vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des Dienst Objekts.</span><span class="sxs-lookup"><span data-stu-id="fe846-108">If different implementations of a service exist, each implementation would result in individual instantiations of the service object.</span></span> <span data-ttu-id="fe846-109">Einzelne Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="fe846-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe846-110">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fe846-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fe846-111">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fe846-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fe846-112">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe846-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fe846-113">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fe846-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe846-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe846-114">Syntax</span></span>

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fe846-115">Member</span><span class="sxs-lookup"><span data-stu-id="fe846-115">Members</span></span>

<span data-ttu-id="fe846-116">Die **CIM- \_ softwarefeatureserviceimplementation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fe846-116">The **CIM\_SoftwareFeatureServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="fe846-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe846-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe846-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe846-118">Properties</span></span>

<span data-ttu-id="fe846-119">Die **CIM- \_ softwarefeatureserviceimplementation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe846-119">The **CIM\_SoftwareFeatureServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe846-120">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="fe846-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe846-121">Datentyp: **CIM \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="fe846-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="fe846-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe846-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe846-123">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="fe846-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fe846-124">Ein [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) , das das Vorgänger Software Feature beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe846-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="fe846-125">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="fe846-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe846-126">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="fe846-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="fe846-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe846-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe846-128">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="fe846-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fe846-129">Ein [**CIM- \_ Dienst**](cim-service.md) , der den abhängigen Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe846-129">A [**CIM\_Service**](cim-service.md) that describes the dependent service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe846-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe846-130">Remarks</span></span>

<span data-ttu-id="fe846-131">Die **CIM- \_ softwarefeatureserviceimplementation** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fe846-131">The **CIM\_SoftwareFeatureServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fe846-132">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fe846-132">WMI does not implement this class.</span></span>

<span data-ttu-id="fe846-133">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fe846-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fe846-134">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fe846-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe846-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe846-135">Requirements</span></span>



| <span data-ttu-id="fe846-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe846-136">Requirement</span></span> | <span data-ttu-id="fe846-137">Wert</span><span class="sxs-lookup"><span data-stu-id="fe846-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe846-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe846-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fe846-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe846-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe846-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe846-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fe846-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe846-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe846-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe846-142">Namespace</span></span><br/>                | <span data-ttu-id="fe846-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fe846-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fe846-144">MOF</span><span class="sxs-lookup"><span data-stu-id="fe846-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe846-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fe846-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe846-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fe846-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe846-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe846-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe846-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe846-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe846-149">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="fe846-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

