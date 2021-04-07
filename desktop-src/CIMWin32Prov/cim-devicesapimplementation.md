---
description: Die CIM \_ -Klasse devicesapimplementation stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und der Art der Implementierung dar.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: CIM_DeviceSAPImplementation-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748697"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a><span data-ttu-id="dae36-103">CIM_DeviceSAPImplementation-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="dae36-103">CIM_DeviceSAPImplementation class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dae36-104">Die **CIM-Klasse \_ devicesapimplementation** stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und der Art der Implementierung dar.</span><span class="sxs-lookup"><span data-stu-id="dae36-104">The **CIM\_DeviceSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="dae36-105">Wenn einem SAP Viele logische Geräte zugeordnet sind, werden die Elemente zusammen mit dem Zugriffspunkt bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dae36-105">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="dae36-106">Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des SAP-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dae36-106">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dae36-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dae36-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dae36-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dae36-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dae36-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="dae36-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dae36-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dae36-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae36-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="dae36-111">Syntax</span></span>

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="dae36-112">Member</span><span class="sxs-lookup"><span data-stu-id="dae36-112">Members</span></span>

<span data-ttu-id="dae36-113">Die CIM-Klasse " **\_ devicesapimplementation** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dae36-113">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="dae36-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dae36-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dae36-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dae36-115">Properties</span></span>

<span data-ttu-id="dae36-116">Die CIM-Klasse " **\_ devicesapimplementation** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dae36-116">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dae36-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="dae36-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae36-118">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="dae36-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="dae36-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dae36-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dae36-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="dae36-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dae36-121">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="dae36-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="dae36-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="dae36-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae36-123">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="dae36-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="dae36-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dae36-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dae36-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="dae36-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="dae36-126">Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der den Dienst Zugriffspunkt beschreibt, der über das logische Gerät implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="dae36-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dae36-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dae36-127">Remarks</span></span>

<span data-ttu-id="dae36-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dae36-128">WMI does not implement this class.</span></span>

<span data-ttu-id="dae36-129">Die **CIM- \_ devicesapimplementation** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dae36-129">The **CIM\_DeviceSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="dae36-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dae36-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dae36-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dae36-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae36-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dae36-132">Requirements</span></span>



| <span data-ttu-id="dae36-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dae36-133">Requirement</span></span> | <span data-ttu-id="dae36-134">Wert</span><span class="sxs-lookup"><span data-stu-id="dae36-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dae36-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dae36-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dae36-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dae36-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dae36-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dae36-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dae36-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dae36-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dae36-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="dae36-139">Namespace</span></span><br/>                | <span data-ttu-id="dae36-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dae36-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dae36-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dae36-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dae36-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dae36-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dae36-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dae36-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dae36-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dae36-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae36-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dae36-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae36-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="dae36-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

