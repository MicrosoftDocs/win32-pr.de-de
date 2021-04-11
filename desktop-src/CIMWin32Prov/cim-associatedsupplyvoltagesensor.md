---
description: Verknüpft eine Stromversorgung mit einem Spannungssensor, der die Eingangsspannung überwacht.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: CIM_AssociatedSupplyVoltageSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127205"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a><span data-ttu-id="0d6f3-103">CIM \_ associatedsupplyvoltagesensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="0d6f3-103">CIM\_AssociatedSupplyVoltageSensor class</span></span>

<span data-ttu-id="0d6f3-104">Die **CIM \_ associatedsupplyvoltagesensor** -Klasse ordnet eine Stromversorgung einem Spannungssensor zu, der die Eingangsspannung überwacht.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-104">The **CIM\_AssociatedSupplyVoltageSensor** class associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d6f3-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d6f3-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0d6f3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d6f3-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0d6f3-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d6f3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d6f3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="0d6f3-110">Member</span><span class="sxs-lookup"><span data-stu-id="0d6f3-110">Members</span></span>

<span data-ttu-id="0d6f3-111">Die **CIM \_ associatedsupplyvoltagesensor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0d6f3-111">The **CIM\_AssociatedSupplyVoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="0d6f3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d6f3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d6f3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d6f3-113">Properties</span></span>

<span data-ttu-id="0d6f3-114">Die **CIM \_ associatedsupplyvoltagesensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-114">The **CIM\_AssociatedSupplyVoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d6f3-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="0d6f3-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d6f3-116">Datentyp: **CIM \_ VoltageSensor**</span><span class="sxs-lookup"><span data-stu-id="0d6f3-116">Data type: **CIM\_VoltageSensor**</span></span>
</dt> <dt>

<span data-ttu-id="0d6f3-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d6f3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d6f3-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="0d6f3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0d6f3-119">Ein [**CIM \_**](cim-voltagesensor.md) -Strom Sensor, der den Spannungssensor beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-119">A [**CIM\_VoltageSensor**](cim-voltagesensor.md) that describes the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="0d6f3-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="0d6f3-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d6f3-121">Datentyp: **CIM- \_ Netzteil**</span><span class="sxs-lookup"><span data-stu-id="0d6f3-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="0d6f3-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d6f3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d6f3-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="0d6f3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0d6f3-124">Ein [**CIM- \_ Netzteil**](cim-powersupply.md) , der die dem Spannungssensor zugeordnete Stromversorgung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="0d6f3-125">**Monitoringrange**</span><span class="sxs-lookup"><span data-stu-id="0d6f3-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d6f3-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d6f3-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d6f3-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0d6f3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d6f3-128">Gibt den Eingabe Spannungsbereich des Netzteils an, der vom zugeordneten Sensor gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-128">Indicates the power supply's input voltage range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d6f3-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0d6f3-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d6f3-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0d6f3-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="0d6f3-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Bereich 1** (2)</span><span class="sxs-lookup"><span data-stu-id="0d6f3-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="0d6f3-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Bereich 2** (3)</span><span class="sxs-lookup"><span data-stu-id="0d6f3-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="0d6f3-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Bereich 1 und 2** (4)</span><span class="sxs-lookup"><span data-stu-id="0d6f3-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0d6f3-134">Bereich 1 und 2</span><span class="sxs-lookup"><span data-stu-id="0d6f3-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d6f3-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d6f3-135">Remarks</span></span>

<span data-ttu-id="0d6f3-136">Die **CIM \_ associatedsupplyvoltagesensor** -Klasse wird von [**CIM \_ associatedsensor**](cim-associatedsensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-136">The **CIM\_AssociatedSupplyVoltageSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="0d6f3-137">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-137">WMI does not implement this class.</span></span>

<span data-ttu-id="0d6f3-138">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d6f3-139">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0d6f3-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d6f3-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d6f3-140">Requirements</span></span>



| <span data-ttu-id="0d6f3-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d6f3-141">Requirement</span></span> | <span data-ttu-id="0d6f3-142">Wert</span><span class="sxs-lookup"><span data-stu-id="0d6f3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6f3-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d6f3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6f3-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d6f3-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d6f3-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d6f3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6f3-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d6f3-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d6f3-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d6f3-147">Namespace</span></span><br/>                | <span data-ttu-id="0d6f3-148">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d6f3-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d6f3-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0d6f3-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d6f3-150"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0d6f3-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d6f3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0d6f3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d6f3-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d6f3-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d6f3-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d6f3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d6f3-154">**CIM \_ associatedsensor**</span><span class="sxs-lookup"><span data-stu-id="0d6f3-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

