---
description: Die CIM \_ -Speicher Klasse stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.
ms.assetid: ddc72aad-5687-4bc1-b402-e27b27eca9be
ms.tgt_platform: multiple
title: CIM_Memory-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Caption
- CIM_Memory.Description
- CIM_Memory.InstallDate
- CIM_Memory.Name
- CIM_Memory.Status
- CIM_Memory.Availability
- CIM_Memory.ConfigManagerErrorCode
- CIM_Memory.ConfigManagerUserConfig
- CIM_Memory.CreationClassName
- CIM_Memory.DeviceID
- CIM_Memory.PowerManagementCapabilities
- CIM_Memory.ErrorCleared
- CIM_Memory.ErrorDescription
- CIM_Memory.LastErrorCode
- CIM_Memory.PNPDeviceID
- CIM_Memory.PowerManagementSupported
- CIM_Memory.StatusInfo
- CIM_Memory.SystemCreationClassName
- CIM_Memory.SystemName
- CIM_Memory.Access
- CIM_Memory.BlockSize
- CIM_Memory.NumberOfBlocks
- CIM_Memory.Purpose
- CIM_Memory.ErrorMethodology
- CIM_Memory.AdditionalErrorData
- CIM_Memory.CorrectableError
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorAddress
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorInfo
- CIM_Memory.ErrorResolution
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorTransferSize
- CIM_Memory.OtherErrorDescription
- CIM_Memory.StartingAddress
- CIM_Memory.SystemLevelAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35fbb8467337da1ceab044a42533a6ca8628cf63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127177"
---
# <a name="cim_memory-class-cimwin32-wmi-providers"></a><span data-ttu-id="c090a-103">CIM_Memory-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="c090a-103">CIM_Memory class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c090a-104">Die **CIM- \_ Speicher** Klasse stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.</span><span class="sxs-lookup"><span data-stu-id="c090a-104">The **CIM\_Memory** class represents the capabilities and management of memory-related logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c090a-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c090a-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c090a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c090a-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c090a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c090a-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c090a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c090a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c090a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B64-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
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
};
```

## <a name="members"></a><span data-ttu-id="c090a-110">Member</span><span class="sxs-lookup"><span data-stu-id="c090a-110">Members</span></span>

<span data-ttu-id="c090a-111">Die **CIM- \_ Speicher** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c090a-111">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="c090a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c090a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c090a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c090a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c090a-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="c090a-114">Methods</span></span>

<span data-ttu-id="c090a-115">Die **CIM- \_ Speicher** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c090a-115">The **CIM\_Memory** class has these methods.</span></span>



| <span data-ttu-id="c090a-116">Methode</span><span class="sxs-lookup"><span data-stu-id="c090a-116">Method</span></span>                                                            | <span data-ttu-id="c090a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c090a-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c090a-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="c090a-118">**Reset**</span></span>](reset-method-in-class-cim-memory.md)                 | <span data-ttu-id="c090a-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c090a-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="c090a-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c090a-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c090a-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c090a-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-memory.md) | <span data-ttu-id="c090a-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c090a-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c090a-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c090a-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c090a-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c090a-124">Properties</span></span>

<span data-ttu-id="c090a-125">Die **CIM- \_ Speicher** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c090a-125">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c090a-126">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="c090a-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c090a-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-129">Beschreibt die Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="c090a-129">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="c090a-130">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-131">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c090a-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="c090a-132">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="c090a-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="c090a-133">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="c090a-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="c090a-134">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="c090a-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="c090a-135">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="c090a-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="c090a-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-137">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="c090a-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c090a-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,18 "," MIF. DMTF \| physikalisches Speicher Array \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c090a-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c090a-140">Ein Array von Oktetten, die zusätzliche Fehlerinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c090a-140">Array of octets that hold additional error information.</span></span> <span data-ttu-id="c090a-141">Ein Beispiel hierfür ist die Fehlerüberprüfung und Korrektur (ECC) oder die Rückgabe der Prüfbits, wenn eine CRC-basierte Fehler Methodik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c090a-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="c090a-142">Wenn in letzterem Fall ein Single-Bit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, kann das genaue Bit, das fehlgeschlagen ist, bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="c090a-143">Diese Art von Daten (ECC-Syndrom, Check-Bit-oder Paritäts Bitdaten oder andere vom Hersteller bereitgestellte Informationen) ist in diesem Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="c090a-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="c090a-144">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-145">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c090a-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-146">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c090a-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="c090a-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-149">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c090a-149">Availability and status of the device.</span></span>

<span data-ttu-id="c090a-150">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c090a-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c090a-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c090a-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c090a-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="c090a-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c090a-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="c090a-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c090a-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="c090a-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c090a-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="c090a-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c090a-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="c090a-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c090a-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="c090a-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c090a-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="c090a-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c090a-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="c090a-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c090a-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="c090a-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c090a-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="c090a-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c090a-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="c090a-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-164">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c090a-164">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c090a-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="c090a-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-166">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c090a-166">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c090a-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="c090a-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-168">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-168">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c090a-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="c090a-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c090a-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="c090a-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-171">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="c090a-171">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c090a-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="c090a-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-173">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="c090a-173">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c090a-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="c090a-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-175">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="c090a-175">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c090a-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="c090a-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-177">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c090a-177">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c090a-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="c090a-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-179">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="c090a-179">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-180">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="c090a-180">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-181">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c090a-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-183">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="c090a-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-184">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="c090a-184">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="c090a-185">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-185">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="c090a-186">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="c090a-186">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="c090a-187">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c090a-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c090a-188">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-188">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c090a-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-192">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c090a-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-193">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c090a-193">A short textual description of the object.</span></span>

<span data-ttu-id="c090a-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-195">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="c090a-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-196">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c090a-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-198">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c090a-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-199">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c090a-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c090a-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c090a-201">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="c090a-201">**This device is working properly.**</span></span> <span data-ttu-id="c090a-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="c090a-202">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c090a-203">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="c090a-203">**This device is not configured correctly.**</span></span> <span data-ttu-id="c090a-204">(1)</span><span class="sxs-lookup"><span data-stu-id="c090a-204">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c090a-205">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="c090a-205">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c090a-206">(2)</span><span class="sxs-lookup"><span data-stu-id="c090a-206">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c090a-207">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="c090a-207">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c090a-208">(3)</span><span class="sxs-lookup"><span data-stu-id="c090a-208">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c090a-209">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c090a-209">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c090a-210">(4)</span><span class="sxs-lookup"><span data-stu-id="c090a-210">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c090a-211">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="c090a-211">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c090a-212">(5)</span><span class="sxs-lookup"><span data-stu-id="c090a-212">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c090a-213">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="c090a-213">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c090a-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="c090a-214">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c090a-215">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="c090a-215">**Cannot filter.**</span></span> <span data-ttu-id="c090a-216">(7)</span><span class="sxs-lookup"><span data-stu-id="c090a-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c090a-217">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="c090a-217">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c090a-218">(8)</span><span class="sxs-lookup"><span data-stu-id="c090a-218">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c090a-219">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="c090a-219">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c090a-220">(9)</span><span class="sxs-lookup"><span data-stu-id="c090a-220">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c090a-221">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="c090a-221">**This device cannot start.**</span></span> <span data-ttu-id="c090a-222">(10)</span><span class="sxs-lookup"><span data-stu-id="c090a-222">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c090a-223">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="c090a-223">**This device failed.**</span></span> <span data-ttu-id="c090a-224">(11)</span><span class="sxs-lookup"><span data-stu-id="c090a-224">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c090a-225">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="c090a-225">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c090a-226">(12)</span><span class="sxs-lookup"><span data-stu-id="c090a-226">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c090a-227">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="c090a-227">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c090a-228">(13)</span><span class="sxs-lookup"><span data-stu-id="c090a-228">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c090a-229">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="c090a-229">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c090a-230">(14)</span><span class="sxs-lookup"><span data-stu-id="c090a-230">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c090a-231">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="c090a-231">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c090a-232">(15)</span><span class="sxs-lookup"><span data-stu-id="c090a-232">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c090a-233">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="c090a-233">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c090a-234">(16)</span><span class="sxs-lookup"><span data-stu-id="c090a-234">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c090a-235">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="c090a-235">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c090a-236">(17)</span><span class="sxs-lookup"><span data-stu-id="c090a-236">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c090a-237">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="c090a-237">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c090a-238">(18)</span><span class="sxs-lookup"><span data-stu-id="c090a-238">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c090a-239">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="c090a-239">**Failure using the VxD loader.**</span></span> <span data-ttu-id="c090a-240">(19)</span><span class="sxs-lookup"><span data-stu-id="c090a-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c090a-241">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c090a-241">**Your registry might be corrupted.**</span></span> <span data-ttu-id="c090a-242">(20)</span><span class="sxs-lookup"><span data-stu-id="c090a-242">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c090a-243">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="c090a-243">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c090a-244">(21)</span><span class="sxs-lookup"><span data-stu-id="c090a-244">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c090a-245">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="c090a-245">**This device is disabled.**</span></span> <span data-ttu-id="c090a-246">(22)</span><span class="sxs-lookup"><span data-stu-id="c090a-246">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c090a-247">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="c090a-247">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c090a-248">(23)</span><span class="sxs-lookup"><span data-stu-id="c090a-248">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c090a-249">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="c090a-249">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c090a-250">(24)</span><span class="sxs-lookup"><span data-stu-id="c090a-250">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c090a-251">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c090a-251">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c090a-252">(25)</span><span class="sxs-lookup"><span data-stu-id="c090a-252">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c090a-253">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c090a-253">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c090a-254">(26)</span><span class="sxs-lookup"><span data-stu-id="c090a-254">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c090a-255">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c090a-255">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c090a-256">(27)</span><span class="sxs-lookup"><span data-stu-id="c090a-256">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c090a-257">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="c090a-257">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c090a-258">(28)</span><span class="sxs-lookup"><span data-stu-id="c090a-258">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c090a-259">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="c090a-259">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c090a-260">(29)</span><span class="sxs-lookup"><span data-stu-id="c090a-260">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c090a-261">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="c090a-261">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c090a-262">(30)</span><span class="sxs-lookup"><span data-stu-id="c090a-262">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c090a-263">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="c090a-263">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c090a-264">31,5</span><span class="sxs-lookup"><span data-stu-id="c090a-264">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-265">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="c090a-265">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-266">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c090a-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-268">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c090a-268">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-269">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="c090a-269">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c090a-270">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-271">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="c090a-271">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-272">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c090a-272">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-274">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. Physisches DMTF- \| Speicher Array \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="c090a-274">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-275">**True** gibt an, dass der letzte Fehler korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c090a-275">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="c090a-276">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-276">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-277">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c090a-277">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-280">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c090a-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c090a-281">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c090a-281">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c090a-282">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-282">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c090a-283">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-284">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c090a-284">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-287">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c090a-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-288">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c090a-288">A textual description of the object.</span></span>

<span data-ttu-id="c090a-289">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-289">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-290">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c090a-290">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-291">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-293">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c090a-293">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c090a-294">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="c090a-294">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c090a-295">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-296">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="c090a-296">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-297">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c090a-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-299">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,4 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="c090a-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-300">Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-300">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="c090a-301">Die Endadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="c090a-301">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="c090a-302">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c090a-302">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-303">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="c090a-303">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-304">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c090a-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-306">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,15 "," MIF. Physisches DMTF- \| Speicher Array \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="c090a-306">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-307">Speicherzugriffs Vorgang, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c090a-307">Memory access operation that caused the last error.</span></span> <span data-ttu-id="c090a-308">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c090a-308">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="c090a-309">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-309">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c090a-310">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c090a-310">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-311">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c090a-311">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="c090a-312">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="c090a-312">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="c090a-313">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="c090a-313">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="c090a-314">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="c090a-314">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-315">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="c090a-315">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-316">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c090a-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-318">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,19 "," MIF. DMTF- \| Speichergerät \| 002,20 "," MIF. Physisches DMTF- \| Speicher Array \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="c090a-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-319">Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="c090a-319">Address of the last memory error.</span></span> <span data-ttu-id="c090a-320">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c090a-320">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="c090a-321">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-321">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c090a-322">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c090a-322">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-323">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="c090a-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-324">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c090a-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-326">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c090a-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c090a-327">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-328">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="c090a-328">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-329">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="c090a-329">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c090a-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-331">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,17 "," MIF. DMTF \| physikalisches Speicher Array \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c090a-331">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c090a-332">Daten, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c090a-332">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="c090a-333">Die Daten belegen die ersten *n* Oktette des Arrays, die benötigt werden, um die Anzahl der Bits aufzunehmen, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-333">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="c090a-334">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-334">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-335">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="c090a-335">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-336">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c090a-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-338">Die Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="c090a-338">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="c090a-339">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-339">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c090a-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-341">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c090a-341">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="c090a-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="c090a-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-343">Das am wenigsten signifikante Byte zuerst.</span><span class="sxs-lookup"><span data-stu-id="c090a-343">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="c090a-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="c090a-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-345">Das wichtigste Byte zuerst.</span><span class="sxs-lookup"><span data-stu-id="c090a-345">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-346">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c090a-346">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-349">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="c090a-349">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c090a-350">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-351">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c090a-351">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-352">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c090a-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-354">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. DMTF \| physikalisches Speicher Array \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-Arbeits **\_ Speicher**".**Othererrordescription**")</span><span class="sxs-lookup"><span data-stu-id="c090a-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-355">Der Typ des Fehlers, der zuletzt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c090a-355">Type of error that occurred most recently.</span></span> <span data-ttu-id="c090a-356">Die Werte 12 bis 14 sind im CIM-Schema nicht definiert, da DMI die Semantik des Fehler Typs und die korrigierbare Tabelle vermischt.</span><span class="sxs-lookup"><span data-stu-id="c090a-356">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="c090a-357">Ob ein Fehler korrigiert werden kann, wird in der Eigenschaft " **correctableerror** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="c090a-357">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c090a-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c090a-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-359">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="c090a-359">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c090a-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-361">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c090a-361">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c090a-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="c090a-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-363">OK.</span><span class="sxs-lookup"><span data-stu-id="c090a-363">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="c090a-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="c090a-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-365">Ungültiger Lesevorgang.</span><span class="sxs-lookup"><span data-stu-id="c090a-365">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="c090a-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="c090a-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-367">Paritätsfehler.</span><span class="sxs-lookup"><span data-stu-id="c090a-367">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="c090a-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="c090a-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-369">Einzelbit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="c090a-369">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="c090a-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="c090a-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-371">Double-Bit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="c090a-371">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="c090a-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="c090a-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-373">Multi-Bit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="c090a-373">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="c090a-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="c090a-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-375">Nibble-Fehler.</span><span class="sxs-lookup"><span data-stu-id="c090a-375">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="c090a-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="c090a-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-377">Prüfsummen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c090a-377">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="c090a-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="c090a-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-379">CRC-Fehler.</span><span class="sxs-lookup"><span data-stu-id="c090a-379">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="c090a-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (12)</span><span class="sxs-lookup"><span data-stu-id="c090a-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-381">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c090a-381">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="c090a-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (13)</span><span class="sxs-lookup"><span data-stu-id="c090a-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-383">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c090a-383">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="c090a-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (14)</span><span class="sxs-lookup"><span data-stu-id="c090a-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-385">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c090a-385">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-386">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="c090a-386">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-389">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("errormethod"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="c090a-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-390">Gibt an, ob Paritäts-oder CRC-Algorithmen, ECC oder andere Mechanismen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-390">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="c090a-391">Details zum Algorithmus können auch bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-391">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-392">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="c090a-392">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-393">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c090a-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-395">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,21 "," MIF. DMTF \| physikalisches Speicher Array \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="c090a-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-396">Gibt den Bereich in Bytes an, in den der letzte Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="c090a-396">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="c090a-397">Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden (d. h. auf einer typischen Seite), können Fehler in 4-KB-Grenzen aufgelöst werden, und diese Eigenschaft wird auf 4000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c090a-397">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="c090a-398">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-398">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c090a-399">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c090a-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-400">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="c090a-400">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-401">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c090a-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-403">Datum und Uhrzeit des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="c090a-403">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="c090a-404">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c090a-404">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="c090a-405">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-405">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-406">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="c090a-406">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-407">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c090a-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-409">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,16 "," MIF. DMTF \| physikalisches Speicher Array \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="c090a-409">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-410">Die Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c090a-410">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="c090a-411">Der Wert 0 gibt an, dass kein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="c090a-411">A value of 0 indicates no error.</span></span> <span data-ttu-id="c090a-412">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, sollte diese Eigenschaft auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-412">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-413">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c090a-413">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-414">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c090a-414">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-416">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c090a-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-417">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c090a-417">Indicates when the object was installed.</span></span> <span data-ttu-id="c090a-418">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c090a-418">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c090a-419">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-419">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-420">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c090a-420">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-421">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c090a-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-423">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c090a-423">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c090a-424">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-425">**Name**</span><span class="sxs-lookup"><span data-stu-id="c090a-425">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-426">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-427">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-428">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c090a-428">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-429">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c090a-429">Label by which the object is known.</span></span> <span data-ttu-id="c090a-430">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-430">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c090a-431">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-431">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-432">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="c090a-432">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-433">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c090a-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-435">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="c090a-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-436">Anzahl der aufeinander folgenden Blöcke, die die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="c090a-436">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="c090a-437">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="c090a-437">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="c090a-438">Wenn der Wert von **BLOCKSIZE** 1 (eins) ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="c090a-438">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="c090a-439">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c090a-439">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c090a-440">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-440">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-441">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="c090a-441">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-444">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Arbeits **\_ Speicher**".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="c090a-444">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-445">Freie Formular Zeichenfolge, die Informationen bereitstellt, wenn die **ErrorType** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c090a-445">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="c090a-446">Wenn Sie nicht auf 1 festgelegt ist, hat diese Zeichenfolge keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-446">If it is not set to 1, then this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-447">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c090a-447">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-450">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c090a-450">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-451">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c090a-451">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c090a-452">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c090a-452">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c090a-453">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-454">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c090a-454">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-455">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c090a-455">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c090a-456">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-457">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c090a-457">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="c090a-458">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c090a-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-460">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c090a-460">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c090a-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="c090a-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-462">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c090a-462">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c090a-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="c090a-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-464">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c090a-464">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c090a-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c090a-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-466">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c090a-466">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c090a-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="c090a-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-468">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="c090a-468">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c090a-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="c090a-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-470">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c090a-470">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="c090a-471">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-471">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="c090a-472">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c090a-472">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c090a-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="c090a-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-474">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="c090a-474">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c090a-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="c090a-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c090a-476">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c090a-476">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-477">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="c090a-477">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-478">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c090a-478">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-479">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-480">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c090a-480">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c090a-481">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="c090a-481">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c090a-482">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-482">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c090a-483">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="c090a-483">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c090a-484">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-485">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="c090a-485">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-486">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-486">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-488">Freie Formular Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c090a-488">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="c090a-489">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-490">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="c090a-490">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-491">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c090a-491">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-492">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-493">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,3 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="c090a-493">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-494">Anfangsadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-494">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="c090a-495">Die Startadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="c090a-495">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="c090a-496">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c090a-496">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-497">**Status**</span><span class="sxs-lookup"><span data-stu-id="c090a-497">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-498">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-500">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c090a-500">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-501">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c090a-501">String that indicates the current status of the object.</span></span> <span data-ttu-id="c090a-502">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-502">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c090a-503">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c090a-503">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c090a-504">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="c090a-504">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c090a-505">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c090a-505">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c090a-506">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c090a-506">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c090a-507">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c090a-507">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c090a-508">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-508">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c090a-509">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c090a-509">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c090a-510">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c090a-510">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c090a-511">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c090a-511">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c090a-512">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c090a-512">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-513">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c090a-513">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c090a-514">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c090a-514">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c090a-515">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c090a-515">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c090a-516">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c090a-516">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c090a-517">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c090a-517">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c090a-518">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c090a-518">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c090a-519">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c090a-519">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c090a-520">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c090a-520">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c090a-521">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c090a-521">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-522">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c090a-522">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-523">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c090a-523">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-525">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c090a-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c090a-526">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c090a-526">State of the logical device.</span></span> <span data-ttu-id="c090a-527">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c090a-527">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="c090a-528">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c090a-529">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c090a-529">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c090a-530">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c090a-530">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c090a-531">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c090a-531">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c090a-532">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="c090a-532">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c090a-533">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="c090a-533">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c090a-534">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c090a-534">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-535">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-536">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-537">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c090a-537">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c090a-538">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c090a-538">The scoping system's creation class name.</span></span>

<span data-ttu-id="c090a-539">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-539">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c090a-540">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="c090a-540">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-541">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c090a-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c090a-543">Gibt an, ob die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene (**true**) oder eine physische Adresse (**false**) sind.</span><span class="sxs-lookup"><span data-stu-id="c090a-543">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="c090a-544">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c090a-544">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="c090a-545">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c090a-545">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c090a-546">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c090a-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c090a-547">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c090a-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c090a-548">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c090a-548">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c090a-549">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c090a-549">The scoping system's name.</span></span>

<span data-ttu-id="c090a-550">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c090a-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c090a-551">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c090a-551">Remarks</span></span>

<span data-ttu-id="c090a-552">Die **CIM- \_ Speicher** Klasse wird von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c090a-552">The **CIM\_Memory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c090a-553">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c090a-553">WMI does not implement this class.</span></span> <span data-ttu-id="c090a-554">Informationen zu Klassen, die vom **CIM- \_ Speicher** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c090a-554">For classes that are derived from **CIM\_Memory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c090a-555">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c090a-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c090a-556">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c090a-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c090a-557">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c090a-557">Requirements</span></span>



| <span data-ttu-id="c090a-558">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c090a-558">Requirement</span></span> | <span data-ttu-id="c090a-559">Wert</span><span class="sxs-lookup"><span data-stu-id="c090a-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c090a-560">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c090a-560">Minimum supported client</span></span><br/> | <span data-ttu-id="c090a-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c090a-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c090a-562">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c090a-562">Minimum supported server</span></span><br/> | <span data-ttu-id="c090a-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c090a-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c090a-564">Namespace</span><span class="sxs-lookup"><span data-stu-id="c090a-564">Namespace</span></span><br/>                | <span data-ttu-id="c090a-565">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c090a-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c090a-566">MOF</span><span class="sxs-lookup"><span data-stu-id="c090a-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c090a-567"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c090a-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c090a-568">DLL</span><span class="sxs-lookup"><span data-stu-id="c090a-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c090a-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c090a-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c090a-570">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c090a-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c090a-571">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="c090a-571">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

