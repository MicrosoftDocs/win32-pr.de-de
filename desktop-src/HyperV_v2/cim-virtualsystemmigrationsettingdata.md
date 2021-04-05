---
description: Definiert die Einstellungen für die Migration virtueller Systeme, die von einer Instanz der CIM \_ virtualsystemmigrationservice-Klasse verwaltet werden.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756271"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="0a681-103">CIM \_ virtualsystemmigrationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a681-103">CIM\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="0a681-104">Definiert die Einstellungen für die Migration virtueller Systeme, die von einer Instanz der [**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md) -Klasse verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0a681-104">Defines the settings for virtual system migration that is managed by an instance of the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a681-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a681-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a><span data-ttu-id="0a681-106">Member</span><span class="sxs-lookup"><span data-stu-id="0a681-106">Members</span></span>

<span data-ttu-id="0a681-107">Die **CIM- \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0a681-107">The **CIM\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0a681-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a681-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a681-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a681-109">Properties</span></span>

<span data-ttu-id="0a681-110">Die **CIM \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a681-110">The **CIM\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a681-111">**Bandwidth**</span><span class="sxs-lookup"><span data-stu-id="0a681-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a681-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a681-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a681-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a681-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a681-114">Qualifizierer: [**Messgerät**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**.**Bandwidthunit**")</span><span class="sxs-lookup"><span data-stu-id="0a681-114">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span></span>
</dt> </dl>

<span data-ttu-id="0a681-115">Die Bandbreite, die einem virtuellen System Migrations Vorgang zugewiesen oder angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="0a681-115">The bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="0a681-116">"0" ist die Standard Bandbreite für Migrations Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="0a681-116">"0" is default bandwidth for migration requests.</span></span>

<span data-ttu-id="0a681-117">Die Eigenschaften **Bandbreite** und **Priorität** können zusammen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a681-117">The **Bandwidth** and **Priority** properties may be used in conjunction.</span></span> <span data-ttu-id="0a681-118">Migrationsprozesse mit den höchsten Werten für die gleiche **Priorität** haben die verfügbare Bandbreite basierend auf der angeforderten Bandbreite gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="0a681-118">Migration processes that have the highest equal **Priority** values share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="0a681-119">Wenn nicht die gesamte Bandbreite von diesem Satz von Prozessen genutzt wird, nutzen Migrationsprozesse mit den nächst niedrigeren Werten mit gleicher **Priorität** die verbleibende Bandbreite gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="0a681-119">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal **Priority** values share the remaining bandwidth.</span></span> <span data-ttu-id="0a681-120">Wenn noch mehr Bandbreite verbleiben, werden Migrationsprozesse mit den nächst niedrigeren Werten der gleichen **Priorität** berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0a681-120">If more bandwidth remains, migration processes with the next lower equal **Priority** values are considered.</span></span>

<span data-ttu-id="0a681-121">Die in der **Bandbreiten** Eigenschaft verwendete Einheit wird durch den Wert der **bandwidthunit** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="0a681-121">The unit used in **Bandwidth** property is specified by the value of the **BandwidthUnit** property.</span></span>

<span data-ttu-id="0a681-122">Wenn der Wert der **bandwidthunit** -Eigenschaft "Prozent" ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="0a681-122">If the value of the **BandwidthUnit** property is "percent", the following rules apply:</span></span>

-   <span data-ttu-id="0a681-123">Der Wert der **Bandbreiten** Eigenschaft muss zwischen "0" und "100" liegen, wobei höhere Werte eine höhere Bandbreite angeben.</span><span class="sxs-lookup"><span data-stu-id="0a681-123">The value of the **Bandwidth** property must be between "0" and "100", with higher values indicating a higher bandwidth.</span></span>
-   <span data-ttu-id="0a681-124">Der Wert "100" gibt die gesamte verfügbare Bandbreite für die Durchführung von virtuellen System Migrations Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="0a681-124">A value of "100" indicates all available bandwidth for performing virtual system migration operations.</span></span>
-   <span data-ttu-id="0a681-125">Werte zwischen "1" und "100" sind linear mit dem verfügbaren Bandbreiten Bereich korreliert.</span><span class="sxs-lookup"><span data-stu-id="0a681-125">Values between "1" and "100" linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="0a681-126">Beispielsweise fordert der Wert 50 die Hälfte der verfügbaren Bandbreite an.</span><span class="sxs-lookup"><span data-stu-id="0a681-126">For example, a value of 50 requests half of the available bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="0a681-127">**Bandwidthunit**</span><span class="sxs-lookup"><span data-stu-id="0a681-127">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a681-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a681-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a681-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a681-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a681-130">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**".**Bandbreite**"), **ispunit**</span><span class="sxs-lookup"><span data-stu-id="0a681-130">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**Bandwidth**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="0a681-131">Die Einheit, die von der **Bandbreiten** Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a681-131">The unit used by the **Bandwidth** property.</span></span> <span data-ttu-id="0a681-132">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, der in Anhang C. 1 von DSP0004 v 2.4 oder höher definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0a681-132">The value of this property should be a legal value of the Programmatic Units qualifier defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

> [!Note]  
> <span data-ttu-id="0a681-133">Profile wie DMTF DSP1081 definieren, wie Clients die Gruppe von Einheiten ermitteln können, die von einer Implementierung unterstützt werden, und Bereiche und Inkremente für Werte der **Bandbreiten** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0a681-133">Profiles such as DMTF DSP1081 define how clients can discover the set of units supported by an implementation, and ranges and increments for values of the **Bandwidth** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="0a681-134">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="0a681-134">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a681-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a681-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a681-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a681-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a681-137">Der Typ des auszuführenden Migrations Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0a681-137">The type of migration operation to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a681-138">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0a681-138">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0a681-139">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0a681-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

<span data-ttu-id="0a681-140">**Live** (2)</span><span class="sxs-lookup"><span data-stu-id="0a681-140">**Live** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

<span data-ttu-id="0a681-141">Fort **setzen (3** )</span><span class="sxs-lookup"><span data-stu-id="0a681-141">**Resume** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="0a681-142">**Neu starten** (4)</span><span class="sxs-lookup"><span data-stu-id="0a681-142">**Restart** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a681-143">**Othertransporttype**</span><span class="sxs-lookup"><span data-stu-id="0a681-143">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a681-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a681-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a681-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a681-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a681-146">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**".**TransportType**")</span><span class="sxs-lookup"><span data-stu-id="0a681-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**TransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="0a681-147">Der Transporttyp, der angewendet werden soll, wenn der Wert von **TransportType** "1" (sonstige) ist.</span><span class="sxs-lookup"><span data-stu-id="0a681-147">The type of transport to apply if the value of **TransportType** is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="0a681-148">**Priority**</span><span class="sxs-lookup"><span data-stu-id="0a681-148">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a681-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a681-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a681-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a681-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a681-151">Die relative Migrations Wichtigkeit, die von der Implementierung der virtuellen System Migration verwendet werden kann, um mehrere ausstehende Migrations Anforderungen zu sortieren oder zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0a681-151">The relative migration importance that the virtual system migration implementation may use to order or assign preference among multiple pending migration requests.</span></span> <span data-ttu-id="0a681-152">Je niedriger der Wert, desto höher ist die Priorität.</span><span class="sxs-lookup"><span data-stu-id="0a681-152">The lower the value, the higher the priority.</span></span> <span data-ttu-id="0a681-153">"0" ist die Standard Bandbreite für Migrations Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="0a681-153">"0" is default bandwidth for migration requests.</span></span>

</dd> <dt>

<span data-ttu-id="0a681-154">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="0a681-154">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a681-155">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a681-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a681-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a681-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a681-157">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**".**Othertransporttype**")</span><span class="sxs-lookup"><span data-stu-id="0a681-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**OtherTransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="0a681-158">Der Transporttyp, der auf einen virtuellen System Migrations Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a681-158">The type of transport to apply to a virtual system migration operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a681-159">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0a681-159">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0a681-160">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0a681-160">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="0a681-161">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="0a681-161">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="0a681-162">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="0a681-162">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="0a681-163">**TLS Strict** (4)</span><span class="sxs-lookup"><span data-stu-id="0a681-163">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="0a681-164">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="0a681-164">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="0a681-165">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="0a681-165">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0a681-166">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0a681-166">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0a681-167">**Anbieter reserviert** (32768..)</span><span class="sxs-lookup"><span data-stu-id="0a681-167">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="0a681-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0a681-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0a681-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a681-169">Requirements</span></span>



| <span data-ttu-id="0a681-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a681-170">Requirement</span></span> | <span data-ttu-id="0a681-171">Wert</span><span class="sxs-lookup"><span data-stu-id="0a681-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a681-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a681-172">Minimum supported client</span></span><br/> | <span data-ttu-id="0a681-173">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0a681-173">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0a681-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a681-174">Minimum supported server</span></span><br/> | <span data-ttu-id="0a681-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0a681-175">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0a681-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a681-176">Namespace</span></span><br/>                | <span data-ttu-id="0a681-177">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0a681-177">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0a681-178">MOF</span><span class="sxs-lookup"><span data-stu-id="0a681-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a681-179"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0a681-179"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a681-180">DLL</span><span class="sxs-lookup"><span data-stu-id="0a681-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a681-181"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a681-181"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a681-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a681-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a681-183">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="0a681-183">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

