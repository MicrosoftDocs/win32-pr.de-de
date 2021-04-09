---
description: Die CIM \_ VolatileStorage-Klasse stellt die Funktionen und die Verwaltung von flüchtigem Speicher dar.
ms.assetid: c2f7e11e-d7e4-4709-be55-1c94a0b14010
ms.tgt_platform: multiple
title: CIM_VolatileStorage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage
- CIM_VolatileStorage.Access
- CIM_VolatileStorage.AdditionalErrorData
- CIM_VolatileStorage.Availability
- CIM_VolatileStorage.BlockSize
- CIM_VolatileStorage.Cacheable
- CIM_VolatileStorage.CacheType
- CIM_VolatileStorage.Caption
- CIM_VolatileStorage.ConfigManagerErrorCode
- CIM_VolatileStorage.ConfigManagerUserConfig
- CIM_VolatileStorage.CorrectableError
- CIM_VolatileStorage.CreationClassName
- CIM_VolatileStorage.Description
- CIM_VolatileStorage.DeviceID
- CIM_VolatileStorage.EndingAddress
- CIM_VolatileStorage.ErrorAccess
- CIM_VolatileStorage.ErrorAddress
- CIM_VolatileStorage.ErrorCleared
- CIM_VolatileStorage.ErrorData
- CIM_VolatileStorage.ErrorDataOrder
- CIM_VolatileStorage.ErrorDescription
- CIM_VolatileStorage.ErrorInfo
- CIM_VolatileStorage.ErrorMethodology
- CIM_VolatileStorage.ErrorResolution
- CIM_VolatileStorage.ErrorTime
- CIM_VolatileStorage.ErrorTransferSize
- CIM_VolatileStorage.InstallDate
- CIM_VolatileStorage.LastErrorCode
- CIM_VolatileStorage.Name
- CIM_VolatileStorage.NumberOfBlocks
- CIM_VolatileStorage.OtherErrorDescription
- CIM_VolatileStorage.PNPDeviceID
- CIM_VolatileStorage.PowerManagementCapabilities
- CIM_VolatileStorage.PowerManagementSupported
- CIM_VolatileStorage.Purpose
- CIM_VolatileStorage.StartingAddress
- CIM_VolatileStorage.Status
- CIM_VolatileStorage.StatusInfo
- CIM_VolatileStorage.SystemCreationClassName
- CIM_VolatileStorage.SystemLevelAddress
- CIM_VolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99add7401d92d82385a4182e466de8b28ad4fc09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860736"
---
# <a name="cim_volatilestorage-class"></a><span data-ttu-id="773ed-103">CIM- \_ VolatileStorage-Klasse</span><span class="sxs-lookup"><span data-stu-id="773ed-103">CIM\_VolatileStorage class</span></span>

<span data-ttu-id="773ed-104">Die **CIM \_ VolatileStorage** -Klasse stellt die Funktionen und die Verwaltung von flüchtigem Speicher dar.</span><span class="sxs-lookup"><span data-stu-id="773ed-104">The **CIM\_VolatileStorage** class represents the capabilities and management of volatile storage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="773ed-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="773ed-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="773ed-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="773ed-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="773ed-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="773ed-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="773ed-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="773ed-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="773ed-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36851DFE-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_VolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  boolean  Cacheable;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="773ed-110">Member</span><span class="sxs-lookup"><span data-stu-id="773ed-110">Members</span></span>

<span data-ttu-id="773ed-111">Die **CIM- \_ VolatileStorage** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="773ed-111">The **CIM\_VolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="773ed-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="773ed-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="773ed-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="773ed-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="773ed-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="773ed-114">Methods</span></span>

<span data-ttu-id="773ed-115">Die **CIM \_ VolatileStorage** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="773ed-115">The **CIM\_VolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="773ed-116">Methode</span><span class="sxs-lookup"><span data-stu-id="773ed-116">Method</span></span>                                                                     | <span data-ttu-id="773ed-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="773ed-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="773ed-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="773ed-118">**Reset**</span></span>](reset-method-in-class-cim-volatilestorage.md)                 | <span data-ttu-id="773ed-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="773ed-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="773ed-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="773ed-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="773ed-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="773ed-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volatilestorage.md) | <span data-ttu-id="773ed-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="773ed-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="773ed-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="773ed-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="773ed-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="773ed-124">Properties</span></span>

<span data-ttu-id="773ed-125">Die **CIM \_ VolatileStorage** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="773ed-125">The **CIM\_VolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="773ed-126">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="773ed-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="773ed-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-129">Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="773ed-129">Read/write properties of the media.</span></span>

<span data-ttu-id="773ed-130">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-131">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="773ed-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="773ed-132">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="773ed-133">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="773ed-134">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="773ed-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="773ed-135">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="773ed-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="773ed-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-137">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="773ed-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="773ed-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,18 "," MIF. DMTF \| physikalisches Speicher Array \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="773ed-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="773ed-140">Zusätzliche Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="773ed-140">Additional error information.</span></span> <span data-ttu-id="773ed-141">Ein Beispiel hierfür ist die Fehlerüberprüfung und Korrektur (ECC) oder die Rückgabe der Prüfbits, wenn eine CRC-basierte Fehler Methodik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="773ed-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="773ed-142">Wenn in letzterem Fall ein Single-Bit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, kann das genaue Bit, das fehlgeschlagen ist, bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="773ed-143">Diese Art von Daten (ECC-Syndrom, Check-Bit-oder Paritäts Bitdaten oder andere vom Hersteller bereitgestellte Informationen) ist in diesem Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="773ed-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="773ed-144">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="773ed-145">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-145">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-146">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="773ed-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-147">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="773ed-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-149">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="773ed-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-150">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="773ed-150">Availability and status of the device.</span></span>

<span data-ttu-id="773ed-151">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="773ed-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="773ed-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="773ed-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-155">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="773ed-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="773ed-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="773ed-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="773ed-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="773ed-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="773ed-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="773ed-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="773ed-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="773ed-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="773ed-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="773ed-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="773ed-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="773ed-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="773ed-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="773ed-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="773ed-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="773ed-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="773ed-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="773ed-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="773ed-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="773ed-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-166">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="773ed-166">The device is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="773ed-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="773ed-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-168">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="773ed-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="773ed-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="773ed-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-170">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="773ed-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="773ed-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="773ed-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="773ed-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-173">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="773ed-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="773ed-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="773ed-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-175">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="773ed-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="773ed-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="773ed-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-177">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="773ed-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="773ed-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="773ed-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-179">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="773ed-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="773ed-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="773ed-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-181">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="773ed-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="773ed-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-183">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="773ed-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-185">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="773ed-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-186">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="773ed-186">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="773ed-187">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-187">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="773ed-188">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="773ed-188">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="773ed-189">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="773ed-190">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="773ed-190">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-191">**Zwischenspeicherbar**</span><span class="sxs-lookup"><span data-stu-id="773ed-191">**Cacheable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-192">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="773ed-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-194">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressourcen Speicher Info \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="773ed-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-195">Wenn der Wert **true** ist, kann dieser Arbeitsspeicher zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-195">If **TRUE**, this memory can be cached.</span></span>

</dd> <dt>

<span data-ttu-id="773ed-196">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="773ed-196">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-197">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="773ed-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-199">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressourcen Speicher Info \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="773ed-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-200">Der Cachetyp, der mit dem Arbeitsspeicher kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-200">Cache type that is compatible with the memory.</span></span> <span data-ttu-id="773ed-201">Wenn die **cachable** -Eigenschaft auf **false** festgelegt ist, hat diese Eigenschaft keine Bedeutung und sollte auf 4 ("nicht zutreffend") festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-201">If the **Cacheable** property is set to **FALSE**, then this property does not have meaning and should be set to 4 ("Not Applicable").</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="773ed-202">**Sonstige** (0)</span><span class="sxs-lookup"><span data-stu-id="773ed-202">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-203">**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-203">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Back"></span><span id="write-back"></span><span id="WRITE-BACK"></span>

<span data-ttu-id="773ed-204">**Zurückschreiben** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-204">**Write-Back** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Through"></span><span id="write-through"></span><span id="WRITE-THROUGH"></span>

<span data-ttu-id="773ed-205">**Write-Through** (3)</span><span class="sxs-lookup"><span data-stu-id="773ed-205">**Write-Through** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="773ed-206">**Nicht zutreffend** (4)</span><span class="sxs-lookup"><span data-stu-id="773ed-206">**Not Applicable** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="773ed-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-210">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="773ed-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-211">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="773ed-211">Short textual description of the object.</span></span>

<span data-ttu-id="773ed-212">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-213">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="773ed-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-214">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="773ed-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-216">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="773ed-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-217">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="773ed-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="773ed-218">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="773ed-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="773ed-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="773ed-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="773ed-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-221">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="773ed-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="773ed-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="773ed-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="773ed-223">(1)</span><span class="sxs-lookup"><span data-stu-id="773ed-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-224">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="773ed-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="773ed-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="773ed-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="773ed-226">(2)</span><span class="sxs-lookup"><span data-stu-id="773ed-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="773ed-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="773ed-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="773ed-228">(3)</span><span class="sxs-lookup"><span data-stu-id="773ed-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-229">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="773ed-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="773ed-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="773ed-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="773ed-231">(4)</span><span class="sxs-lookup"><span data-stu-id="773ed-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-232">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="773ed-232">Device is not working properly.</span></span> <span data-ttu-id="773ed-233">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="773ed-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="773ed-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="773ed-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="773ed-235">(5)</span><span class="sxs-lookup"><span data-stu-id="773ed-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-236">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="773ed-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="773ed-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="773ed-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="773ed-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="773ed-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-239">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="773ed-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="773ed-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="773ed-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="773ed-241">(7)</span><span class="sxs-lookup"><span data-stu-id="773ed-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="773ed-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="773ed-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="773ed-243">(8)</span><span class="sxs-lookup"><span data-stu-id="773ed-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-244">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="773ed-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="773ed-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="773ed-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="773ed-246">(9)</span><span class="sxs-lookup"><span data-stu-id="773ed-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-247">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="773ed-247">Device is not working properly.</span></span> <span data-ttu-id="773ed-248">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="773ed-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="773ed-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="773ed-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="773ed-250">(10)</span><span class="sxs-lookup"><span data-stu-id="773ed-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-251">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="773ed-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="773ed-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="773ed-253">(11)</span><span class="sxs-lookup"><span data-stu-id="773ed-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-254">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="773ed-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="773ed-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="773ed-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="773ed-256">(12)</span><span class="sxs-lookup"><span data-stu-id="773ed-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-257">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="773ed-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="773ed-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="773ed-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="773ed-259">(13)</span><span class="sxs-lookup"><span data-stu-id="773ed-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-260">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="773ed-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="773ed-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="773ed-262">(14)</span><span class="sxs-lookup"><span data-stu-id="773ed-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-263">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="773ed-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="773ed-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="773ed-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="773ed-265">(15)</span><span class="sxs-lookup"><span data-stu-id="773ed-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-266">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="773ed-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="773ed-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="773ed-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="773ed-268">(16)</span><span class="sxs-lookup"><span data-stu-id="773ed-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-269">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="773ed-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="773ed-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="773ed-271">(17)</span><span class="sxs-lookup"><span data-stu-id="773ed-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-272">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="773ed-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="773ed-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="773ed-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="773ed-274">(18)</span><span class="sxs-lookup"><span data-stu-id="773ed-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-275">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="773ed-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="773ed-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="773ed-277">(19)</span><span class="sxs-lookup"><span data-stu-id="773ed-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="773ed-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="773ed-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="773ed-279">(20)</span><span class="sxs-lookup"><span data-stu-id="773ed-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-280">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="773ed-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="773ed-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="773ed-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="773ed-282">(21)</span><span class="sxs-lookup"><span data-stu-id="773ed-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-283">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="773ed-283">System failure.</span></span> <span data-ttu-id="773ed-284">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="773ed-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="773ed-285">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="773ed-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="773ed-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="773ed-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="773ed-287">(22)</span><span class="sxs-lookup"><span data-stu-id="773ed-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-288">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="773ed-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="773ed-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="773ed-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="773ed-290">(23)</span><span class="sxs-lookup"><span data-stu-id="773ed-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-291">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="773ed-291">System failure.</span></span> <span data-ttu-id="773ed-292">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="773ed-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="773ed-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="773ed-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="773ed-294">(24)</span><span class="sxs-lookup"><span data-stu-id="773ed-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-295">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="773ed-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="773ed-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="773ed-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="773ed-297">(25)</span><span class="sxs-lookup"><span data-stu-id="773ed-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-298">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="773ed-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="773ed-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="773ed-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="773ed-300">(26)</span><span class="sxs-lookup"><span data-stu-id="773ed-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-301">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="773ed-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="773ed-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="773ed-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="773ed-303">(27)</span><span class="sxs-lookup"><span data-stu-id="773ed-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-304">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="773ed-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="773ed-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="773ed-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="773ed-306">(28)</span><span class="sxs-lookup"><span data-stu-id="773ed-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-307">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="773ed-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="773ed-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="773ed-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="773ed-309">(29)</span><span class="sxs-lookup"><span data-stu-id="773ed-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-310">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="773ed-310">Device is disabled.</span></span> <span data-ttu-id="773ed-311">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="773ed-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="773ed-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="773ed-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="773ed-313">(30)</span><span class="sxs-lookup"><span data-stu-id="773ed-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-314">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="773ed-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="773ed-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="773ed-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="773ed-316">31,5</span><span class="sxs-lookup"><span data-stu-id="773ed-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-317">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="773ed-317">Device is not working properly.</span></span> <span data-ttu-id="773ed-318">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-319">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="773ed-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-320">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="773ed-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-322">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="773ed-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-323">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="773ed-323">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="773ed-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-325">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="773ed-325">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-326">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="773ed-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-328">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. Physisches DMTF- \| Speicher Array \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="773ed-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-329">**True** gibt an, dass der letzte Fehler korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="773ed-329">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="773ed-330">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-330">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="773ed-331">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-331">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-332">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="773ed-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-335">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="773ed-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="773ed-336">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="773ed-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="773ed-337">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="773ed-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-339">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="773ed-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-342">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="773ed-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-343">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="773ed-343">Textual description of the object.</span></span>

<span data-ttu-id="773ed-344">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="773ed-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-348">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="773ed-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="773ed-349">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="773ed-349">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="773ed-350">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-351">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="773ed-351">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-352">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="773ed-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-354">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,4 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="773ed-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-355">Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für das Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-355">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="773ed-356">Die Endadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="773ed-356">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="773ed-357">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-357">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="773ed-358">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="773ed-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-359">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="773ed-359">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-360">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="773ed-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-362">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,15 "," MIF. Physisches DMTF- \| Speicher Array \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="773ed-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-363">Speicherzugriffs Vorgang, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="773ed-363">Memory access operation that caused the last error.</span></span> <span data-ttu-id="773ed-364">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="773ed-364">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="773ed-365">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-365">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="773ed-366">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-366">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="773ed-367">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-367">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-368">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-368">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="773ed-369">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="773ed-369">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="773ed-370">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="773ed-370">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="773ed-371">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="773ed-371">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-372">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="773ed-372">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-373">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="773ed-373">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-375">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,19 "," MIF. DMTF- \| Speichergerät \| 002,20 "," MIF. Physisches DMTF- \| Speicher Array \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="773ed-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-376">Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="773ed-376">Address of the last memory error.</span></span> <span data-ttu-id="773ed-377">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="773ed-377">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="773ed-378">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-378">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="773ed-379">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-379">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="773ed-380">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="773ed-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-381">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="773ed-381">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-382">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="773ed-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-384">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="773ed-384">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="773ed-385">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-386">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="773ed-386">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-387">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="773ed-387">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="773ed-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-389">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,17 "," MIF. DMTF \| physikalisches Speicher Array \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="773ed-389">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="773ed-390">Daten, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="773ed-390">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="773ed-391">Die Daten belegen die ersten *n* Oktette des Arrays, die die Anzahl der Bits enthalten muss, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-391">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="773ed-392">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-392">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="773ed-393">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-394">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="773ed-394">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-395">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="773ed-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-397">Reihenfolge der im **ErrorData** -Array gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="773ed-397">Ordering for data stored in the **ErrorData** array.</span></span> <span data-ttu-id="773ed-398">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-398">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="773ed-399">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="773ed-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-401">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="773ed-401">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="773ed-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-403">Das am wenigsten signifikante Byte zuerst.</span><span class="sxs-lookup"><span data-stu-id="773ed-403">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="773ed-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-405">Das wichtigste Byte zuerst.</span><span class="sxs-lookup"><span data-stu-id="773ed-405">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-406">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="773ed-406">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-407">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-409">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="773ed-409">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="773ed-410">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-411">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="773ed-411">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-412">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="773ed-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-414">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. DMTF \| physikalisches Speicher Array \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**Othererrordescription**")</span><span class="sxs-lookup"><span data-stu-id="773ed-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-415">Der Typ des Fehlers, der zuletzt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-415">Type of error that occurred most recently.</span></span> <span data-ttu-id="773ed-416">Die Werte 12-14 sind im CIM-Schema nicht definiert, da die Semantik des Fehler Typs und der Fehler, der korrigiert werden konnte, in DMI gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-416">The values 12-14 are undefined in the CIM schema since the semantics of the type of error and whether or not it was correctable are mixed in DMI.</span></span> <span data-ttu-id="773ed-417">Die Eigenschaft " **correctableerror** " gibt an, ob Sie korrigiert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="773ed-417">The **CorrectableError** property indicates whether it was correctable.</span></span>

<span data-ttu-id="773ed-418">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-418">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="773ed-419">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-419">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-420">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-420">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="773ed-421">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="773ed-421">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="773ed-422">Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="773ed-422">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="773ed-423">**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="773ed-423">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="773ed-424">**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="773ed-424">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="773ed-425">**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="773ed-425">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="773ed-426">**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="773ed-426">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="773ed-427">**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="773ed-427">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="773ed-428">**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="773ed-428">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="773ed-429">**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="773ed-429">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="773ed-430">Nicht **definiert** (12)</span><span class="sxs-lookup"><span data-stu-id="773ed-430">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="773ed-431">Nicht **definiert** (13)</span><span class="sxs-lookup"><span data-stu-id="773ed-431">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="773ed-432">Nicht **definiert** (14)</span><span class="sxs-lookup"><span data-stu-id="773ed-432">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-433">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="773ed-433">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-436">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="773ed-436">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-437">Eine frei Form Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, der vom Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="773ed-437">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="773ed-438">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-438">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-439">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="773ed-439">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-440">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="773ed-440">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-442">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,21 "," MIF. DMTF \| physikalisches Speicher Array \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="773ed-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-443">Bereich in Bytes, in den der letzte Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="773ed-443">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="773ed-444">Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden (d. h. auf einer typischen Seite), können Fehler in 4-KB-Grenzen aufgelöst werden, und diese Eigenschaft wird auf 4000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="773ed-444">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="773ed-445">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-445">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="773ed-446">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-446">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="773ed-447">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="773ed-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-448">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="773ed-448">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-449">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="773ed-449">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-451">Zeitpunkt, zu dem der letzte Speicherfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-451">Time that the last memory error occurred.</span></span> <span data-ttu-id="773ed-452">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="773ed-452">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="773ed-453">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-453">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="773ed-454">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-454">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-455">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="773ed-455">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-456">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="773ed-456">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-458">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,16 "," MIF. DMTF \| physikalisches Speicher Array \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="773ed-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-459">Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="773ed-459">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="773ed-460">0 gibt keinen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="773ed-460">0 indicates no error.</span></span> <span data-ttu-id="773ed-461">Wenn die **errorInfo** -Eigenschaft gleich 3, "OK" ist, sollte diese Eigenschaft auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-461">If the **ErrorInfo** property is equal to 3, "OK", then this property should be set to 0.</span></span>

<span data-ttu-id="773ed-462">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-462">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-463">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="773ed-463">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-464">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="773ed-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-466">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="773ed-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-467">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="773ed-467">Date and time the object was installed.</span></span> <span data-ttu-id="773ed-468">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-468">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="773ed-469">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-469">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="773ed-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-471">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="773ed-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-473">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="773ed-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="773ed-474">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-475">**Name**</span><span class="sxs-lookup"><span data-stu-id="773ed-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-476">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-478">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="773ed-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-479">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-479">Label by which the object is known.</span></span> <span data-ttu-id="773ed-480">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="773ed-481">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="773ed-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-483">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="773ed-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-484">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-485">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="773ed-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-486">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="773ed-486">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="773ed-487">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="773ed-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="773ed-488">Wenn der Wert von **BLOCKSIZE** 1 (eins) ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="773ed-488">If the value of **BlockSize** is 1 (one), then this property is the total size of the storage extent.</span></span>

<span data-ttu-id="773ed-489">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="773ed-490">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="773ed-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-491">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="773ed-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-492">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-493">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-494">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="773ed-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-495">Eine frei Form Zeichenfolge, die zusätzliche Informationen bereitstellt, wenn die **ErrorType** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-495">Free-form string that provides additional information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="773ed-496">Wenn ein anderer Wert als 1 (eins) ist, hat diese Zeichenfolge keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-496">If a value other than 1 (one), this string has no meaning.</span></span>

<span data-ttu-id="773ed-497">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="773ed-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-499">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-501">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="773ed-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-502">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="773ed-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="773ed-503">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="773ed-504">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="773ed-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="773ed-505">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="773ed-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-506">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="773ed-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="773ed-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-508">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="773ed-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="773ed-509">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="773ed-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="773ed-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="773ed-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="773ed-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="773ed-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-514">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="773ed-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="773ed-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="773ed-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-516">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="773ed-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="773ed-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="773ed-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-518">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="773ed-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="773ed-519">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="773ed-520">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="773ed-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="773ed-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="773ed-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-522">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="773ed-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="773ed-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="773ed-524">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="773ed-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-525">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="773ed-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-526">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="773ed-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-527">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-528">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="773ed-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="773ed-529">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="773ed-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="773ed-530">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="773ed-531">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="773ed-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="773ed-532">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-533">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="773ed-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-534">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-535">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-536">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="773ed-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="773ed-537">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-538">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="773ed-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-539">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="773ed-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-540">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-541">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,3 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="773ed-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-542">Anfangsadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für das Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-542">Beginning address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="773ed-543">Die Startadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="773ed-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="773ed-544">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="773ed-545">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="773ed-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-546">**Status**</span><span class="sxs-lookup"><span data-stu-id="773ed-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-547">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-549">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="773ed-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-550">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="773ed-550">Current status of the object.</span></span> <span data-ttu-id="773ed-551">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="773ed-552">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="773ed-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="773ed-553">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="773ed-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="773ed-554">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="773ed-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="773ed-555">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="773ed-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-556">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="773ed-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="773ed-557">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="773ed-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="773ed-558">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="773ed-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="773ed-559">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="773ed-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="773ed-560">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="773ed-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="773ed-561">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="773ed-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="773ed-562">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="773ed-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="773ed-563">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="773ed-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="773ed-564">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="773ed-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="773ed-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-566">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="773ed-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-567">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-568">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="773ed-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="773ed-569">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="773ed-569">State of the logical device.</span></span> <span data-ttu-id="773ed-570">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="773ed-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="773ed-571">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="773ed-572">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="773ed-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="773ed-573">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="773ed-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="773ed-574">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="773ed-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="773ed-575">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="773ed-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="773ed-576">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="773ed-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="773ed-577">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="773ed-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-578">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-579">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-580">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="773ed-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="773ed-581">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="773ed-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="773ed-582">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="773ed-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-584">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="773ed-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-585">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="773ed-586">**True** gibt an, dass die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene sind. **false** gibt an, dass es sich um eine physische Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="773ed-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address; if **FALSE**, it is a physical address.</span></span> <span data-ttu-id="773ed-587">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="773ed-587">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="773ed-588">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-588">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="773ed-589">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="773ed-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="773ed-590">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="773ed-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="773ed-591">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="773ed-591">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="773ed-592">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="773ed-592">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="773ed-593">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="773ed-593">Scoping system's name.</span></span>

<span data-ttu-id="773ed-594">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="773ed-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="773ed-595">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="773ed-595">Remarks</span></span>

<span data-ttu-id="773ed-596">Die **CIM- \_ VolatileStorage** -Klasse wird vom [**CIM- \_ Speicher**](cim-memory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="773ed-596">The **CIM\_VolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="773ed-597">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="773ed-597">WMI does not implement this class.</span></span>

<span data-ttu-id="773ed-598">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="773ed-598">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="773ed-599">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="773ed-599">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="773ed-600">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="773ed-600">Requirements</span></span>



| <span data-ttu-id="773ed-601">Anforderung</span><span class="sxs-lookup"><span data-stu-id="773ed-601">Requirement</span></span> | <span data-ttu-id="773ed-602">Wert</span><span class="sxs-lookup"><span data-stu-id="773ed-602">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="773ed-603">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="773ed-603">Minimum supported client</span></span><br/> | <span data-ttu-id="773ed-604">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="773ed-604">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="773ed-605">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="773ed-605">Minimum supported server</span></span><br/> | <span data-ttu-id="773ed-606">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="773ed-606">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="773ed-607">Namespace</span><span class="sxs-lookup"><span data-stu-id="773ed-607">Namespace</span></span><br/>                | <span data-ttu-id="773ed-608">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="773ed-608">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="773ed-609">MOF</span><span class="sxs-lookup"><span data-stu-id="773ed-609">MOF</span></span><br/>                      | <dl> <span data-ttu-id="773ed-610"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="773ed-610"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="773ed-611">DLL</span><span class="sxs-lookup"><span data-stu-id="773ed-611">DLL</span></span><br/>                      | <dl> <span data-ttu-id="773ed-612"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="773ed-612"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="773ed-613">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="773ed-613">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773ed-614">**CIM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="773ed-614">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

