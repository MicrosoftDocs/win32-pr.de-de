---
description: Die \_ abstrakte WMI-Klasse für den Win32 smbiosmemory stellt die Eigenschaften eines Computersystem Arbeitsspeichers dar, die über die SMBIOS-Schnittstelle (Systemverwaltungs-BIOS) angezeigt werden.
ms.assetid: 2f609fc6-f0f5-45a5-9f9a-3873da034d49
ms.tgt_platform: multiple
title: Win32_SMBIOSMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SMBIOSMemory
- Win32_SMBIOSMemory.Reset
- Win32_SMBIOSMemory.SetPowerState
- Win32_SMBIOSMemory.Access
- Win32_SMBIOSMemory.AdditionalErrorData
- Win32_SMBIOSMemory.Availability
- Win32_SMBIOSMemory.BlockSize
- Win32_SMBIOSMemory.Caption
- Win32_SMBIOSMemory.ConfigManagerErrorCode
- Win32_SMBIOSMemory.ConfigManagerUserConfig
- Win32_SMBIOSMemory.CorrectableError
- Win32_SMBIOSMemory.CreationClassName
- Win32_SMBIOSMemory.Description
- Win32_SMBIOSMemory.DeviceID
- Win32_SMBIOSMemory.EndingAddress
- Win32_SMBIOSMemory.ErrorAccess
- Win32_SMBIOSMemory.ErrorAddress
- Win32_SMBIOSMemory.ErrorCleared
- Win32_SMBIOSMemory.ErrorData
- Win32_SMBIOSMemory.ErrorDataOrder
- Win32_SMBIOSMemory.ErrorDescription
- Win32_SMBIOSMemory.ErrorInfo
- Win32_SMBIOSMemory.ErrorMethodology
- Win32_SMBIOSMemory.ErrorResolution
- Win32_SMBIOSMemory.ErrorTime
- Win32_SMBIOSMemory.ErrorTransferSize
- Win32_SMBIOSMemory.InstallDate
- Win32_SMBIOSMemory.LastErrorCode
- Win32_SMBIOSMemory.Name
- Win32_SMBIOSMemory.NumberOfBlocks
- Win32_SMBIOSMemory.OtherErrorDescription
- Win32_SMBIOSMemory.PNPDeviceID
- Win32_SMBIOSMemory.PowerManagementCapabilities
- Win32_SMBIOSMemory.PowerManagementSupported
- Win32_SMBIOSMemory.Purpose
- Win32_SMBIOSMemory.StartingAddress
- Win32_SMBIOSMemory.Status
- Win32_SMBIOSMemory.StatusInfo
- Win32_SMBIOSMemory.SystemCreationClassName
- Win32_SMBIOSMemory.SystemLevelAddress
- Win32_SMBIOSMemory.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4dc7a42732dfb00d965f79045254878f690309fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127453"
---
# <a name="win32_smbiosmemory-class"></a><span data-ttu-id="ebe37-103">Win32 \_ smbiosmemory-Klasse</span><span class="sxs-lookup"><span data-stu-id="ebe37-103">Win32\_SMBIOSMemory class</span></span>

<span data-ttu-id="ebe37-104">Die abstrakte [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32 \_ smbiosmemory** stellt die Eigenschaften eines Computersystem Arbeitsspeichers dar, die über die SMBIOS-Schnittstelle (Systemverwaltungs-BIOS) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-104">The **Win32\_SMBIOSMemory** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a computer system memory as seen through the system management BIOS (SMBIOS) interface.</span></span> <span data-ttu-id="ebe37-105">Die SMBIOS-Schnittstelle unterscheidet nicht zwischen nicht flüchtiger, flüchtiger und Flash-Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="ebe37-105">The SMBIOS interface does not distinguish between nonvolatile, volatile, and flash memories.</span></span> <span data-ttu-id="ebe37-106">Die [**CIM- \_ Speicher**](cim-memory.md) Klasse ist die übergeordnete Klasse aller Arbeitsspeicher Typen.</span><span class="sxs-lookup"><span data-stu-id="ebe37-106">The [**CIM\_Memory**](cim-memory.md) class is the parent class of all types of memory.</span></span>

<span data-ttu-id="ebe37-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ebe37-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ebe37-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ebe37-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe37-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebe37-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FECB095B-F0FA-11d2-8617-0000F8102E5F}"), AMENDMENT]
class Win32_SMBIOSMemory : CIM_StorageExtent
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
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
  uint16e  StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="ebe37-110">Member</span><span class="sxs-lookup"><span data-stu-id="ebe37-110">Members</span></span>

<span data-ttu-id="ebe37-111">Die **Win32 \_ smbiosmemory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ebe37-111">The **Win32\_SMBIOSMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="ebe37-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="ebe37-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ebe37-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ebe37-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ebe37-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ebe37-114">Methods</span></span>

<span data-ttu-id="ebe37-115">Die **Win32 \_ smbiosmemory** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-115">The **Win32\_SMBIOSMemory** class has these methods.</span></span>



| <span data-ttu-id="ebe37-116">Methode</span><span class="sxs-lookup"><span data-stu-id="ebe37-116">Method</span></span>            | <span data-ttu-id="ebe37-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebe37-117">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe37-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ebe37-118">**Reset**</span></span>         | <span data-ttu-id="ebe37-119">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-119">Not implemented.</span></span> <span data-ttu-id="ebe37-120">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ storageblock**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/>                 |
| <span data-ttu-id="ebe37-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ebe37-121">**SetPowerState**</span></span> | <span data-ttu-id="ebe37-122">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-122">Not implemented.</span></span> <span data-ttu-id="ebe37-123">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ storageblock**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ebe37-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ebe37-124">Properties</span></span>

<span data-ttu-id="ebe37-125">Die **Win32 \_ smbiosmemory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ebe37-125">The **Win32\_SMBIOSMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ebe37-126">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="ebe37-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ebe37-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-129">Der Zugriffstyp.</span><span class="sxs-lookup"><span data-stu-id="ebe37-129">Type of access.</span></span>

<span data-ttu-id="ebe37-130">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ebe37-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="ebe37-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="ebe37-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-134">Schreibbar</span><span class="sxs-lookup"><span data-stu-id="ebe37-134">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="ebe37-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="ebe37-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="ebe37-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="ebe37-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-137">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="ebe37-137">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-138">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="ebe37-138">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-140">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| -Typ 18 \| 32-Bit-Speicherfehler Informationen \| Hersteller-Syndrom"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="ebe37-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-141">Ein Array von Oktetten, die zusätzliche Fehlerinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ebe37-141">Array of octets that hold additional error information.</span></span> <span data-ttu-id="ebe37-142">Ein Beispiel hierfür ist die Fehlerüberprüfung und Korrektur (ECC) oder die Rückgabe der Prüfbits, wenn eine CRC-basierte Fehler Methodik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebe37-142">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="ebe37-143">Wenn in letzterem Fall ein Single-Bit-Fehler erkannt wird und der CRC-Algorithmus (zyklische Redundanz Überprüfung) bekannt ist, ist es möglich, das genaue Bit zu ermitteln, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-143">In the latter case, if a single bit error is recognized and the cyclical redundancy check (CRC) algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="ebe37-144">Diese Art von Daten (ECC-, Bit-oder Paritäts Bitdaten oder andere vom Hersteller bereitgestellte Informationen) ist in diesem Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="ebe37-144">This type of data (ECC Syndrome, Check Bit or Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="ebe37-145">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-145">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-146">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="ebe37-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-147">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ebe37-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-149">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-150">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-150">Availability and status of the device.</span></span>

<span data-ttu-id="ebe37-151">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ebe37-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ebe37-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="ebe37-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-155">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="ebe37-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ebe37-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="ebe37-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ebe37-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="ebe37-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ebe37-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="ebe37-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ebe37-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="ebe37-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ebe37-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="ebe37-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ebe37-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ebe37-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ebe37-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="ebe37-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ebe37-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="ebe37-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ebe37-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="ebe37-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ebe37-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="ebe37-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-166">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-166">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ebe37-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="ebe37-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-168">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ebe37-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ebe37-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ebe37-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-170">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ebe37-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="ebe37-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ebe37-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="ebe37-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-173">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="ebe37-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ebe37-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="ebe37-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-175">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="ebe37-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ebe37-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="ebe37-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-177">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="ebe37-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ebe37-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="ebe37-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-179">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ebe37-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="ebe37-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-181">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="ebe37-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="ebe37-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-183">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ebe37-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-185">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-186">Größe in Byte der Blöcke, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-186">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="ebe37-187">Wenn unbekannt oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 ein.</span><span class="sxs-lookup"><span data-stu-id="ebe37-187">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="ebe37-188">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="ebe37-189">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ebe37-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-193">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ebe37-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-194">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ebe37-194">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="ebe37-195">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-196">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="ebe37-196">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ebe37-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-199">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ebe37-199">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-200">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ebe37-200">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ebe37-201">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-201">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ebe37-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ebe37-203"> (0)</span><span class="sxs-lookup"><span data-stu-id="ebe37-203">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-204">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ebe37-204">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ebe37-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ebe37-206">(1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-206">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-207">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-207">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ebe37-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ebe37-209">(2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-209">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ebe37-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ebe37-211">(3)</span><span class="sxs-lookup"><span data-stu-id="ebe37-211">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-212">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ebe37-212">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ebe37-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ebe37-214">(4)</span><span class="sxs-lookup"><span data-stu-id="ebe37-214">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-215">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ebe37-215">Device is not working properly.</span></span> <span data-ttu-id="ebe37-216">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-216">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ebe37-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ebe37-218">(5)</span><span class="sxs-lookup"><span data-stu-id="ebe37-218">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-219">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ebe37-219">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ebe37-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ebe37-221"> (6)</span><span class="sxs-lookup"><span data-stu-id="ebe37-221">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-222">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="ebe37-222">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ebe37-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ebe37-224">(7)</span><span class="sxs-lookup"><span data-stu-id="ebe37-224">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ebe37-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ebe37-226">(8)</span><span class="sxs-lookup"><span data-stu-id="ebe37-226">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-227">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-227">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ebe37-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ebe37-229">(9)</span><span class="sxs-lookup"><span data-stu-id="ebe37-229">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-230">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ebe37-230">Device is not working properly.</span></span> <span data-ttu-id="ebe37-231">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="ebe37-231">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ebe37-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ebe37-233">(10)</span><span class="sxs-lookup"><span data-stu-id="ebe37-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-234">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ebe37-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ebe37-236">(11)</span><span class="sxs-lookup"><span data-stu-id="ebe37-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-237">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="ebe37-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ebe37-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ebe37-239">(12)</span><span class="sxs-lookup"><span data-stu-id="ebe37-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-240">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ebe37-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ebe37-242">(13)</span><span class="sxs-lookup"><span data-stu-id="ebe37-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-243">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ebe37-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ebe37-245">(14)</span><span class="sxs-lookup"><span data-stu-id="ebe37-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-246">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ebe37-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ebe37-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ebe37-248">(15)</span><span class="sxs-lookup"><span data-stu-id="ebe37-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-249">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ebe37-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ebe37-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ebe37-251">(16)</span><span class="sxs-lookup"><span data-stu-id="ebe37-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-252">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ebe37-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ebe37-254">(17)</span><span class="sxs-lookup"><span data-stu-id="ebe37-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-255">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="ebe37-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ebe37-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ebe37-257">(18)</span><span class="sxs-lookup"><span data-stu-id="ebe37-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-258">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ebe37-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ebe37-260">(19)</span><span class="sxs-lookup"><span data-stu-id="ebe37-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ebe37-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ebe37-262">(20)</span><span class="sxs-lookup"><span data-stu-id="ebe37-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-263">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ebe37-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ebe37-265">(21)</span><span class="sxs-lookup"><span data-stu-id="ebe37-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-266">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="ebe37-266">System failure.</span></span> <span data-ttu-id="ebe37-267">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ebe37-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ebe37-268">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ebe37-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ebe37-270">(22)</span><span class="sxs-lookup"><span data-stu-id="ebe37-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-271">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ebe37-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ebe37-273">(23)</span><span class="sxs-lookup"><span data-stu-id="ebe37-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-274">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="ebe37-274">System failure.</span></span> <span data-ttu-id="ebe37-275">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ebe37-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ebe37-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ebe37-277">(24)</span><span class="sxs-lookup"><span data-stu-id="ebe37-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-278">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ebe37-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ebe37-280">(25)</span><span class="sxs-lookup"><span data-stu-id="ebe37-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-281">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ebe37-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ebe37-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ebe37-283">(26)</span><span class="sxs-lookup"><span data-stu-id="ebe37-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-284">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ebe37-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ebe37-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ebe37-286">(27)</span><span class="sxs-lookup"><span data-stu-id="ebe37-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-287">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ebe37-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ebe37-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ebe37-289">(28)</span><span class="sxs-lookup"><span data-stu-id="ebe37-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-290">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ebe37-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ebe37-292">(29)</span><span class="sxs-lookup"><span data-stu-id="ebe37-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-293">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ebe37-293">Device is disabled.</span></span> <span data-ttu-id="ebe37-294">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-294">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ebe37-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ebe37-296">(30)</span><span class="sxs-lookup"><span data-stu-id="ebe37-296">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-297">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebe37-297">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ebe37-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="ebe37-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ebe37-299">31,5</span><span class="sxs-lookup"><span data-stu-id="ebe37-299">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-300">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ebe37-300">Device is not working properly.</span></span> <span data-ttu-id="ebe37-301">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-301">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-302">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="ebe37-302">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-303">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ebe37-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-305">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ebe37-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-306">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="ebe37-306">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ebe37-307">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-308">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="ebe37-308">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-309">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ebe37-309">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-311">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehlertyp")</span><span class="sxs-lookup"><span data-stu-id="ebe37-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-312">**True** gibt an, dass der letzte Fehler korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ebe37-312">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="ebe37-313">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-313">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-314">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="ebe37-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-317">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ebe37-317">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-318">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebe37-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ebe37-319">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="ebe37-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-321">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebe37-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-324">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ebe37-324">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-325">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-325">Description of the object.</span></span>

<span data-ttu-id="ebe37-326">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ebe37-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-330">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ebe37-330">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-331">Eindeutiger Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-331">Unique identifier of the logical device.</span></span>

<span data-ttu-id="ebe37-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-333">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="ebe37-333">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-334">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ebe37-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-336">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 19 \| Speichergerät zugeordnete Adressen \| Endadresse")</span><span class="sxs-lookup"><span data-stu-id="ebe37-336">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-337">Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-337">Ending address, referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="ebe37-338">Die Endadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="ebe37-338">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="ebe37-339">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-339">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-340">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="ebe37-340">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-341">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ebe37-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-343">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehler Vorgang")</span><span class="sxs-lookup"><span data-stu-id="ebe37-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-344">Speicherzugriffs Vorgang, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="ebe37-344">Memory access operation that caused the last error.</span></span> <span data-ttu-id="ebe37-345">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ebe37-345">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="ebe37-346">Wenn **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-346">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ebe37-347">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-348">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="ebe37-349">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="ebe37-349">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="ebe37-350">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="ebe37-350">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="ebe37-351">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="ebe37-351">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-352">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="ebe37-352">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-353">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ebe37-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-355">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehler Adresse")</span><span class="sxs-lookup"><span data-stu-id="ebe37-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-356">Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="ebe37-356">Address of the last memory error.</span></span> <span data-ttu-id="ebe37-357">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ebe37-357">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="ebe37-358">Wenn **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-358">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="ebe37-359">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-359">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-360">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="ebe37-360">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-361">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ebe37-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-363">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ebe37-363">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="ebe37-364">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-365">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="ebe37-365">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-366">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="ebe37-366">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-368">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="ebe37-368">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-369">Ein Array von Daten, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-369">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="ebe37-370">Die Daten belegen die ersten *n* Oktette des Arrays, die die Anzahl der Bits enthalten muss, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-370">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="ebe37-371">Wenn **ErrorTransferSize** gleich 0 (null) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-371">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-372">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="ebe37-372">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-373">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ebe37-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-375">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="ebe37-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-376">Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="ebe37-376">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="ebe37-377">Wenn **ErrorTransferSize** gleich 0 (null) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-377">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-378">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ebe37-378">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="ebe37-379">**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-379">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="ebe37-380">**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-380">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ebe37-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-384">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="ebe37-384">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="ebe37-385">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ebe37-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-387">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ebe37-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-389">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**Othererrordescription**"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS \| -Typ 18 \| 32-Bit-Arbeitsspeicher Fehlerinformationen \| Fehlertyp ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-389">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-390">Der Typ des Fehlers, der zuletzt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="ebe37-391">Die Werte 12 bis 14 werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ebe37-391">The values 12 through 14 are unused.</span></span> <span data-ttu-id="ebe37-392">Die korrigierende Fähigkeit wird in der Eigenschaft " **correctableerror**" angegeben.</span><span class="sxs-lookup"><span data-stu-id="ebe37-392">The ability to be corrected is indicated in the property **CorrectableError**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ebe37-393">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-394">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ebe37-395">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="ebe37-395">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="ebe37-396">Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="ebe37-396">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="ebe37-397">**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="ebe37-397">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="ebe37-398">**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="ebe37-398">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="ebe37-399">**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="ebe37-399">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="ebe37-400">**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="ebe37-400">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="ebe37-401">**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="ebe37-401">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="ebe37-402">**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="ebe37-402">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="ebe37-403">**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="ebe37-403">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="ebe37-404">**Korrigierter Einzelbit-Fehler** (12)</span><span class="sxs-lookup"><span data-stu-id="ebe37-404">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="ebe37-405">**Korrigierter Fehler** (13)</span><span class="sxs-lookup"><span data-stu-id="ebe37-405">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="ebe37-406">**Nicht korrigier barer Fehler** (14)</span><span class="sxs-lookup"><span data-stu-id="ebe37-406">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-407">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="ebe37-407">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-408">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-410">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("errormethod"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 16 \| physischer Arbeitsspeicher Array- \| Fehlerkorrektur")</span><span class="sxs-lookup"><span data-stu-id="ebe37-410">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-411">Details zu den Paritäts-oder CRC-Algorithmen, ECC oder anderen verwendeten Mechanismen.</span><span class="sxs-lookup"><span data-stu-id="ebe37-411">Details on the parity or CRC algorithms, ECC or other mechanisms used.</span></span>

<span data-ttu-id="ebe37-412">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-412">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ebe37-413">**Sonstige** ("Sonstige")</span><span class="sxs-lookup"><span data-stu-id="ebe37-413">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-414">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ebe37-414">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ebe37-415">**None** ("None")</span><span class="sxs-lookup"><span data-stu-id="ebe37-415">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="ebe37-416">**Parität** ("Parität")</span><span class="sxs-lookup"><span data-stu-id="ebe37-416">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="ebe37-417">**Single-Bit ECC** ("Single-Bit ECC")</span><span class="sxs-lookup"><span data-stu-id="ebe37-417">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="ebe37-418">**Multi-Bit ECC** ("Multi-Bit ECC")</span><span class="sxs-lookup"><span data-stu-id="ebe37-418">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="ebe37-419">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="ebe37-419">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-420">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="ebe37-420">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-421">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ebe37-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-423">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| -Typ 18 \| 32-Bit-Arbeitsspeicher Fehlerinformationen \| Fehlerbehebung"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="ebe37-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-424">Bereich in Bytes, in den der letzte Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="ebe37-424">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="ebe37-425">Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden (d. h. auf einer typischen Seite), können Fehler in 4-KB-Grenzen aufgelöst werden, und diese Eigenschaft wird auf 4000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-425">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="ebe37-426">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-426">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="ebe37-427">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-427">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-428">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="ebe37-428">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-429">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ebe37-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-431">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="ebe37-431">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-432">Zeitpunkt, zu dem der letzte Speicherfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-432">Time that the last memory error occurred.</span></span> <span data-ttu-id="ebe37-433">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ebe37-433">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="ebe37-434">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-434">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-435">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="ebe37-435">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-436">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ebe37-436">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-438">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="ebe37-438">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-439">Die Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat – 0 (null) zeigt an, dass kein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-439">Size of the data transfer in bits that caused the last error—0 (zero) indicates no error.</span></span> <span data-ttu-id="ebe37-440">Wenn die **errorInfo** -Eigenschaft gleich 3 (OK) ist, sollte diese Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-440">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-441">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ebe37-441">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-442">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ebe37-442">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-444">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-444">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-445">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-445">Date and time the object was installed.</span></span> <span data-ttu-id="ebe37-446">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-446">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ebe37-447">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-448">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ebe37-448">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-449">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ebe37-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-451">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ebe37-451">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ebe37-452">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-453">**Name**</span><span class="sxs-lookup"><span data-stu-id="ebe37-453">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-454">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-456">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ebe37-456">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-457">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-457">Label by which the object is known.</span></span> <span data-ttu-id="ebe37-458">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-458">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="ebe37-459">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-459">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-460">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="ebe37-460">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-461">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ebe37-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-462">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-463">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-464">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-464">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="ebe37-465">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ebe37-465">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="ebe37-466">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="ebe37-466">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="ebe37-467">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-467">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="ebe37-468">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-468">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-469">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="ebe37-469">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-470">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-470">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-471">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-472">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**ErrorInfo**"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-472">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-473">Eine frei Form Zeichenfolge, die weitere Informationen bereitstellt, wenn die **ErrorType** -Eigenschaft auf 1 festgelegt ist. Andernfalls hat diese Zeichenfolge keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-473">Free-form string that provides more information if the **ErrorType** property is set to 1; otherwise, this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-474">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ebe37-474">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-475">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-476">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-477">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ebe37-477">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-478">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-478">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="ebe37-479">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ebe37-479">Example: "\*PNP030b"</span></span>

<span data-ttu-id="ebe37-480">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-481">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="ebe37-481">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-482">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ebe37-482">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-483">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-484">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-484">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ebe37-485">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ebe37-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ebe37-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ebe37-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ebe37-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ebe37-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-490">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ebe37-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ebe37-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="ebe37-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-492">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="ebe37-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ebe37-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="ebe37-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-494">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ebe37-495">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-495">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ebe37-496">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-496">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ebe37-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="ebe37-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-498">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ebe37-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="ebe37-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ebe37-500">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-500">Timed Power-On Supported</span></span>

<span data-ttu-id="ebe37-501">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-502">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="ebe37-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-503">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ebe37-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-505">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="ebe37-505">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="ebe37-506">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ebe37-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="ebe37-507">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-508">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="ebe37-508">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-509">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-509">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-510">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-511">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-511">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="ebe37-512">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-512">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-513">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="ebe37-513">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-514">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ebe37-514">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-515">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-516">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 19 \| Speichergerät zugeordnete Adressen \| Startadresse")</span><span class="sxs-lookup"><span data-stu-id="ebe37-516">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-517">Die Anfangsadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="ebe37-517">Beginning address that is referenced by an application or operating system, and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="ebe37-518">Die Startadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="ebe37-518">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="ebe37-519">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ebe37-519">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-520">**Status**</span><span class="sxs-lookup"><span data-stu-id="ebe37-520">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-521">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-522">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-523">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ebe37-523">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-524">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-524">Current status of the object.</span></span> <span data-ttu-id="ebe37-525">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-525">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ebe37-526">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="ebe37-526">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ebe37-527">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="ebe37-527">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ebe37-528">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-528">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ebe37-529">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ebe37-529">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ebe37-530">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-530">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ebe37-531">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ebe37-531">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ebe37-532">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ebe37-532">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ebe37-533">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ebe37-533">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ebe37-534">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ebe37-534">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-535">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ebe37-535">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ebe37-536">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ebe37-536">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ebe37-537">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ebe37-537">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ebe37-538">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-538">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ebe37-539">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ebe37-539">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ebe37-540">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="ebe37-540">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ebe37-541">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="ebe37-541">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ebe37-542">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="ebe37-542">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ebe37-543">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="ebe37-543">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-544">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ebe37-544">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-545">Datentyp: **uint16e**</span><span class="sxs-lookup"><span data-stu-id="ebe37-545">Data type: **uint16e**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-546">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-547">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ebe37-547">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-548">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ebe37-548">State of the logical device.</span></span> <span data-ttu-id="ebe37-549">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe37-549">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ebe37-550">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ebe37-551">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ebe37-551">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ebe37-552">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ebe37-552">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ebe37-553">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ebe37-553">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ebe37-554">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="ebe37-554">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ebe37-555">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="ebe37-555">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ebe37-556">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="ebe37-556">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-557">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-558">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-559">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ebe37-559">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-560">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="ebe37-560">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="ebe37-561">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-561">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-562">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="ebe37-562">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-563">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ebe37-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-564">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-565">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehler Adresse")</span><span class="sxs-lookup"><span data-stu-id="ebe37-565">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-566">**True** gibt an, dass die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene sind.</span><span class="sxs-lookup"><span data-stu-id="ebe37-566">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="ebe37-567">**False** gibt an, dass es sich um eine physische Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-567">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="ebe37-568">Wenn die Eigenschaft **errorInfo** gleich 3 (OK) ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ebe37-568">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="ebe37-569">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="ebe37-569">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe37-570">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ebe37-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-571">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ebe37-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe37-572">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ebe37-572">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ebe37-573">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="ebe37-573">Name of the scoping system.</span></span>

<span data-ttu-id="ebe37-574">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe37-574">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebe37-575">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebe37-575">Remarks</span></span>

<span data-ttu-id="ebe37-576">Die **Win32-Klasse \_ smbiosmemory** wird von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ebe37-576">The **Win32\_SMBIOSMemory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe37-577">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebe37-577">Requirements</span></span>



| <span data-ttu-id="ebe37-578">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebe37-578">Requirement</span></span> | <span data-ttu-id="ebe37-579">Wert</span><span class="sxs-lookup"><span data-stu-id="ebe37-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe37-580">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebe37-580">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe37-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebe37-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ebe37-582">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebe37-582">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe37-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebe37-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ebe37-584">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebe37-584">Namespace</span></span><br/>                | <span data-ttu-id="ebe37-585">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ebe37-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ebe37-586">MOF</span><span class="sxs-lookup"><span data-stu-id="ebe37-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebe37-587"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ebe37-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebe37-588">DLL</span><span class="sxs-lookup"><span data-stu-id="ebe37-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebe37-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebe37-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe37-590">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebe37-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe37-591">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="ebe37-591">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="ebe37-592">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="ebe37-592">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
