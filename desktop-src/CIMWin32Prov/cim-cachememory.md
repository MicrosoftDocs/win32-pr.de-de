---
description: Die CIM \_ CacheMemory-Klasse definiert die Funktionen und die Verwaltung des Cache Speichers.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: CIM_CacheMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861363"
---
# <a name="cim_cachememory-class"></a><span data-ttu-id="f2067-103">CIM- \_ CacheMemory-Klasse</span><span class="sxs-lookup"><span data-stu-id="f2067-103">CIM\_CacheMemory class</span></span>

<span data-ttu-id="f2067-104">Die **CIM \_ CacheMemory** -Klasse definiert die Funktionen und die Verwaltung des Cache Speichers.</span><span class="sxs-lookup"><span data-stu-id="f2067-104">The **CIM\_CacheMemory** class defines the capabilities and management of cache memory.</span></span>

<span data-ttu-id="f2067-105">Cache Speicher ist der dedizierte oder zugeordnete RAM, bei dem ein Prozessor zuerst nach Daten sucht.</span><span class="sxs-lookup"><span data-stu-id="f2067-105">Cache memory is the dedicated or allocated RAM where a processor first searches for data.</span></span> <span data-ttu-id="f2067-106">Daten im Cache Speicher werden schnell an den Prozessor übermittelt und in der Regel durch die Nähe des Prozessors (z. b. primär-oder sekundär Cache) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2067-106">Data in cache memory is quickly delivered to the processor and is usually described by its proximity to the processor (for example, primary or secondary cache).</span></span> <span data-ttu-id="f2067-107">Ein Laufwerk, das RAM enthält, das zum Speichern der zuletzt gelesenen oder angrenzenden Daten des Datenträgers reserviert ist (um den Abruf zu beschleunigen), wird ebenfalls als Cache Speicher modelliert.</span><span class="sxs-lookup"><span data-stu-id="f2067-107">A disk drive that includes RAM allocated for holding the disk's most recently read or adjacent data (to speed up retrieval) is also modeled as cache memory.</span></span>

> [!Note]  
> <span data-ttu-id="f2067-108">Der Cache Speicher ist kein Betriebssystem-oder Anwendungs ebenenpuffer. Es handelt sich um RAM, der zum Zwischenspeichern von Prozessor Daten zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2067-108">Cache memory is not an operating-system or application-level buffer; it is RAM that has been allocated for caching processor data.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="f2067-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f2067-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f2067-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f2067-111">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f2067-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f2067-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f2067-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2067-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2067-113">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="f2067-114">Member</span><span class="sxs-lookup"><span data-stu-id="f2067-114">Members</span></span>

<span data-ttu-id="f2067-115">Die **CIM- \_ CacheMemory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f2067-115">The **CIM\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="f2067-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="f2067-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="f2067-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2067-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f2067-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="f2067-118">Methods</span></span>

<span data-ttu-id="f2067-119">Die **CIM- \_ CacheMemory** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f2067-119">The **CIM\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="f2067-120">Methode</span><span class="sxs-lookup"><span data-stu-id="f2067-120">Method</span></span>                                                                 | <span data-ttu-id="f2067-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2067-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2067-122">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="f2067-122">**Reset**</span></span>](reset-method-in-class-cim-cachememory.md)                 | <span data-ttu-id="f2067-123">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f2067-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="f2067-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f2067-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="f2067-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f2067-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cachememory.md) | <span data-ttu-id="f2067-126">Definiert den gewünschten Energiezustand für ein logisches Gerät und den Zeitpunkt, zu dem das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2067-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="f2067-127">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f2067-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f2067-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2067-128">Properties</span></span>

<span data-ttu-id="f2067-129">Die **CIM- \_ CacheMemory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2067-129">The **CIM\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2067-130">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="f2067-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-133">Beschreibt die Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="f2067-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="f2067-134">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-135">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f2067-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="f2067-136">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="f2067-137">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="f2067-138">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="f2067-139">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="f2067-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-141">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="f2067-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f2067-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,18 "," MIF. DMTF \| physikalisches Speicher Array \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f2067-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f2067-144">Ein Array von Oktetten, die zusätzliche Fehlerinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f2067-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="f2067-145">Ein Beispiel hierfür ist die Fehlerüberprüfung und Korrektur (ECC) oder die Rückgabe der Prüfbits, wenn eine CRC-basierte Fehler Methodik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2067-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="f2067-146">Wenn in letzterem Fall ein Single-Bit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, kann das genaue Bit, das fehlgeschlagen ist, bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="f2067-147">Diese Art von Daten (ECC-Syndrom, Check-Bit-oder Paritäts Bitdaten oder andere vom Hersteller bereitgestellte Informationen) ist in diesem Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="f2067-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="f2067-148">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f2067-149">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-150">**Assoziativität**</span><span class="sxs-lookup"><span data-stu-id="f2067-150">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-153">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-154">Enumeration, die die Assoziativität des System Caches definiert.</span><span class="sxs-lookup"><span data-stu-id="f2067-154">Enumeration that defines the system cache associativity.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-155">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-156">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-156">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="f2067-157">**Direkt zugeordnet** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-157">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f2067-158">**2WAY Set-associative** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-158">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f2067-159">**4-Wege-Gruppe-assoziativ** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-159">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="f2067-160">**Vollständig assoziativ** (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-160">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f2067-161">**8-Wege-Gruppe-assoziativ** (7)</span><span class="sxs-lookup"><span data-stu-id="f2067-161">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f2067-162">**16-Wege-Satz-assoziativ** (8)</span><span class="sxs-lookup"><span data-stu-id="f2067-162">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-163">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="f2067-163">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-164">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-166">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="f2067-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-167">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f2067-167">Availability and status of the device.</span></span>

<span data-ttu-id="f2067-168">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-168">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f2067-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f2067-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f2067-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f2067-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f2067-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="f2067-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f2067-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="f2067-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f2067-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f2067-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f2067-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="f2067-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f2067-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="f2067-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f2067-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="f2067-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f2067-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="f2067-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-182">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f2067-182">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f2067-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="f2067-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-184">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f2067-184">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f2067-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f2067-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-186">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-186">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f2067-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="f2067-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f2067-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="f2067-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-189">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="f2067-189">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f2067-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="f2067-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-191">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="f2067-191">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f2067-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="f2067-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-193">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="f2067-193">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f2067-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="f2067-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-195">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f2067-195">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f2067-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="f2067-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-197">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="f2067-197">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-198">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="f2067-198">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-199">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2067-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-201">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="f2067-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-202">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="f2067-202">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="f2067-203">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-203">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="f2067-204">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="f2067-204">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="f2067-205">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f2067-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f2067-206">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-207">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="f2067-207">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-210">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-211">Gibt Anweisungs Zwischenspeicherung, Daten Caching oder beides an.</span><span class="sxs-lookup"><span data-stu-id="f2067-211">Specifies instruction caching, data caching, or both.</span></span> <span data-ttu-id="f2067-212">"Other" und "unknown" können ebenfalls definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-212">"Other" and "Unknown" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-213">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-213">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-214">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-214">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="f2067-215">**Anweisung** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-215">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="f2067-216">**Daten** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-216">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="f2067-217">**Einheitlich** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-217">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f2067-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-221">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f2067-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-222">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f2067-222">A short textual description of the object.</span></span>

<span data-ttu-id="f2067-223">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-224">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="f2067-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-225">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2067-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-227">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f2067-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-228">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f2067-228">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f2067-229">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f2067-230">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="f2067-230">**This device is working properly.**</span></span> <span data-ttu-id="f2067-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="f2067-231">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f2067-232">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="f2067-232">**This device is not configured correctly.**</span></span> <span data-ttu-id="f2067-233">(1)</span><span class="sxs-lookup"><span data-stu-id="f2067-233">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f2067-234">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="f2067-234">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f2067-235">(2)</span><span class="sxs-lookup"><span data-stu-id="f2067-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f2067-236">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="f2067-236">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f2067-237">(3)</span><span class="sxs-lookup"><span data-stu-id="f2067-237">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f2067-238">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f2067-238">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f2067-239">(4)</span><span class="sxs-lookup"><span data-stu-id="f2067-239">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f2067-240">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="f2067-240">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f2067-241">(5)</span><span class="sxs-lookup"><span data-stu-id="f2067-241">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f2067-242">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="f2067-242">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f2067-243"> (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-243">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f2067-244">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="f2067-244">**Cannot filter.**</span></span> <span data-ttu-id="f2067-245">(7)</span><span class="sxs-lookup"><span data-stu-id="f2067-245">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f2067-246">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="f2067-246">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f2067-247">(8)</span><span class="sxs-lookup"><span data-stu-id="f2067-247">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f2067-248">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="f2067-248">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f2067-249">(9)</span><span class="sxs-lookup"><span data-stu-id="f2067-249">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f2067-250">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="f2067-250">**This device cannot start.**</span></span> <span data-ttu-id="f2067-251">(10)</span><span class="sxs-lookup"><span data-stu-id="f2067-251">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f2067-252">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="f2067-252">**This device failed.**</span></span> <span data-ttu-id="f2067-253">(11)</span><span class="sxs-lookup"><span data-stu-id="f2067-253">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f2067-254">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="f2067-254">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f2067-255">(12)</span><span class="sxs-lookup"><span data-stu-id="f2067-255">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f2067-256">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="f2067-256">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f2067-257">(13)</span><span class="sxs-lookup"><span data-stu-id="f2067-257">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f2067-258">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="f2067-258">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f2067-259">(14)</span><span class="sxs-lookup"><span data-stu-id="f2067-259">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f2067-260">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="f2067-260">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f2067-261">(15)</span><span class="sxs-lookup"><span data-stu-id="f2067-261">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f2067-262">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="f2067-262">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f2067-263">(16)</span><span class="sxs-lookup"><span data-stu-id="f2067-263">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f2067-264">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="f2067-264">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f2067-265">(17)</span><span class="sxs-lookup"><span data-stu-id="f2067-265">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f2067-266">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="f2067-266">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f2067-267">(18)</span><span class="sxs-lookup"><span data-stu-id="f2067-267">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f2067-268">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="f2067-268">**Failure using the VxD loader.**</span></span> <span data-ttu-id="f2067-269">(19)</span><span class="sxs-lookup"><span data-stu-id="f2067-269">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f2067-270">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f2067-270">**Your registry might be corrupted.**</span></span> <span data-ttu-id="f2067-271">(20)</span><span class="sxs-lookup"><span data-stu-id="f2067-271">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f2067-272">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="f2067-272">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f2067-273">(21)</span><span class="sxs-lookup"><span data-stu-id="f2067-273">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f2067-274">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f2067-274">**This device is disabled.**</span></span> <span data-ttu-id="f2067-275">(22)</span><span class="sxs-lookup"><span data-stu-id="f2067-275">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f2067-276">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="f2067-276">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f2067-277">(23)</span><span class="sxs-lookup"><span data-stu-id="f2067-277">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f2067-278">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="f2067-278">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f2067-279">(24)</span><span class="sxs-lookup"><span data-stu-id="f2067-279">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f2067-280">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f2067-280">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f2067-281">(25)</span><span class="sxs-lookup"><span data-stu-id="f2067-281">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f2067-282">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f2067-282">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f2067-283">(26)</span><span class="sxs-lookup"><span data-stu-id="f2067-283">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f2067-284">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="f2067-284">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f2067-285">(27)</span><span class="sxs-lookup"><span data-stu-id="f2067-285">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f2067-286">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="f2067-286">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f2067-287">(28)</span><span class="sxs-lookup"><span data-stu-id="f2067-287">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f2067-288">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="f2067-288">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f2067-289">(29)</span><span class="sxs-lookup"><span data-stu-id="f2067-289">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f2067-290">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="f2067-290">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f2067-291">(30)</span><span class="sxs-lookup"><span data-stu-id="f2067-291">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f2067-292">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="f2067-292">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f2067-293">31,5</span><span class="sxs-lookup"><span data-stu-id="f2067-293">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-294">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="f2067-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-295">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f2067-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-297">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f2067-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-298">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2067-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f2067-299">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-300">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="f2067-300">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-301">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f2067-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-303">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. Physisches DMTF- \| Speicher Array \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-304">**True** gibt an, dass der letzte Fehler korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f2067-304">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="f2067-305">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-305">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f2067-306">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-306">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-307">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f2067-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-310">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f2067-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f2067-311">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2067-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f2067-312">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f2067-313">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-314">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2067-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-317">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f2067-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-318">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f2067-318">A textual description of the object.</span></span>

<span data-ttu-id="f2067-319">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f2067-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-323">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f2067-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f2067-324">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="f2067-324">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f2067-325">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-326">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="f2067-326">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-327">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2067-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-329">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,4 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="f2067-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-330">Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-330">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="f2067-331">Die Endadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2067-331">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="f2067-332">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f2067-332">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f2067-333">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-333">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-334">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="f2067-334">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-335">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-337">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,15 "," MIF. Physisches DMTF- \| Speicher Array \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-338">Speicherzugriffs Vorgang, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="f2067-338">Memory access operation that caused the last error.</span></span> <span data-ttu-id="f2067-339">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2067-339">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f2067-340">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-340">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f2067-341">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-342">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-343">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f2067-344">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-344">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="f2067-345">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-345">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="f2067-346">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-346">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-347">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="f2067-347">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-348">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2067-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-350">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,19 "," MIF. DMTF- \| Speichergerät \| 002,20 "," MIF. Physisches DMTF- \| Speicher Array \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-350">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-351">Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="f2067-351">Address of the last memory error.</span></span> <span data-ttu-id="f2067-352">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2067-352">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f2067-353">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-353">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f2067-354">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f2067-354">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f2067-355">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-355">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-356">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="f2067-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-357">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f2067-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-359">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f2067-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f2067-360">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-361">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="f2067-361">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-362">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="f2067-362">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f2067-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-364">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,17 "," MIF. DMTF \| physikalisches Speicher Array \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f2067-364">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f2067-365">Daten, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="f2067-365">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="f2067-366">Die Daten belegen die ersten *n* Oktette des Arrays, die benötigt werden, um die Anzahl der Bits aufzunehmen, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-366">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="f2067-367">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-367">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="f2067-368">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-368">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-369">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="f2067-369">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-370">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-372">Die Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="f2067-372">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="f2067-373">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-373">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="f2067-374">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-374">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f2067-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-376">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="f2067-376">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f2067-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-378">Das am wenigsten signifikante Byte zuerst.</span><span class="sxs-lookup"><span data-stu-id="f2067-378">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f2067-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-380">Das wichtigste Byte zuerst.</span><span class="sxs-lookup"><span data-stu-id="f2067-380">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f2067-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-384">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="f2067-384">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f2067-385">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f2067-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-387">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-389">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. DMTF \| physikalisches Speicher Array \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**Othererrordescription**")</span><span class="sxs-lookup"><span data-stu-id="f2067-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-390">Der Typ des Fehlers, der zuletzt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f2067-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="f2067-391">Die Werte 12 bis 14 sind im CIM-Schema nicht definiert, da DMI die Semantik des Fehler Typs und die korrigierbare Tabelle vermischt.</span><span class="sxs-lookup"><span data-stu-id="f2067-391">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="f2067-392">Ob ein Fehler korrigiert werden kann, wird in der Eigenschaft " **correctableerror** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2067-392">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<span data-ttu-id="f2067-393">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-395">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f2067-395">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-397">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="f2067-397">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f2067-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-399">OK.</span><span class="sxs-lookup"><span data-stu-id="f2067-399">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="f2067-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-401">Ungültiger Lesevorgang.</span><span class="sxs-lookup"><span data-stu-id="f2067-401">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="f2067-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-403">Paritätsfehler.</span><span class="sxs-lookup"><span data-stu-id="f2067-403">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="f2067-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-405">Einzelbit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2067-405">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="f2067-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="f2067-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-407">Double-Bit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2067-407">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="f2067-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="f2067-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-409">Multi-Bit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2067-409">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="f2067-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="f2067-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-411">Nibble-Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2067-411">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="f2067-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="f2067-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-413">Prüfsummen Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2067-413">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="f2067-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="f2067-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-415">CRC-Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2067-415">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f2067-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (12)</span><span class="sxs-lookup"><span data-stu-id="f2067-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-417">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f2067-417">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f2067-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (13)</span><span class="sxs-lookup"><span data-stu-id="f2067-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-419">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f2067-419">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f2067-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (14)</span><span class="sxs-lookup"><span data-stu-id="f2067-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-421">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f2067-421">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-422">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="f2067-422">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-423">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-425">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-426">Gibt an, ob Paritäts-oder CRC-Algorithmen, ECC oder andere Mechanismen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-426">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="f2067-427">Details zum Algorithmus können auch bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-427">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="f2067-428">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-428">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-429">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="f2067-429">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-430">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2067-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-432">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,21 "," MIF. DMTF \| physikalisches Speicher Array \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="f2067-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-433">Gibt den Bereich in Bytes an, in den der letzte Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2067-433">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="f2067-434">Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden (d. h. auf einer typischen Seite), können Fehler in 4-KB-Grenzen aufgelöst werden, und diese Eigenschaft wird auf 4000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2067-434">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="f2067-435">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-435">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f2067-436">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f2067-436">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f2067-437">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-437">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-438">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="f2067-438">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-439">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f2067-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-441">Datum und Uhrzeit des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="f2067-441">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="f2067-442">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2067-442">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f2067-443">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-443">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f2067-444">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-444">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-445">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="f2067-445">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-446">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2067-446">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-448">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,16 "," MIF. DMTF \| physikalisches Speicher Array \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="f2067-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-449">Die Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="f2067-449">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="f2067-450">Der Wert 0 gibt an, dass kein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f2067-450">A value of 0 indicates no error.</span></span> <span data-ttu-id="f2067-451">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, sollte diese Eigenschaft auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-451">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

<span data-ttu-id="f2067-452">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-452">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-453">**Flushtimer**</span><span class="sxs-lookup"><span data-stu-id="f2067-453">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-454">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2067-454">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-456">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,14 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Sekunden ")</span><span class="sxs-lookup"><span data-stu-id="f2067-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-457">Maximale Zeitspanne (in Sekunden), die geänderte Zeilen oder Bucket im Cache verbleiben können, bevor Sie geleert werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-457">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="f2067-458">Der Wert 0 gibt an, dass eine Cache Leerung nicht von einem leeren Timer gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="f2067-458">A value of 0 indicates that a cache flush is not controlled by a flushing timer.</span></span>

</dd> <dt>

<span data-ttu-id="f2067-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f2067-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-460">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f2067-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-461">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-462">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f2067-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-463">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f2067-463">Indicates when the object was installed.</span></span> <span data-ttu-id="f2067-464">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f2067-464">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f2067-465">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-466">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f2067-466">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-467">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2067-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-469">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f2067-469">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f2067-470">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-471">**Level**</span><span class="sxs-lookup"><span data-stu-id="f2067-471">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-472">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-473">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-474">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-475">Gibt an, ob es sich um den primären, sekundären oder tertiären Cache handelt.</span><span class="sxs-lookup"><span data-stu-id="f2067-475">Specifies whether this is the primary, secondary or tertiary cache.</span></span> <span data-ttu-id="f2067-476">"Other", "unknown" und "nicht zutreffend" können ebenfalls definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-476">"Other", "Unknown", and "Not Applicable" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-478">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f2067-478">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-480">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="f2067-480">Unknown.</span></span>

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="f2067-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primär** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-482">Primär.</span><span class="sxs-lookup"><span data-stu-id="f2067-482">Primary.</span></span>

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="f2067-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Sekundär** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-484">Mittleren.</span><span class="sxs-lookup"><span data-stu-id="f2067-484">Secondary.</span></span>

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="f2067-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiär** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-486">Aten.</span><span class="sxs-lookup"><span data-stu-id="f2067-486">Tertiary.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f2067-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-488">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="f2067-488">Not applicable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-489">**Linesize**</span><span class="sxs-lookup"><span data-stu-id="f2067-489">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-490">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2067-490">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-491">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-492">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="f2067-492">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-493">Größe (in Bytes) eines einzelnen cachebucket oder einer einzelnen Zeile.</span><span class="sxs-lookup"><span data-stu-id="f2067-493">Size, in bytes, of a single cache bucket or line.</span></span>

</dd> <dt>

<span data-ttu-id="f2067-494">**Name**</span><span class="sxs-lookup"><span data-stu-id="f2067-494">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-495">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-496">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-497">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f2067-497">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-498">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f2067-498">Label by which the object is known.</span></span> <span data-ttu-id="f2067-499">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-499">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f2067-500">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-500">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-501">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="f2067-501">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-502">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2067-502">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-503">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-504">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="f2067-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-505">Anzahl der aufeinander folgenden Blöcke, die die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="f2067-505">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="f2067-506">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="f2067-506">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="f2067-507">Wenn der Wert von **BLOCKSIZE** 1 (eins) ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="f2067-507">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="f2067-508">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f2067-508">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f2067-509">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-509">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-510">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="f2067-510">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-511">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-512">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-513">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="f2067-513">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-514">Freie Formular Zeichenfolge, die Informationen bereitstellt, wenn die **ErrorType** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2067-514">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="f2067-515">Wenn Sie nicht auf 1 festgelegt ist, hat diese Zeichenfolge keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-515">If it is not set to 1, then this string has no meaning.</span></span>

<span data-ttu-id="f2067-516">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-516">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-517">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f2067-517">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-518">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-520">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f2067-520">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-521">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f2067-521">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f2067-522">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f2067-522">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f2067-523">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-524">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f2067-524">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-525">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f2067-525">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f2067-526">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-527">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f2067-527">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="f2067-528">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f2067-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-530">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f2067-530">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f2067-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-532">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2067-532">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f2067-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-534">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f2067-534">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f2067-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-536">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2067-536">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f2067-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-538">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="f2067-538">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f2067-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-540">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2067-540">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="f2067-541">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-541">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="f2067-542">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f2067-542">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f2067-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-544">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="f2067-544">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f2067-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="f2067-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-546">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2067-546">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-547">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="f2067-547">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-548">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f2067-548">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-549">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-550">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f2067-550">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f2067-551">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="f2067-551">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f2067-552">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-552">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f2067-553">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="f2067-553">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f2067-554">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-554">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-555">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="f2067-555">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-556">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-557">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-557">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-558">Freie Formular Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f2067-558">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="f2067-559">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-559">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-560">**ReadPolicy**</span><span class="sxs-lookup"><span data-stu-id="f2067-560">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-561">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-562">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-563">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-563">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-564">Richtlinie, die vom Cache für die Verarbeitung von Lese Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2067-564">Policy employed by the cache for handling read requests.</span></span> <span data-ttu-id="f2067-565">Wenn die Richtlinie für den Lesevorgang einzeln bestimmt wird, d. h. für jede Anforderung, sollte der Wert 6 ("Bestimmung pro e/a") angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-565">If the read policy is determined individually, that is, for each request, then the value 6 ("Determination per I/O") should be specified.</span></span> <span data-ttu-id="f2067-566">"Other" und "unknown" sind ebenfalls gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="f2067-566">"Other" and "Unknown" are also valid values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-568">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f2067-568">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-570">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="f2067-570">Unknown.</span></span>

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f2067-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-572">Lesen.</span><span class="sxs-lookup"><span data-stu-id="f2067-572">Read.</span></span>

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="f2067-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-574">Read-Ahead.</span><span class="sxs-lookup"><span data-stu-id="f2067-574">Read-ahead.</span></span>

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="f2067-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read und Read-Ahead** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read and Read-Ahead** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-576">Lesen und lesen.</span><span class="sxs-lookup"><span data-stu-id="f2067-576">Read and read-ahead.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="f2067-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Bestimmung pro e/** a (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-578">Bestimmung pro e/a.</span><span class="sxs-lookup"><span data-stu-id="f2067-578">Determination per I/O.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-579">**Replacementpolicy**</span><span class="sxs-lookup"><span data-stu-id="f2067-579">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-580">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-580">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-581">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-582">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-583">Ganzzahlige Enumeration, die den Algorithmus beschreibt, der bestimmt, welche Cache Zeilen oder-Bucket wieder verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2067-583">Integer enumeration describing the algorithm that determines which cache lines or buckets should be re-used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-585">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f2067-585">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-587">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="f2067-587">Unknown.</span></span>

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="f2067-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Zuletzt verwendet (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-589">Zuletzt verwendet (LRU).</span><span class="sxs-lookup"><span data-stu-id="f2067-589">Least recently used (LRU).</span></span>

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="f2067-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First in First Out (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-591">First in, First Out (FIFO).</span><span class="sxs-lookup"><span data-stu-id="f2067-591">First-in, first-out (FIFO).</span></span>

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="f2067-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last in First Out (LIFO)** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-593">Last-in, First-Out (LIFO).</span><span class="sxs-lookup"><span data-stu-id="f2067-593">Last-in, first-out (LIFO).</span></span>

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="f2067-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Am wenigsten häufig verwendet (LfU)** (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-595">Am wenigsten häufig verwendet (LfU)</span><span class="sxs-lookup"><span data-stu-id="f2067-595">Least frequently used (LFU.)</span></span>

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="f2067-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Am häufigsten verwendet (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="f2067-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-597">Am häufigsten verwendet (MFU).</span><span class="sxs-lookup"><span data-stu-id="f2067-597">Most frequently used (MFU).</span></span>

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="f2067-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Daten abhängige mehrere Algorithmen** (8)</span><span class="sxs-lookup"><span data-stu-id="f2067-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-599">Daten abhängige mehrere Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="f2067-599">Data-dependent multiple algorithms.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-600">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="f2067-600">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-601">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2067-601">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-602">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-603">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,3 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="f2067-603">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-604">Anfangsadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-604">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="f2067-605">Die Startadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2067-605">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="f2067-606">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f2067-606">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f2067-607">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-607">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-608">**Status**</span><span class="sxs-lookup"><span data-stu-id="f2067-608">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-609">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-609">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-610">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-610">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-611">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f2067-611">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-612">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="f2067-612">String that indicates the current status of the object.</span></span> <span data-ttu-id="f2067-613">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-613">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f2067-614">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f2067-614">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f2067-615">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="f2067-615">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f2067-616">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f2067-616">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f2067-617">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f2067-617">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f2067-618">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f2067-618">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f2067-619">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-619">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f2067-620">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f2067-620">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f2067-621">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f2067-621">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f2067-622">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f2067-622">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f2067-623">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f2067-623">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-624">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f2067-624">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f2067-625">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f2067-625">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f2067-626">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f2067-626">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f2067-627">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f2067-627">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f2067-628">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f2067-628">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f2067-629">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f2067-629">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f2067-630">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f2067-630">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f2067-631">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f2067-631">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f2067-632">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f2067-632">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-633">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f2067-633">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-634">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-634">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-635">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-636">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-637">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f2067-637">State of the logical device.</span></span> <span data-ttu-id="f2067-638">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-638">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="f2067-639">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-640">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-640">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-641">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-641">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f2067-642">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-642">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f2067-643">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-643">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f2067-644">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-644">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2067-645">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f2067-645">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-646">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-647">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-648">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f2067-648">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f2067-649">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f2067-649">The scoping system's creation class name.</span></span>

<span data-ttu-id="f2067-650">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-650">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-651">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="f2067-651">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-652">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f2067-652">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-653">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-653">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2067-654">Gibt an, ob die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene (**true**) oder eine physische Adresse (**false**) sind.</span><span class="sxs-lookup"><span data-stu-id="f2067-654">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="f2067-655">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2067-655">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f2067-656">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-656">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-657">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f2067-657">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-658">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f2067-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-659">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-659">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-660">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f2067-660">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f2067-661">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f2067-661">The scoping system's name.</span></span>

<span data-ttu-id="f2067-662">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f2067-662">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2067-663">**"Write Policy"**</span><span class="sxs-lookup"><span data-stu-id="f2067-663">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2067-664">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2067-664">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2067-665">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2067-665">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2067-666">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="f2067-666">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="f2067-667">Definiert, ob der Cache einen Schreib-oder Lesevorgang durchläuft oder ob die Informationen für jede Eingabe/Ausgabe unterschiedlich sind oder einzeln definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-667">Defines whether the cache is write-back or write-through, or whether the information "Varies with Address" or is defined individually for each input/output.</span></span> <span data-ttu-id="f2067-668">"Other" und "unknown" können ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2067-668">"Other" and "Unknown" also can be specified.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2067-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f2067-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-670">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f2067-670">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2067-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f2067-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-672">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="f2067-672">Unknown.</span></span>

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="f2067-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Zurückschreiben** (3)</span><span class="sxs-lookup"><span data-stu-id="f2067-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write Back** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-674">Schreiben Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="f2067-674">Write back.</span></span>

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="f2067-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Schreiben durch** (4)</span><span class="sxs-lookup"><span data-stu-id="f2067-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Write Through** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-676">Schreiben Sie.</span><span class="sxs-lookup"><span data-stu-id="f2067-676">Write through.</span></span>

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="f2067-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Variiert mit der Adresse** (5)</span><span class="sxs-lookup"><span data-stu-id="f2067-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varies with Address** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-678">Variiert mit der Adresse.</span><span class="sxs-lookup"><span data-stu-id="f2067-678">Varies with address.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="f2067-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Bestimmung pro e/** a (6)</span><span class="sxs-lookup"><span data-stu-id="f2067-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2067-680">Bestimmung pro e/a.</span><span class="sxs-lookup"><span data-stu-id="f2067-680">Determination per I/O.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2067-681">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2067-681">Remarks</span></span>

<span data-ttu-id="f2067-682">Die **CIM- \_ CacheMemory** -Klasse wird vom [**CIM- \_ Speicher**](cim-memory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f2067-682">The **CIM\_CacheMemory** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="f2067-683">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f2067-683">WMI does not implement this class.</span></span> <span data-ttu-id="f2067-684">Weitere Informationen zu Klassen, die von **CIM \_ CacheMemory** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f2067-684">For more information about classes derived from **CIM\_CacheMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f2067-685">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f2067-685">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f2067-686">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f2067-686">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2067-687">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2067-687">Requirements</span></span>



| <span data-ttu-id="f2067-688">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2067-688">Requirement</span></span> | <span data-ttu-id="f2067-689">Wert</span><span class="sxs-lookup"><span data-stu-id="f2067-689">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2067-690">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2067-690">Minimum supported client</span></span><br/> | <span data-ttu-id="f2067-691">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2067-691">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2067-692">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2067-692">Minimum supported server</span></span><br/> | <span data-ttu-id="f2067-693">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2067-693">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2067-694">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2067-694">Namespace</span></span><br/>                | <span data-ttu-id="f2067-695">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f2067-695">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2067-696">MOF</span><span class="sxs-lookup"><span data-stu-id="f2067-696">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2067-697"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f2067-697"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2067-698">DLL</span><span class="sxs-lookup"><span data-stu-id="f2067-698">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2067-699"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2067-699"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2067-700">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2067-700">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2067-701">**CIM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="f2067-701">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

