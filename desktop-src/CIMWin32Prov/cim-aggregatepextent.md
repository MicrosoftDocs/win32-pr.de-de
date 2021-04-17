---
description: Die CIM- \_ aggregatepblock-Klasse bietet zusammenfassende Informationen über adressierbare logische Blöcke, die sich in derselben Speicher Redundanz Gruppe befinden und sich auf demselben physischen Medium befinden.
ms.assetid: c8def347-e8d7-48d5-94d0-f6e704e7b40e
ms.tgt_platform: multiple
title: CIM_AggregatePExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent
- CIM_AggregatePExtent.Caption
- CIM_AggregatePExtent.Description
- CIM_AggregatePExtent.InstallDate
- CIM_AggregatePExtent.Name
- CIM_AggregatePExtent.Status
- CIM_AggregatePExtent.Availability
- CIM_AggregatePExtent.ConfigManagerErrorCode
- CIM_AggregatePExtent.ConfigManagerUserConfig
- CIM_AggregatePExtent.CreationClassName
- CIM_AggregatePExtent.DeviceID
- CIM_AggregatePExtent.PowerManagementCapabilities
- CIM_AggregatePExtent.ErrorCleared
- CIM_AggregatePExtent.ErrorDescription
- CIM_AggregatePExtent.LastErrorCode
- CIM_AggregatePExtent.PNPDeviceID
- CIM_AggregatePExtent.PowerManagementSupported
- CIM_AggregatePExtent.StatusInfo
- CIM_AggregatePExtent.SystemCreationClassName
- CIM_AggregatePExtent.SystemName
- CIM_AggregatePExtent.Access
- CIM_AggregatePExtent.BlockSize
- CIM_AggregatePExtent.ErrorMethodology
- CIM_AggregatePExtent.Purpose
- CIM_AggregatePExtent.NumberOfBlocks
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2f1b2b5b7e08876317888d02d4830cd72659bc0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523904"
---
# <a name="cim_aggregatepextent-class"></a><span data-ttu-id="5173a-103">CIM- \_ aggregatepblock-Klasse</span><span class="sxs-lookup"><span data-stu-id="5173a-103">CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="5173a-104">Die **CIM- \_ aggregatepblock** -Klasse bietet zusammenfassende Informationen über adressierbare logische Blöcke, die sich in derselben Speicher Redundanz Gruppe befinden und sich auf demselben physischen Medium befinden.</span><span class="sxs-lookup"><span data-stu-id="5173a-104">The **CIM\_AggregatePExtent** class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

<span data-ttu-id="5173a-105">Die **CIM- \_ aggregatepblock** -Klasse ist eine alternative Gruppierung für physische Blöcke, wenn nur Zusammenfassungs Informationen benötigt werden oder wenn die automatische Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5173a-105">The **CIM\_AggregatePExtent** class is an alternative grouping for physical extents when only summary information is needed, or when automatic configuration is used.</span></span> <span data-ttu-id="5173a-106">Die automatische Konfiguration kann dazu führen, dass Tausende physischer Blöcke definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-106">Automatic configuration can result in thousands of physical extents being defined.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5173a-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5173a-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5173a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5173a-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="5173a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5173a-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5173a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5173a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5173a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979F-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AggregatePExtent : CIM_StorageExtent
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
  string   ErrorMethodology;
  string   Purpose;
  uint64   NumberOfBlocks;
};
```

## <a name="members"></a><span data-ttu-id="5173a-112">Member</span><span class="sxs-lookup"><span data-stu-id="5173a-112">Members</span></span>

<span data-ttu-id="5173a-113">Die **CIM- \_ aggregatepblock** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5173a-113">The **CIM\_AggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="5173a-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="5173a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="5173a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5173a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5173a-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="5173a-116">Methods</span></span>

<span data-ttu-id="5173a-117">Die **CIM- \_ aggregatepblock** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5173a-117">The **CIM\_AggregatePExtent** class has these methods.</span></span>



| <span data-ttu-id="5173a-118">Methode</span><span class="sxs-lookup"><span data-stu-id="5173a-118">Method</span></span>                                                                      | <span data-ttu-id="5173a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5173a-119">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5173a-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="5173a-120">**Reset**</span></span>](reset-method-in-class-cim-aggregatepextent.md)                 | <span data-ttu-id="5173a-121">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="5173a-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="5173a-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="5173a-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="5173a-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5173a-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md) | <span data-ttu-id="5173a-124">Definiert den gewünschten Energiezustand für ein logisches Gerät und den Zeitpunkt, zu dem das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5173a-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="5173a-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="5173a-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5173a-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5173a-126">Properties</span></span>

<span data-ttu-id="5173a-127">Die **CIM- \_ aggregatepblock** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5173a-127">The **CIM\_AggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5173a-128">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="5173a-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5173a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-131">Beschreibt die Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="5173a-131">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="5173a-132">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5173a-133">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5173a-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="5173a-134">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="5173a-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="5173a-135">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="5173a-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="5173a-136">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="5173a-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="5173a-137">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="5173a-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5173a-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="5173a-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5173a-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-141">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="5173a-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-142">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="5173a-142">Availability and status of the device.</span></span>

<span data-ttu-id="5173a-143">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5173a-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="5173a-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5173a-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="5173a-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5173a-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="5173a-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5173a-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="5173a-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5173a-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="5173a-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5173a-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="5173a-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5173a-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="5173a-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5173a-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="5173a-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5173a-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="5173a-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5173a-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="5173a-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5173a-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="5173a-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5173a-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="5173a-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5173a-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="5173a-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-157">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="5173a-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5173a-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="5173a-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-159">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5173a-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5173a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="5173a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-161">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-161">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5173a-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="5173a-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5173a-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="5173a-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-164">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="5173a-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5173a-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="5173a-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-166">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="5173a-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5173a-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="5173a-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-168">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="5173a-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5173a-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="5173a-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-170">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5173a-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5173a-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="5173a-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-172">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="5173a-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5173a-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="5173a-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-174">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5173a-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-176">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="5173a-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-177">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="5173a-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="5173a-178">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="5173a-179">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="5173a-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="5173a-180">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5173a-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5173a-181">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5173a-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-185">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5173a-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-186">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5173a-186">A short textual description of the object.</span></span>

<span data-ttu-id="5173a-187">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-188">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="5173a-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-189">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5173a-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-191">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5173a-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-192">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5173a-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5173a-193">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5173a-194">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="5173a-194">**This device is working properly.**</span></span> <span data-ttu-id="5173a-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="5173a-195">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5173a-196">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="5173a-196">**This device is not configured correctly.**</span></span> <span data-ttu-id="5173a-197">(1)</span><span class="sxs-lookup"><span data-stu-id="5173a-197">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5173a-198">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="5173a-198">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5173a-199">(2)</span><span class="sxs-lookup"><span data-stu-id="5173a-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5173a-200">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="5173a-200">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5173a-201">(3)</span><span class="sxs-lookup"><span data-stu-id="5173a-201">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5173a-202">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="5173a-202">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5173a-203">(4)</span><span class="sxs-lookup"><span data-stu-id="5173a-203">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5173a-204">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="5173a-204">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5173a-205">(5)</span><span class="sxs-lookup"><span data-stu-id="5173a-205">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5173a-206">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="5173a-206">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5173a-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="5173a-207">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5173a-208">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="5173a-208">**Cannot filter.**</span></span> <span data-ttu-id="5173a-209">(7)</span><span class="sxs-lookup"><span data-stu-id="5173a-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5173a-210">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="5173a-210">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5173a-211">(8)</span><span class="sxs-lookup"><span data-stu-id="5173a-211">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5173a-212">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="5173a-212">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5173a-213">(9)</span><span class="sxs-lookup"><span data-stu-id="5173a-213">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5173a-214">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="5173a-214">**This device cannot start.**</span></span> <span data-ttu-id="5173a-215">(10)</span><span class="sxs-lookup"><span data-stu-id="5173a-215">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5173a-216">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="5173a-216">**This device failed.**</span></span> <span data-ttu-id="5173a-217">(11)</span><span class="sxs-lookup"><span data-stu-id="5173a-217">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5173a-218">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="5173a-218">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5173a-219">(12)</span><span class="sxs-lookup"><span data-stu-id="5173a-219">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5173a-220">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="5173a-220">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5173a-221">(13)</span><span class="sxs-lookup"><span data-stu-id="5173a-221">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5173a-222">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="5173a-222">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5173a-223">(14)</span><span class="sxs-lookup"><span data-stu-id="5173a-223">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5173a-224">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="5173a-224">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5173a-225">(15)</span><span class="sxs-lookup"><span data-stu-id="5173a-225">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5173a-226">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="5173a-226">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5173a-227">(16)</span><span class="sxs-lookup"><span data-stu-id="5173a-227">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5173a-228">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="5173a-228">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5173a-229">(17)</span><span class="sxs-lookup"><span data-stu-id="5173a-229">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5173a-230">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="5173a-230">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5173a-231">(18)</span><span class="sxs-lookup"><span data-stu-id="5173a-231">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5173a-232">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="5173a-232">**Failure using the VxD loader.**</span></span> <span data-ttu-id="5173a-233">(19)</span><span class="sxs-lookup"><span data-stu-id="5173a-233">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5173a-234">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="5173a-234">**Your registry might be corrupted.**</span></span> <span data-ttu-id="5173a-235">(20)</span><span class="sxs-lookup"><span data-stu-id="5173a-235">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5173a-236">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="5173a-236">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5173a-237">(21)</span><span class="sxs-lookup"><span data-stu-id="5173a-237">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5173a-238">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="5173a-238">**This device is disabled.**</span></span> <span data-ttu-id="5173a-239">(22)</span><span class="sxs-lookup"><span data-stu-id="5173a-239">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5173a-240">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="5173a-240">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5173a-241">(23)</span><span class="sxs-lookup"><span data-stu-id="5173a-241">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5173a-242">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="5173a-242">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5173a-243">(24)</span><span class="sxs-lookup"><span data-stu-id="5173a-243">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5173a-244">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="5173a-244">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5173a-245">(25)</span><span class="sxs-lookup"><span data-stu-id="5173a-245">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5173a-246">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="5173a-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5173a-247">(26)</span><span class="sxs-lookup"><span data-stu-id="5173a-247">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5173a-248">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="5173a-248">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5173a-249">(27)</span><span class="sxs-lookup"><span data-stu-id="5173a-249">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5173a-250">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="5173a-250">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5173a-251">(28)</span><span class="sxs-lookup"><span data-stu-id="5173a-251">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5173a-252">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="5173a-252">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5173a-253">(29)</span><span class="sxs-lookup"><span data-stu-id="5173a-253">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5173a-254">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="5173a-254">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5173a-255">(30)</span><span class="sxs-lookup"><span data-stu-id="5173a-255">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5173a-256">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="5173a-256">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5173a-257">31,5</span><span class="sxs-lookup"><span data-stu-id="5173a-257">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5173a-258">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="5173a-258">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-259">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5173a-259">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-261">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5173a-261">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-262">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="5173a-262">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5173a-263">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-263">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-264">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="5173a-264">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-265">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-267">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5173a-267">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5173a-268">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5173a-268">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5173a-269">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-269">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5173a-270">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-271">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5173a-271">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-274">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5173a-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-275">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5173a-275">A textual description of the object.</span></span>

<span data-ttu-id="5173a-276">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-277">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5173a-277">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-280">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5173a-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5173a-281">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="5173a-281">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5173a-282">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-283">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="5173a-283">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-284">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5173a-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-286">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5173a-286">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5173a-287">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-288">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5173a-288">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-291">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="5173a-291">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5173a-292">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-293">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="5173a-293">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-296">Eine frei Form Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, der vom Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5173a-296">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="5173a-297">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-297">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5173a-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-299">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5173a-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-301">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="5173a-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-302">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5173a-302">Indicates when the object was installed.</span></span> <span data-ttu-id="5173a-303">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5173a-303">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5173a-304">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-305">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5173a-305">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-306">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5173a-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-308">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5173a-308">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5173a-309">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-310">**Name**</span><span class="sxs-lookup"><span data-stu-id="5173a-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-311">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-313">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5173a-313">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-314">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="5173a-314">Label by which the object is known.</span></span> <span data-ttu-id="5173a-315">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-315">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5173a-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-317">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="5173a-317">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-318">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5173a-318">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-320">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("anzahlblöcke"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Aggregat physischer Block \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="5173a-320">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Aggregate Physical Extent\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-321">Die Gesamtanzahl der Blöcke (einschließlich der Check-Datenblöcke), die in diesem aggregierten physischen Block enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5173a-321">Total number of blocks (including the check data blocks) contained in this aggregate physical extent.</span></span> <span data-ttu-id="5173a-322">Die Blockgröße (eine geerbte Eigenschaft) sollte auf denselben Wert festgelegt werden wie für das Medien Zugriffsgerät, das diesem Block zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5173a-322">The block size (an inherited property) should be set to the same value as for the media access device associated with this extent.</span></span>

</dd> <dt>

<span data-ttu-id="5173a-323">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5173a-323">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-326">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5173a-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-327">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="5173a-327">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5173a-328">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5173a-328">Example: "\*PNP030b"</span></span>

<span data-ttu-id="5173a-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-330">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="5173a-330">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-331">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="5173a-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5173a-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-333">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="5173a-333">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="5173a-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5173a-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5173a-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-336">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="5173a-336">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5173a-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="5173a-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-338">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5173a-338">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5173a-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="5173a-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-340">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5173a-340">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5173a-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="5173a-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-342">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5173a-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5173a-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="5173a-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-344">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="5173a-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5173a-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="5173a-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-346">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5173a-346">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="5173a-347">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-347">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="5173a-348">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5173a-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5173a-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="5173a-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-350">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="5173a-350">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5173a-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="5173a-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5173a-352">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5173a-352">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5173a-353">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="5173a-353">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-354">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5173a-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-356">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5173a-356">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5173a-357">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="5173a-357">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5173a-358">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-358">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5173a-359">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="5173a-359">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5173a-360">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-361">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="5173a-361">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-362">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5173a-364">Freie Formular Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5173a-364">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="5173a-365">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-365">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-366">**Status**</span><span class="sxs-lookup"><span data-stu-id="5173a-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-369">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="5173a-369">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-370">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="5173a-370">String that indicates the current status of the object.</span></span> <span data-ttu-id="5173a-371">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-371">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5173a-372">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="5173a-372">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5173a-373">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="5173a-373">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5173a-374">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="5173a-374">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5173a-375">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5173a-375">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5173a-376">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="5173a-376">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5173a-377">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5173a-378">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="5173a-378">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5173a-379">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5173a-379">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5173a-380">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="5173a-380">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5173a-381">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="5173a-381">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5173a-382">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="5173a-382">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5173a-383">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5173a-383">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5173a-384">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="5173a-384">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5173a-385">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="5173a-385">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5173a-386">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="5173a-386">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5173a-387">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="5173a-387">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5173a-388">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="5173a-388">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5173a-389">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="5173a-389">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5173a-390">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="5173a-390">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5173a-391">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5173a-391">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-392">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5173a-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-394">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5173a-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5173a-395">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="5173a-395">State of the logical device.</span></span> <span data-ttu-id="5173a-396">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5173a-396">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="5173a-397">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5173a-398">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="5173a-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5173a-399">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="5173a-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5173a-400">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="5173a-400">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5173a-401">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="5173a-401">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5173a-402">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="5173a-402">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5173a-403">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="5173a-403">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-404">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-406">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5173a-406">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5173a-407">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="5173a-407">The scoping system's creation class name.</span></span>

<span data-ttu-id="5173a-408">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5173a-409">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="5173a-409">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5173a-410">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5173a-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5173a-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5173a-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5173a-412">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5173a-412">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5173a-413">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="5173a-413">The scoping system's name.</span></span>

<span data-ttu-id="5173a-414">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5173a-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5173a-415">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5173a-415">Remarks</span></span>

<span data-ttu-id="5173a-416">Die **CIM- \_ aggregatepblock** -Klasse wird von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5173a-416">The **CIM\_AggregatePExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="5173a-417">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5173a-417">WMI does not implement this class.</span></span>

<span data-ttu-id="5173a-418">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5173a-418">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5173a-419">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5173a-419">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5173a-420">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5173a-420">Requirements</span></span>



| <span data-ttu-id="5173a-421">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5173a-421">Requirement</span></span> | <span data-ttu-id="5173a-422">Wert</span><span class="sxs-lookup"><span data-stu-id="5173a-422">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5173a-423">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5173a-423">Minimum supported client</span></span><br/> | <span data-ttu-id="5173a-424">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5173a-424">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5173a-425">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5173a-425">Minimum supported server</span></span><br/> | <span data-ttu-id="5173a-426">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5173a-426">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5173a-427">Namespace</span><span class="sxs-lookup"><span data-stu-id="5173a-427">Namespace</span></span><br/>                | <span data-ttu-id="5173a-428">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5173a-428">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5173a-429">MOF</span><span class="sxs-lookup"><span data-stu-id="5173a-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5173a-430"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5173a-430"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5173a-431">DLL</span><span class="sxs-lookup"><span data-stu-id="5173a-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5173a-432"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5173a-432"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5173a-433">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5173a-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5173a-434">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="5173a-434">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="5173a-435">CIM-Klassen</span><span class="sxs-lookup"><span data-stu-id="5173a-435">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

