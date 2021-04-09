---
description: Die CIM \_ -deviceserviceimplementation-Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung dar.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: CIM_DeviceServiceImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ae96d94c95ddda684dbb4d17a2d8eb52fc6ffd4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958477"
---
# <a name="cim_deviceserviceimplementation-class"></a><span data-ttu-id="426f1-103">CIM- \_ deviceserviceimplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="426f1-103">CIM\_DeviceServiceImplementation class</span></span>

<span data-ttu-id="426f1-104">Die **CIM- \_ deviceserviceimplementation** -Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung dar.</span><span class="sxs-lookup"><span data-stu-id="426f1-104">The **CIM\_DeviceServiceImplementation** class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="426f1-105">Wenn mehrere Geräte einem Dienst zugeordnet sind, werden die Elemente zusammen verwendet, um den Dienst bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="426f1-105">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="426f1-106">Wenn verschiedene Implementierungen eines Dienstanbieter vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des Dienst Objekts.</span><span class="sxs-lookup"><span data-stu-id="426f1-106">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="426f1-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="426f1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="426f1-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="426f1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="426f1-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="426f1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="426f1-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="426f1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="426f1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="426f1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="426f1-112">Member</span><span class="sxs-lookup"><span data-stu-id="426f1-112">Members</span></span>

<span data-ttu-id="426f1-113">Die **CIM- \_ deviceserviceimplementation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="426f1-113">The **CIM\_DeviceServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="426f1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="426f1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="426f1-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="426f1-115">Properties</span></span>

<span data-ttu-id="426f1-116">Die **CIM- \_ deviceserviceimplementation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="426f1-116">The **CIM\_DeviceServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="426f1-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="426f1-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426f1-118">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="426f1-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="426f1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="426f1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="426f1-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="426f1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="426f1-121">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="426f1-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="426f1-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="426f1-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426f1-123">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="426f1-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="426f1-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="426f1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="426f1-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="426f1-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="426f1-126">Ein [**CIM- \_ Dienst**](cim-service.md) , der den mit dem logischen Gerät implementierten Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="426f1-126">A [**CIM\_Service**](cim-service.md) that describes the service implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="426f1-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="426f1-127">Remarks</span></span>

<span data-ttu-id="426f1-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="426f1-128">WMI does not implement this class.</span></span>

<span data-ttu-id="426f1-129">Die **CIM- \_ deviceserviceimplementation** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="426f1-129">The **CIM\_DeviceServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="426f1-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="426f1-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="426f1-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="426f1-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="426f1-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="426f1-132">Requirements</span></span>



| <span data-ttu-id="426f1-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="426f1-133">Requirement</span></span> | <span data-ttu-id="426f1-134">Wert</span><span class="sxs-lookup"><span data-stu-id="426f1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="426f1-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="426f1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="426f1-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="426f1-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="426f1-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="426f1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="426f1-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="426f1-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="426f1-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="426f1-139">Namespace</span></span><br/>                | <span data-ttu-id="426f1-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="426f1-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="426f1-141">MOF</span><span class="sxs-lookup"><span data-stu-id="426f1-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="426f1-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="426f1-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="426f1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="426f1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="426f1-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="426f1-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="426f1-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="426f1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="426f1-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="426f1-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

