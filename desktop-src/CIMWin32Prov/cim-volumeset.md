---
description: Die CIM \_ volumeset-Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die der Betriebsumgebung zum Lesen und Schreiben von Benutzerdaten präsentiert werden.
ms.assetid: f0350185-6210-4f95-a2a2-23de61b1af1f
ms.tgt_platform: multiple
title: CIM_VolumeSet-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolumeSet
- CIM_VolumeSet.Access
- CIM_VolumeSet.Availability
- CIM_VolumeSet.BlockSize
- CIM_VolumeSet.Caption
- CIM_VolumeSet.ConfigManagerErrorCode
- CIM_VolumeSet.ConfigManagerUserConfig
- CIM_VolumeSet.CreationClassName
- CIM_VolumeSet.Description
- CIM_VolumeSet.DeviceID
- CIM_VolumeSet.ErrorCleared
- CIM_VolumeSet.ErrorDescription
- CIM_VolumeSet.ErrorMethodology
- CIM_VolumeSet.InstallDate
- CIM_VolumeSet.LastErrorCode
- CIM_VolumeSet.Name
- CIM_VolumeSet.NumberOfBlocks
- CIM_VolumeSet.PNPDeviceID
- CIM_VolumeSet.PowerManagementCapabilities
- CIM_VolumeSet.PowerManagementSupported
- CIM_VolumeSet.PSExtentInterleaveDepth
- CIM_VolumeSet.PSExtentStripeLength
- CIM_VolumeSet.Purpose
- CIM_VolumeSet.Status
- CIM_VolumeSet.StatusInfo
- CIM_VolumeSet.SystemCreationClassName
- CIM_VolumeSet.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ee8cd96381901250c9a15e544ee1963470565b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340105"
---
# <a name="cim_volumeset-class"></a><span data-ttu-id="2ed08-103">CIM \_ volumeset-Klasse</span><span class="sxs-lookup"><span data-stu-id="2ed08-103">CIM\_VolumeSet class</span></span>

<span data-ttu-id="2ed08-104">Die **CIM \_ volumeset** -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die der Betriebsumgebung zum Lesen und Schreiben von Benutzerdaten präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-104">The **CIM\_VolumeSet** class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span> <span data-ttu-id="2ed08-105">Volumesets sollten sich nicht überlappen und basieren auf einem oder mehreren physischen Blöcken, Blöcke mit geschütztem Speicherplatz oder Aggregat Blöcken (alle vom gleichen Typ).</span><span class="sxs-lookup"><span data-stu-id="2ed08-105">Volume sets should not overlap one another and are based on one or more physical extents, protected space extents, or aggregate extents (all of the same type).</span></span> <span data-ttu-id="2ed08-106">Die basierten Zuordnungen sollten bei Bedarf instanziiert oder untergeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-106">The based-on associations should be instantiated or subclassed as needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ed08-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2ed08-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2ed08-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2ed08-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2ed08-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2ed08-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2ed08-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed08-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ed08-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{35E25AA5-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VolumeSet : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   PSExtentInterleaveDepth;
  uint64   PSExtentStripeLength;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="2ed08-112">Member</span><span class="sxs-lookup"><span data-stu-id="2ed08-112">Members</span></span>

<span data-ttu-id="2ed08-113">Die **CIM \_ volumeset** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2ed08-113">The **CIM\_VolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="2ed08-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ed08-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ed08-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ed08-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ed08-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ed08-116">Methods</span></span>

<span data-ttu-id="2ed08-117">Die **CIM \_ volumeset** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-117">The **CIM\_VolumeSet** class has these methods.</span></span>



| <span data-ttu-id="2ed08-118">Methode</span><span class="sxs-lookup"><span data-stu-id="2ed08-118">Method</span></span>                                                               | <span data-ttu-id="2ed08-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ed08-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ed08-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="2ed08-120">**Reset**</span></span>](reset-method-in-class-cim-volumeset.md)                 | <span data-ttu-id="2ed08-121">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="2ed08-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="2ed08-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2ed08-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2ed08-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volumeset.md) | <span data-ttu-id="2ed08-124">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ed08-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2ed08-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2ed08-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ed08-126">Properties</span></span>

<span data-ttu-id="2ed08-127">Die **CIM \_ volumeset** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2ed08-127">The **CIM\_VolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ed08-128">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="2ed08-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ed08-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-131">Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="2ed08-131">Read/write properties of the media.</span></span>

<span data-ttu-id="2ed08-132">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2ed08-133">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2ed08-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="2ed08-134">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="2ed08-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="2ed08-135">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="2ed08-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="2ed08-136">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="2ed08-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="2ed08-137">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="2ed08-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2ed08-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="2ed08-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ed08-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-141">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-142">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-142">Availability and status of the device.</span></span>

<span data-ttu-id="2ed08-143">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2ed08-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2ed08-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2ed08-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="2ed08-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2ed08-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="2ed08-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2ed08-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="2ed08-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2ed08-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="2ed08-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2ed08-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="2ed08-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2ed08-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="2ed08-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2ed08-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="2ed08-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2ed08-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="2ed08-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2ed08-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="2ed08-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2ed08-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="2ed08-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2ed08-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="2ed08-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2ed08-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="2ed08-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-157">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2ed08-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="2ed08-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-159">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2ed08-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2ed08-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="2ed08-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-161">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2ed08-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="2ed08-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2ed08-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="2ed08-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-164">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="2ed08-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2ed08-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="2ed08-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-166">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="2ed08-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2ed08-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="2ed08-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-168">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="2ed08-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2ed08-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="2ed08-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-170">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2ed08-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="2ed08-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-172">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="2ed08-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2ed08-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2ed08-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-174">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2ed08-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-176">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-177">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="2ed08-178">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="2ed08-179">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="2ed08-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="2ed08-180">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-180">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2ed08-181">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2ed08-181">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2ed08-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-185">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2ed08-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-186">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-186">Short textual description of the object.</span></span>

<span data-ttu-id="2ed08-187">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-188">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="2ed08-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-189">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2ed08-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-191">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2ed08-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-192">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2ed08-192">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="2ed08-193">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2ed08-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2ed08-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="2ed08-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-196">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2ed08-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2ed08-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2ed08-198">(1)</span><span class="sxs-lookup"><span data-stu-id="2ed08-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-199">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2ed08-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2ed08-201">(2)</span><span class="sxs-lookup"><span data-stu-id="2ed08-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2ed08-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2ed08-203">(3)</span><span class="sxs-lookup"><span data-stu-id="2ed08-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-204">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2ed08-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2ed08-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2ed08-206">(4)</span><span class="sxs-lookup"><span data-stu-id="2ed08-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-207">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2ed08-207">Device is not working properly.</span></span> <span data-ttu-id="2ed08-208">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2ed08-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2ed08-210">(5)</span><span class="sxs-lookup"><span data-stu-id="2ed08-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-211">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ed08-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2ed08-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2ed08-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="2ed08-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-214">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="2ed08-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2ed08-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2ed08-216">(7)</span><span class="sxs-lookup"><span data-stu-id="2ed08-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2ed08-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2ed08-218">(8)</span><span class="sxs-lookup"><span data-stu-id="2ed08-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-219">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2ed08-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2ed08-221">(9)</span><span class="sxs-lookup"><span data-stu-id="2ed08-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-222">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2ed08-222">Device is not working properly.</span></span> <span data-ttu-id="2ed08-223">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="2ed08-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2ed08-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2ed08-225">(10)</span><span class="sxs-lookup"><span data-stu-id="2ed08-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-226">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2ed08-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2ed08-228">(11)</span><span class="sxs-lookup"><span data-stu-id="2ed08-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-229">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="2ed08-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2ed08-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2ed08-231">(12)</span><span class="sxs-lookup"><span data-stu-id="2ed08-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-232">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2ed08-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2ed08-234">(13)</span><span class="sxs-lookup"><span data-stu-id="2ed08-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-235">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2ed08-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2ed08-237">(14)</span><span class="sxs-lookup"><span data-stu-id="2ed08-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-238">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2ed08-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2ed08-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2ed08-240">(15)</span><span class="sxs-lookup"><span data-stu-id="2ed08-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-241">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2ed08-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2ed08-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2ed08-243">(16)</span><span class="sxs-lookup"><span data-stu-id="2ed08-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-244">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2ed08-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2ed08-246">(17)</span><span class="sxs-lookup"><span data-stu-id="2ed08-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-247">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="2ed08-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2ed08-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2ed08-249">(18)</span><span class="sxs-lookup"><span data-stu-id="2ed08-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-250">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2ed08-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2ed08-252">(19)</span><span class="sxs-lookup"><span data-stu-id="2ed08-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2ed08-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2ed08-254">(20)</span><span class="sxs-lookup"><span data-stu-id="2ed08-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-255">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2ed08-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2ed08-257">(21)</span><span class="sxs-lookup"><span data-stu-id="2ed08-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-258">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="2ed08-258">System failure.</span></span> <span data-ttu-id="2ed08-259">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2ed08-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2ed08-260">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2ed08-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2ed08-262">(22)</span><span class="sxs-lookup"><span data-stu-id="2ed08-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-263">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2ed08-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2ed08-265">(23)</span><span class="sxs-lookup"><span data-stu-id="2ed08-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-266">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="2ed08-266">System failure.</span></span> <span data-ttu-id="2ed08-267">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2ed08-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2ed08-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2ed08-269">(24)</span><span class="sxs-lookup"><span data-stu-id="2ed08-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-270">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2ed08-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2ed08-272">(25)</span><span class="sxs-lookup"><span data-stu-id="2ed08-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-273">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="2ed08-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2ed08-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2ed08-275">(26)</span><span class="sxs-lookup"><span data-stu-id="2ed08-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-276">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="2ed08-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2ed08-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2ed08-278">(27)</span><span class="sxs-lookup"><span data-stu-id="2ed08-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-279">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2ed08-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2ed08-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2ed08-281">(28)</span><span class="sxs-lookup"><span data-stu-id="2ed08-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-282">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2ed08-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2ed08-284">(29)</span><span class="sxs-lookup"><span data-stu-id="2ed08-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-285">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-285">Device is disabled.</span></span> <span data-ttu-id="2ed08-286">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2ed08-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2ed08-288">(30)</span><span class="sxs-lookup"><span data-stu-id="2ed08-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-289">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ed08-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2ed08-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="2ed08-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2ed08-291">31,5</span><span class="sxs-lookup"><span data-stu-id="2ed08-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-292">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2ed08-292">Device is not working properly.</span></span> <span data-ttu-id="2ed08-293">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2ed08-294">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="2ed08-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-295">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2ed08-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-297">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2ed08-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-298">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ed08-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2ed08-299">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-300">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="2ed08-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-303">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2ed08-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-304">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ed08-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2ed08-305">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2ed08-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-307">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ed08-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-310">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2ed08-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-311">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-311">Textual description of the object.</span></span>

<span data-ttu-id="2ed08-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2ed08-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-316">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2ed08-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-317">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="2ed08-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2ed08-318">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-319">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="2ed08-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-320">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2ed08-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-322">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2ed08-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2ed08-323">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2ed08-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-327">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="2ed08-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2ed08-328">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-329">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="2ed08-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-332">Eine frei Form Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, der vom Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2ed08-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="2ed08-333">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2ed08-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-335">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2ed08-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-337">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-338">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-338">Date and time the object was installed.</span></span> <span data-ttu-id="2ed08-339">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2ed08-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2ed08-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2ed08-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-342">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2ed08-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-344">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2ed08-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2ed08-345">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-346">**Name**</span><span class="sxs-lookup"><span data-stu-id="2ed08-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-349">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2ed08-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-350">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2ed08-350">Label by which the object is known.</span></span> <span data-ttu-id="2ed08-351">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2ed08-352">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="2ed08-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-354">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2ed08-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-356">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-357">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="2ed08-358">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="2ed08-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="2ed08-359">Wenn der Wert von **BLOCKSIZE** 1 (eins) ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="2ed08-359">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="2ed08-360">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2ed08-361">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2ed08-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2ed08-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-363">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-365">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2ed08-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-366">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="2ed08-367">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2ed08-368">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2ed08-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-369">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="2ed08-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-370">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2ed08-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-372">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2ed08-373">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2ed08-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2ed08-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2ed08-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="2ed08-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2ed08-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="2ed08-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2ed08-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="2ed08-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-378">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ed08-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2ed08-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="2ed08-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-380">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="2ed08-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2ed08-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="2ed08-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-382">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2ed08-383">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-383">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="2ed08-384">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2ed08-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2ed08-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="2ed08-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-386">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2ed08-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2ed08-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="2ed08-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2ed08-388">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2ed08-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2ed08-389">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="2ed08-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-390">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2ed08-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-392">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2ed08-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2ed08-393">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="2ed08-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2ed08-394">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2ed08-395">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="2ed08-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="2ed08-396">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-397">**Psextentinterleavetiefe**</span><span class="sxs-lookup"><span data-stu-id="2ed08-397">**PSExtentInterleaveDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-398">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2ed08-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-400">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| volumensatz \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-401">Die Anzahl der Blöcke, die für den Bereich des geschützten Bereichs als Sammel Satz erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-401">Number of protected space extents to stripe as a collective set.</span></span> <span data-ttu-id="2ed08-402">In SCC ist dieser Wert als die Anzahl der zu zählenden Streifen definiert, bevor die Zuordnung zum nächsten zusammenhängenden Satz von Blöcken hinter dem aktuellen Stripe fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2ed08-402">In SCC, this value is defined as the number of stripes to count before continuing to map into the next contiguous set of extents, beyond the current stripe.</span></span>

<span data-ttu-id="2ed08-403">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2ed08-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-404">**Psextentstripelength**</span><span class="sxs-lookup"><span data-stu-id="2ed08-404">**PSExtentStripeLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-405">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2ed08-405">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-407">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| volumensatz \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-408">Anzahl von zusammenhängenden geschützten Speicherbereichen, die vor dem Schleifen Einzug zum ersten geschützten Bereichs Bereich des aktuellen Streifens gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-408">Number of contiguous protected space extents counted before looping back to the first protected space extent of the current stripe.</span></span> <span data-ttu-id="2ed08-409">Dabei handelt es sich um die Anzahl von Blöcken, die den Benutzerdaten Streifen bilden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-409">It is the number of extents forming the user data stripe.</span></span>

<span data-ttu-id="2ed08-410">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2ed08-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-411">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="2ed08-411">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-414">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-414">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="2ed08-415">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-415">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-416">**Status**</span><span class="sxs-lookup"><span data-stu-id="2ed08-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-417">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-419">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2ed08-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-420">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-420">Current status of the object.</span></span> <span data-ttu-id="2ed08-421">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2ed08-422">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="2ed08-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2ed08-423">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2ed08-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2ed08-424">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="2ed08-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2ed08-425">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="2ed08-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2ed08-426">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="2ed08-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2ed08-427">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="2ed08-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2ed08-428">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="2ed08-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2ed08-429">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2ed08-430">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="2ed08-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2ed08-431">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="2ed08-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2ed08-432">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="2ed08-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2ed08-433">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="2ed08-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2ed08-434">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="2ed08-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2ed08-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2ed08-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-436">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ed08-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-438">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2ed08-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-439">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="2ed08-439">State of the logical device.</span></span> <span data-ttu-id="2ed08-440">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ed08-440">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2ed08-441">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2ed08-442">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2ed08-442">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2ed08-443">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="2ed08-443">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2ed08-444">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="2ed08-444">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2ed08-445">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="2ed08-445">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2ed08-446">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="2ed08-446">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2ed08-447">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="2ed08-447">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-450">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2ed08-450">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-451">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2ed08-451">Scoping system's creation class name.</span></span>

<span data-ttu-id="2ed08-452">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed08-453">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="2ed08-453">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ed08-454">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ed08-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ed08-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ed08-456">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2ed08-456">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2ed08-457">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2ed08-457">Scoping system's name.</span></span>

<span data-ttu-id="2ed08-458">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2ed08-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ed08-459">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ed08-459">Remarks</span></span>

<span data-ttu-id="2ed08-460">Die **CIM- \_ volumeset** -Klasse wird von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2ed08-460">The **CIM\_VolumeSet** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2ed08-461">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2ed08-461">WMI does not implement this class.</span></span>

<span data-ttu-id="2ed08-462">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2ed08-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2ed08-463">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2ed08-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed08-464">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ed08-464">Requirements</span></span>



| <span data-ttu-id="2ed08-465">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ed08-465">Requirement</span></span> | <span data-ttu-id="2ed08-466">Wert</span><span class="sxs-lookup"><span data-stu-id="2ed08-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed08-467">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ed08-467">Minimum supported client</span></span><br/> | <span data-ttu-id="2ed08-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ed08-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ed08-469">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ed08-469">Minimum supported server</span></span><br/> | <span data-ttu-id="2ed08-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ed08-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ed08-471">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ed08-471">Namespace</span></span><br/>                | <span data-ttu-id="2ed08-472">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2ed08-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2ed08-473">MOF</span><span class="sxs-lookup"><span data-stu-id="2ed08-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ed08-474"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2ed08-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ed08-475">DLL</span><span class="sxs-lookup"><span data-stu-id="2ed08-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ed08-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ed08-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed08-477">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ed08-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed08-478">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="2ed08-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

