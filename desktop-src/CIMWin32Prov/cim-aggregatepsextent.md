---
description: Die CIM- \_ aggregatepsextent-Klasse definiert die Anzahl der adressierbaren logischen Blöcke auf einem einzelnen Speichergerät, ausgenommen logische Blöcke, die als Prüfdaten zugeordnet sind.
ms.assetid: 6c188955-a963-414d-94f9-b7e1cb5960ed
ms.tgt_platform: multiple
title: CIM_AggregatePSExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent
- CIM_AggregatePSExtent.Caption
- CIM_AggregatePSExtent.Description
- CIM_AggregatePSExtent.InstallDate
- CIM_AggregatePSExtent.Name
- CIM_AggregatePSExtent.Status
- CIM_AggregatePSExtent.Availability
- CIM_AggregatePSExtent.ConfigManagerErrorCode
- CIM_AggregatePSExtent.ConfigManagerUserConfig
- CIM_AggregatePSExtent.CreationClassName
- CIM_AggregatePSExtent.DeviceID
- CIM_AggregatePSExtent.PowerManagementCapabilities
- CIM_AggregatePSExtent.ErrorCleared
- CIM_AggregatePSExtent.ErrorDescription
- CIM_AggregatePSExtent.LastErrorCode
- CIM_AggregatePSExtent.PNPDeviceID
- CIM_AggregatePSExtent.PowerManagementSupported
- CIM_AggregatePSExtent.StatusInfo
- CIM_AggregatePSExtent.SystemCreationClassName
- CIM_AggregatePSExtent.SystemName
- CIM_AggregatePSExtent.Access
- CIM_AggregatePSExtent.BlockSize
- CIM_AggregatePSExtent.ErrorMethodology
- CIM_AggregatePSExtent.NumberOfBlocks
- CIM_AggregatePSExtent.Purpose
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: edc3f5b91bc39e18321778dbfdbc53446c6c27d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748720"
---
# <a name="cim_aggregatepsextent-class"></a><span data-ttu-id="1635a-103">CIM- \_ aggregatepsextent-Klasse</span><span class="sxs-lookup"><span data-stu-id="1635a-103">CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="1635a-104">Die **CIM- \_ aggregatepsextent** -Klasse definiert die Anzahl der adressierbaren logischen Blöcke auf einem einzelnen Speichergerät, ausgenommen logische Blöcke, die als Prüfdaten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1635a-104">The **CIM\_AggregatePSExtent** class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="1635a-105">Wenn Volumesets definiert sind, sind die logischen Blöcke innerhalb eines einzelnen Volumesatzes enthalten.</span><span class="sxs-lookup"><span data-stu-id="1635a-105">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="1635a-106">Dies ist eine alternative Gruppierung für [**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md), wenn nur Zusammenfassungs Informationen benötigt werden oder wenn die automatische Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1635a-106">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

<span data-ttu-id="1635a-107">Die automatische Konfiguration kann dazu führen, dass Tausende von [**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md) -Klassen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-107">Automatic configuration can result in thousands of [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) classes being defined.</span></span> <span data-ttu-id="1635a-108">Die **CIM- \_ aggregatepsextent** -Klasse wurde so definiert, dass einzelne Blöcke nicht modelliert werden müssten.</span><span class="sxs-lookup"><span data-stu-id="1635a-108">The **CIM\_AggregatePSExtent** class was defined so that individual extents would not have to be modeled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1635a-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1635a-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1635a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1635a-111">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1635a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1635a-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1635a-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1635a-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="1635a-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D0E255C-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AggregatePSExtent : CIM_StorageExtent
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
  uint64   NumberOfBlocks;
  string   Purpose;
};
```

## <a name="members"></a><span data-ttu-id="1635a-114">Member</span><span class="sxs-lookup"><span data-stu-id="1635a-114">Members</span></span>

<span data-ttu-id="1635a-115">Die **CIM- \_ aggregatepsextent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1635a-115">The **CIM\_AggregatePSExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="1635a-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="1635a-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="1635a-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1635a-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1635a-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="1635a-118">Methods</span></span>

<span data-ttu-id="1635a-119">Die **CIM- \_ aggregatepsextent** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1635a-119">The **CIM\_AggregatePSExtent** class has these methods.</span></span>



| <span data-ttu-id="1635a-120">Methode</span><span class="sxs-lookup"><span data-stu-id="1635a-120">Method</span></span>                                                                       | <span data-ttu-id="1635a-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1635a-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1635a-122">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="1635a-122">**Reset**</span></span>](reset-method-in-class-cim-aggregatepsextent.md)                 | <span data-ttu-id="1635a-123">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="1635a-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="1635a-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="1635a-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="1635a-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1635a-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepsextent.md) | <span data-ttu-id="1635a-126">Definiert den gewünschten Energiezustand für ein logisches Gerät und den Zeitpunkt, zu dem das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1635a-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="1635a-127">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="1635a-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1635a-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1635a-128">Properties</span></span>

<span data-ttu-id="1635a-129">Die **CIM- \_ aggregatepsextent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1635a-129">The **CIM\_AggregatePSExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1635a-130">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="1635a-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1635a-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-133">Beschreibt die Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="1635a-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="1635a-134">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1635a-135">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1635a-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="1635a-136">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1635a-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="1635a-137">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="1635a-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="1635a-138">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="1635a-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="1635a-139">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="1635a-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1635a-140">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="1635a-140">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-141">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1635a-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="1635a-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-144">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="1635a-144">Availability and status of the device.</span></span>

<span data-ttu-id="1635a-145">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-145">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1635a-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="1635a-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1635a-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="1635a-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1635a-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="1635a-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1635a-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="1635a-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1635a-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="1635a-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1635a-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="1635a-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1635a-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="1635a-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1635a-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="1635a-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1635a-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="1635a-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1635a-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="1635a-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1635a-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="1635a-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1635a-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="1635a-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1635a-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="1635a-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-159">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="1635a-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1635a-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="1635a-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-161">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1635a-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1635a-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="1635a-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-163">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-163">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1635a-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="1635a-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1635a-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="1635a-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-166">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="1635a-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1635a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="1635a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-168">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="1635a-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1635a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="1635a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-170">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="1635a-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1635a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="1635a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-172">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1635a-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1635a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="1635a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-174">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="1635a-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1635a-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="1635a-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-176">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1635a-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-178">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="1635a-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-179">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="1635a-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="1635a-180">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="1635a-181">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="1635a-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="1635a-182">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1635a-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1635a-183">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-183">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1635a-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-187">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1635a-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-188">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1635a-188">A short textual description of the object.</span></span>

<span data-ttu-id="1635a-189">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-190">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="1635a-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-191">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1635a-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-193">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1635a-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-194">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1635a-194">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1635a-195">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1635a-196">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="1635a-196">**This device is working properly.**</span></span> <span data-ttu-id="1635a-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="1635a-197">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1635a-198">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="1635a-198">**This device is not configured correctly.**</span></span> <span data-ttu-id="1635a-199">(1)</span><span class="sxs-lookup"><span data-stu-id="1635a-199">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1635a-200">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="1635a-200">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1635a-201">(2)</span><span class="sxs-lookup"><span data-stu-id="1635a-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1635a-202">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="1635a-202">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1635a-203">(3)</span><span class="sxs-lookup"><span data-stu-id="1635a-203">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1635a-204">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="1635a-204">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1635a-205">(4)</span><span class="sxs-lookup"><span data-stu-id="1635a-205">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1635a-206">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="1635a-206">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1635a-207">(5)</span><span class="sxs-lookup"><span data-stu-id="1635a-207">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1635a-208">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="1635a-208">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1635a-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="1635a-209">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1635a-210">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="1635a-210">**Cannot filter.**</span></span> <span data-ttu-id="1635a-211">(7)</span><span class="sxs-lookup"><span data-stu-id="1635a-211">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1635a-212">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="1635a-212">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1635a-213">(8)</span><span class="sxs-lookup"><span data-stu-id="1635a-213">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1635a-214">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="1635a-214">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1635a-215">(9)</span><span class="sxs-lookup"><span data-stu-id="1635a-215">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1635a-216">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="1635a-216">**This device cannot start.**</span></span> <span data-ttu-id="1635a-217">(10)</span><span class="sxs-lookup"><span data-stu-id="1635a-217">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1635a-218">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="1635a-218">**This device failed.**</span></span> <span data-ttu-id="1635a-219">(11)</span><span class="sxs-lookup"><span data-stu-id="1635a-219">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1635a-220">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="1635a-220">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1635a-221">(12)</span><span class="sxs-lookup"><span data-stu-id="1635a-221">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1635a-222">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="1635a-222">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1635a-223">(13)</span><span class="sxs-lookup"><span data-stu-id="1635a-223">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1635a-224">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="1635a-224">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1635a-225">(14)</span><span class="sxs-lookup"><span data-stu-id="1635a-225">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1635a-226">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="1635a-226">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1635a-227">(15)</span><span class="sxs-lookup"><span data-stu-id="1635a-227">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1635a-228">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="1635a-228">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1635a-229">(16)</span><span class="sxs-lookup"><span data-stu-id="1635a-229">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1635a-230">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="1635a-230">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1635a-231">(17)</span><span class="sxs-lookup"><span data-stu-id="1635a-231">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1635a-232">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="1635a-232">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1635a-233">(18)</span><span class="sxs-lookup"><span data-stu-id="1635a-233">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1635a-234">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="1635a-234">**Failure using the VxD loader.**</span></span> <span data-ttu-id="1635a-235">(19)</span><span class="sxs-lookup"><span data-stu-id="1635a-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1635a-236">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="1635a-236">**Your registry might be corrupted.**</span></span> <span data-ttu-id="1635a-237">(20)</span><span class="sxs-lookup"><span data-stu-id="1635a-237">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1635a-238">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="1635a-238">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1635a-239">(21)</span><span class="sxs-lookup"><span data-stu-id="1635a-239">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1635a-240">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="1635a-240">**This device is disabled.**</span></span> <span data-ttu-id="1635a-241">(22)</span><span class="sxs-lookup"><span data-stu-id="1635a-241">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1635a-242">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="1635a-242">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1635a-243">(23)</span><span class="sxs-lookup"><span data-stu-id="1635a-243">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1635a-244">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="1635a-244">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1635a-245">(24)</span><span class="sxs-lookup"><span data-stu-id="1635a-245">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1635a-246">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="1635a-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="1635a-247">(25)</span><span class="sxs-lookup"><span data-stu-id="1635a-247">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1635a-248">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="1635a-248">**Windows is still setting up this device.**</span></span> <span data-ttu-id="1635a-249">(26)</span><span class="sxs-lookup"><span data-stu-id="1635a-249">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1635a-250">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="1635a-250">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1635a-251">(27)</span><span class="sxs-lookup"><span data-stu-id="1635a-251">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1635a-252">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="1635a-252">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1635a-253">(28)</span><span class="sxs-lookup"><span data-stu-id="1635a-253">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1635a-254">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="1635a-254">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1635a-255">(29)</span><span class="sxs-lookup"><span data-stu-id="1635a-255">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1635a-256">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="1635a-256">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1635a-257">(30)</span><span class="sxs-lookup"><span data-stu-id="1635a-257">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1635a-258">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="1635a-258">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1635a-259">31,5</span><span class="sxs-lookup"><span data-stu-id="1635a-259">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1635a-260">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="1635a-260">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-261">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1635a-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-263">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1635a-263">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-264">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="1635a-264">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1635a-265">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-266">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="1635a-266">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-269">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1635a-269">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1635a-270">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1635a-270">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1635a-271">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-271">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1635a-272">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-273">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1635a-273">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-276">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1635a-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-277">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1635a-277">A textual description of the object.</span></span>

<span data-ttu-id="1635a-278">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-278">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-279">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1635a-279">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-282">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1635a-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1635a-283">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="1635a-283">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1635a-284">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-285">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="1635a-285">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-286">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1635a-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-288">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1635a-288">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1635a-289">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-290">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1635a-290">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-291">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-293">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="1635a-293">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1635a-294">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-295">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="1635a-295">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-298">Eine frei Form Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, der vom Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1635a-298">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="1635a-299">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-299">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1635a-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-301">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1635a-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-303">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="1635a-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-304">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1635a-304">Indicates when the object was installed.</span></span> <span data-ttu-id="1635a-305">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1635a-305">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1635a-306">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-307">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1635a-307">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-308">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1635a-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-310">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1635a-310">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1635a-311">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-312">**Name**</span><span class="sxs-lookup"><span data-stu-id="1635a-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-315">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1635a-315">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-316">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1635a-316">Label by which the object is known.</span></span> <span data-ttu-id="1635a-317">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-317">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1635a-318">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-319">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="1635a-319">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-320">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1635a-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-322">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="1635a-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-323">Anzahl der aufeinander folgenden Blöcke, die die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="1635a-323">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="1635a-324">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="1635a-324">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="1635a-325">Wenn der Wert von **BLOCKSIZE** 1 (eins) ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="1635a-325">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="1635a-326">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1635a-326">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1635a-327">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-327">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-328">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1635a-328">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-331">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1635a-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-332">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="1635a-332">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1635a-333">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1635a-333">Example: "\*PNP030b"</span></span>

<span data-ttu-id="1635a-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-335">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="1635a-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-336">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1635a-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1635a-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-338">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="1635a-338">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="1635a-339">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1635a-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1635a-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-341">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="1635a-341">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1635a-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="1635a-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-343">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1635a-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1635a-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="1635a-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-345">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1635a-345">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1635a-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="1635a-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-347">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1635a-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1635a-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="1635a-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-349">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="1635a-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1635a-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="1635a-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-351">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1635a-351">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="1635a-352">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-352">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="1635a-353">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1635a-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1635a-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="1635a-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-355">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="1635a-355">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1635a-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="1635a-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1635a-357">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1635a-357">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1635a-358">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="1635a-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-359">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1635a-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-361">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1635a-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1635a-362">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="1635a-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1635a-363">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1635a-364">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="1635a-364">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1635a-365">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-366">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="1635a-366">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1635a-369">Freie Formular Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1635a-369">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="1635a-370">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-370">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-371">**Status**</span><span class="sxs-lookup"><span data-stu-id="1635a-371">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-372">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-374">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="1635a-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-375">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="1635a-375">String that indicates the current status of the object.</span></span> <span data-ttu-id="1635a-376">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-376">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="1635a-377">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="1635a-377">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="1635a-378">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="1635a-378">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="1635a-379">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="1635a-379">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1635a-380">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="1635a-380">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1635a-381">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="1635a-381">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1635a-382">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-382">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1635a-383">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="1635a-383">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1635a-384">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1635a-384">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1635a-385">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="1635a-385">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1635a-386">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="1635a-386">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1635a-387">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="1635a-387">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1635a-388">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1635a-388">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1635a-389">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="1635a-389">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1635a-390">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="1635a-390">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1635a-391">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="1635a-391">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1635a-392">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="1635a-392">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1635a-393">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="1635a-393">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1635a-394">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="1635a-394">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1635a-395">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="1635a-395">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1635a-396">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1635a-396">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-397">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1635a-397">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-399">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1635a-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1635a-400">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="1635a-400">State of the logical device.</span></span> <span data-ttu-id="1635a-401">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1635a-401">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="1635a-402">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1635a-403">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="1635a-403">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1635a-404">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="1635a-404">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1635a-405">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="1635a-405">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1635a-406">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="1635a-406">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1635a-407">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="1635a-407">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1635a-408">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="1635a-408">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-409">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-411">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1635a-411">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1635a-412">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="1635a-412">The scoping system's creation class name.</span></span>

<span data-ttu-id="1635a-413">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1635a-414">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="1635a-414">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1635a-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1635a-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1635a-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1635a-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1635a-417">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1635a-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1635a-418">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="1635a-418">The scoping system's name.</span></span>

<span data-ttu-id="1635a-419">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1635a-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1635a-420">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1635a-420">Remarks</span></span>

<span data-ttu-id="1635a-421">Die **CIM- \_ aggregatepsextent** -Klasse wird von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1635a-421">The **CIM\_AggregatePSExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="1635a-422">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1635a-422">WMI does not implement this class.</span></span>

<span data-ttu-id="1635a-423">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1635a-423">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1635a-424">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1635a-424">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1635a-425">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1635a-425">Requirements</span></span>



| <span data-ttu-id="1635a-426">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1635a-426">Requirement</span></span> | <span data-ttu-id="1635a-427">Wert</span><span class="sxs-lookup"><span data-stu-id="1635a-427">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1635a-428">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1635a-428">Minimum supported client</span></span><br/> | <span data-ttu-id="1635a-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1635a-429">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1635a-430">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1635a-430">Minimum supported server</span></span><br/> | <span data-ttu-id="1635a-431">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1635a-431">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1635a-432">Namespace</span><span class="sxs-lookup"><span data-stu-id="1635a-432">Namespace</span></span><br/>                | <span data-ttu-id="1635a-433">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1635a-433">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1635a-434">MOF</span><span class="sxs-lookup"><span data-stu-id="1635a-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1635a-435"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1635a-435"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1635a-436">DLL</span><span class="sxs-lookup"><span data-stu-id="1635a-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1635a-437"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1635a-437"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1635a-438">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1635a-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1635a-439">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="1635a-439">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="1635a-440">CIM-Klassen</span><span class="sxs-lookup"><span data-stu-id="1635a-440">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

