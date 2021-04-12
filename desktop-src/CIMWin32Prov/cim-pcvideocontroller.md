---
description: Der CIM \_ pcvideocontroller stellt die Funktionen und die Verwaltung eines Video Controllers für persönliche Computer dar, einen Untertyp eines Video Controllers.
ms.assetid: bf937727-a332-445b-9397-7d87d58c4a5b
ms.tgt_platform: multiple
title: CIM_PCVideoController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController
- CIM_PCVideoController.AcceleratorCapabilities
- CIM_PCVideoController.Availability
- CIM_PCVideoController.CapabilityDescriptions
- CIM_PCVideoController.Caption
- CIM_PCVideoController.ConfigManagerErrorCode
- CIM_PCVideoController.ConfigManagerUserConfig
- CIM_PCVideoController.CreationClassName
- CIM_PCVideoController.CurrentBitsPerPixel
- CIM_PCVideoController.CurrentHorizontalResolution
- CIM_PCVideoController.CurrentNumberOfColors
- CIM_PCVideoController.CurrentNumberOfColumns
- CIM_PCVideoController.CurrentNumberOfRows
- CIM_PCVideoController.CurrentRefreshRate
- CIM_PCVideoController.CurrentScanMode
- CIM_PCVideoController.CurrentVerticalResolution
- CIM_PCVideoController.Description
- CIM_PCVideoController.DeviceID
- CIM_PCVideoController.ErrorCleared
- CIM_PCVideoController.ErrorDescription
- CIM_PCVideoController.InstallDate
- CIM_PCVideoController.LastErrorCode
- CIM_PCVideoController.MaxMemorySupported
- CIM_PCVideoController.MaxNumberControlled
- CIM_PCVideoController.MaxRefreshRate
- CIM_PCVideoController.MinRefreshRate
- CIM_PCVideoController.Name
- CIM_PCVideoController.NumberOfColorPlanes
- CIM_PCVideoController.NumberOfVideoPages
- CIM_PCVideoController.PNPDeviceID
- CIM_PCVideoController.PowerManagementCapabilities
- CIM_PCVideoController.PowerManagementSupported
- CIM_PCVideoController.ProtocolSupported
- CIM_PCVideoController.Status
- CIM_PCVideoController.StatusInfo
- CIM_PCVideoController.SystemCreationClassName
- CIM_PCVideoController.SystemName
- CIM_PCVideoController.TimeOfLastReset
- CIM_PCVideoController.VideoArchitecture
- CIM_PCVideoController.VideoMemoryType
- CIM_PCVideoController.VideoMode
- CIM_PCVideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94465862c34cc9c6fb645f63c0add48d0fded56b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393114"
---
# <a name="cim_pcvideocontroller-class"></a><span data-ttu-id="929db-103">CIM \_ pcvideocontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="929db-103">CIM\_PCVideoController class</span></span>

<span data-ttu-id="929db-104">Der **CIM \_ pcvideocontroller** stellt die Funktionen und die Verwaltung eines Video Controllers für persönliche Computer dar, einen Untertyp eines Video Controllers.</span><span class="sxs-lookup"><span data-stu-id="929db-104">The **CIM\_PCVideoController** represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="929db-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="929db-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="929db-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="929db-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="929db-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="929db-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="929db-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="929db-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="929db-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="929db-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE6-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_PCVideoController : CIM_VideoController
{
  uint16   AcceleratorCapabilities[];
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="929db-110">Member</span><span class="sxs-lookup"><span data-stu-id="929db-110">Members</span></span>

<span data-ttu-id="929db-111">Die **CIM \_ pcvideocontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="929db-111">The **CIM\_PCVideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="929db-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="929db-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="929db-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="929db-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="929db-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="929db-114">Methods</span></span>

<span data-ttu-id="929db-115">Die **CIM \_ pcvideocontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="929db-115">The **CIM\_PCVideoController** class has these methods.</span></span>



| <span data-ttu-id="929db-116">Methode</span><span class="sxs-lookup"><span data-stu-id="929db-116">Method</span></span>                                                                       | <span data-ttu-id="929db-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="929db-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929db-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="929db-118">**Reset**</span></span>](reset-method-in-class-cim-pcvideocontroller.md)                 | <span data-ttu-id="929db-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="929db-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="929db-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="929db-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="929db-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="929db-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md) | <span data-ttu-id="929db-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="929db-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="929db-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="929db-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="929db-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="929db-124">Properties</span></span>

<span data-ttu-id="929db-125">Die **CIM \_ pcvideocontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="929db-125">The **CIM\_PCVideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="929db-126">**Beschleuniger Funktionen**</span><span class="sxs-lookup"><span data-stu-id="929db-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-127">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="929db-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="929db-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-129">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="929db-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="929db-130">Grafiken und 3D-Funktionen des Video Controllers.</span><span class="sxs-lookup"><span data-stu-id="929db-130">Graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="929db-131">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-131">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="929db-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="929db-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="929db-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Grafikbeschleuniger** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="929db-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D-Accelerator** (3)</span><span class="sxs-lookup"><span data-stu-id="929db-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="929db-136">3D-Accelerator</span><span class="sxs-lookup"><span data-stu-id="929db-136">3-D accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-137">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="929db-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-138">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="929db-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="929db-141">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="929db-141">Availability and status of the device.</span></span>

<span data-ttu-id="929db-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="929db-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="929db-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="929db-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="929db-146">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="929db-146">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="929db-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="929db-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="929db-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="929db-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="929db-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="929db-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="929db-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="929db-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="929db-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="929db-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="929db-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="929db-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="929db-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="929db-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="929db-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="929db-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="929db-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="929db-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="929db-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="929db-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="929db-157">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="929db-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="929db-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="929db-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="929db-159">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="929db-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="929db-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="929db-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="929db-161">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="929db-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="929db-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="929db-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="929db-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="929db-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="929db-164">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="929db-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="929db-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="929db-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="929db-166">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="929db-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="929db-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="929db-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="929db-168">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="929db-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="929db-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="929db-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="929db-170">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="929db-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="929db-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="929db-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="929db-172">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="929db-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-173">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="929db-173">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-174">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="929db-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="929db-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-176">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Acceleratorfunktionen**")</span><span class="sxs-lookup"><span data-stu-id="929db-176">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="929db-177">Freiform-Zeichen folgen, die ausführliche Erläuterungen zu den im **acceleratorfunktionalitäten** -Array angegebenen Features für die Videobeschleunigung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="929db-177">Free-form strings that provide detailed explanations for video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="929db-178">Jeder Array Eintrag bezieht sich auf den Eintrag im **acceleratorfunktionalitäten** -Array, der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="929db-178">Each array entry is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="929db-179">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-179">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-180">**Caption**</span><span class="sxs-lookup"><span data-stu-id="929db-180">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-183">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="929db-183">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="929db-184">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="929db-184">Short textual description of the object.</span></span>

<span data-ttu-id="929db-185">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-186">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="929db-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-189">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="929db-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="929db-190">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="929db-190">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="929db-191">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="929db-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="929db-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="929db-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="929db-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="929db-194">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="929db-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="929db-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="929db-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="929db-196">(1)</span><span class="sxs-lookup"><span data-stu-id="929db-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="929db-197">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="929db-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="929db-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="929db-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="929db-199">(2)</span><span class="sxs-lookup"><span data-stu-id="929db-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="929db-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="929db-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="929db-201">(3)</span><span class="sxs-lookup"><span data-stu-id="929db-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="929db-202">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="929db-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="929db-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="929db-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="929db-204">(4)</span><span class="sxs-lookup"><span data-stu-id="929db-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="929db-205">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="929db-205">Device is not working properly.</span></span> <span data-ttu-id="929db-206">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="929db-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="929db-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="929db-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="929db-208">(5)</span><span class="sxs-lookup"><span data-stu-id="929db-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="929db-209">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="929db-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="929db-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="929db-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="929db-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="929db-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="929db-212">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="929db-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="929db-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="929db-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="929db-214">(7)</span><span class="sxs-lookup"><span data-stu-id="929db-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="929db-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="929db-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="929db-216">(8)</span><span class="sxs-lookup"><span data-stu-id="929db-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="929db-217">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="929db-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="929db-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="929db-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="929db-219">(9)</span><span class="sxs-lookup"><span data-stu-id="929db-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="929db-220">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="929db-220">Device is not working properly.</span></span> <span data-ttu-id="929db-221">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="929db-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="929db-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="929db-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="929db-223">(10)</span><span class="sxs-lookup"><span data-stu-id="929db-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="929db-224">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="929db-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="929db-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="929db-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="929db-226">(11)</span><span class="sxs-lookup"><span data-stu-id="929db-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="929db-227">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="929db-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="929db-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="929db-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="929db-229">(12)</span><span class="sxs-lookup"><span data-stu-id="929db-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="929db-230">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="929db-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="929db-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="929db-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="929db-232">(13)</span><span class="sxs-lookup"><span data-stu-id="929db-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="929db-233">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="929db-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="929db-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="929db-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="929db-235">(14)</span><span class="sxs-lookup"><span data-stu-id="929db-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="929db-236">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="929db-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="929db-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="929db-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="929db-238">(15)</span><span class="sxs-lookup"><span data-stu-id="929db-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="929db-239">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="929db-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="929db-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="929db-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="929db-241">(16)</span><span class="sxs-lookup"><span data-stu-id="929db-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="929db-242">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="929db-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="929db-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="929db-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="929db-244">(17)</span><span class="sxs-lookup"><span data-stu-id="929db-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="929db-245">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="929db-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="929db-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="929db-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="929db-247">(18)</span><span class="sxs-lookup"><span data-stu-id="929db-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="929db-248">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="929db-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="929db-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="929db-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="929db-250">(19)</span><span class="sxs-lookup"><span data-stu-id="929db-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="929db-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="929db-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="929db-252">(20)</span><span class="sxs-lookup"><span data-stu-id="929db-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="929db-253">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="929db-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="929db-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="929db-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="929db-255">(21)</span><span class="sxs-lookup"><span data-stu-id="929db-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="929db-256">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="929db-256">System failure.</span></span> <span data-ttu-id="929db-257">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="929db-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="929db-258">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="929db-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="929db-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="929db-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="929db-260">(22)</span><span class="sxs-lookup"><span data-stu-id="929db-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="929db-261">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="929db-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="929db-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="929db-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="929db-263">(23)</span><span class="sxs-lookup"><span data-stu-id="929db-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="929db-264">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="929db-264">System failure.</span></span> <span data-ttu-id="929db-265">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="929db-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="929db-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="929db-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="929db-267">(24)</span><span class="sxs-lookup"><span data-stu-id="929db-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="929db-268">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="929db-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="929db-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="929db-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="929db-270">(25)</span><span class="sxs-lookup"><span data-stu-id="929db-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="929db-271">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="929db-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="929db-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="929db-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="929db-273">(26)</span><span class="sxs-lookup"><span data-stu-id="929db-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="929db-274">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="929db-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="929db-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="929db-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="929db-276">(27)</span><span class="sxs-lookup"><span data-stu-id="929db-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="929db-277">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="929db-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="929db-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="929db-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="929db-279">(28)</span><span class="sxs-lookup"><span data-stu-id="929db-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="929db-280">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="929db-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="929db-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="929db-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="929db-282">(29)</span><span class="sxs-lookup"><span data-stu-id="929db-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="929db-283">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="929db-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="929db-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="929db-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="929db-285">(30)</span><span class="sxs-lookup"><span data-stu-id="929db-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="929db-286">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="929db-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="929db-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="929db-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="929db-288">31,5</span><span class="sxs-lookup"><span data-stu-id="929db-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="929db-289">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="929db-289">Device is not working properly.</span></span> <span data-ttu-id="929db-290">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="929db-290">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-291">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="929db-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-292">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="929db-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="929db-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-294">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="929db-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="929db-295">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="929db-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="929db-296">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-297">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="929db-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-300">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="929db-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="929db-301">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="929db-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="929db-302">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="929db-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="929db-303">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-304">**Currentbitsperpixel**</span><span class="sxs-lookup"><span data-stu-id="929db-304">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-305">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-305">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-307">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,12 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="929db-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="929db-308">Anzahl von Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="929db-308">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="929db-309">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-309">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-310">**Ereignis Auflösung**</span><span class="sxs-lookup"><span data-stu-id="929db-310">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-311">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-313">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="929db-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="929db-314">Aktuelle Anzahl von horizontalen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="929db-314">Current number of horizontal pixels.</span></span>

<span data-ttu-id="929db-315">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-315">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-316">**Currentzahlofcolors**</span><span class="sxs-lookup"><span data-stu-id="929db-316">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-317">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="929db-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="929db-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-319">Anzahl von Farben, die in den aktuellen Auflösungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="929db-319">Number of colors supported at the current resolutions.</span></span>

<span data-ttu-id="929db-320">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-320">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="929db-321">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="929db-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="929db-322">**Currentzahlofcolumns**</span><span class="sxs-lookup"><span data-stu-id="929db-322">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-323">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-325">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="929db-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="929db-326">Wenn im Zeichenmodus die Anzahl der Spalten für den Videocontroller. Andernfalls geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="929db-326">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="929db-327">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-327">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-328">**Currentnumofrows**</span><span class="sxs-lookup"><span data-stu-id="929db-328">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-329">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-331">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="929db-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="929db-332">Im Zeichenmodus die Anzahl der Zeilen für diesen Videocontroller. Andernfalls geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="929db-332">If in character mode, number of rows for this video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="929db-333">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-333">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-334">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="929db-334">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-337">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="929db-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="929db-338">Aktuelle Aktualisierungsrate in Hertz.</span><span class="sxs-lookup"><span data-stu-id="929db-338">Current refresh rate in hertz.</span></span>

<span data-ttu-id="929db-339">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-339">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-340">**Currentscanmode**</span><span class="sxs-lookup"><span data-stu-id="929db-340">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-341">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-343">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="929db-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="929db-344">Aktueller Scanmodus.</span><span class="sxs-lookup"><span data-stu-id="929db-344">Current scan mode.</span></span> <span data-ttu-id="929db-345">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-345">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="929db-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="929db-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>Zeilen **Sprung (3** )</span><span class="sxs-lookup"><span data-stu-id="929db-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="929db-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Nicht** Zeilen Sprung (4)</span><span class="sxs-lookup"><span data-stu-id="929db-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="929db-350">Nicht Zeilen Sprung</span><span class="sxs-lookup"><span data-stu-id="929db-350">Non-interlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-351">**Currentverticalresolution**</span><span class="sxs-lookup"><span data-stu-id="929db-351">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-352">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-354">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="929db-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="929db-355">Aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="929db-355">Current number of vertical pixels.</span></span>

<span data-ttu-id="929db-356">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-356">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-357">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="929db-357">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-360">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="929db-360">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="929db-361">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="929db-361">Textual description of the object.</span></span>

<span data-ttu-id="929db-362">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-363">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="929db-363">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-366">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="929db-366">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="929db-367">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="929db-367">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="929db-368">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-369">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="929db-369">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-370">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="929db-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="929db-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-372">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="929db-372">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="929db-373">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-374">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="929db-374">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-375">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-377">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="929db-377">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="929db-378">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-379">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="929db-379">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-380">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="929db-380">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="929db-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-382">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="929db-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="929db-383">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="929db-383">Date and time the object was installed.</span></span> <span data-ttu-id="929db-384">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="929db-384">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="929db-385">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-386">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="929db-386">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-387">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-389">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="929db-389">Last error code reported by the logical device.</span></span>

<span data-ttu-id="929db-390">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-391">**Maxmemorysupported**</span><span class="sxs-lookup"><span data-stu-id="929db-391">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-392">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-394">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="929db-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="929db-395">Maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="929db-395">Maximum amount of memory supported, in bytes.</span></span>

<span data-ttu-id="929db-396">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-396">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-397">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="929db-397">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-398">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-400">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="929db-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="929db-401">Maximale Anzahl direkt Adressier barer Entitäten, die vom Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="929db-401">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="929db-402">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="929db-402">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="929db-403">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-404">**Maxfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="929db-404">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-405">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-407">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="929db-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="929db-408">Maximale Aktualisierungsrate des Video Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="929db-408">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="929db-409">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-409">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-410">**Minfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="929db-410">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-411">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-413">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="929db-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="929db-414">Minimale Aktualisierungsrate des Video Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="929db-414">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="929db-415">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-415">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-416">**Name**</span><span class="sxs-lookup"><span data-stu-id="929db-416">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-417">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-419">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="929db-419">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="929db-420">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="929db-420">Label by which the object is known.</span></span> <span data-ttu-id="929db-421">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="929db-421">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="929db-422">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-423">**Anzahl von colorplane**</span><span class="sxs-lookup"><span data-stu-id="929db-423">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-424">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-426">Aktuelle Anzahl von Farbebenen.</span><span class="sxs-lookup"><span data-stu-id="929db-426">Current number of color planes.</span></span> <span data-ttu-id="929db-427">Wenn dieser Wert für die aktuelle Video Konfiguration nicht anwendbar ist, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="929db-427">If this value is not applicable for the current video configuration, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="929db-428">**Anzahl der videopages**</span><span class="sxs-lookup"><span data-stu-id="929db-428">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-429">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="929db-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="929db-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-431">Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="929db-431">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="929db-432">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-432">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-433">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="929db-433">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-436">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="929db-436">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="929db-437">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="929db-437">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="929db-438">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="929db-439">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="929db-439">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="929db-440">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="929db-440">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-441">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="929db-441">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="929db-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-443">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="929db-443">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="929db-444">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-444">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="929db-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="929db-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="929db-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="929db-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="929db-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="929db-449">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="929db-449">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="929db-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="929db-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="929db-451">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="929db-451">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="929db-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="929db-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="929db-453">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="929db-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="929db-454">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="929db-454">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="929db-455">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="929db-455">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="929db-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="929db-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="929db-457">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="929db-457">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="929db-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="929db-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="929db-459">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="929db-459">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-460">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="929db-460">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-461">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="929db-461">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="929db-462">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-463">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="929db-463">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="929db-464">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="929db-464">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="929db-465">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="929db-465">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="929db-466">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="929db-466">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="929db-467">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-468">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="929db-468">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-469">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-471">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="929db-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="929db-472">Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="929db-472">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="929db-473">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-473">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="929db-474">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="929db-474">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="929db-475">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-476">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="929db-477">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="929db-477">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="929db-478">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="929db-478">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="929db-479">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="929db-479">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="929db-480">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="929db-480">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="929db-481">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="929db-481">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="929db-482">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="929db-482">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="929db-483">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="929db-483">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="929db-484">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="929db-484">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="929db-485">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="929db-485">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="929db-486">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="929db-486">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="929db-487">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="929db-487">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="929db-488">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="929db-488">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="929db-489">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="929db-489">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="929db-490">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="929db-490">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="929db-491">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="929db-491">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="929db-492">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="929db-492">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="929db-493">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="929db-493">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="929db-494">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="929db-494">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="929db-495">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="929db-495">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="929db-496">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="929db-496">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="929db-497">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="929db-497">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="929db-498">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="929db-498">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="929db-499">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="929db-499">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="929db-500">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="929db-500">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="929db-501">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="929db-501">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="929db-502">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="929db-502">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="929db-503">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="929db-503">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="929db-504">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="929db-504">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="929db-505">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="929db-505">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="929db-506">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="929db-506">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="929db-507">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="929db-507">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="929db-508">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="929db-508">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="929db-509">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="929db-509">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="929db-510">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="929db-510">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="929db-511">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="929db-511">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="929db-512">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="929db-512">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="929db-513">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="929db-513">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="929db-514">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="929db-514">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="929db-515">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="929db-515">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="929db-516">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="929db-516">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="929db-517">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="929db-517">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="929db-518">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="929db-518">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="929db-519">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="929db-519">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="929db-520">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="929db-520">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="929db-521">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="929db-521">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="929db-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-525">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="929db-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="929db-526">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="929db-526">Current status of the object.</span></span> <span data-ttu-id="929db-527">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-527">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="929db-528">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="929db-528">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="929db-529">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="929db-529">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="929db-530">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="929db-530">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="929db-531">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="929db-531">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-532">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="929db-532">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="929db-533">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="929db-533">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="929db-534">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="929db-534">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="929db-535">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="929db-535">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="929db-536">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="929db-536">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="929db-537">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="929db-537">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="929db-538">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="929db-538">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="929db-539">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="929db-539">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="929db-540">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="929db-540">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-541">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="929db-541">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-542">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-542">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-543">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-544">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="929db-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="929db-545">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="929db-545">State of the logical device.</span></span> <span data-ttu-id="929db-546">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="929db-546">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="929db-547">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-547">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="929db-548">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-548">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-549">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-549">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="929db-550">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="929db-550">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="929db-551">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="929db-551">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="929db-552">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="929db-552">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-553">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="929db-553">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-554">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-554">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-555">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-555">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-556">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="929db-556">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="929db-557">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="929db-557">Scoping system's creation class name.</span></span>

<span data-ttu-id="929db-558">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-558">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-559">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="929db-559">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-560">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-561">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-562">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="929db-562">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="929db-563">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="929db-563">Scoping system's name.</span></span>

<span data-ttu-id="929db-564">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-564">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-565">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="929db-565">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-566">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="929db-566">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="929db-567">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-568">Datum und Uhrzeit des letzten zurück Setzens des Controllers, was bedeutet, dass der Controller heruntergefahren oder erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="929db-568">Date and time this controller was last reset meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="929db-569">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-569">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="929db-570">**Videoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="929db-570">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-571">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-572">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-573">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="929db-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="929db-574">Video Architektur.</span><span class="sxs-lookup"><span data-stu-id="929db-574">Video architecture.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="929db-575">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-575">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-576">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-576">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="929db-577">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="929db-577">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="929db-578">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="929db-578">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="929db-579">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="929db-579">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="929db-580">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="929db-580">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="929db-581">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="929db-581">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="929db-582">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="929db-582">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="929db-583">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="929db-583">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="929db-584">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="929db-584">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="929db-585">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="929db-585">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="929db-586">**Linearer Rahmen Puffer** (12)</span><span class="sxs-lookup"><span data-stu-id="929db-586">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="929db-587">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="929db-587">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-588">**Videomemorytype**</span><span class="sxs-lookup"><span data-stu-id="929db-588">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-589">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-589">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-590">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-591">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="929db-591">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="929db-592">Typ des Video Speichers.</span><span class="sxs-lookup"><span data-stu-id="929db-592">Type of video memory.</span></span>

<span data-ttu-id="929db-593">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-593">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="929db-594">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="929db-594">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="929db-595">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="929db-595">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="929db-596">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="929db-596">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="929db-597">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="929db-597">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="929db-598">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="929db-598">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="929db-599">**Wram** (6)</span><span class="sxs-lookup"><span data-stu-id="929db-599">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="929db-600">**EDO RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="929db-600">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="929db-601">**Burst synchroner DRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="929db-601">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="929db-602">**Pipelined Burst-SRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="929db-602">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="929db-603">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="929db-603">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="929db-604">**3dram** (11)</span><span class="sxs-lookup"><span data-stu-id="929db-604">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="929db-605">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="929db-605">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="929db-606">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="929db-606">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="929db-607">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="929db-607">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-608">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="929db-608">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="929db-609">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-609">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929db-610">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="929db-610">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="929db-611">Aktueller Videomodus.</span><span class="sxs-lookup"><span data-stu-id="929db-611">Current video mode.</span></span>

</dd> <dt>

<span data-ttu-id="929db-612">**Videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="929db-612">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929db-613">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="929db-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929db-614">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="929db-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="929db-615">Eine frei Form Zeichenfolge, die den Videoprozessor/-Controller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="929db-615">Free-form string that describes the video processor/controller.</span></span>

<span data-ttu-id="929db-616">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="929db-616">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="929db-617">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="929db-617">Remarks</span></span>

<span data-ttu-id="929db-618">Die **CIM \_ pcvideocontroller** -Klasse wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="929db-618">The **CIM\_PCVideoController** class is derived from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="929db-619">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="929db-619">WMI does not implement this class.</span></span> <span data-ttu-id="929db-620">Informationen zu WMI-Klassen, die von [**CIM \_ pcvideocontroller**](cim-videocontroller.md)abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="929db-620">For WMI classes derived from [**CIM\_PCVideoController**](cim-videocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="929db-621">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="929db-621">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="929db-622">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="929db-622">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="929db-623">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="929db-623">Requirements</span></span>



| <span data-ttu-id="929db-624">Anforderung</span><span class="sxs-lookup"><span data-stu-id="929db-624">Requirement</span></span> | <span data-ttu-id="929db-625">Wert</span><span class="sxs-lookup"><span data-stu-id="929db-625">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="929db-626">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="929db-626">Minimum supported client</span></span><br/> | <span data-ttu-id="929db-627">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="929db-627">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="929db-628">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="929db-628">Minimum supported server</span></span><br/> | <span data-ttu-id="929db-629">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="929db-629">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="929db-630">Namespace</span><span class="sxs-lookup"><span data-stu-id="929db-630">Namespace</span></span><br/>                | <span data-ttu-id="929db-631">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="929db-631">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="929db-632">MOF</span><span class="sxs-lookup"><span data-stu-id="929db-632">MOF</span></span><br/>                      | <dl> <span data-ttu-id="929db-633"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="929db-633"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="929db-634">DLL</span><span class="sxs-lookup"><span data-stu-id="929db-634">DLL</span></span><br/>                      | <dl> <span data-ttu-id="929db-635"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="929db-635"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="929db-636">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="929db-636">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929db-637">**CIM- \_ Videocontroller**</span><span class="sxs-lookup"><span data-stu-id="929db-637">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 

