---
description: Die CIM \_ serviceservicedepen-Klasse stellt eine Zuordnung zwischen zwei Diensten dar.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: CIM_ServiceServiceDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338903"
---
# <a name="cim_serviceservicedependency-class"></a><span data-ttu-id="71bec-103">CIM \_ serviceservicequeue-Klasse</span><span class="sxs-lookup"><span data-stu-id="71bec-103">CIM\_ServiceServiceDependency class</span></span>

<span data-ttu-id="71bec-104">Die **CIM \_ serviceservicedepen-Klasse** stellt eine Zuordnung zwischen zwei Diensten dar.</span><span class="sxs-lookup"><span data-stu-id="71bec-104">The **CIM\_ServiceServiceDependency** class represents an association between two services.</span></span> <span data-ttu-id="71bec-105">Der zugeordnete Dienst muss vorhanden sein, muss abgeschlossen sein oder nicht vorhanden sein, damit der andere Dienst ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="71bec-105">The associated service must be present, must have completed, or must be absent for the other service to function.</span></span> <span data-ttu-id="71bec-106">Beispielsweise können Start Dienste von zugrunde liegenden BIOS-, Datenträger-und Initialisierungs Diensten abhängig sein.</span><span class="sxs-lookup"><span data-stu-id="71bec-106">For example, boot services can be dependent on underlying BIOS, disk, and initialization services.</span></span> <span data-ttu-id="71bec-107">Für Initialisierungs Dienste ist der Start Dienst davon abhängig, dass die Initialisierungs Dienste abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="71bec-107">For initialization services, the boot service is dependent on the initialization services completing.</span></span> <span data-ttu-id="71bec-108">Für Datenträger Dienste können Start Dienste tatsächlich die SAPS dieses Diensts verwenden.</span><span class="sxs-lookup"><span data-stu-id="71bec-108">For disk services, boot services can actually use the SAPs of this service.</span></span> <span data-ttu-id="71bec-109">Diese Verwendungs Abhängigkeit wird anhand der [**CIM \_ servicesapdepen-Zuordnung**](cim-servicesapdependency.md) modelliert.</span><span class="sxs-lookup"><span data-stu-id="71bec-109">This usage dependency is modeled on the [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71bec-110">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="71bec-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="71bec-111">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="71bec-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="71bec-112">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="71bec-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="71bec-113">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="71bec-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71bec-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="71bec-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="71bec-115">Member</span><span class="sxs-lookup"><span data-stu-id="71bec-115">Members</span></span>

<span data-ttu-id="71bec-116">Die **CIM \_ serviceservicequeue** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="71bec-116">The **CIM\_ServiceServiceDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="71bec-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71bec-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71bec-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71bec-118">Properties</span></span>

<span data-ttu-id="71bec-119">Die **CIM \_ serviceservicequeue** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="71bec-119">The **CIM\_ServiceServiceDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71bec-120">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="71bec-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71bec-121">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="71bec-121">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="71bec-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71bec-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71bec-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="71bec-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="71bec-124">Ein [**CIM- \_ Dienst**](cim-service.md) , der den erforderlichen Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="71bec-124">A [**CIM\_Service**](cim-service.md) that describes the required service.</span></span>

</dd> <dt>

<span data-ttu-id="71bec-125">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="71bec-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71bec-126">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="71bec-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="71bec-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71bec-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71bec-128">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="71bec-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="71bec-129">Ein [**CIM- \_ Dienst**](cim-service.md) , der den Dienst beschreibt, der von einem zugrunde liegenden Dienst abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="71bec-129">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying service.</span></span>

</dd> <dt>

<span data-ttu-id="71bec-130">**Typeofabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="71bec-130">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71bec-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71bec-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71bec-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71bec-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71bec-133">Die Art der Dienst-zu-Dienst-Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="71bec-133">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="71bec-134">Diese Eigenschaft gibt an, dass der zugehörige Dienst abgeschlossen werden muss, muss gestartet werden oder nicht gestartet werden, damit der Dienst funktioniert.</span><span class="sxs-lookup"><span data-stu-id="71bec-134">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71bec-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="71bec-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71bec-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="71bec-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="71bec-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>Der **Dienst muss abgeschlossen sein** (2).</span><span class="sxs-lookup"><span data-stu-id="71bec-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="71bec-138">Der Dienst muss abgeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="71bec-138">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="71bec-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>Der **Dienst muss gestartet werden** (3).</span><span class="sxs-lookup"><span data-stu-id="71bec-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="71bec-140">Der Dienst muss gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="71bec-140">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="71bec-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>Der **Dienst darf nicht gestartet werden** (4).</span><span class="sxs-lookup"><span data-stu-id="71bec-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="71bec-142">Der Dienst darf nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="71bec-142">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71bec-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71bec-143">Remarks</span></span>

<span data-ttu-id="71bec-144">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="71bec-144">WMI does not implement this class.</span></span> <span data-ttu-id="71bec-145">Informationen zu WMI-Klassen, die von **CIM \_ serviceserviceabhängigkeiten** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="71bec-145">For WMI classes derived from **CIM\_ServiceServiceDependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="71bec-146">Die **CIM- \_ serviceservicequeue** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="71bec-146">The **CIM\_ServiceServiceDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="71bec-147">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="71bec-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="71bec-148">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="71bec-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="71bec-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71bec-149">Requirements</span></span>



| <span data-ttu-id="71bec-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71bec-150">Requirement</span></span> | <span data-ttu-id="71bec-151">Wert</span><span class="sxs-lookup"><span data-stu-id="71bec-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71bec-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71bec-152">Minimum supported client</span></span><br/> | <span data-ttu-id="71bec-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71bec-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71bec-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71bec-154">Minimum supported server</span></span><br/> | <span data-ttu-id="71bec-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71bec-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71bec-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="71bec-156">Namespace</span></span><br/>                | <span data-ttu-id="71bec-157">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="71bec-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71bec-158">MOF</span><span class="sxs-lookup"><span data-stu-id="71bec-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71bec-159"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="71bec-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71bec-160">DLL</span><span class="sxs-lookup"><span data-stu-id="71bec-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71bec-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71bec-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71bec-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71bec-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71bec-163">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="71bec-163">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

