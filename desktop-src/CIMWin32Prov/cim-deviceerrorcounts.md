---
description: Die CIM \_ deviceerrorcounts-Klasse ist eine statistische Klasse, die Fehler bezogene Leistungsindikatoren für ein logisches Gerät enthält. Die Fehlertypen werden von CCITT (REC X. 733) und ISO (IEC 10164-4) definiert.
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: CIM_DeviceErrorCounts-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958479"
---
# <a name="cim_deviceerrorcounts-class"></a><span data-ttu-id="2f8a7-104">CIM \_ deviceerrorcounts-Klasse</span><span class="sxs-lookup"><span data-stu-id="2f8a7-104">CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="2f8a7-105">Die **CIM \_ deviceerrorcounts** -Klasse ist eine statistische Klasse, die Fehler bezogene Leistungsindikatoren für ein logisches Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-105">The **CIM\_DeviceErrorCounts** class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="2f8a7-106">Die Fehlertypen werden von CCITT (REC X. 733) und ISO (IEC 10164-4) definiert.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-106">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f8a7-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2f8a7-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2f8a7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2f8a7-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2f8a7-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8a7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f8a7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a><span data-ttu-id="2f8a7-112">Member</span><span class="sxs-lookup"><span data-stu-id="2f8a7-112">Members</span></span>

<span data-ttu-id="2f8a7-113">Die **CIM \_ deviceerrorcounts** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2f8a7-113">The **CIM\_DeviceErrorCounts** class has these types of members:</span></span>

-   [<span data-ttu-id="2f8a7-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="2f8a7-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f8a7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f8a7-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f8a7-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="2f8a7-116">Methods</span></span>

<span data-ttu-id="2f8a7-117">Die **CIM \_ deviceerrorcounts** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-117">The **CIM\_DeviceErrorCounts** class has these methods.</span></span>



| <span data-ttu-id="2f8a7-118">Methode</span><span class="sxs-lookup"><span data-stu-id="2f8a7-118">Method</span></span>                                                                     | <span data-ttu-id="2f8a7-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f8a7-119">Description</span></span>                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="2f8a7-120">**ResetCounter**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-120">**ResetCounter**</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md) | <span data-ttu-id="2f8a7-121">Setzt die Fehler-und Warnungs Zähler zurück.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-121">Resets the error and warning counters.</span></span> <span data-ttu-id="2f8a7-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2f8a7-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f8a7-123">Properties</span></span>

<span data-ttu-id="2f8a7-124">Die **CIM \_ deviceerrorcounts** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-124">The **CIM\_DeviceErrorCounts** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f8a7-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-128">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-129">Kurze Textbeschreibung für die Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-129">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="2f8a7-130">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-130">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-131">**Criticalerrorcount**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-131">**CriticalErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-132">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-134">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="2f8a7-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-135">Anzahl der kritischen Fehler.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-135">Count of the critical errors.</span></span>

<span data-ttu-id="2f8a7-136">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2f8a7-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-140">Die Textbeschreibung der Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-140">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="2f8a7-141">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-141">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-142">**Geräteklassen Name**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-142">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-145">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ LogicalDevice**](cim-logicaldevice.md).**"Kreationclassname**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-146">Die Eigenschaft " **kreationclassname** " des Bereichs Geräts.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-146">The scoping device's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-147">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-147">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-150">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ LogicalDevice**](cim-logicaldevice.md).**De viceid**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-151">Der Bezeichner des Bereichs Geräts.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-151">The scoping device's identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-152">**Indeterminateerrorcount**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-152">**IndeterminateErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-153">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-155">Anzahl der unbestimmten Fehler.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-155">Count of the indeterminate errors.</span></span>

<span data-ttu-id="2f8a7-156">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2f8a7-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-157">**Majorerrorcount**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-157">**MajorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-158">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-160">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="2f8a7-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-161">Anzahl der Hauptfehler.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-161">Count of the major errors.</span></span>

<span data-ttu-id="2f8a7-162">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2f8a7-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-163">**Minorerrorcount**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-163">**MinorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-164">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-166">Anzahl der geringfügigen Fehler.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-166">Count of the minor errors.</span></span>

<span data-ttu-id="2f8a7-167">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2f8a7-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-168">**Name**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-171">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-171">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-172">Die geerbte Name-Eigenschaft dient als Teil des Schlüssels für die **CIM \_ deviceerrorcounts** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-172">The inherited Name property serves as part of the key for the **CIM\_DeviceErrorCounts** instance.</span></span> <span data-ttu-id="2f8a7-173">Das Objekt ist auf das logische Gerät beschränkt, für das die Statistiken gelten.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-173">The object is scoped by the logical device to which the statistics apply.</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-174">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-177">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ LogicalDevice**](cim-logicaldevice.md).**Systemkreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-178">Der **Name** des Bereichs Systems "".</span><span class="sxs-lookup"><span data-stu-id="2f8a7-178">Scoping system's **CreationClassName**.</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-179">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-182">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ LogicalDevice**](cim-logicaldevice.md).**Systemname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-183">Die **Name** -Eigenschaft des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-183">Scoping system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="2f8a7-184">**Warningcount**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-184">**WarningCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8a7-185">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-185">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f8a7-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8a7-187">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="2f8a7-187">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="2f8a7-188">Anzahl der Warnungen.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-188">Count of the warnings.</span></span>

<span data-ttu-id="2f8a7-189">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2f8a7-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f8a7-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f8a7-190">Remarks</span></span>

<span data-ttu-id="2f8a7-191">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-191">WMI does not implement this class.</span></span>

<span data-ttu-id="2f8a7-192">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2f8a7-193">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2f8a7-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8a7-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f8a7-194">Requirements</span></span>



| <span data-ttu-id="2f8a7-195">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f8a7-195">Requirement</span></span> | <span data-ttu-id="2f8a7-196">Wert</span><span class="sxs-lookup"><span data-stu-id="2f8a7-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8a7-197">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-197">Minimum supported client</span></span><br/> | <span data-ttu-id="2f8a7-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f8a7-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f8a7-199">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f8a7-199">Minimum supported server</span></span><br/> | <span data-ttu-id="2f8a7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f8a7-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f8a7-201">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f8a7-201">Namespace</span></span><br/>                | <span data-ttu-id="2f8a7-202">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2f8a7-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f8a7-203">MOF</span><span class="sxs-lookup"><span data-stu-id="2f8a7-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f8a7-204"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f8a7-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f8a7-205">DLL</span><span class="sxs-lookup"><span data-stu-id="2f8a7-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f8a7-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f8a7-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f8a7-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f8a7-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8a7-208">**CIM- \_ statisticalinformation**</span><span class="sxs-lookup"><span data-stu-id="2f8a7-208">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> </dl>

 

