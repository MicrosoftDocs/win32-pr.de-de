---
description: Die CIM \_ -Klasse NonVolatileStorage stellt die Funktionen und die Verwaltung von nichtflüchtigem Speicher dar. Nicht flüchtiger Speicher umfasst nativ Flash-und ROM-Speicher.
ms.assetid: 39158b31-31f7-460c-aef1-1ca423badad6
ms.tgt_platform: multiple
title: CIM_NonVolatileStorage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage
- CIM_NonVolatileStorage.Access
- CIM_NonVolatileStorage.AdditionalErrorData
- CIM_NonVolatileStorage.Availability
- CIM_NonVolatileStorage.BlockSize
- CIM_NonVolatileStorage.Caption
- CIM_NonVolatileStorage.ConfigManagerErrorCode
- CIM_NonVolatileStorage.ConfigManagerUserConfig
- CIM_NonVolatileStorage.CorrectableError
- CIM_NonVolatileStorage.CreationClassName
- CIM_NonVolatileStorage.Description
- CIM_NonVolatileStorage.DeviceID
- CIM_NonVolatileStorage.EndingAddress
- CIM_NonVolatileStorage.ErrorAccess
- CIM_NonVolatileStorage.ErrorAddress
- CIM_NonVolatileStorage.ErrorCleared
- CIM_NonVolatileStorage.ErrorData
- CIM_NonVolatileStorage.ErrorDataOrder
- CIM_NonVolatileStorage.ErrorDescription
- CIM_NonVolatileStorage.ErrorInfo
- CIM_NonVolatileStorage.ErrorMethodology
- CIM_NonVolatileStorage.ErrorResolution
- CIM_NonVolatileStorage.ErrorTime
- CIM_NonVolatileStorage.ErrorTransferSize
- CIM_NonVolatileStorage.InstallDate
- CIM_NonVolatileStorage.IsWriteable
- CIM_NonVolatileStorage.LastErrorCode
- CIM_NonVolatileStorage.Name
- CIM_NonVolatileStorage.NumberOfBlocks
- CIM_NonVolatileStorage.OtherErrorDescription
- CIM_NonVolatileStorage.PNPDeviceID
- CIM_NonVolatileStorage.PowerManagementCapabilities
- CIM_NonVolatileStorage.PowerManagementSupported
- CIM_NonVolatileStorage.Purpose
- CIM_NonVolatileStorage.StartingAddress
- CIM_NonVolatileStorage.Status
- CIM_NonVolatileStorage.StatusInfo
- CIM_NonVolatileStorage.SystemCreationClassName
- CIM_NonVolatileStorage.SystemLevelAddress
- CIM_NonVolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fca29f0b279994dc0b844127fd1925850094da8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860756"
---
# <a name="cim_nonvolatilestorage-class"></a><span data-ttu-id="aff3b-104">CIM- \_ Nonvolatile Storage-Klasse</span><span class="sxs-lookup"><span data-stu-id="aff3b-104">CIM\_NonVolatileStorage class</span></span>

<span data-ttu-id="aff3b-105">Die **CIM-Klasse \_ NonVolatileStorage** stellt die Funktionen und die Verwaltung von nichtflüchtigem Speicher dar.</span><span class="sxs-lookup"><span data-stu-id="aff3b-105">The **CIM\_NonVolatileStorage** class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="aff3b-106">Nicht flüchtiger Speicher umfasst nativ Flash-und ROM-Speicher.</span><span class="sxs-lookup"><span data-stu-id="aff3b-106">Nonvolatile memory natively includes flash and ROM storage.</span></span> <span data-ttu-id="aff3b-107">Außerdem kann ein nicht flüchtiger Speicher auf flüchtiger Speicherung basieren, wenn der flüchtige Speicher durch einen Akku gestützt wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-107">In addition, nonvolatile memory can be based on volatile storage, if the volatile memory is backed by a battery.</span></span> <span data-ttu-id="aff3b-108">Dieses Szenario wird z. b. durch eine Instanz der [**CIM \_ associatedakku**](cim-associatedbattery.md) -Beziehung beschrieben, die auf den nicht flüchtigen Speicher als **abhängigen** und den Akku als **Vorgänger** verweist, und eine Instanz der [**CIM- \_ BasedOn**](cim-basedon.md) -Beziehung, die auf den nicht flüchtigen Speicher als **abhängigen** und den flüchtigen Speicher als **Vorgänger** verweist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-108">For example, this scenario would be described by an instance of the [**CIM\_AssociatedBattery**](cim-associatedbattery.md) relationship that references the nonvolatile storage as the **Dependent** and the battery as the **Antecedent**; and an instance of the [**CIM\_BasedOn**](cim-basedon.md) relationship that references the non-volatile storage as the **Dependent** and the volatile storage as the **Antecedent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aff3b-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aff3b-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aff3b-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aff3b-111">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="aff3b-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aff3b-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff3b-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff3b-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{18074AFA-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_NonVolatileStorage : CIM_Memory
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
  boolean  IsWriteable;
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

## <a name="members"></a><span data-ttu-id="aff3b-114">Member</span><span class="sxs-lookup"><span data-stu-id="aff3b-114">Members</span></span>

<span data-ttu-id="aff3b-115">Die **CIM-Klasse \_ Nonvolatile Storage** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aff3b-115">The **CIM\_NonVolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="aff3b-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="aff3b-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="aff3b-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aff3b-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aff3b-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="aff3b-118">Methods</span></span>

<span data-ttu-id="aff3b-119">Die **CIM-Klasse \_ Nonvolatile Storage** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-119">The **CIM\_NonVolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="aff3b-120">Methode</span><span class="sxs-lookup"><span data-stu-id="aff3b-120">Method</span></span>                                                                        | <span data-ttu-id="aff3b-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aff3b-121">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aff3b-122">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="aff3b-122">**Reset**</span></span>](reset-method-in-class-cim-nonvolatilestorage.md)                 | <span data-ttu-id="aff3b-123">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="aff3b-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="aff3b-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="aff3b-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="aff3b-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-nonvolatilestorage.md) | <span data-ttu-id="aff3b-126">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aff3b-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="aff3b-127">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="aff3b-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aff3b-128">Properties</span></span>

<span data-ttu-id="aff3b-129">Die **CIM-Klasse \_ Nonvolatile Storage** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aff3b-129">The **CIM\_NonVolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aff3b-130">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="aff3b-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aff3b-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-133">Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="aff3b-133">Read/write properties of the media.</span></span>

<span data-ttu-id="aff3b-134">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-135">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="aff3b-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="aff3b-136">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="aff3b-137">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="aff3b-138">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="aff3b-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="aff3b-139">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="aff3b-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="aff3b-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-141">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="aff3b-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,18 "," MIF. DMTF \| physikalisches Speicher Array \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="aff3b-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-144">Ein Array von Oktetten, die zusätzliche Fehlerinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="aff3b-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="aff3b-145">Ein Beispiel hierfür ist die Fehlerüberprüfung und Korrektur (ECC) oder die Rückgabe der Prüfbits, wenn eine CRC-basierte Fehler Methodik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="aff3b-146">Wenn in letzterem Fall ein Single-Bit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, kann das genaue Bit, das fehlgeschlagen ist, bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="aff3b-147">Diese Art von Daten (ECC-Syndrom, Check-Bit-oder Paritäts Bitdaten oder andere vom Hersteller bereitgestellte Informationen) ist in diesem Feld enthalten.</span><span class="sxs-lookup"><span data-stu-id="aff3b-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="aff3b-148">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-149">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-150">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="aff3b-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aff3b-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-153">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-154">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-154">Availability and status of the device.</span></span>

<span data-ttu-id="aff3b-155">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-155">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aff3b-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="aff3b-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="aff3b-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="aff3b-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="aff3b-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="aff3b-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="aff3b-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aff3b-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="aff3b-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="aff3b-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="aff3b-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="aff3b-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="aff3b-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="aff3b-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="aff3b-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aff3b-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="aff3b-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="aff3b-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="aff3b-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="aff3b-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="aff3b-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="aff3b-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="aff3b-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-169">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-169">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="aff3b-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="aff3b-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-171">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aff3b-171">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="aff3b-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="aff3b-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-173">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-173">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="aff3b-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="aff3b-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="aff3b-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="aff3b-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-176">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-176">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="aff3b-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="aff3b-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-178">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="aff3b-178">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="aff3b-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="aff3b-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-180">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="aff3b-180">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="aff3b-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="aff3b-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-182">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-182">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="aff3b-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="aff3b-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-184">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="aff3b-184">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-185">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="aff3b-185">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-186">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aff3b-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-188">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-189">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-189">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="aff3b-190">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-190">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="aff3b-191">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="aff3b-191">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter 1 (one).</span></span>

<span data-ttu-id="aff3b-192">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-192">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="aff3b-193">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aff3b-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-194">**Caption**</span><span class="sxs-lookup"><span data-stu-id="aff3b-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-197">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aff3b-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-198">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-198">Short textual description of the object.</span></span>

<span data-ttu-id="aff3b-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-200">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="aff3b-200">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aff3b-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-203">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aff3b-203">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-204">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="aff3b-204">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="aff3b-205">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-205">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="aff3b-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="aff3b-207"> (0)</span><span class="sxs-lookup"><span data-stu-id="aff3b-207">(0)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-208">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="aff3b-208">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="aff3b-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="aff3b-210">(1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-210">(1)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-211">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-211">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aff3b-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="aff3b-213">(2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-213">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="aff3b-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="aff3b-215">(3)</span><span class="sxs-lookup"><span data-stu-id="aff3b-215">(3)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-216">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="aff3b-216">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aff3b-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="aff3b-218">(4)</span><span class="sxs-lookup"><span data-stu-id="aff3b-218">(4)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-219">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="aff3b-219">Device is not working properly.</span></span> <span data-ttu-id="aff3b-220">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-220">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="aff3b-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="aff3b-222">(5)</span><span class="sxs-lookup"><span data-stu-id="aff3b-222">(5)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-223">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="aff3b-223">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="aff3b-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="aff3b-225"> (6)</span><span class="sxs-lookup"><span data-stu-id="aff3b-225">(6)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-226">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="aff3b-226">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="aff3b-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="aff3b-228">(7)</span><span class="sxs-lookup"><span data-stu-id="aff3b-228">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="aff3b-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="aff3b-230">(8)</span><span class="sxs-lookup"><span data-stu-id="aff3b-230">(8)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-231">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-231">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="aff3b-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="aff3b-233">(9)</span><span class="sxs-lookup"><span data-stu-id="aff3b-233">(9)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-234">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="aff3b-234">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="aff3b-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="aff3b-236">(10)</span><span class="sxs-lookup"><span data-stu-id="aff3b-236">(10)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-237">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-237">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="aff3b-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="aff3b-239">(11)</span><span class="sxs-lookup"><span data-stu-id="aff3b-239">(11)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-240">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="aff3b-240">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="aff3b-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="aff3b-242">(12)</span><span class="sxs-lookup"><span data-stu-id="aff3b-242">(12)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-243">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-243">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="aff3b-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="aff3b-245">(13)</span><span class="sxs-lookup"><span data-stu-id="aff3b-245">(13)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-246">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-246">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="aff3b-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="aff3b-248">(14)</span><span class="sxs-lookup"><span data-stu-id="aff3b-248">(14)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-249">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-249">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="aff3b-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="aff3b-251">(15)</span><span class="sxs-lookup"><span data-stu-id="aff3b-251">(15)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-252">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="aff3b-252">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="aff3b-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="aff3b-254">(16)</span><span class="sxs-lookup"><span data-stu-id="aff3b-254">(16)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-255">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-255">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="aff3b-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="aff3b-257">(17)</span><span class="sxs-lookup"><span data-stu-id="aff3b-257">(17)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-258">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="aff3b-258">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aff3b-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="aff3b-260">(18)</span><span class="sxs-lookup"><span data-stu-id="aff3b-260">(18)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-261">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-261">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="aff3b-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="aff3b-263">(19)</span><span class="sxs-lookup"><span data-stu-id="aff3b-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aff3b-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="aff3b-265">(20)</span><span class="sxs-lookup"><span data-stu-id="aff3b-265">(20)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-266">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-266">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="aff3b-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="aff3b-268">(21)</span><span class="sxs-lookup"><span data-stu-id="aff3b-268">(21)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-269">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-269">System failure.</span></span> <span data-ttu-id="aff3b-270">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="aff3b-270">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="aff3b-271">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-271">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="aff3b-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="aff3b-273">(22)</span><span class="sxs-lookup"><span data-stu-id="aff3b-273">(22)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-274">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-274">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="aff3b-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="aff3b-276">(23)</span><span class="sxs-lookup"><span data-stu-id="aff3b-276">(23)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-277">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-277">System failure.</span></span> <span data-ttu-id="aff3b-278">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="aff3b-278">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="aff3b-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="aff3b-280">(24)</span><span class="sxs-lookup"><span data-stu-id="aff3b-280">(24)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-281">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-281">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aff3b-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aff3b-283">(25)</span><span class="sxs-lookup"><span data-stu-id="aff3b-283">(25)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-284">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aff3b-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aff3b-286">(26)</span><span class="sxs-lookup"><span data-stu-id="aff3b-286">(26)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-287">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-287">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="aff3b-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="aff3b-289">(27)</span><span class="sxs-lookup"><span data-stu-id="aff3b-289">(27)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-290">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aff3b-290">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="aff3b-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="aff3b-292">(28)</span><span class="sxs-lookup"><span data-stu-id="aff3b-292">(28)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-293">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-293">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="aff3b-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="aff3b-295">(29)</span><span class="sxs-lookup"><span data-stu-id="aff3b-295">(29)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-296">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-296">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="aff3b-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="aff3b-298">(30)</span><span class="sxs-lookup"><span data-stu-id="aff3b-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-299">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aff3b-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="aff3b-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="aff3b-301">31,5</span><span class="sxs-lookup"><span data-stu-id="aff3b-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-302">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-302">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-303">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="aff3b-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-304">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="aff3b-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-306">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aff3b-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-307">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="aff3b-308">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-309">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="aff3b-309">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-310">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="aff3b-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-312">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. Physisches DMTF- \| Speicher Array \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-313">**True** gibt an, dass der letzte Fehler korrigiert wurde.</span><span class="sxs-lookup"><span data-stu-id="aff3b-313">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="aff3b-314">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-314">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-315">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-315">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-316">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="aff3b-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-319">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aff3b-319">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-320">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-320">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="aff3b-321">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-321">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aff3b-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-323">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aff3b-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-326">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="aff3b-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-327">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-327">Textual description of the object.</span></span>

<span data-ttu-id="aff3b-328">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-329">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="aff3b-329">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-332">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aff3b-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-333">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="aff3b-333">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="aff3b-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-335">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="aff3b-335">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-336">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aff3b-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-338">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,4 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-339">Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für das Speicher Objekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-339">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="aff3b-340">Die Endadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="aff3b-340">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="aff3b-341">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="aff3b-342">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aff3b-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-343">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="aff3b-343">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aff3b-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-346">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,15 "," MIF. Physisches DMTF- \| Speicher Array \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-347">Enumeration, die den Speicherzugriffs Vorgang angibt, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="aff3b-347">Enumeration that indicates the memory access operation that caused the last error.</span></span> <span data-ttu-id="aff3b-348">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aff3b-348">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="aff3b-349">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-349">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-350">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-350">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aff3b-351">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-351">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-352">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-352">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="aff3b-353">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="aff3b-353">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="aff3b-354">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="aff3b-354">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="aff3b-355">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="aff3b-355">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-356">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="aff3b-356">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-357">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aff3b-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-359">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,19 "," MIF. DMTF- \| Speichergerät \| 002,20 "," MIF. Physisches DMTF- \| Speicher Array \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-360">Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="aff3b-360">Address of the last memory error.</span></span> <span data-ttu-id="aff3b-361">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aff3b-361">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="aff3b-362">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-362">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-363">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-363">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="aff3b-364">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aff3b-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-365">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="aff3b-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-366">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="aff3b-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-368">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="aff3b-368">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="aff3b-369">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-370">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="aff3b-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-371">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="aff3b-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-373">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,17 "," MIF. DMTF \| physikalisches Speicher Array \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="aff3b-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-374">Daten, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-374">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="aff3b-375">Die Daten belegen die ersten *n* Oktette des Arrays, die benötigt werden, um die Anzahl der Bits aufzunehmen, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-375">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="aff3b-376">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-376">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-377">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-377">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="aff3b-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-379">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aff3b-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-381">Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="aff3b-381">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="aff3b-382">Wenn **ErrorTransferSize** gleich 0 ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-382">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-383">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-383">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-384">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="aff3b-384">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="aff3b-385">**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-385">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="aff3b-386">**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-386">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-387">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="aff3b-387">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-390">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="aff3b-390">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="aff3b-391">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-392">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="aff3b-392">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-393">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aff3b-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-395">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,12 "," MIF. DMTF \| physikalisches Speicher Array \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**Othererrordescription**")</span><span class="sxs-lookup"><span data-stu-id="aff3b-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-396">Der Typ des Fehlers, der zuletzt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-396">Type of error that occurred most recently.</span></span> <span data-ttu-id="aff3b-397">Die Werte 12 bis 14 sind im CIM-Schema nicht definiert, da DMI die Semantik des Fehler Typs und die korrigierbare Tabelle vermischt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-397">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="aff3b-398">Ob ein Fehler korrigiert werden kann, wird in der Eigenschaft " **correctableerror** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="aff3b-398">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span> <span data-ttu-id="aff3b-399">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aff3b-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-401">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="aff3b-401">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-403">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="aff3b-403">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aff3b-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="aff3b-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-405">OK.</span><span class="sxs-lookup"><span data-stu-id="aff3b-405">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="aff3b-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="aff3b-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-407">Ungültiger Lesevorgang.</span><span class="sxs-lookup"><span data-stu-id="aff3b-407">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="aff3b-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="aff3b-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-409">Paritätsfehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-409">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="aff3b-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="aff3b-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-411">Einzelbit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-411">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="aff3b-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="aff3b-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-413">Double-Bit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-413">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="aff3b-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="aff3b-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-415">Multi-Bit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-415">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="aff3b-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="aff3b-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-417">Nibble-Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-417">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="aff3b-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="aff3b-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-419">Prüfsummen Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-419">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="aff3b-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="aff3b-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-421">CRC-Fehler.</span><span class="sxs-lookup"><span data-stu-id="aff3b-421">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="aff3b-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (12)</span><span class="sxs-lookup"><span data-stu-id="aff3b-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-423">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-423">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="aff3b-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (13)</span><span class="sxs-lookup"><span data-stu-id="aff3b-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-425">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-425">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="aff3b-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (14)</span><span class="sxs-lookup"><span data-stu-id="aff3b-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-427">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-427">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-428">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="aff3b-428">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-429">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-431">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-431">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-432">Gibt an, ob Paritäts Algorithmen, CRC-Algorithmen, ECC oder andere Mechanismen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-432">Specifies whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used.</span></span> <span data-ttu-id="aff3b-433">Details zum Algorithmus können auch bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-433">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="aff3b-434">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-434">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-435">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="aff3b-435">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-436">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aff3b-436">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-438">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,21 "," MIF. DMTF \| physikalisches Speicher Array \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-439">Bereich in Bytes, in den der letzte Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="aff3b-439">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="aff3b-440">Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden (d. h. auf einer typischen Seite), können Fehler in 4-KB-Grenzen aufgelöst werden, und diese Eigenschaft wird auf 4000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-440">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="aff3b-441">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-441">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-442">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="aff3b-443">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aff3b-443">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-444">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="aff3b-444">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-445">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="aff3b-445">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-447">Zeitpunkt, zu dem der letzte Speicherfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-447">Time that the last memory error occurred.</span></span> <span data-ttu-id="aff3b-448">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aff3b-448">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="aff3b-449">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-449">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-450">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-450">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-451">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="aff3b-451">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-452">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aff3b-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-454">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 002,16 "," MIF. DMTF \| physikalisches Speicher Array \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-455">Die Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="aff3b-455">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="aff3b-456">Der Wert 0 (null) gibt an, dass kein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-456">A value of 0 (zero) indicates no error.</span></span> <span data-ttu-id="aff3b-457">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, sollte diese Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-457">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="aff3b-458">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aff3b-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-460">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="aff3b-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-461">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-462">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-463">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-463">Date and time the object was installed.</span></span> <span data-ttu-id="aff3b-464">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-464">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aff3b-465">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-466">**Isschreibbar**</span><span class="sxs-lookup"><span data-stu-id="aff3b-466">**IsWriteable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-467">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="aff3b-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-469">**True** gibt an, dass ein nicht flüchtiger Speicher beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-469">If **TRUE**, non-volatile storage is writeable.</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aff3b-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-471">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aff3b-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-473">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="aff3b-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="aff3b-474">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-475">**Name**</span><span class="sxs-lookup"><span data-stu-id="aff3b-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-476">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-478">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="aff3b-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-479">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-479">Label by which the object is known.</span></span> <span data-ttu-id="aff3b-480">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="aff3b-481">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="aff3b-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-483">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aff3b-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-484">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-485">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-486">Gesamtanzahl der aufeinander folgenden Blöcke: jeder Block ist die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts, der den Speicherblock bildet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-486">Total number of consecutive blocks, each block is the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="aff3b-487">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="aff3b-488">Wenn der Wert von **BLOCKSIZE** 1 (eins) ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="aff3b-488">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="aff3b-489">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="aff3b-490">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aff3b-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-491">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="aff3b-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-492">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-493">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-494">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-Arbeits [**\_ Speicher**](cim-memory.md)".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="aff3b-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-495">Eine frei Form Zeichenfolge, die Informationen bereitstellt, wenn die **ErrorType** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-495">Free-form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="aff3b-496">Wenn nicht auf 1 festgelegt, hat diese Zeichenfolge keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-496">If not set to 1, this string has no meaning.</span></span>

<span data-ttu-id="aff3b-497">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="aff3b-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-499">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-501">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aff3b-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-502">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="aff3b-503">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="aff3b-504">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="aff3b-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-505">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="aff3b-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-506">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="aff3b-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-508">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="aff3b-509">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="aff3b-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aff3b-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aff3b-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aff3b-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="aff3b-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-514">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aff3b-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="aff3b-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="aff3b-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-516">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="aff3b-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="aff3b-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="aff3b-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-518">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="aff3b-519">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="aff3b-520">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="aff3b-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="aff3b-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="aff3b-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-522">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="aff3b-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="aff3b-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aff3b-524">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aff3b-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-525">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="aff3b-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-526">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="aff3b-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-527">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-528">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="aff3b-529">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="aff3b-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="aff3b-530">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="aff3b-531">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="aff3b-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="aff3b-532">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-533">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="aff3b-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-534">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-535">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-536">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="aff3b-537">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-538">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="aff3b-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-539">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aff3b-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-540">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-541">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,3 "," MIF "zugeordnet. Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-542">Die Anfangsadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="aff3b-542">Beginning address that is referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="aff3b-543">Die Startadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="aff3b-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="aff3b-544">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="aff3b-545">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aff3b-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-546">**Status**</span><span class="sxs-lookup"><span data-stu-id="aff3b-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-547">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-549">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="aff3b-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-550">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-550">Current status of the object.</span></span>

<span data-ttu-id="aff3b-551">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aff3b-552">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="aff3b-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aff3b-553">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="aff3b-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aff3b-554">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="aff3b-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aff3b-555">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="aff3b-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-556">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="aff3b-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aff3b-557">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="aff3b-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aff3b-558">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="aff3b-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aff3b-559">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aff3b-560">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="aff3b-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aff3b-561">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="aff3b-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aff3b-562">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="aff3b-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aff3b-563">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="aff3b-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aff3b-564">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="aff3b-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="aff3b-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-566">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aff3b-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-567">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-568">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="aff3b-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-569">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="aff3b-569">State of the logical device.</span></span> <span data-ttu-id="aff3b-570">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aff3b-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="aff3b-571">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aff3b-572">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="aff3b-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aff3b-573">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="aff3b-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aff3b-574">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="aff3b-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aff3b-575">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="aff3b-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aff3b-576">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="aff3b-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aff3b-577">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="aff3b-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-578">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-579">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-580">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aff3b-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-581">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="aff3b-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="aff3b-582">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="aff3b-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-584">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="aff3b-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-585">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-586">**True** gibt an, dass die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene sind.</span><span class="sxs-lookup"><span data-stu-id="aff3b-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="aff3b-587">**False** gibt an, dass es sich um eine physische Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-587">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="aff3b-588">Wenn die **errorInfo** -Eigenschaft gleich 3 ("OK") ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="aff3b-588">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="aff3b-589">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](cim-memory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-589">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff3b-590">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="aff3b-590">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aff3b-591">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aff3b-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-592">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aff3b-592">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aff3b-593">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aff3b-593">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aff3b-594">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="aff3b-594">Scoping system's name.</span></span>

<span data-ttu-id="aff3b-595">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aff3b-595">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aff3b-596">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aff3b-596">Remarks</span></span>

<span data-ttu-id="aff3b-597">Die **CIM-Klasse \_ Nonvolatile Storage** wird vom [**CIM- \_ Speicher**](cim-memory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-597">The **CIM\_NonVolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="aff3b-598">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="aff3b-598">WMI does not implement this class.</span></span>

<span data-ttu-id="aff3b-599">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="aff3b-599">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aff3b-600">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aff3b-600">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff3b-601">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff3b-601">Requirements</span></span>



| <span data-ttu-id="aff3b-602">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff3b-602">Requirement</span></span> | <span data-ttu-id="aff3b-603">Wert</span><span class="sxs-lookup"><span data-stu-id="aff3b-603">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aff3b-604">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aff3b-604">Minimum supported client</span></span><br/> | <span data-ttu-id="aff3b-605">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aff3b-605">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aff3b-606">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aff3b-606">Minimum supported server</span></span><br/> | <span data-ttu-id="aff3b-607">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aff3b-607">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aff3b-608">Namespace</span><span class="sxs-lookup"><span data-stu-id="aff3b-608">Namespace</span></span><br/>                | <span data-ttu-id="aff3b-609">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aff3b-609">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aff3b-610">MOF</span><span class="sxs-lookup"><span data-stu-id="aff3b-610">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aff3b-611"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aff3b-611"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aff3b-612">DLL</span><span class="sxs-lookup"><span data-stu-id="aff3b-612">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aff3b-613"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aff3b-613"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff3b-614">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aff3b-614">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff3b-615">**CIM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="aff3b-615">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

