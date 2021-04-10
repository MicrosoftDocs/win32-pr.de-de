---
description: Die Win32 \_ memorydevice-WMI-Klasse stellt die Eigenschaften eines Computersystem-Speichergeräts und der zugeordneten zugeordneten Adressen dar.
ms.assetid: d609dca5-2f5f-4f23-8fcc-bcc197d6c24b
ms.tgt_platform: multiple
title: Win32_MemoryDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDevice
- Win32_MemoryDevice.Reset
- Win32_MemoryDevice.SetPowerState
- Win32_MemoryDevice.Access
- Win32_MemoryDevice.AdditionalErrorData
- Win32_MemoryDevice.Availability
- Win32_MemoryDevice.BlockSize
- Win32_MemoryDevice.Caption
- Win32_MemoryDevice.ConfigManagerErrorCode
- Win32_MemoryDevice.ConfigManagerUserConfig
- Win32_MemoryDevice.CorrectableError
- Win32_MemoryDevice.CreationClassName
- Win32_MemoryDevice.Description
- Win32_MemoryDevice.DeviceID
- Win32_MemoryDevice.EndingAddress
- Win32_MemoryDevice.ErrorAccess
- Win32_MemoryDevice.ErrorAddress
- Win32_MemoryDevice.ErrorCleared
- Win32_MemoryDevice.ErrorData
- Win32_MemoryDevice.ErrorDataOrder
- Win32_MemoryDevice.ErrorDescription
- Win32_MemoryDevice.ErrorGranularity
- Win32_MemoryDevice.ErrorInfo
- Win32_MemoryDevice.ErrorMethodology
- Win32_MemoryDevice.ErrorResolution
- Win32_MemoryDevice.ErrorTime
- Win32_MemoryDevice.ErrorTransferSize
- Win32_MemoryDevice.InstallDate
- Win32_MemoryDevice.LastErrorCode
- Win32_MemoryDevice.Name
- Win32_MemoryDevice.NumberOfBlocks
- Win32_MemoryDevice.OtherErrorDescription
- Win32_MemoryDevice.PNPDeviceID
- Win32_MemoryDevice.PowerManagementCapabilities
- Win32_MemoryDevice.PowerManagementSupported
- Win32_MemoryDevice.Purpose
- Win32_MemoryDevice.StartingAddress
- Win32_MemoryDevice.Status
- Win32_MemoryDevice.StatusInfo
- Win32_MemoryDevice.SystemCreationClassName
- Win32_MemoryDevice.SystemLevelAddress
- Win32_MemoryDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 277b868f1b92b9f7c6a0c520c77ab76fac6b544d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958232"
---
# <a name="win32_memorydevice-class"></a><span data-ttu-id="308cb-103">Win32 \_ memorydevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="308cb-103">Win32\_MemoryDevice class</span></span>

<span data-ttu-id="308cb-104">Die **Win32 \_ memorydevice** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Eigenschaften eines Computersystem-Speichergeräts und der zugeordneten zugeordneten Adressen dar.</span><span class="sxs-lookup"><span data-stu-id="308cb-104">The **Win32\_MemoryDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a computer system memory device and its associated mapped addresses.</span></span>

<span data-ttu-id="308cb-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="308cb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="308cb-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="308cb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="308cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="308cb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDevice : Win32_SMBIOSMemory
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
  uint16   ErrorGranularity;
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

## <a name="members"></a><span data-ttu-id="308cb-108">Member</span><span class="sxs-lookup"><span data-stu-id="308cb-108">Members</span></span>

<span data-ttu-id="308cb-109">Die **Win32- \_ memorydevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="308cb-109">The **Win32\_MemoryDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="308cb-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="308cb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="308cb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="308cb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="308cb-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="308cb-112">Methods</span></span>

<span data-ttu-id="308cb-113">Die **Win32 \_ memorydevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="308cb-113">The **Win32\_MemoryDevice** class has these methods.</span></span>



| <span data-ttu-id="308cb-114">Methode</span><span class="sxs-lookup"><span data-stu-id="308cb-114">Method</span></span>            | <span data-ttu-id="308cb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="308cb-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308cb-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="308cb-116">**Reset**</span></span>         | <span data-ttu-id="308cb-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="308cb-117">Not implemented.</span></span> <span data-ttu-id="308cb-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="308cb-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/>                 |
| <span data-ttu-id="308cb-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="308cb-119">**SetPowerState**</span></span> | <span data-ttu-id="308cb-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="308cb-120">Not implemented.</span></span> <span data-ttu-id="308cb-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="308cb-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="308cb-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="308cb-122">Properties</span></span>

<span data-ttu-id="308cb-123">Die **Win32 \_ memorydevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="308cb-123">The **Win32\_MemoryDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="308cb-124">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="308cb-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="308cb-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cb-127">Der Medien Zugriff ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="308cb-127">Media access available.</span></span>

<span data-ttu-id="308cb-128">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="308cb-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="308cb-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="308cb-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-132">Schreibbar</span><span class="sxs-lookup"><span data-stu-id="308cb-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="308cb-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="308cb-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="308cb-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="308cb-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="308cb-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-136">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="308cb-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="308cb-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| -Typ 18 \| 32-Bit-Speicherfehler Informationen \| Hersteller-Syndrom"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="308cb-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="308cb-139">Array zusätzlicher Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="308cb-139">Array of additional error information.</span></span> <span data-ttu-id="308cb-140">Ein Beispiel hierfür ist die Fehlerüberprüfung und Korrektur (ECC) oder die Rückgabe der Prüfbits, wenn eine CRC-basierte Fehler Methodik (zyklische Redundanz Überprüfung) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based error methodology is used.</span></span> <span data-ttu-id="308cb-141">Wenn in letzterem Fall ein Einzelbit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, können Sie das genaue Bit ermitteln, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="308cb-142">Diese Art von Daten (ECC-Syndrom, Check-Bit, Paritäts Bitdaten oder andere vom Hersteller bereitgestellte Informationen) ist in diesem Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="308cb-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="308cb-143">Diese Eigenschaft wird nur verwendet, wenn die **errorInfo** -Eigenschaft nicht gleich 3 ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="308cb-144">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-145">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="308cb-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-146">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="308cb-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="308cb-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-149">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="308cb-149">Availability and status of the device.</span></span>

<span data-ttu-id="308cb-150">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="308cb-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="308cb-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="308cb-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-154">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="308cb-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="308cb-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="308cb-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="308cb-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="308cb-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="308cb-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="308cb-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="308cb-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="308cb-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="308cb-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="308cb-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="308cb-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="308cb-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="308cb-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="308cb-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="308cb-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="308cb-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="308cb-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="308cb-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="308cb-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="308cb-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-165">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="308cb-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="308cb-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="308cb-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-167">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="308cb-167">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="308cb-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="308cb-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-169">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="308cb-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="308cb-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="308cb-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="308cb-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-172">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="308cb-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="308cb-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="308cb-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-174">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="308cb-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="308cb-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="308cb-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-176">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="308cb-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="308cb-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="308cb-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-178">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="308cb-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="308cb-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="308cb-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-180">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="308cb-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="308cb-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-182">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="308cb-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-184">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="308cb-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-185">Größe in Byte der Blöcke, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="308cb-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="308cb-186">Wenn unbekannt oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 ein.</span><span class="sxs-lookup"><span data-stu-id="308cb-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="308cb-187">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="308cb-188">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="308cb-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="308cb-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-192">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="308cb-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-193">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="308cb-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="308cb-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-195">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="308cb-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-196">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="308cb-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-198">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="308cb-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-199">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="308cb-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="308cb-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="308cb-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="308cb-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="308cb-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="308cb-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-203">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="308cb-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="308cb-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="308cb-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="308cb-205">(1)</span><span class="sxs-lookup"><span data-stu-id="308cb-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-206">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="308cb-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="308cb-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="308cb-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="308cb-208">(2)</span><span class="sxs-lookup"><span data-stu-id="308cb-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="308cb-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="308cb-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="308cb-210">(3)</span><span class="sxs-lookup"><span data-stu-id="308cb-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-211">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="308cb-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="308cb-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="308cb-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="308cb-213">(4)</span><span class="sxs-lookup"><span data-stu-id="308cb-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-214">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="308cb-214">Device is not working properly.</span></span> <span data-ttu-id="308cb-215">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="308cb-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="308cb-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="308cb-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="308cb-217">(5)</span><span class="sxs-lookup"><span data-stu-id="308cb-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-218">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="308cb-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="308cb-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="308cb-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="308cb-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="308cb-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-221">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="308cb-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="308cb-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="308cb-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="308cb-223">(7)</span><span class="sxs-lookup"><span data-stu-id="308cb-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="308cb-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="308cb-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="308cb-225">(8)</span><span class="sxs-lookup"><span data-stu-id="308cb-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-226">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="308cb-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="308cb-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="308cb-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="308cb-228">(9)</span><span class="sxs-lookup"><span data-stu-id="308cb-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-229">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="308cb-229">Device is not working properly.</span></span> <span data-ttu-id="308cb-230">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="308cb-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="308cb-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="308cb-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="308cb-232">(10)</span><span class="sxs-lookup"><span data-stu-id="308cb-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-233">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="308cb-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="308cb-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="308cb-235">(11)</span><span class="sxs-lookup"><span data-stu-id="308cb-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-236">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="308cb-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="308cb-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="308cb-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="308cb-238">(12)</span><span class="sxs-lookup"><span data-stu-id="308cb-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-239">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="308cb-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="308cb-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="308cb-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="308cb-241">(13)</span><span class="sxs-lookup"><span data-stu-id="308cb-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-242">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="308cb-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="308cb-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="308cb-244">(14)</span><span class="sxs-lookup"><span data-stu-id="308cb-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-245">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="308cb-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="308cb-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="308cb-247">(15)</span><span class="sxs-lookup"><span data-stu-id="308cb-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-248">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="308cb-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="308cb-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="308cb-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="308cb-250">(16)</span><span class="sxs-lookup"><span data-stu-id="308cb-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-251">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="308cb-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="308cb-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="308cb-253">(17)</span><span class="sxs-lookup"><span data-stu-id="308cb-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-254">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="308cb-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="308cb-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="308cb-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="308cb-256">(18)</span><span class="sxs-lookup"><span data-stu-id="308cb-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-257">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="308cb-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="308cb-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="308cb-259">(19)</span><span class="sxs-lookup"><span data-stu-id="308cb-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="308cb-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="308cb-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="308cb-261">(20)</span><span class="sxs-lookup"><span data-stu-id="308cb-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-262">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="308cb-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="308cb-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="308cb-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="308cb-264">(21)</span><span class="sxs-lookup"><span data-stu-id="308cb-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-265">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="308cb-265">System failure.</span></span> <span data-ttu-id="308cb-266">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="308cb-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="308cb-267">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="308cb-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="308cb-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="308cb-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="308cb-269">(22)</span><span class="sxs-lookup"><span data-stu-id="308cb-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-270">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="308cb-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="308cb-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="308cb-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="308cb-272">(23)</span><span class="sxs-lookup"><span data-stu-id="308cb-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-273">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="308cb-273">System failure.</span></span> <span data-ttu-id="308cb-274">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="308cb-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="308cb-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="308cb-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="308cb-276">(24)</span><span class="sxs-lookup"><span data-stu-id="308cb-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-277">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="308cb-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="308cb-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="308cb-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="308cb-279">(25)</span><span class="sxs-lookup"><span data-stu-id="308cb-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-280">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="308cb-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="308cb-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="308cb-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="308cb-282">(26)</span><span class="sxs-lookup"><span data-stu-id="308cb-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-283">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="308cb-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="308cb-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="308cb-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="308cb-285">(27)</span><span class="sxs-lookup"><span data-stu-id="308cb-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-286">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="308cb-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="308cb-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="308cb-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="308cb-288">(28)</span><span class="sxs-lookup"><span data-stu-id="308cb-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-289">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="308cb-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="308cb-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="308cb-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="308cb-291">(29)</span><span class="sxs-lookup"><span data-stu-id="308cb-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-292">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="308cb-292">Device is disabled.</span></span> <span data-ttu-id="308cb-293">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="308cb-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="308cb-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="308cb-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="308cb-295">(30)</span><span class="sxs-lookup"><span data-stu-id="308cb-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-296">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="308cb-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="308cb-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="308cb-298">31,5</span><span class="sxs-lookup"><span data-stu-id="308cb-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-299">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="308cb-299">Device is not working properly.</span></span> <span data-ttu-id="308cb-300">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-301">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="308cb-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-302">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="308cb-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-304">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="308cb-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-305">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="308cb-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="308cb-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-307">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="308cb-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-308">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="308cb-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-310">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehlertyp")</span><span class="sxs-lookup"><span data-stu-id="308cb-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-311">**True** gibt an, dass der letzte Fehler korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="308cb-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="308cb-312">Diese Eigenschaft wird nicht verwendet, wenn **errorInfo** auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="308cb-313">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-314">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="308cb-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-317">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="308cb-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="308cb-318">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-318">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="308cb-319">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="308cb-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-321">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="308cb-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-324">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="308cb-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-325">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="308cb-325">Description of the object.</span></span>

<span data-ttu-id="308cb-326">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="308cb-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-330">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="308cb-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-331">Eindeutiger Bezeichner des Speichergeräts.</span><span class="sxs-lookup"><span data-stu-id="308cb-331">Unique identifier of the memory device.</span></span>

<span data-ttu-id="308cb-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="308cb-333">Beispiel: "Speichergerät 1"</span><span class="sxs-lookup"><span data-stu-id="308cb-333">Example: "Memory Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="308cb-334">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="308cb-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-335">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="308cb-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-337">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 19 \| Speichergerät zugeordnete Adressen \| Endadresse")</span><span class="sxs-lookup"><span data-stu-id="308cb-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-338">Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="308cb-339">Diese Speicheradresse wird von einem Speichercontroller für dieses Speicher Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="308cb-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="308cb-340">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-340">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="308cb-341">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="308cb-341">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-342">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="308cb-342">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-343">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="308cb-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-345">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehler Vorgang")</span><span class="sxs-lookup"><span data-stu-id="308cb-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-346">Typ des Speicherzugriffs Vorgangs, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="308cb-346">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="308cb-347">Diese Eigenschaft ist nur gültig, wenn **errorInfo** nicht auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-347">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="308cb-348">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-348">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="308cb-349">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-350">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="308cb-351">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="308cb-351">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="308cb-352">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="308cb-352">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="308cb-353">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="308cb-353">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-354">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="308cb-354">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-355">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="308cb-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-357">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehler Adresse")</span><span class="sxs-lookup"><span data-stu-id="308cb-357">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-358">Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="308cb-358">Address of the last memory error.</span></span> <span data-ttu-id="308cb-359">Diese Eigenschaft wird nur verwendet, wenn **errorInfo** nicht auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-359">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="308cb-360">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-360">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="308cb-361">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="308cb-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-362">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="308cb-362">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-363">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="308cb-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cb-365">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-365">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="308cb-366">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-367">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="308cb-367">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-368">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="308cb-368">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="308cb-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-370">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="308cb-370">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="308cb-371">Ein Array von Daten, die aus dem letzten Speicherzugriff mit einem Fehler aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="308cb-371">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="308cb-372">Die Daten belegen die ersten *n* Oktette des Arrays, die die Anzahl der Bits enthalten muss, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-372">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="308cb-373">Wenn **ErrorTransferSize** gleich 0 (null) ist, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="308cb-373">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="308cb-374">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-374">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-375">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="308cb-375">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-376">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="308cb-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-378">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="308cb-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-379">Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="308cb-379">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="308cb-380">Diese Eigenschaft wird nur verwendet, wenn **ErrorTransferSize** den Wert 0 (null) aufweist.</span><span class="sxs-lookup"><span data-stu-id="308cb-380">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="308cb-381">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-381">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-382">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="308cb-382">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="308cb-383">**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-383">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="308cb-384">**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-384">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-385">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="308cb-385">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-386">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cb-388">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="308cb-388">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="308cb-389">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-390">**Errorgranularität**</span><span class="sxs-lookup"><span data-stu-id="308cb-390">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-391">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="308cb-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-393">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 18 \| Error-Granularität")</span><span class="sxs-lookup"><span data-stu-id="308cb-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-394">Ebene, auf der der Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="308cb-394">Level where the error can be resolved.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="308cb-395">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-396">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_level"></span><span id="device_level"></span><span id="DEVICE_LEVEL"></span>

<span data-ttu-id="308cb-397">**Geräteebene** (3)</span><span class="sxs-lookup"><span data-stu-id="308cb-397">**Device level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_partition_level"></span><span id="memory_partition_level"></span><span id="MEMORY_PARTITION_LEVEL"></span>

<span data-ttu-id="308cb-398">**Speicher Partitions Ebene** (4)</span><span class="sxs-lookup"><span data-stu-id="308cb-398">**Memory partition level** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-399">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="308cb-399">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-400">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="308cb-400">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-401">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-402">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**Othererrordescription**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| -Typ 18 \| 32-Bit-Arbeitsspeicher Fehlerinformationen \| Fehlertyp ")</span><span class="sxs-lookup"><span data-stu-id="308cb-402">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-403">Der Typ des Fehlers, der zuletzt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-403">Type of error that occurred most recently.</span></span> <span data-ttu-id="308cb-404">Die Werte 12-14, die angeben, ob ein Fehler korrigiert werden kann, werden nicht mit dieser Eigenschaft verwendet. diese Informationen befinden sich jedoch in der Eigenschaft " **correctableerror** ".</span><span class="sxs-lookup"><span data-stu-id="308cb-404">The values 12-14, indicating whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="308cb-405">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-405">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="308cb-406">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-406">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-407">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-407">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="308cb-408">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="308cb-408">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="308cb-409">Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="308cb-409">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="308cb-410">**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="308cb-410">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="308cb-411">**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="308cb-411">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="308cb-412">**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="308cb-412">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="308cb-413">**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="308cb-413">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="308cb-414">**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="308cb-414">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="308cb-415">**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="308cb-415">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="308cb-416">**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="308cb-416">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="308cb-417">**Korrigierter Einzelbit-Fehler** (12)</span><span class="sxs-lookup"><span data-stu-id="308cb-417">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="308cb-418">**Korrigierter Fehler** (13)</span><span class="sxs-lookup"><span data-stu-id="308cb-418">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="308cb-419">**Nicht korrigier barer Fehler** (14)</span><span class="sxs-lookup"><span data-stu-id="308cb-419">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-420">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="308cb-420">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-423">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 16 \| physischer Arbeitsspeicher Array \| Fehlerkorrektur")</span><span class="sxs-lookup"><span data-stu-id="308cb-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-424">Typen von Fehlerüberprüfungen, die von der Speicherhardware verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-424">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="308cb-425">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-425">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="308cb-426">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="308cb-426">The values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="308cb-427">**Sonstige** ("Sonstige")</span><span class="sxs-lookup"><span data-stu-id="308cb-427">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-428">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="308cb-428">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="308cb-429">**Parität** ("Parität")</span><span class="sxs-lookup"><span data-stu-id="308cb-429">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="308cb-430">**Single-Bit ECC** ("Single-Bit ECC")</span><span class="sxs-lookup"><span data-stu-id="308cb-430">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="308cb-431">**Multi-Bit ECC** ("Multi-Bit ECC")</span><span class="sxs-lookup"><span data-stu-id="308cb-431">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="308cb-432">**None** ("None")</span><span class="sxs-lookup"><span data-stu-id="308cb-432">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="308cb-433">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="308cb-433">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-434">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="308cb-434">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-435">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="308cb-435">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-437">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| -Typ 18 \| 32-Bit-Arbeitsspeicher Fehlerinformationen \| Fehlerbehebung"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="308cb-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-438">Die Menge der Daten, die tatsächlich zur Ursache des Fehlers bestimmt wurde.</span><span class="sxs-lookup"><span data-stu-id="308cb-438">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="308cb-439">Diese Eigenschaft wird nicht verwendet, wenn die **errorInfo** -Eigenschaft auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-439">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="308cb-440">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-440">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="308cb-441">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="308cb-441">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-442">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="308cb-442">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-443">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="308cb-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-445">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="308cb-445">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-446">Zeitpunkt, zu dem der letzte Speicherfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-446">Time that the last memory error occurred.</span></span> <span data-ttu-id="308cb-447">Diese Eigenschaft ist nur gültig, wenn **errorInfo** nicht auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-447">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="308cb-448">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-448">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-449">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="308cb-449">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-450">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="308cb-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-452">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="308cb-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-453">Größe der Daten (mit dem letzten Fehler), die übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-453">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="308cb-454">Diese Eigenschaft wird auf 0 (null) festgelegt, wenn kein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="308cb-454">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="308cb-455">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-455">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-456">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="308cb-456">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-457">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="308cb-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-459">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="308cb-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-460">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="308cb-460">Date and time the object was installed.</span></span> <span data-ttu-id="308cb-461">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-461">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="308cb-462">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-462">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-463">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="308cb-463">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-464">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="308cb-464">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cb-466">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="308cb-466">Last error code reported by the logical device.</span></span>

<span data-ttu-id="308cb-467">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-468">**Name**</span><span class="sxs-lookup"><span data-stu-id="308cb-468">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-471">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="308cb-471">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-472">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-472">Label by which the object is known.</span></span> <span data-ttu-id="308cb-473">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-473">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="308cb-474">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-474">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-475">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="308cb-475">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-476">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="308cb-476">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-478">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="308cb-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-479">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="308cb-479">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="308cb-480">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-480">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="308cb-481">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="308cb-481">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="308cb-482">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-482">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="308cb-483">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="308cb-483">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-484">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="308cb-484">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-485">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-487">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**ErrorInfo**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="308cb-487">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-488">Weitere Informationen, wenn die **errorInfo** -Eigenschaft auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-488">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="308cb-489">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-489">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-490">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="308cb-490">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-491">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-492">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-493">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="308cb-493">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-494">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="308cb-494">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="308cb-495">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="308cb-496">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="308cb-496">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="308cb-497">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="308cb-497">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-498">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="308cb-498">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="308cb-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cb-500">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="308cb-500">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="308cb-501">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-501">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="308cb-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="308cb-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="308cb-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="308cb-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="308cb-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-506">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="308cb-506">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="308cb-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="308cb-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-508">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="308cb-508">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="308cb-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="308cb-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-510">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="308cb-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="308cb-511">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-511">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="308cb-512">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="308cb-512">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="308cb-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="308cb-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-514">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-514">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="308cb-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="308cb-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="308cb-516">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="308cb-516">Timed Power-On Supported</span></span>

<span data-ttu-id="308cb-517">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-517">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-518">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="308cb-518">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-519">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="308cb-519">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-520">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-520">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cb-521">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="308cb-521">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="308cb-522">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-522">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="308cb-523">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-524">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="308cb-524">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-525">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-526">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cb-527">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="308cb-527">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="308cb-528">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-528">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-529">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="308cb-529">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-530">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="308cb-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-531">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-532">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 19 \| Speichergerät zugeordnete Adressen \| Startadresse")</span><span class="sxs-lookup"><span data-stu-id="308cb-532">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-533">Die Anfangsadresse, auf die von einer Anwendung oder dem Betriebssystem verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="308cb-533">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="308cb-534">Diese Speicheradresse wird von einem Speichercontroller für dieses Speicher Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="308cb-534">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="308cb-535">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-535">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="308cb-536">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="308cb-536">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-537">**Status**</span><span class="sxs-lookup"><span data-stu-id="308cb-537">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-538">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-539">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-540">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="308cb-540">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-541">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="308cb-541">Current status of the object.</span></span> <span data-ttu-id="308cb-542">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-542">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="308cb-543">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="308cb-543">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="308cb-544">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="308cb-544">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="308cb-545">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-545">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="308cb-546">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="308cb-546">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="308cb-547">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-547">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="308cb-548">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="308cb-548">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="308cb-549">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="308cb-549">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="308cb-550">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="308cb-550">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="308cb-551">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="308cb-551">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-552">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="308cb-552">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="308cb-553">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="308cb-553">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="308cb-554">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="308cb-554">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="308cb-555">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="308cb-555">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="308cb-556">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="308cb-556">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="308cb-557">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="308cb-557">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="308cb-558">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="308cb-558">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="308cb-559">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="308cb-559">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="308cb-560">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="308cb-560">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-561">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="308cb-561">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-562">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="308cb-562">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-563">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-563">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-564">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="308cb-564">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-565">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="308cb-565">State of the logical device.</span></span> <span data-ttu-id="308cb-566">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="308cb-566">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="308cb-567">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-567">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="308cb-568">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="308cb-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="308cb-569">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="308cb-569">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="308cb-570">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="308cb-570">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="308cb-571">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="308cb-571">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="308cb-572">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="308cb-572">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="308cb-573">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="308cb-573">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-574">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-575">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-575">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-576">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="308cb-576">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="308cb-577">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="308cb-577">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="308cb-578">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-578">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-579">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="308cb-579">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-580">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="308cb-580">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-581">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-582">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| -Typ 18 \| 32-Bit Arbeitsspeicher Fehlerinformationen \| Fehler Adresse")</span><span class="sxs-lookup"><span data-stu-id="308cb-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="308cb-583">**True** gibt an, dass die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene sind.</span><span class="sxs-lookup"><span data-stu-id="308cb-583">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="308cb-584">**False** gibt an, dass es sich um eine physische Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="308cb-584">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="308cb-585">Diese Eigenschaft wird nur verwendet, wenn **errorInfo** nicht auf 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="308cb-585">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="308cb-586">Diese Eigenschaft wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-586">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cb-587">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="308cb-587">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cb-588">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="308cb-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cb-589">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="308cb-589">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cb-590">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="308cb-590">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="308cb-591">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="308cb-591">Name of the scoping system.</span></span>

<span data-ttu-id="308cb-592">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="308cb-592">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="308cb-593">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="308cb-593">Remarks</span></span>

<span data-ttu-id="308cb-594">Die **Win32- \_ memorydevice** -Klasse wird von [**Win32 \_ smbiosmemory**](win32-smbiosmemory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="308cb-594">The **Win32\_MemoryDevice** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="308cb-595">Beispiele</span><span class="sxs-lookup"><span data-stu-id="308cb-595">Examples</span></span>

<span data-ttu-id="308cb-596">Das Beispiel zum [Auflisten von Speichergeräten](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) in Perl gibt Start-und Endadressen für alle Speichergeräte zurück, die auf einem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="308cb-596">The [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl sample returns starting and ending addresses for all memory devices installed on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="308cb-597">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="308cb-597">Requirements</span></span>



| <span data-ttu-id="308cb-598">Anforderung</span><span class="sxs-lookup"><span data-stu-id="308cb-598">Requirement</span></span> | <span data-ttu-id="308cb-599">Wert</span><span class="sxs-lookup"><span data-stu-id="308cb-599">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="308cb-600">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="308cb-600">Minimum supported client</span></span><br/> | <span data-ttu-id="308cb-601">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="308cb-601">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="308cb-602">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="308cb-602">Minimum supported server</span></span><br/> | <span data-ttu-id="308cb-603">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="308cb-603">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="308cb-604">Namespace</span><span class="sxs-lookup"><span data-stu-id="308cb-604">Namespace</span></span><br/>                | <span data-ttu-id="308cb-605">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="308cb-605">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="308cb-606">MOF</span><span class="sxs-lookup"><span data-stu-id="308cb-606">MOF</span></span><br/>                      | <dl> <span data-ttu-id="308cb-607"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="308cb-607"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="308cb-608">DLL</span><span class="sxs-lookup"><span data-stu-id="308cb-608">DLL</span></span><br/>                      | <dl> <span data-ttu-id="308cb-609"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="308cb-609"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="308cb-610">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="308cb-610">See also</span></span>

<dl> <dt>

[<span data-ttu-id="308cb-611">**Win32 \_ smbiosmemory**</span><span class="sxs-lookup"><span data-stu-id="308cb-611">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="308cb-612">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="308cb-612">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

