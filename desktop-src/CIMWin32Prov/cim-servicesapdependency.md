---
description: Die CIM \_ servicesapdepen-Klasse stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der angibt, dass der referenzierte SAP vom Dienst verwendet wird, um seine Funktionalität bereitzustellen.
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: CIM_ServiceSAPDependency-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126662"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="48e8d-103">CIM_ServiceSAPDependency-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="48e8d-103">CIM_ServiceSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="48e8d-104">Die **CIM \_ servicesapdepen-Klasse** stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der angibt, dass der referenzierte SAP vom Dienst verwendet wird, um seine Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="48e8d-104">The **CIM\_ServiceSAPDependency** class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span> <span data-ttu-id="48e8d-105">Start Dienste können z. b. BIOS-Datenträger Dienste (Interrupts) aufrufen, um zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="48e8d-105">For example, boot services can invoke BIOS disk services (interrupts) to function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48e8d-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48e8d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48e8d-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="48e8d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48e8d-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="48e8d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="48e8d-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="48e8d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e8d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="48e8d-110">Syntax</span></span>

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="48e8d-111">Member</span><span class="sxs-lookup"><span data-stu-id="48e8d-111">Members</span></span>

<span data-ttu-id="48e8d-112">Die **CIM \_ servicesapdepenpklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="48e8d-112">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="48e8d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48e8d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48e8d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48e8d-114">Properties</span></span>

<span data-ttu-id="48e8d-115">Die **CIM \_ servicesapdepenpklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48e8d-115">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48e8d-116">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="48e8d-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e8d-117">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="48e8d-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="48e8d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48e8d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e8d-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="48e8d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="48e8d-120">Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der den erforderlichen Dienst Zugriffspunkt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="48e8d-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="48e8d-121">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="48e8d-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e8d-122">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="48e8d-122">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="48e8d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48e8d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e8d-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="48e8d-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="48e8d-125">Ein [**CIM- \_ Dienst**](cim-service.md) , der den Dienst beschreibt, der von einem zugrunde liegenden SAP abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="48e8d-125">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48e8d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48e8d-126">Remarks</span></span>

<span data-ttu-id="48e8d-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="48e8d-127">WMI does not implement this class.</span></span>

<span data-ttu-id="48e8d-128">Die **CIM- \_ servicesapdepenpklasse** wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="48e8d-128">The **CIM\_ServiceSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="48e8d-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="48e8d-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48e8d-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="48e8d-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48e8d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48e8d-131">Requirements</span></span>



| <span data-ttu-id="48e8d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48e8d-132">Requirement</span></span> | <span data-ttu-id="48e8d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="48e8d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e8d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48e8d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="48e8d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48e8d-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48e8d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48e8d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="48e8d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48e8d-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48e8d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="48e8d-138">Namespace</span></span><br/>                | <span data-ttu-id="48e8d-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="48e8d-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48e8d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="48e8d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48e8d-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48e8d-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48e8d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="48e8d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e8d-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e8d-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e8d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48e8d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e8d-145">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="48e8d-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

