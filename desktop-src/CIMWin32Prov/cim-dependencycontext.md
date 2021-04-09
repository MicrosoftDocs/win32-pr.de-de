---
description: Die CIM \_ dependencycontext-Beziehung ordnet eine CIM- \_ Abhängigkeits Klasse einem oder mehreren CIM- \_ Konfigurationsobjekten zu. Beispielsweise können die Abhängigkeiten eines Computer Systems je nach Netzwerk, an das das System angefügt ist, geändert werden.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyContext-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861271"
---
# <a name="cim_dependencycontext-class"></a><span data-ttu-id="7e10e-104">CIM \_ dependencycontext-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e10e-104">CIM\_DependencyContext class</span></span>

<span data-ttu-id="7e10e-105">Die **CIM \_ dependencycontext** -Beziehung ordnet eine [**CIM- \_ Abhängigkeits**](cim-dependency.md) Klasse einem oder mehreren [**CIM- \_ Konfigurations**](cim-configuration.md) Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="7e10e-105">The **CIM\_DependencyContext** relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="7e10e-106">Beispielsweise können die Abhängigkeiten eines Computer Systems je nach Netzwerk, an das das System angefügt ist, geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7e10e-106">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e10e-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7e10e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7e10e-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7e10e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7e10e-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7e10e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7e10e-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7e10e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e10e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e10e-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a><span data-ttu-id="7e10e-112">Member</span><span class="sxs-lookup"><span data-stu-id="7e10e-112">Members</span></span>

<span data-ttu-id="7e10e-113">Die **CIM \_ dependencycontext** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7e10e-113">The **CIM\_DependencyContext** class has these types of members:</span></span>

-   [<span data-ttu-id="7e10e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e10e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e10e-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e10e-115">Properties</span></span>

<span data-ttu-id="7e10e-116">Die **CIM \_ dependencycontext** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e10e-116">The **CIM\_DependencyContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e10e-117">**Context**</span><span class="sxs-lookup"><span data-stu-id="7e10e-117">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e10e-118">Datentyp: **CIM- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="7e10e-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="7e10e-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e10e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e10e-120">Qualifizierer: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7e10e-120">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7e10e-121">Verweis auf das Konfigurationsobjekt, das die Abhängigkeit aggregiert.</span><span class="sxs-lookup"><span data-stu-id="7e10e-121">Reference to the configuration object that aggregates the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="7e10e-122">**Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="7e10e-122">**Dependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e10e-123">Datentyp: **CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="7e10e-123">Data type: **CIM\_Dependency**</span></span>
</dt> <dt>

<span data-ttu-id="7e10e-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e10e-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e10e-125">Verweis auf eine aggregierte Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="7e10e-125">Reference to an aggregated dependency.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e10e-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e10e-126">Remarks</span></span>

<span data-ttu-id="7e10e-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7e10e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7e10e-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7e10e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7e10e-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7e10e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e10e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e10e-130">Requirements</span></span>



| <span data-ttu-id="7e10e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e10e-131">Requirement</span></span> | <span data-ttu-id="7e10e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7e10e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e10e-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e10e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7e10e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e10e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e10e-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e10e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7e10e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e10e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e10e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e10e-137">Namespace</span></span><br/>                | <span data-ttu-id="7e10e-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e10e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e10e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7e10e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e10e-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e10e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e10e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7e10e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e10e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e10e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

