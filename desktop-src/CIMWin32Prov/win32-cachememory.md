---
description: Win32- \_ CacheMemory-&\# 32; Die WMI-Klasse stellt den internen und externen Cache Speicher auf einem Computersystem dar.
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Win32_CacheMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83a8fefbe1104f24f208d232b8f6bc134efefd83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861520"
---
# <a name="win32_cachememory-class"></a><span data-ttu-id="dbaf4-103">Win32- \_ CacheMemory-Klasse</span><span class="sxs-lookup"><span data-stu-id="dbaf4-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="dbaf4-104">Die **Win32 \_ CacheMemory** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt den internen und externen Cache Speicher auf einem Computersystem dar.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="dbaf4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dbaf4-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbaf4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbaf4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="dbaf4-108">Member</span><span class="sxs-lookup"><span data-stu-id="dbaf4-108">Members</span></span>

<span data-ttu-id="dbaf4-109">Die **Win32- \_ CacheMemory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dbaf4-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="dbaf4-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="dbaf4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dbaf4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbaf4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dbaf4-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="dbaf4-112">Methods</span></span>

<span data-ttu-id="dbaf4-113">Die **Win32- \_ CacheMemory** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="dbaf4-114">Methode</span><span class="sxs-lookup"><span data-stu-id="dbaf4-114">Method</span></span>            | <span data-ttu-id="dbaf4-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbaf4-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbaf4-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-116">**Reset**</span></span>         | <span data-ttu-id="dbaf4-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-117">Not implemented.</span></span> <span data-ttu-id="dbaf4-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ CacheMemory**](cim-cachememory.md) für die Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="dbaf4-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-119">**SetPowerState**</span></span> | <span data-ttu-id="dbaf4-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-120">Not implemented.</span></span> <span data-ttu-id="dbaf4-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ CacheMemory**](cim-cachememory.md) für die Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dbaf4-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbaf4-122">Properties</span></span>

<span data-ttu-id="dbaf4-123">Die **Win32- \_ CacheMemory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbaf4-124">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-127">Der Zugriffstyp.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-127">Type of access.</span></span>

<span data-ttu-id="dbaf4-128">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="dbaf4-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="dbaf4-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-132">Schreibbar</span><span class="sxs-lookup"><span data-stu-id="dbaf4-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="dbaf4-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="dbaf4-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-136">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="dbaf4-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,18 "," MIF. DMTF \| physikalisches Speicher Array \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-139">Ein Array von Oktetten, die zusätzliche Fehlerinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="dbaf4-140">Ein Beispiel hierfür ist ECC-Syndrom oder die Rückgabe der Kontroll Bits, wenn eine CRC-basierte Fehler Methodik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="dbaf4-141">Wenn in letzterem Fall ein Einzelbit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, können Sie das genaue Bit ermitteln, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="dbaf4-142">Diese Art von Daten (ECC-Syndrom, Check-Bit, Paritäts Bitdaten oder andere vom Hersteller bereitgestellte Informationen) ist in diesem Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="dbaf4-143">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-144">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-145">**Assoziativität**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-146">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-149">Eine ganzzahlige Enumeration, die die Assoziativität des System Caches definiert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="dbaf4-150">Dieser Wert stammt aus dem **Assoziativität** -Member der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="dbaf4-151">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-152">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-153">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="dbaf4-154">**Direkt zugeordnet** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="dbaf4-155">**2WAY Set-associative** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="dbaf4-156">**4-Wege-Gruppe-assoziativ** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="dbaf4-157">**Vollständig assoziativ** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="dbaf4-158">**8-Wege-Gruppe-assoziativ** (7)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="dbaf4-159">**16-Wege-Satz-assoziativ** (8)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-160">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-163">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-164">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-164">Availability and status of the device.</span></span>

<span data-ttu-id="dbaf4-165">Dieser Wert stammt aus dem **Cache Konfigurations** Mitglied der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="dbaf4-166">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dbaf4-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-170">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="dbaf4-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dbaf4-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dbaf4-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dbaf4-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dbaf4-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dbaf4-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dbaf4-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dbaf4-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="dbaf4-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dbaf4-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dbaf4-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dbaf4-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-181">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dbaf4-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-183">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dbaf4-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-185">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dbaf4-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dbaf4-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-188">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dbaf4-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-190">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dbaf4-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-192">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dbaf4-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-194">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dbaf4-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="dbaf4-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-196">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-198">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-200">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-201">Größe in Byte der Blöcke, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="dbaf4-202">Wenn unbekannt oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 ein.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="dbaf4-203">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="dbaf4-204">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-205">**CacheSpeed**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-206">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-208">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 7 \| Cache Geschwindigkeit"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nanosekunden")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-209">Geschwindigkeit des Caches.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-209">Speed of the cache.</span></span>

<span data-ttu-id="dbaf4-210">Dieser Wert stammt aus dem **Cache Geschwindigkeits** Element der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-214">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-215">Typ des Caches.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-215">Type of cache.</span></span>

<span data-ttu-id="dbaf4-216">Dieser Wert stammt aus dem Member des **System Cache Typs** der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="dbaf4-217">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-218">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-219">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="dbaf4-220">**Anweisung** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="dbaf4-221">**Daten** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="dbaf4-222">**Einheitlich** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-223">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-226">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-227">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="dbaf4-228">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-229">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-230">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-232">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-233">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="dbaf4-234">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dbaf4-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dbaf4-236"> (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-237">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dbaf4-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dbaf4-239">(1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-240">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dbaf4-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dbaf4-242">(2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dbaf4-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dbaf4-244">(3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-245">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dbaf4-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dbaf4-247">(4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-248">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-248">Device is not working properly.</span></span> <span data-ttu-id="dbaf4-249">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dbaf4-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dbaf4-251">(5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-252">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dbaf4-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dbaf4-254"> (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-255">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dbaf4-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dbaf4-257">(7)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dbaf4-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dbaf4-259">(8)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-260">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dbaf4-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dbaf4-262">(9)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-263">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-263">Device is not working properly.</span></span> <span data-ttu-id="dbaf4-264">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dbaf4-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dbaf4-266">(10)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-267">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dbaf4-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dbaf4-269">(11)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-270">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dbaf4-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dbaf4-272">(12)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-273">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dbaf4-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dbaf4-275">(13)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-276">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dbaf4-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dbaf4-278">(14)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-279">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dbaf4-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dbaf4-281">(15)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-282">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dbaf4-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dbaf4-284">(16)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-285">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dbaf4-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dbaf4-287">(17)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-288">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dbaf4-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dbaf4-290">(18)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-291">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dbaf4-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dbaf4-293">(19)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dbaf4-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dbaf4-295">(20)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-296">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dbaf4-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dbaf4-298">(21)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-299">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-299">System failure.</span></span> <span data-ttu-id="dbaf4-300">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dbaf4-301">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dbaf4-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dbaf4-303">(22)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-304">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dbaf4-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dbaf4-306">(23)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-307">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-307">System failure.</span></span> <span data-ttu-id="dbaf4-308">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dbaf4-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dbaf4-310">(24)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-311">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dbaf4-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dbaf4-313">(25)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-314">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dbaf4-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dbaf4-316">(26)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-317">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dbaf4-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dbaf4-319">(27)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-320">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dbaf4-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dbaf4-322">(28)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-323">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dbaf4-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dbaf4-325">(29)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-326">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-326">Device is disabled.</span></span> <span data-ttu-id="dbaf4-327">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dbaf4-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dbaf4-329">(30)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-330">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dbaf4-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dbaf4-332">31,5</span><span class="sxs-lookup"><span data-stu-id="dbaf4-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-333">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-333">Device is not working properly.</span></span> <span data-ttu-id="dbaf4-334">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-335">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-336">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbaf4-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-338">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-339">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dbaf4-340">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-341">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-342">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbaf4-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-344">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. Physisches DMTF- \| Speicher Array \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-345">**True** gibt an, dass der letzte Fehler korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="dbaf4-346">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-347">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-348">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-351">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-352">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dbaf4-353">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dbaf4-354">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-355">**Currentsram**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-356">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="dbaf4-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-358">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| Current SRAM Type")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-359">Array von Typen von statischem Random Access Memory (SRAM), die für den Cache Speicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="dbaf4-360">Dieser Wert stammt aus dem **aktuellen SRAM-Typmember** der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-361">**Sonstige** (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-362">**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="dbaf4-363">**Nicht Burst** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="dbaf4-364">**Burst** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="dbaf4-365">**Pipeline Burst** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="dbaf4-366">**Synchron** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="dbaf4-367">**Asynchron** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-368">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-369">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-371">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-372">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-372">Description of the object.</span></span>

<span data-ttu-id="dbaf4-373">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-374">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-375">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-377">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-378">Eindeutiger Bezeichner des Caches, der durch eine Instanz von **Win32 \_ CacheMemory** dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="dbaf4-379">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dbaf4-380">Beispiel: "Cache Speicher 1"</span><span class="sxs-lookup"><span data-stu-id="dbaf4-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-381">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-382">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-384">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,4 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-385">Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="dbaf4-386">Die Endadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="dbaf4-387">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="dbaf4-388">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-389">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-390">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-392">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,15 "," MIF. Physisches DMTF- \| Speicher Array \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-393">Speicherzugriffs Vorgang, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="dbaf4-394">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="dbaf4-395">Wenn **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-396">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-397">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-398">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="dbaf4-399">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="dbaf4-400">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="dbaf4-401">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-402">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-403">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-405">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,19 "," MIF. DMTF- \| Speichergerät \| 002,20 "," MIF. Physisches DMTF- \| Speicher Array \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-406">Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-406">Address of the last memory error.</span></span> <span data-ttu-id="dbaf4-407">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="dbaf4-408">Wenn **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-409">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="dbaf4-410">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-411">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-412">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbaf4-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-414">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="dbaf4-415">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-416">**ErrorCorrectType**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-417">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-419">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| Error Correction Type")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-420">Fehlerkorrektur Methode, die vom Cache Speicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="dbaf4-421">Dieser Wert stammt aus dem **Fehlerkorrektur-Typmember** der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="dbaf4-422">**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-423">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-424">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="dbaf4-425">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="dbaf4-426">**Parität** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="dbaf4-427">**Single-Bit ECC** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="dbaf4-428">**Multi-Bit ECC** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-429">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-430">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="dbaf4-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-432">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,17 "," MIF. DMTF \| physikalisches Speicher Array \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-433">Ein Array von Daten, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="dbaf4-434">Die Daten belegen die ersten *n* Oktette des Arrays, die die Anzahl der Bits enthalten muss, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="dbaf4-435">Wenn **ErrorTransferSize** gleich 0 (null) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-436">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-437">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-438">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-440">Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="dbaf4-441">Wenn **ErrorTransferSize** gleich 0 (null) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-442">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-443">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="dbaf4-444">**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="dbaf4-445">**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-447">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-449">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. getroffenen Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="dbaf4-450">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-452">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-454">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. DMTF \| physikalisches Speicher Array \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**Othererrordescription**")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-455">Der Typ des Fehlers, der zuletzt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="dbaf4-456">Die Werte 12-14 sind im CIM-Schema nicht definiert, da Sie in DMI die Semantik des Fehler Typs mischen und angeben können, ob Sie korrigiert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="dbaf4-457">Letzteres wird in der Eigenschaft " **correctableerror**" angegeben.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="dbaf4-458">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-459">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-460">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dbaf4-461">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="dbaf4-462">Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="dbaf4-463">**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="dbaf4-464">**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="dbaf4-465">**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="dbaf4-466">**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="dbaf4-467">**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="dbaf4-468">**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="dbaf4-469">**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="dbaf4-470">Nicht **definiert** (12)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="dbaf4-471">Nicht **definiert** (13)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="dbaf4-472">Nicht **definiert** (14)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-473">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-476">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-477">Details über die Parität oder CRC-Algorithmen, ECC oder andere Mechanismen, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="dbaf4-478">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-479">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-480">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-482">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,21 "," MIF. DMTF \| physikalisches Speicher Array \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-483">Bereich in Bytes, in den der letzte Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="dbaf4-484">Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden (d. h. auf einer typischen Seite), können Fehler in 4-KB-Grenzen aufgelöst werden, und diese Eigenschaft wird auf 4000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="dbaf4-485">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-486">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="dbaf4-487">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-489">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-490">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-491">Zeitpunkt, zu dem der letzte Speicherfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="dbaf4-492">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="dbaf4-493">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-494">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-495">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-496">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-497">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-498">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,16 "," MIF. DMTF \| physikalisches Speicher Array \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-499">Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="dbaf4-500">0 (null) gibt an, dass kein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="dbaf4-501">Wenn die **errorInfo** -Eigenschaft gleich 3 (OK) ist, sollte diese Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="dbaf4-502">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-503">**Flushtimer**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-504">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-505">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-506">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,14 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Sekunden ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-507">Maximale Zeitspanne (in Sekunden), die geänderte Zeilen oder Bucket im Cache verbleiben können, bevor Sie geleert werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="dbaf4-508">Der Wert 0 (null) gibt an, dass eine Cache Leerung nicht von einem leeren Timer gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="dbaf4-509">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-511">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-512">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-513">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-514">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-514">Date and time the object was installed.</span></span> <span data-ttu-id="dbaf4-515">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dbaf4-516">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-517">**Installedsize**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-518">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-520">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| installierte Größe"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-521">Die aktuelle Größe des installierten Cache Speichers.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="dbaf4-522">Dieser Wert stammt aus dem **installierten size** -Element der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-523">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-524">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-525">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-526">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dbaf4-527">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-528">**Level**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-529">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-530">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-531">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-532">Cache Ebene.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-532">Level of the cache.</span></span>

<span data-ttu-id="dbaf4-533">Dieser Wert stammt aus dem **Cache Konfigurations** Mitglied der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="dbaf4-534">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="dbaf4-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primär** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="dbaf4-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Sekundär** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="dbaf4-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiär** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dbaf4-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-541">**Linesize**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-542">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-543">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-544">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-545">Größe (in Bytes) eines einzelnen cachebucket oder einer einzelnen Zeile.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="dbaf4-546">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-547">**Location**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-548">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-549">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-550">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 7- \| Speicherort")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-551">Physischer Speicherort des Cache Speichers.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="dbaf4-552">Dieser Wert stammt aus dem **Cache Konfigurations** Mitglied der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="dbaf4-553">**Intern** (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="dbaf4-554">**Extern** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="dbaf4-555">**Reserviert** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-556">**Unbekannt** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-557">**MaxCacheSize**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-558">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-559">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-560">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 7 \| maximale Cache Größe"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-561">Maximale Cache Größe, die für diesen bestimmten Cache Speicher installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="dbaf4-562">Dieser Wert stammt aus dem **maximalen Cache Größen** Element der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-563">**Name**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-564">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-565">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-566">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-567">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-567">Label by which the object is known.</span></span> <span data-ttu-id="dbaf4-568">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="dbaf4-569">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-571">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-572">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-573">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-574">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="dbaf4-575">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="dbaf4-576">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="dbaf4-577">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="dbaf4-578">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-579">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-580">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-581">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-582">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-583">Frei Form Zeichenfolge, die weitere Informationen bereitstellt, wenn die **ErrorType** -Eigenschaft auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="dbaf4-584">Andernfalls hat diese Zeichenfolge keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="dbaf4-585">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-587">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-588">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-589">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-590">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="dbaf4-591">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dbaf4-592">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dbaf4-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-593">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-594">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="dbaf4-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-595">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-596">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dbaf4-597">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dbaf4-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dbaf4-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dbaf4-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-602">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dbaf4-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-604">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dbaf4-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-606">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dbaf4-607">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dbaf4-608">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dbaf4-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-610">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dbaf4-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dbaf4-612">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-612">Timed Power-On Supported</span></span>

<span data-ttu-id="dbaf4-613">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-614">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-615">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbaf4-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-616">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-617">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="dbaf4-618">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="dbaf4-619">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-620">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-621">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-622">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-623">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="dbaf4-624">Dieser Wert stammt aus dem **socketbenennungs** -Member der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="dbaf4-625">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-626">**ReadPolicy**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-627">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-628">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-629">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-630">Richtlinie, die vom Cache für die Verarbeitung von Lese Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="dbaf4-631">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-632">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-633">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="dbaf4-634">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="dbaf4-635">**Read-Ahead** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="dbaf4-636">**Read und Read-Ahead** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="dbaf4-637">**Bestimmung pro e/** a (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-638">**Replacementpolicy**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-639">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-640">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-641">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-642">Algorithmus, um zu bestimmen, welche Cache Zeilen oder-Bucket wieder verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="dbaf4-643">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-644">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-645">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="dbaf4-646">**Zuletzt verwendet (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="dbaf4-647">**First in First Out (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="dbaf4-648">**Last in First Out (LIFO)** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="dbaf4-649">**Am wenigsten häufig verwendet (LfU)** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="dbaf4-650">**Am häufigsten verwendet (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="dbaf4-651">**Daten abhängige mehrere Algorithmen** (8)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-652">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-653">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-654">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-655">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,3 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-656">Anfangsadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="dbaf4-657">Die Startadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="dbaf4-658">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="dbaf4-659">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-660">**Status**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-661">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-662">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-663">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-664">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-664">Current status of the object.</span></span> <span data-ttu-id="dbaf4-665">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dbaf4-666">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="dbaf4-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dbaf4-667">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="dbaf4-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dbaf4-668">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dbaf4-669">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dbaf4-670">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dbaf4-671">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="dbaf4-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dbaf4-672">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dbaf4-673">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dbaf4-674">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-675">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dbaf4-676">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dbaf4-677">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dbaf4-678">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dbaf4-679">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dbaf4-680">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dbaf4-681">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dbaf4-682">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dbaf4-683">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-685">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-686">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-687">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-688">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-688">State of the logical device.</span></span> <span data-ttu-id="dbaf4-689">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dbaf4-690">Dieser Wert stammt aus dem **Cache Konfigurations** Mitglied der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="dbaf4-691">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-692">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-693">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dbaf4-694">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dbaf4-695">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dbaf4-696">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-697">**SupportedSRAM**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-698">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="dbaf4-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-699">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-700">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| Supported SRAM Type")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-701">Array unterstützter Typen von statischem Random Access Memory (SRAM), der für den Cache Speicher verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="dbaf4-702">Dieser Wert stammt aus dem **unterstützten SRAM-Typmember** der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-703">**Sonstige** (0)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-704">**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="dbaf4-705">**Nicht Burst** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="dbaf4-706">**Burst** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="dbaf4-707">**Pipeline Burst** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="dbaf4-708">**Synchron** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="dbaf4-709">**Asynchron** (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbaf4-710">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-711">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-712">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-713">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-714">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="dbaf4-715">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-716">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-717">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbaf4-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-718">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-719">**True** gibt an, dass die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene sind.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="dbaf4-720">**False** gibt an, dass es sich um eine physische Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="dbaf4-721">Wenn die Eigenschaft **errorInfo** gleich 3 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="dbaf4-722">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-723">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-724">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-725">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-726">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-727">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-727">Name of the scoping system.</span></span>

<span data-ttu-id="dbaf4-728">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbaf4-729">**"Write Policy"**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbaf4-730">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-731">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbaf4-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbaf4-732">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Cache \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="dbaf4-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="dbaf4-733">Richtlinien Definition schreiben.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-733">Write policy definition.</span></span>

<span data-ttu-id="dbaf4-734">Dieser Wert stammt aus dem **Cache Konfigurations** Mitglied der **Cache Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="dbaf4-735">Diese Eigenschaft wird von [**CIM \_ CacheMemory**](cim-cachememory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbaf4-736">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbaf4-737">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="dbaf4-738">**Zurückschreiben** (3)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="dbaf4-739">**Schreiben durch** (4)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="dbaf4-740">**Variiert mit der Adresse** (5)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="dbaf4-741">**Bestimmung pro e/** a (6)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="dbaf4-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dbaf4-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dbaf4-743">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbaf4-743">Remarks</span></span>

<span data-ttu-id="dbaf4-744">Die **Win32- \_ CacheMemory** -Klasse wird von [**CIM \_ CacheMemory**](cim-cachememory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dbaf4-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbaf4-745">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbaf4-745">Requirements</span></span>



| <span data-ttu-id="dbaf4-746">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbaf4-746">Requirement</span></span> | <span data-ttu-id="dbaf4-747">Wert</span><span class="sxs-lookup"><span data-stu-id="dbaf4-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbaf4-748">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-748">Minimum supported client</span></span><br/> | <span data-ttu-id="dbaf4-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbaf4-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbaf4-750">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbaf4-750">Minimum supported server</span></span><br/> | <span data-ttu-id="dbaf4-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbaf4-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbaf4-752">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbaf4-752">Namespace</span></span><br/>                | <span data-ttu-id="dbaf4-753">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbaf4-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbaf4-754">MOF</span><span class="sxs-lookup"><span data-stu-id="dbaf4-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbaf4-755"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dbaf4-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbaf4-756">DLL</span><span class="sxs-lookup"><span data-stu-id="dbaf4-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbaf4-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbaf4-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbaf4-758">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbaf4-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbaf4-759">**CIM- \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="dbaf4-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="dbaf4-760">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="dbaf4-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

