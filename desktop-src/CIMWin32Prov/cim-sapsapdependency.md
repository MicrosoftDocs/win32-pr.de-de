---
description: Die CIM \_ sapsapabhängigkeits-Klasse ist eine Zuordnung zwischen zwei Dienst Zugriffs Punkten (SAPS), mit der angegeben wird, dass die zweite SAP-Komponente erforderlich ist, damit der erste SAP eine Verbindung mit dem Dienst herstellt.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: CIM_SAPSAPDependency-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958270"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="8f6cf-103">CIM_SAPSAPDependency-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="8f6cf-103">CIM_SAPSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8f6cf-104">Die **CIM \_ sapsapabhängigkeits** -Klasse ist eine Zuordnung zwischen zwei Dienst Zugriffs Punkten (SAPS), mit der angegeben wird, dass die zweite SAP-Komponente erforderlich ist, damit der erste SAP eine Verbindung mit dem Dienst herstellt.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-104">The **CIM\_SAPSAPDependency** class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span> <span data-ttu-id="8f6cf-105">Um z. b. auf einem Netzwerkdrucker zu drucken, müssen lokale Drucker Zugriffspunkte zugrunde liegende netzwerkbezogene SAPS oder Protokoll Endpunkte verwenden, um die Druck Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-105">For example, to print on a network printer, local printer access points must use underlying network-related SAPs, or protocol endpoints, to send the print request.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f6cf-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f6cf-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f6cf-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f6cf-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8f6cf-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f6cf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f6cf-110">Syntax</span></span>

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8f6cf-111">Member</span><span class="sxs-lookup"><span data-stu-id="8f6cf-111">Members</span></span>

<span data-ttu-id="8f6cf-112">Die **CIM \_ sapsapdepenpklasse** verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8f6cf-112">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="8f6cf-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f6cf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f6cf-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f6cf-114">Properties</span></span>

<span data-ttu-id="8f6cf-115">Die **CIM \_ sapsapdepenpklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-115">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f6cf-116">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="8f6cf-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f6cf-117">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="8f6cf-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="8f6cf-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f6cf-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f6cf-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="8f6cf-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8f6cf-120">Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der den erforderlichen Dienst Zugriffspunkt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="8f6cf-121">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="8f6cf-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f6cf-122">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="8f6cf-122">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="8f6cf-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f6cf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f6cf-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="8f6cf-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8f6cf-125">Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der den Dienst Zugriffspunkt beschreibt, der von einem zugrunde liegenden SAP abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-125">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f6cf-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f6cf-126">Remarks</span></span>

<span data-ttu-id="8f6cf-127">Die **CIM- \_ sapsapabhängigkeits** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-127">The **CIM\_SAPSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8f6cf-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-128">WMI does not implement this class.</span></span>

<span data-ttu-id="8f6cf-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f6cf-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8f6cf-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6cf-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f6cf-131">Requirements</span></span>



| <span data-ttu-id="8f6cf-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f6cf-132">Requirement</span></span> | <span data-ttu-id="8f6cf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8f6cf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6cf-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f6cf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8f6cf-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f6cf-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f6cf-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f6cf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8f6cf-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f6cf-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f6cf-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f6cf-138">Namespace</span></span><br/>                | <span data-ttu-id="8f6cf-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f6cf-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f6cf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8f6cf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f6cf-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f6cf-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f6cf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8f6cf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f6cf-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f6cf-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f6cf-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f6cf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6cf-145">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="8f6cf-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

