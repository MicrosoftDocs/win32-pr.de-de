---
description: Stellt die Migrations Einstellungen zum Migrieren eines virtuellen Systems und des Speichers dar, der an ein virtuelles System angeschlossen ist.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Msvm_VirtualSystemMigrationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862055"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="78c98-103">MSVM \_ virtualsystemmigrationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="78c98-103">Msvm\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="78c98-104">Stellt die Migrations Einstellungen zum Migrieren eines virtuellen Systems und des Speichers dar, der an ein virtuelles System angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="78c98-104">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span>

<span data-ttu-id="78c98-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78c98-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c98-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="78c98-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a><span data-ttu-id="78c98-107">Member</span><span class="sxs-lookup"><span data-stu-id="78c98-107">Members</span></span>

<span data-ttu-id="78c98-108">Die **MSVM \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="78c98-108">The **Msvm\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="78c98-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78c98-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78c98-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78c98-110">Properties</span></span>

<span data-ttu-id="78c98-111">Die **MSVM \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78c98-111">The **Msvm\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78c98-112">**"Zuweisung von Dateien"**</span><span class="sxs-lookup"><span data-stu-id="78c98-112">**AllowOverwriteExistingFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78c98-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-115">Hiermit wird der Speicher Migrations Vorgang ermöglicht, vorhandene vhdx-Dateien zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="78c98-115">Allow the storage migration operation to overwrite existing .vhdx files.</span></span>

> [!Note]  
> <span data-ttu-id="78c98-116">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="78c98-116">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="78c98-117">**Vermeidremuvingvhds**</span><span class="sxs-lookup"><span data-stu-id="78c98-117">**AvoidRemovingVHDs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-118">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78c98-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-120">Entfernen Sie während der Migration keine VHDs, d. h. VHDs auf der Quelle in erfolgreich und VHDs auf dem Ziel Fehler.</span><span class="sxs-lookup"><span data-stu-id="78c98-120">Do not remove any VHDs during the migration, i.e. VHDs on the source in successand VHDs on the destination in failure.</span></span>

> [!Note]  
> <span data-ttu-id="78c98-121">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="78c98-121">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="78c98-122">**Bandwidth**</span><span class="sxs-lookup"><span data-stu-id="78c98-122">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-123">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78c98-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c98-125">Gibt die Bandbreite an, die einem virtuellen System Migrations Vorgang zugewiesen oder angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="78c98-125">Specifies the bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="78c98-126">Die Bandbreiten Einheiten werden durch die **bandwidthunit** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="78c98-126">The bandwidth units are specified by the **BandwidthUnit** property.</span></span> <span data-ttu-id="78c98-127">Innerhalb einer Migration gibt der Wert 0 die Standard Bandbreite an.</span><span class="sxs-lookup"><span data-stu-id="78c98-127">Within a migration, a value of 0 indicates the default bandwidth.</span></span> <span data-ttu-id="78c98-128">Andernfalls gibt der Wert 0 an, dass keine Bandbreiten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="78c98-128">Otherwise, a value of 0 indicates that bandwidths are not supported.</span></span>

<span data-ttu-id="78c98-129">**Bandbreite** und **Priorität** können zusammen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c98-129">**Bandwidth** and **Priority** can be used in conjunction.</span></span> <span data-ttu-id="78c98-130">Migrationsprozesse mit dem höchsten Wert für die gleiche Priorität haben die verfügbare Bandbreite basierend auf der angeforderten Bandbreite gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="78c98-130">Migration processes that have the highest equal priority value share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="78c98-131">Wenn nicht die gesamte Bandbreite von diesem Satz von Prozessen beansprucht wird, wird die verbleibende Bandbreite von Migrationsprozessen mit der nächst niedrigeren gleichen Priorität gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="78c98-131">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal priority share the remaining bandwidth.</span></span> <span data-ttu-id="78c98-132">Wenn noch mehr Bandbreite übrig bleibt, werden Migrationsprozesse mit der nächst niedrigeren gleichen Priorität als gleich betrachtet usw.</span><span class="sxs-lookup"><span data-stu-id="78c98-132">If still more bandwidth remains, migration processes with the next lower equal priority are considered, and so forth.</span></span>

<span data-ttu-id="78c98-133">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-133">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-134">**Bandwidthunit**</span><span class="sxs-lookup"><span data-stu-id="78c98-134">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78c98-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c98-137">Gibt die Einheiten an, die von der **Bandbreiten** Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c98-137">Specifies the units used by the **Bandwidth** property.</span></span> <span data-ttu-id="78c98-138">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.4 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="78c98-138">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

<span data-ttu-id="78c98-139">Wenn der Wert dieser Eigenschaft "Prozent" ist, muss der Wert der **Bandbreiten** Eigenschaft zwischen 0 und 100 liegen, wobei höhere Werte eine höhere Bandbreite angeben.</span><span class="sxs-lookup"><span data-stu-id="78c98-139">If the value of this property is "percent", the value of the **Bandwidth** property must be between 0 and 100, with higher values indicating a higher bandwidth.</span></span> <span data-ttu-id="78c98-140">Der Wert 100 gibt die gesamte verfügbare Bandbreite für die Durchführung von virtuellen System Migrations Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="78c98-140">A value of 100 indicates the total available bandwidth for performing virtual system migration operations.</span></span> <span data-ttu-id="78c98-141">Werte zwischen 1 und 100 sollten linear mit dem verfügbaren Bandbreiten Bereich korrelieren.</span><span class="sxs-lookup"><span data-stu-id="78c98-141">Values between 1 and 100 should linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="78c98-142">Beispielsweise sollte der Wert 50 die Hälfte der verfügbaren Bandbreite anfordern.</span><span class="sxs-lookup"><span data-stu-id="78c98-142">For example, a value of 50 should request half of the available bandwidth.</span></span>

<span data-ttu-id="78c98-143">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-143">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-144">**Cancelifblackoutcedoldexcegetretenen**</span><span class="sxs-lookup"><span data-stu-id="78c98-144">**CancelIfBlackoutThresholdExceeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78c98-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-147">Bricht die Migration ab, wenn der Schwellenwert für den Blackout überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="78c98-147">Cancels migration if the blackout threshold time is exceeded.</span></span>

> [!Note]  
> <span data-ttu-id="78c98-148">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="78c98-148">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="78c98-149">**Caption**</span><span class="sxs-lookup"><span data-stu-id="78c98-149">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78c98-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c98-152">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="78c98-152">A short description of the object.</span></span> <span data-ttu-id="78c98-153">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78c98-154">**Cpucappingmagnitude**</span><span class="sxs-lookup"><span data-stu-id="78c98-154">**CPUCappingMagnitude**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-155">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78c98-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="78c98-157">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("cpucappingmagnitude")</span><span class="sxs-lookup"><span data-stu-id="78c98-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span></span>
</dt> </dl>

<span data-ttu-id="78c98-158">Grad der CPU-capperung während der Migration.</span><span class="sxs-lookup"><span data-stu-id="78c98-158">Degree of CPU capping during migration.</span></span>

> [!Note]  
> <span data-ttu-id="78c98-159">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="78c98-159">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="78c98-160">**Normal** (0)</span><span class="sxs-lookup"><span data-stu-id="78c98-160">**Normal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="78c98-161">**Niedrig** (1)</span><span class="sxs-lookup"><span data-stu-id="78c98-161">**Low** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="78c98-162">**Hoch** (2)</span><span class="sxs-lookup"><span data-stu-id="78c98-162">**High** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78c98-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78c98-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78c98-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c98-166">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="78c98-166">A description of the object.</span></span> <span data-ttu-id="78c98-167">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78c98-168">**Destinationipaddresslist**</span><span class="sxs-lookup"><span data-stu-id="78c98-168">**DestinationIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-169">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="78c98-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="78c98-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-171">Dieser Wert wird für die Speicher Migration **null** sein.</span><span class="sxs-lookup"><span data-stu-id="78c98-171">This will be **Null** for storage migration.</span></span> <span data-ttu-id="78c98-172">Bei der Migration virtueller Systeme kann dies eine Liste der IP-Adressen des Zielhosts enthalten.</span><span class="sxs-lookup"><span data-stu-id="78c98-172">For virtual system migration, this can contain a list of IP addresses of the destination host.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-173">**Destinationplannedvirtualsystemid**</span><span class="sxs-lookup"><span data-stu-id="78c98-173">**DestinationPlannedVirtualSystemId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78c98-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-176">Wenn eine geplante virtuelle Maschine am Migrations Ziel vorhanden ist, wird diese Eigenschaft auf die GUID des geplanten virtuellen Ziel Computers festgelegt, auf dem die virtuelle Maschine migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="78c98-176">If a planned virtual machine exists at the migration destination, this property will be set to the GUID of the destination planned virtual machine where the virtual machine needs to migrate.</span></span> <span data-ttu-id="78c98-177">Dies ist hilfreich in Fällen, in denen ein Benutzer einen geplanten virtuellen Computer am Ziel zusammen mit der Ressourcen Einrichtung erstellt hat und möchte, dass ein virtueller Computer aus der Quelle zu dieser geplanten virtuellen Maschine migriert wird.</span><span class="sxs-lookup"><span data-stu-id="78c98-177">This is useful for cases where a user has created a planned virtual machine at the destination, along with resource setup, and wants a virtual machine from the source to migrate into this planned virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-178">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="78c98-178">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78c98-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c98-181">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="78c98-181">A display name for the object.</span></span> <span data-ttu-id="78c98-182">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78c98-183">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="78c98-183">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78c98-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-186">Gibt an, ob der Live Migrations Datenverkehr komprimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="78c98-186">Indicates whether to compress the live migration traffic.</span></span> <span data-ttu-id="78c98-187">**True** gibt an, dass komprimiert werden soll andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="78c98-187">**True** indicates to compress; otherwise **False**.</span></span>

<span data-ttu-id="78c98-188">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78c98-188">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-189">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="78c98-189">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78c98-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78c98-192">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="78c98-192">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="78c98-193">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="78c98-193">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="78c98-194">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78c98-195">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="78c98-195">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78c98-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-197">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="78c98-198">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("migrationType")</span><span class="sxs-lookup"><span data-stu-id="78c98-198">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span></span>
</dt> </dl>

<span data-ttu-id="78c98-199">Gibt den Typ des auszuführenden Migrations Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="78c98-199">Specifies the type of migration operation to be performed.</span></span> <span data-ttu-id="78c98-200">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-200">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78c98-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="78c98-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span data-ttu-id="78c98-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**Virtualsystem** (32768)</span><span class="sxs-lookup"><span data-stu-id="78c98-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="78c98-203">Migriert das virtuelle System zum Zielhost.</span><span class="sxs-lookup"><span data-stu-id="78c98-203">Migrates the virtual system to the destination host.</span></span>

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="78c98-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Speicher** (32769)</span><span class="sxs-lookup"><span data-stu-id="78c98-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="78c98-205">Migriert nur die Speicherressourcen des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="78c98-205">Migrates only the storage resources of the virtual system.</span></span>

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span data-ttu-id="78c98-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Gestaffelt** (32770)</span><span class="sxs-lookup"><span data-stu-id="78c98-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="78c98-207">Mit der Konfiguration des virtuellen Systems wird ein geplantes virtuelles System auf dem Zielhost erstellt.</span><span class="sxs-lookup"><span data-stu-id="78c98-207">Using the virtual system configuration, creates a planned virtual system at the destination host.</span></span>

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span data-ttu-id="78c98-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**Virtualsystemandstorage** (32771)</span><span class="sxs-lookup"><span data-stu-id="78c98-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span></span>


</dt> <dd>

<span data-ttu-id="78c98-209">Migriert das virtuelle System und seinen Speicher auf den Zielhost.</span><span class="sxs-lookup"><span data-stu-id="78c98-209">Migrates the virtual system and its storage to the destination host.</span></span>

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span data-ttu-id="78c98-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**Storagedeepcheck** (32772)</span><span class="sxs-lookup"><span data-stu-id="78c98-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span></span>


</dt> <dd>

<span data-ttu-id="78c98-211">Führt eine Überprüfung der Verfügbarkeit virtueller Systemspeicher Ressourcen auf dem Zielhost durch.</span><span class="sxs-lookup"><span data-stu-id="78c98-211">Performs a virtual system storage resource migration ability check at the destination host.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78c98-212">**Othertransporttype**</span><span class="sxs-lookup"><span data-stu-id="78c98-212">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78c98-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c98-215">Gibt den Transporttyp an, der angewendet werden soll, wenn der Wert von **TransportType** 1 (Sonstiges) ist.</span><span class="sxs-lookup"><span data-stu-id="78c98-215">Specifies the type of transport to be applied if the value of **TransportType** is 1 (Other).</span></span> <span data-ttu-id="78c98-216">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-216">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-217">**Priority**</span><span class="sxs-lookup"><span data-stu-id="78c98-217">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-218">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78c98-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78c98-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78c98-220">Gibt eine relative Migrations Wichtigkeit an, die das Migrationssystem möglicherweise verwendet, um mehrere ausstehende Migrations Anforderungen zu sortieren oder anderweitig zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="78c98-220">Specifies a relative migration importance, which the migration system may use to order or otherwise give preference among multiple pending migration requests.</span></span> <span data-ttu-id="78c98-221">Je niedriger der Wert, desto höher ist die Priorität.</span><span class="sxs-lookup"><span data-stu-id="78c98-221">The lower the value, the higher the priority.</span></span> <span data-ttu-id="78c98-222">Innerhalb einer Migration gibt der Wert 0 die Standardpriorität an.</span><span class="sxs-lookup"><span data-stu-id="78c98-222">Within a migration, a value of 0 indicates the default priority.</span></span> <span data-ttu-id="78c98-223">Andernfalls gibt der Wert 0 an, dass Prioritäten nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="78c98-223">Otherwise, a value of 0 indicates that priorities are not supported.</span></span>

<span data-ttu-id="78c98-224">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-224">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-225">**Removesourceunmanagedvhds**</span><span class="sxs-lookup"><span data-stu-id="78c98-225">**RemoveSourceUnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-226">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78c98-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-227">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-227">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-228">Entfernen von nicht verwalteten Quell-VHDs.</span><span class="sxs-lookup"><span data-stu-id="78c98-228">Remove source unmanaged VHDs.</span></span>

> [!Note]  
> <span data-ttu-id="78c98-229">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="78c98-229">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="78c98-230">**Retainvhdcopiesonsource**</span><span class="sxs-lookup"><span data-stu-id="78c98-230">**RetainVhdCopiesOnSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78c98-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="78c98-233">Bei einer Speicher Migration geben Sie an, ob die schreibgeschützten VHDs auf dem Quellhost nach Abschluss der Migration entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="78c98-233">For a storage migration, this specifies whether the read-only VHDs on the source host should be removed after the migration is completed.</span></span>

</dd> <dt>

<span data-ttu-id="78c98-234">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="78c98-234">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-235">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78c98-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78c98-236">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-236">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="78c98-237">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("TransportType")</span><span class="sxs-lookup"><span data-stu-id="78c98-237">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span></span>
</dt> </dl>

<span data-ttu-id="78c98-238">Gibt den Transporttyp an, der für einen virtuellen System Migrations Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78c98-238">Specifies the type of transport to be applied for a virtual system migration operation.</span></span> <span data-ttu-id="78c98-239">Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="78c98-239">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78c98-240">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="78c98-240">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78c98-241">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="78c98-241">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="78c98-242">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="78c98-242">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="78c98-243">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="78c98-243">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="78c98-244">**TLS Strict** (4)</span><span class="sxs-lookup"><span data-stu-id="78c98-244">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="78c98-245">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="78c98-245">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="78c98-246">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="78c98-246">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="78c98-247">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="78c98-247">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="78c98-248">**Anbieter reserviert** (32768..)</span><span class="sxs-lookup"><span data-stu-id="78c98-248">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="78c98-249"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="78c98-249"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="78c98-250">Bei der Live Migration gibt diese Eigenschaft den Transporttyp an, der zum Übertragen des Zustands des virtuellen Systems auf den Zielhost verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78c98-250">For live migration, this property specifies the transport type to be used for transferring virtual system state to the destination host.</span></span> <span data-ttu-id="78c98-251">Die unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="78c98-251">The supported values are:</span></span>

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="78c98-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="78c98-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="78c98-253">Gibt den TCP-Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="78c98-253">Indicates the TCP transport type.</span></span>

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span data-ttu-id="78c98-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span><span class="sxs-lookup"><span data-stu-id="78c98-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="78c98-255">Gibt den Transporttyp für die Übertragung des Zustands der virtuellen Maschine an SMB.</span><span class="sxs-lookup"><span data-stu-id="78c98-255">Indicates the transport type for transferring the virtual machine state is SMB.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78c98-256">**Unmanagedvhds**</span><span class="sxs-lookup"><span data-stu-id="78c98-256">**UnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c98-257">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="78c98-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="78c98-258">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="78c98-258">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="78c98-259">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), **hypervembeddedinstance** ("MSVM \_ fiveunmanagedvhd")</span><span class="sxs-lookup"><span data-stu-id="78c98-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_MoveUnmanagedVhd")</span></span>
</dt> </dl>

<span data-ttu-id="78c98-260">Ein Array von eingebetteten [**MSVM \_ -MSVM**](msvm-moveunmanagedvhd.md) -Instanzen, die nicht verwaltete VHDs-Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="78c98-260">An array of embedded [**Msvm\_MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) instances which contain unmanaged VHDs information.</span></span>

> [!Note]  
> <span data-ttu-id="78c98-261">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="78c98-261">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78c98-262">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78c98-262">Requirements</span></span>



| <span data-ttu-id="78c98-263">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78c98-263">Requirement</span></span> | <span data-ttu-id="78c98-264">Wert</span><span class="sxs-lookup"><span data-stu-id="78c98-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c98-265">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78c98-265">Minimum supported client</span></span><br/> | <span data-ttu-id="78c98-266">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78c98-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="78c98-267">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78c98-267">Minimum supported server</span></span><br/> | <span data-ttu-id="78c98-268">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78c98-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78c98-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="78c98-269">Namespace</span></span><br/>                | <span data-ttu-id="78c98-270">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="78c98-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="78c98-271">MOF</span><span class="sxs-lookup"><span data-stu-id="78c98-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78c98-272"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="78c98-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78c98-273">DLL</span><span class="sxs-lookup"><span data-stu-id="78c98-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c98-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78c98-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="78c98-275">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78c98-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c98-276">**CIM \_ virtualsystemmigrationsettingdata**</span><span class="sxs-lookup"><span data-stu-id="78c98-276">**CIM\_VirtualSystemMigrationSettingData**</span></span>](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="78c98-277">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="78c98-277">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

