---
description: Die CIM \_ memorycapacity-Klasse stellt den Arbeitsspeicher dar, der auf einem physischen Element und dessen minimalen und maximalen Konfigurationen installiert werden kann.
ms.assetid: a962ee38-9281-4a7a-b9d7-b321edb5670d
ms.tgt_platform: multiple
title: CIM_MemoryCapacity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCapacity
- CIM_MemoryCapacity.Caption
- CIM_MemoryCapacity.Description
- CIM_MemoryCapacity.Name
- CIM_MemoryCapacity.MaximumMemoryCapacity
- CIM_MemoryCapacity.MemoryType
- CIM_MemoryCapacity.MinimumMemoryCapacity
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa63d06187c76c5add433502d012cdb63905795a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214065"
---
# <a name="cim_memorycapacity-class"></a><span data-ttu-id="b3d1f-103">CIM \_ memorycapacity-Klasse</span><span class="sxs-lookup"><span data-stu-id="b3d1f-103">CIM\_MemoryCapacity class</span></span>

<span data-ttu-id="b3d1f-104">Die **CIM \_ memorycapacity** -Klasse stellt den Arbeitsspeicher dar, der auf einem physischen Element und dessen minimalen und maximalen Konfigurationen installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-104">The **CIM\_MemoryCapacity** class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="b3d1f-105">Informationen zu derzeit installiertem Arbeitsspeicher und den minimalen und maximalen Anforderungen eines Elements befinden sich in Instanzen der [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-105">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3d1f-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b3d1f-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b3d1f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b3d1f-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b3d1f-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d1f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d1f-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryCapacity : CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
  uint64 MaximumMemoryCapacity;
  uint16 MemoryType;
  uint64 MinimumMemoryCapacity;
};
```

## <a name="members"></a><span data-ttu-id="b3d1f-111">Member</span><span class="sxs-lookup"><span data-stu-id="b3d1f-111">Members</span></span>

<span data-ttu-id="b3d1f-112">Die **CIM \_ memorycapacity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b3d1f-112">The **CIM\_MemoryCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="b3d1f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3d1f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3d1f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3d1f-114">Properties</span></span>

<span data-ttu-id="b3d1f-115">Die **CIM \_ memorycapacity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-115">The **CIM\_MemoryCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3d1f-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1f-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3d1f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b3d1f-120">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-120">Short textual description of the object.</span></span>

<span data-ttu-id="b3d1f-121">Diese Eigenschaft wird von [**CIM \_ physicalcapacity**](cim-physicalcapacity.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-121">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3d1f-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1f-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3d1f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3d1f-125">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-125">Textual description of the object.</span></span>

<span data-ttu-id="b3d1f-126">Diese Eigenschaft wird von [**CIM \_ physicalcapacity**](cim-physicalcapacity.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-126">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3d1f-127">**Maximummemorycapacity**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-127">**MaximumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1f-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3d1f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-130">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="b3d1f-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b3d1f-131">Maximale Größe des Arbeitsspeichers in Kilobyte, der vom zugeordneten physischen Element unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-131">Maximum amount of memory, in kilobytes, that can be supported by the associated physical element.</span></span>

<span data-ttu-id="b3d1f-132">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b3d1f-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b3d1f-133">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-133">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1f-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3d1f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-136">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span><span class="sxs-lookup"><span data-stu-id="b3d1f-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="b3d1f-137">Der Typ des Arbeitsspeichers, der Teil des Objektschlüssels ist.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-137">Type of memory, which is part of the object key.</span></span> <span data-ttu-id="b3d1f-138">Werte entsprechen der Liste der möglichen Speichertypen in der [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-138">Values correspond to the list of possible memory types in the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b3d1f-139">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b3d1f-140">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="b3d1f-141">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-141">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="b3d1f-142">**Synchroner DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-142">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="b3d1f-143">**Cache-DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-143">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="b3d1f-144">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-144">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="b3d1f-145">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-145">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="b3d1f-146">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-146">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="b3d1f-147">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-147">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="b3d1f-148">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-148">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="b3d1f-149">**Rom** (10)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-149">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="b3d1f-150">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-150">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="b3d1f-151">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-151">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="b3d1f-152">**Feprom** (13)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-152">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="b3d1f-153">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-153">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="b3d1f-154">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-154">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="b3d1f-155">**3dram** (16)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-155">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="b3d1f-156">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-156">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="b3d1f-157">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-157">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="b3d1f-158">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-158">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="b3d1f-159">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-159">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR-2"></span><span id="ddr-2"></span>

<span data-ttu-id="b3d1f-160">**DDR-2** (21)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-160">**DDR-2** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b3d1f-161">**Minimummemorycapacity**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-161">**MinimumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1f-162">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3d1f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-164">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="b3d1f-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b3d1f-165">Mindestmenge an Arbeitsspeicher in Kilobyte, die benötigt wird, damit das zugehörige physische Element ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-165">Minimum amount of memory, in kilobytes, that is needed for the associated physical element to operate correctly.</span></span>

<span data-ttu-id="b3d1f-166">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b3d1f-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b3d1f-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1f-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3d1f-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1f-170">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b3d1f-171">Der Name des Objekts. dient als Teil des Objektschlüssels.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-171">The name of the object; serves as a part of the object key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3d1f-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3d1f-172">Remarks</span></span>

<span data-ttu-id="b3d1f-173">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-173">WMI does not implement this class.</span></span>

<span data-ttu-id="b3d1f-174">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-174">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b3d1f-175">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-175">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d1f-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3d1f-176">Requirements</span></span>



| <span data-ttu-id="b3d1f-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3d1f-177">Requirement</span></span> | <span data-ttu-id="b3d1f-178">Wert</span><span class="sxs-lookup"><span data-stu-id="b3d1f-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d1f-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-179">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d1f-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3d1f-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3d1f-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-181">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d1f-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3d1f-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3d1f-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3d1f-183">Namespace</span></span><br/>                | <span data-ttu-id="b3d1f-184">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b3d1f-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3d1f-185">MOF</span><span class="sxs-lookup"><span data-stu-id="b3d1f-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3d1f-186"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b3d1f-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3d1f-187">DLL</span><span class="sxs-lookup"><span data-stu-id="b3d1f-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3d1f-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3d1f-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3d1f-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3d1f-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d1f-190">**CIM- \_ physicalcapacity**</span><span class="sxs-lookup"><span data-stu-id="b3d1f-190">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> </dl>

 

