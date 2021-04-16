---
description: Die CIM- \_ devicesoftware-Beziehung identifiziert Software, die einem Gerät zugeordnet ist, z. b. Treiber, Konfigurations-oder Anwendungssoftware oder Firmware.
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: CIM_DeviceSoftware-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523888"
---
# <a name="cim_devicesoftware-class"></a><span data-ttu-id="de351-103">CIM- \_ devicesoftware-Klasse</span><span class="sxs-lookup"><span data-stu-id="de351-103">CIM\_DeviceSoftware class</span></span>

<span data-ttu-id="de351-104">Die **CIM- \_ devicesoftware** -Beziehung identifiziert Software, die einem Gerät zugeordnet ist, z. b. Treiber, Konfigurations-oder Anwendungssoftware oder Firmware.</span><span class="sxs-lookup"><span data-stu-id="de351-104">The **CIM\_DeviceSoftware** relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de351-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="de351-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="de351-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="de351-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="de351-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="de351-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="de351-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="de351-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de351-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de351-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="de351-110">Member</span><span class="sxs-lookup"><span data-stu-id="de351-110">Members</span></span>

<span data-ttu-id="de351-111">Die **CIM- \_ devicesoftware** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="de351-111">The **CIM\_DeviceSoftware** class has these types of members:</span></span>

-   [<span data-ttu-id="de351-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de351-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de351-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de351-113">Properties</span></span>

<span data-ttu-id="de351-114">Die **CIM- \_ devicesoftware** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de351-114">The **CIM\_DeviceSoftware** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de351-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="de351-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de351-116">Datentyp: **CIM \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="de351-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="de351-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de351-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de351-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="de351-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="de351-119">Ein [**CIM- \_ Softwareelement**](cim-softwareelement.md) , das das Softwareelement beschreibt.</span><span class="sxs-lookup"><span data-stu-id="de351-119">A [**CIM\_SoftwareElement**](cim-softwareelement.md) that describes the software element.</span></span>

</dd> <dt>

<span data-ttu-id="de351-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="de351-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de351-121">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="de351-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="de351-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de351-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de351-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="de351-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="de351-124">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt, das die Software benötigt oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="de351-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that requires or uses the software.</span></span>

</dd> <dt>

<span data-ttu-id="de351-125">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="de351-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de351-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de351-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de351-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de351-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de351-128">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Geräte-Agent-**\_ Software**.**Zweck Beschreibung**")</span><span class="sxs-lookup"><span data-stu-id="de351-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="de351-129">Rolle, die die Software in Bezug auf das zugehörige Gerät übernimmt.</span><span class="sxs-lookup"><span data-stu-id="de351-129">Role that the software takes regarding its associated device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="de351-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="de351-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="de351-131">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="de351-131">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="de351-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="de351-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="de351-133">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="de351-133">Other.</span></span>

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="de351-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Treiber** (2)</span><span class="sxs-lookup"><span data-stu-id="de351-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span></span>


</dt> <dd>

<span data-ttu-id="de351-135">Trei.</span><span class="sxs-lookup"><span data-stu-id="de351-135">Driver.</span></span>

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="de351-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Konfigurations Software** (3)</span><span class="sxs-lookup"><span data-stu-id="de351-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3)</span></span>


</dt> <dd>

<span data-ttu-id="de351-137">Konfigurationssoftware.</span><span class="sxs-lookup"><span data-stu-id="de351-137">Configuration software.</span></span>

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="de351-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Anwendungs Software** (4)</span><span class="sxs-lookup"><span data-stu-id="de351-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Application Software** (4)</span></span>


</dt> <dd>

<span data-ttu-id="de351-139">Anwendungssoftware.</span><span class="sxs-lookup"><span data-stu-id="de351-139">Application software.</span></span>

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="de351-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span><span class="sxs-lookup"><span data-stu-id="de351-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span></span>


</dt> <dd>

<span data-ttu-id="de351-141">Instrumentierung:</span><span class="sxs-lookup"><span data-stu-id="de351-141">Instrumentation.</span></span>

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="de351-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="de351-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span></span>


</dt> <dd>

<span data-ttu-id="de351-143">Abhängigen.</span><span class="sxs-lookup"><span data-stu-id="de351-143">Firmware.</span></span>

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span data-ttu-id="de351-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span><span class="sxs-lookup"><span data-stu-id="de351-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="de351-145">Zugreifen.</span><span class="sxs-lookup"><span data-stu-id="de351-145">BIOS.</span></span>

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span data-ttu-id="de351-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Start-ROM** (8)</span><span class="sxs-lookup"><span data-stu-id="de351-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span></span>


</dt> <dd>

<span data-ttu-id="de351-147">Start-ROM.</span><span class="sxs-lookup"><span data-stu-id="de351-147">Boot ROM.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="de351-148">**Zweck Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de351-148">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de351-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de351-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de351-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de351-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de351-151">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Geräte-Agent-**\_ Software**.**Zweck**")</span><span class="sxs-lookup"><span data-stu-id="de351-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**Purpose**")</span></span>
</dt> </dl>

<span data-ttu-id="de351-152">Eine frei Form Zeichenfolge, die weitere Informationen zur Eigenschaft " **Zweck** " bereitstellt, z. b. "Anwendungs Software".</span><span class="sxs-lookup"><span data-stu-id="de351-152">Free-form string that provides more information for the **Purpose** property, for example, "Application Software".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de351-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de351-153">Remarks</span></span>

<span data-ttu-id="de351-154">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="de351-154">WMI does not implement this class.</span></span>

<span data-ttu-id="de351-155">Die **CIM- \_ devicesoftware** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="de351-155">The **CIM\_DeviceSoftware** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="de351-156">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="de351-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="de351-157">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="de351-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="de351-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de351-158">Requirements</span></span>



| <span data-ttu-id="de351-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de351-159">Requirement</span></span> | <span data-ttu-id="de351-160">Wert</span><span class="sxs-lookup"><span data-stu-id="de351-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de351-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de351-161">Minimum supported client</span></span><br/> | <span data-ttu-id="de351-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de351-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de351-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de351-163">Minimum supported server</span></span><br/> | <span data-ttu-id="de351-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de351-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de351-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="de351-165">Namespace</span></span><br/>                | <span data-ttu-id="de351-166">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="de351-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="de351-167">MOF</span><span class="sxs-lookup"><span data-stu-id="de351-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de351-168"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="de351-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de351-169">DLL</span><span class="sxs-lookup"><span data-stu-id="de351-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de351-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de351-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de351-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de351-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de351-172">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="de351-172">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

