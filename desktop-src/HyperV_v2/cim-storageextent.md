---
description: Beschreibt die Funktionen und die Verwaltung von Medien, die Daten speichern und den Abruf der Daten ermöglichen. Diese Superklasse wird zur Darstellung von Software-und Hardware-RAID-Komponenten oder einem logischen Bereich physischer Datenträger verwendet.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: CIM_StorageExtent-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368754"
---
# <a name="cim_storageextent-class-hyper-v-management"></a><span data-ttu-id="dc9b0-104">CIM_StorageExtent-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-104">CIM_StorageExtent class (Hyper-V management)</span></span>

<span data-ttu-id="dc9b0-105">Beschreibt die Funktionen und die Verwaltung von Medien, die Daten speichern und den Abruf der Daten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-105">Describes the capabilities and management of media that stores data and allows retrieval of the data.</span></span> <span data-ttu-id="dc9b0-106">Diese Superklasse wird zur Darstellung von Software-und Hardware-RAID-Komponenten oder einem logischen Bereich physischer Datenträger verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-106">This super class is used to represent software and hardware RAID components, or a raw logical extent of physical media.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc9b0-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="dc9b0-108">Member</span><span class="sxs-lookup"><span data-stu-id="dc9b0-108">Members</span></span>

<span data-ttu-id="dc9b0-109">Die **CIM \_ storageblock** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc9b0-109">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="dc9b0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc9b0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc9b0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc9b0-111">Properties</span></span>

<span data-ttu-id="dc9b0-112">Die **CIM \_ storageblock** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-112">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc9b0-113">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-113">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-116">Eine Beschreibung der Lese-/Schreibunterstützung des Mediums.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-116">A description of the read/write support of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc9b0-117">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="dc9b0-118">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-118">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="dc9b0-119">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-119">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="dc9b0-120">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-120">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="dc9b0-121">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-121">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc9b0-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-123">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-125">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Host Speicher \| 001,4 "," MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "," MIF. DMTF- \| Speichergeräte \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.4", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF.DMTF\|Storage Devices\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-126">Die Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-126">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="dc9b0-127">Wenn Variablen Blockgrößen verwendet werden, sollte diese Eigenschaft die maximale Blockgröße angeben.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-127">If variable block sizes are used, then this property should specify the maximum block size.</span></span> <span data-ttu-id="dc9b0-128">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für **CIM- \_ aggregatblock**, [**CIM- \_ Speicher**](cim-memory.md) oder [**CIM \_ LogicalDisk**](cim-logicaldisk.md)), sollte diese Eigenschaft auf "1" (unbekannt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-128">If the block size is unknown or if a block concept is not valid (for example, for **CIM\_AggregateExtent**, [**CIM\_Memory**](cim-memory.md) or [**CIM\_LogicalDisk**](cim-logicaldisk.md)), then this property should be set to "1" (unknow).</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-129">**Consumableblocks**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-129">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-130">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-132">Die maximale Anzahl von Blöcken, die zur Verwendung bei der Schichten- **CIM- \_ Speicher** Zuweisung mithilfe der [**CIM- \_ BasedOn**](cim-basedon.md) -Klassen Zuordnung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-132">The maximum number of blocks, that are available for use when layering **CIM\_StorageExtent** using the [**CIM\_BasedOn**](cim-basedon.md) class association.</span></span> <span data-ttu-id="dc9b0-133">Diese Eigenschaft hat nur Bedeutung, wenn in der **Vorgänger** Eigenschaft eines **CIM- \_ BasedOn** -Objekts auf den Speicherblock verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-133">This property only has meaning when the storage extent is referenced in the **Antecedent** property in a **CIM\_BasedOn** object.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-134">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-134">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-137">Der Typ der von den Medien verwendeten Datenorganisation.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-137">The type of data organization used by the media.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc9b0-138">**Sonstige** (0)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-138">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc9b0-139">**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-139">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

<span data-ttu-id="dc9b0-140">**Fester Block** (2)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-140">**Fixed Block** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

<span data-ttu-id="dc9b0-141">**Variablen Block** (3)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-141">**Variable Block** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

<span data-ttu-id="dc9b0-142">**Schlüsseldaten zählen** (4)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-142">**Count Key Data** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc9b0-143">**Dataredundancy**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-143">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-146">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)".**Dataredundancygoal**","**CIM \_ StorageSet**.**Dataredundancymax**","**CIM \_ StorageSet**.**Dataredundancymin**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM\_StorageSetting**.**DataRedundancyMax**", "**CIM\_StorageSetting**.**DataRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-147">Die Anzahl der kompletten Kopien von Daten, die zurzeit verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-147">The number of complete copies of data that are currently maintained.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-148">**Delta Service**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-148">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-149">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-151">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozentsatz"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**Delta-eservationgoal**","**CIM \_ StorageSet**.**Delta Service** Type ","**CIM \_ StorageSet**.**Delta Service** Type ")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM\_StorageSetting**.**DeltaReservationMax**", "**CIM\_StorageSetting**.**DeltaReservationMin**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-152">Der aktuelle Wert für die Delta Reservierung.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-152">The current value for delta reservation.</span></span> <span data-ttu-id="dc9b0-153">Dies ist ein Prozentsatz, der den Speicherplatz angibt, der in einem Replikat reserviert werden soll, um Änderungen zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-153">This is a percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-154">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-157">Der Typ der Fehlererkennung und-Korrektur, der vom Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-157">The type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-158">**Extentstatus**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-158">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-159">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="dc9b0-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-161">Weitere Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-161">Additional status information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc9b0-162">**Sonstige** (0)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-162">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc9b0-163">**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-163">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

<span data-ttu-id="dc9b0-164">**Keine/nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-164">**None/Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

<span data-ttu-id="dc9b0-165">**Beschädigt** (3)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-165">**Broken** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

<span data-ttu-id="dc9b0-166">**Verlust von Daten** (4)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-166">**Data Lost** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

<span data-ttu-id="dc9b0-167">**Dynamische Neukonfiguration** (5)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-167">**Dynamic Reconfig** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

<span data-ttu-id="dc9b0-168">Verfügbar **gemacht (6** )</span><span class="sxs-lookup"><span data-stu-id="dc9b0-168">**Exposed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

<span data-ttu-id="dc9b0-169">In **Bruch Komma Sicht** verfügbar (7)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-169">**Fractionally Exposed** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

<span data-ttu-id="dc9b0-170">**Teilweise** verfügbar (8)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-170">**Partially Exposed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

<span data-ttu-id="dc9b0-171">**Schutz deaktiviert** (9)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-171">**Protection Disabled** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

<span data-ttu-id="dc9b0-172">**Lesen** (10)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-172">**Readying** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

<span data-ttu-id="dc9b0-173">**Neu erstellen** (11)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-173">**Rebuild** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

<span data-ttu-id="dc9b0-174">**Neuberechnen** (12)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-174">**Recalculate** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

<span data-ttu-id="dc9b0-175">**Ersatz in Gebrauch** (13)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-175">**Spare in Use** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

<span data-ttu-id="dc9b0-176">**Überprüfen in** Bearbeitung (14)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-176">**Verify In Progress** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

<span data-ttu-id="dc9b0-177">**In-Band-Zugriff gewährt** (15)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-177">**In-Band Access Granted** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

<span data-ttu-id="dc9b0-178">**Importiert** (16)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-178">**Imported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

<span data-ttu-id="dc9b0-179">**Exportiert** (17)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-179">**Exported** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dc9b0-180">**DMTF reserviert** (18.. 32767)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-180">**DMTF Reserved** (18..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="dc9b0-181">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-181">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc9b0-182">**Isbasedonunderlyingredundancy**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-182">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-183">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dc9b0-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-185">**true** , wenn die zugrunde liegenden Speicherblöcke Mitglieder einer [**CIM \_ storageredundancygroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup)sind; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-185">**true** if the underlying storage extents are members of a [**CIM\_StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-186">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-189">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. Begints-T10 \| VPD 83, Association 0 \| Identifier "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**NameFormat**","**CIM \_ storageblock**.**Namenamespace**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**", "**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-190">Ein eindeutiger Bezeichner für den Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-190">A unique identifier for the storage extent.</span></span> <span data-ttu-id="dc9b0-191">Die Eigenschaft **NameFormat** gibt das Benennungs Format an, das in der Eigenschaft **Name** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-191">The **NameFormat** property specifies the naming format to use in the **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-192">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-192">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-193">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-195">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**Name**","**CIM \_ storageblock**.**Namenamespace**","**CIM \_ storageblock**.**Othernameformat**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-195">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**NameNamespace**", "**CIM\_StorageExtent**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-196">Das Benennungs Format für die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-196">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc9b0-197">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-197">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc9b0-198">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-198">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

<span data-ttu-id="dc9b0-199">**VPD83NAA6** (2)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-199">**VPD83NAA6** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

<span data-ttu-id="dc9b0-200">**VPD83NAA5** (3)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-200">**VPD83NAA5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="dc9b0-201">**VPD83Type2** (4)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-201">**VPD83Type2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="dc9b0-202">**VPD83Type1** (5)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-202">**VPD83Type1** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

<span data-ttu-id="dc9b0-203">**VPD83Type0** (6)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-203">**VPD83Type0** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="dc9b0-204">**Snvm** (7)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-204">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="dc9b0-205">**NoDebug** (8)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-205">**NodeWWN** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="dc9b0-206">**Naa** (9)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-206">**NAA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="dc9b0-207">**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-207">**EUI64** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="dc9b0-208">**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-208">**T10VID** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="dc9b0-209">**Betriebssystem-Geräte Name** (12)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-209">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc9b0-210">**Namenamespace**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-210">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-213">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. Begints-T10 \| VPD 83, Association 0 \| Identifier "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**Name**","**CIM \_ storageblock**.**Othernamenamespace**","**CIM \_ storageblock**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**OtherNameNamespace**", "**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-214">Der Namespace der Name-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-214">The namespace of the name property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc9b0-215">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-215">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc9b0-216">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-216">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="dc9b0-217">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-217">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="dc9b0-218">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-218">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="dc9b0-219">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-219">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="dc9b0-220">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-220">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="dc9b0-221">**NoDebug** (6)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-221">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="dc9b0-222">**Snvm** (7)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-222">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="dc9b0-223">**Betriebssystem-Geräte Namespace** (8)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-223">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc9b0-224">**Nosinglepoinpoffailure**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-224">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-225">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dc9b0-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-227">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)".**Nosinglepoinpoffailure**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-227">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-228">**true** , wenn es keine einzelnen Fehlerpunkte gibt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-228">**true** if there are not any single points of failure; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-229">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-229">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-230">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-232">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Host Speicher \| 001,5 "," MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-233">Die Gesamtanzahl logisch zusammenhängender Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-233">The total number of logically contiguous blocks that form the storage extent.</span></span> <span data-ttu-id="dc9b0-234">Die Gesamtgröße des Speicherbereichs wird durch Multiplizieren von **BLOCKSIZE** nach **Anzahl Blöcken** berechnet.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-234">The total size of the storage extent is calculated by multiplying **BlockSize** by **NumberOfBlocks**.</span></span> <span data-ttu-id="dc9b0-235">Wenn **Block Size** den Wert 1 hat, entspricht diese Eigenschaft der Gesamtgröße des Speicherbereichs.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-235">If the **BlockSize** is "1", this property is the total size of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-236">**Othernameformat**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-236">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-239">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-239">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-240">Das Format der **Name** -Eigenschaft, wenn die **NameFormat** -Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-240">The format of the **Name** property when the **NameFormat** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-241">**Othernamenamespace**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-241">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-244">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**Namenamespace**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-244">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-245">Eine Beschreibung des Namespace der **Name** -Eigenschaft, wenn die **namenamespace** -Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-245">A description of the namespace of the **Name** property when the **NameNamespace** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-246">**Packageredundancy**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-246">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-247">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-249">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)".**Packageredundancygoal**","**CIM \_ StorageSet**.**Packageredundancymax**","**CIM \_ StorageSet**.**Packageredundancymin**")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-249">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM\_StorageSetting**.**PackageRedundancyMax**", "**CIM\_StorageSetting**.**PackageRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-250">Die aktuelle Anzahl von physischen Paketen, die ohne Datenverlust ausfallen können.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-250">The current number of physical packages that can fail without data loss.</span></span> <span data-ttu-id="dc9b0-251">In einer Speicher Domäne kann dies z. b. die Anzahl der Datenträger Spindeln sein.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-251">For example, in a storage domain, this might be the number of disk spindles.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-252">**Ursprünglich**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-252">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-253">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dc9b0-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-255">**true** , wenn der Speicherblock ursprünglicher ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-255">**true** if the storage extent is primordial; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-256">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-256">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-259">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragedescr ")</span><span class="sxs-lookup"><span data-stu-id="dc9b0-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageDescr")</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-260">Eine Beschreibung der Medien Verwendung.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-260">A description of the media usage.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b0-261">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-261">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9b0-262">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dc9b0-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc9b0-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc9b0-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9b0-264">**true** , wenn auf den Speicher sequenziell von einem [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md) -Objekt zugegriffen wird, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="dc9b0-264">**true** if storage is sequentially accessed by a [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) object; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc9b0-265">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc9b0-265">Requirements</span></span>



| <span data-ttu-id="dc9b0-266">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc9b0-266">Requirement</span></span> | <span data-ttu-id="dc9b0-267">Wert</span><span class="sxs-lookup"><span data-stu-id="dc9b0-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9b0-268">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-268">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9b0-269">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dc9b0-269">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dc9b0-270">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc9b0-270">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9b0-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc9b0-271">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dc9b0-272">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc9b0-272">Namespace</span></span><br/>                | <span data-ttu-id="dc9b0-273">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dc9b0-273">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dc9b0-274">MOF</span><span class="sxs-lookup"><span data-stu-id="dc9b0-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc9b0-275"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b0-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc9b0-276">DLL</span><span class="sxs-lookup"><span data-stu-id="dc9b0-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc9b0-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b0-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc9b0-278">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc9b0-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9b0-279">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="dc9b0-279">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

