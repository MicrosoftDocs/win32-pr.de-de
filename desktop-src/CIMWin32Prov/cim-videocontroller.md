---
description: Die CIM \_ Videocontroller-Klasse stellt die Funktionen und die Verwaltung des Video Controllers dar.
ms.assetid: 7cf6bf2a-62a5-46fa-8c8f-976604360461
ms.tgt_platform: multiple
title: CIM_VideoController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController
- CIM_VideoController.AcceleratorCapabilities
- CIM_VideoController.Availability
- CIM_VideoController.CapabilityDescriptions
- CIM_VideoController.Caption
- CIM_VideoController.ConfigManagerErrorCode
- CIM_VideoController.ConfigManagerUserConfig
- CIM_VideoController.CreationClassName
- CIM_VideoController.CurrentBitsPerPixel
- CIM_VideoController.CurrentHorizontalResolution
- CIM_VideoController.CurrentNumberOfColors
- CIM_VideoController.CurrentNumberOfColumns
- CIM_VideoController.CurrentNumberOfRows
- CIM_VideoController.CurrentRefreshRate
- CIM_VideoController.CurrentScanMode
- CIM_VideoController.CurrentVerticalResolution
- CIM_VideoController.Description
- CIM_VideoController.DeviceID
- CIM_VideoController.ErrorCleared
- CIM_VideoController.ErrorDescription
- CIM_VideoController.InstallDate
- CIM_VideoController.LastErrorCode
- CIM_VideoController.MaxMemorySupported
- CIM_VideoController.MaxNumberControlled
- CIM_VideoController.MaxRefreshRate
- CIM_VideoController.MinRefreshRate
- CIM_VideoController.Name
- CIM_VideoController.NumberOfVideoPages
- CIM_VideoController.PNPDeviceID
- CIM_VideoController.PowerManagementCapabilities
- CIM_VideoController.PowerManagementSupported
- CIM_VideoController.ProtocolSupported
- CIM_VideoController.Status
- CIM_VideoController.StatusInfo
- CIM_VideoController.SystemCreationClassName
- CIM_VideoController.SystemName
- CIM_VideoController.TimeOfLastReset
- CIM_VideoController.VideoMemoryType
- CIM_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6475c99e7a6f2ee1bef56bf2c266c788efc0b805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861528"
---
# <a name="cim_videocontroller-class"></a><span data-ttu-id="76b4f-103">CIM- \_ Videocontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="76b4f-103">CIM\_VideoController class</span></span>

<span data-ttu-id="76b4f-104">Die **CIM \_ Videocontroller** -Klasse stellt die Funktionen und die Verwaltung des Video Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="76b4f-104">The **CIM\_VideoController** class represents the capabilities and management of the video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76b4f-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="76b4f-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="76b4f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="76b4f-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76b4f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="76b4f-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b4f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76b4f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE5-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoController : CIM_Controller
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
  uint16   VideoMemoryType;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="76b4f-110">Member</span><span class="sxs-lookup"><span data-stu-id="76b4f-110">Members</span></span>

<span data-ttu-id="76b4f-111">Die **CIM \_ Videocontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="76b4f-111">The **CIM\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="76b4f-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="76b4f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="76b4f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76b4f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76b4f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="76b4f-114">Methods</span></span>

<span data-ttu-id="76b4f-115">Die **CIM \_ Videocontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-115">The **CIM\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="76b4f-116">Methode</span><span class="sxs-lookup"><span data-stu-id="76b4f-116">Method</span></span>                                                                     | <span data-ttu-id="76b4f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76b4f-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76b4f-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="76b4f-118">**Reset**</span></span>](reset-method-in-class-cim-videocontroller.md)                 | <span data-ttu-id="76b4f-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="76b4f-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="76b4f-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="76b4f-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="76b4f-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-videocontroller.md) | <span data-ttu-id="76b4f-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76b4f-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="76b4f-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="76b4f-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76b4f-124">Properties</span></span>

<span data-ttu-id="76b4f-125">Die **CIM \_ Videocontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76b4f-125">The **CIM\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76b4f-126">**Beschleuniger Funktionen**</span><span class="sxs-lookup"><span data-stu-id="76b4f-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-127">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="76b4f-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-129">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Videocontroller**".**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="76b4f-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-130">Grafiken und 3D-Funktionen des Video Controllers.</span><span class="sxs-lookup"><span data-stu-id="76b4f-130">Graphics and 3-D capabilities of the video controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-131">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="76b4f-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76b4f-132">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="76b4f-133">**Grafikbeschleuniger** (2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-133">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="76b4f-134">**3D-Accelerator** (3)</span><span class="sxs-lookup"><span data-stu-id="76b4f-134">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-135">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="76b4f-135">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-136">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76b4f-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-139">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-139">Availability and status of the device.</span></span>

<span data-ttu-id="76b4f-140">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-140">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76b4f-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="76b4f-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="76b4f-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="76b4f-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="76b4f-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="76b4f-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="76b4f-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="76b4f-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="76b4f-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="76b4f-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="76b4f-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="76b4f-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="76b4f-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="76b4f-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="76b4f-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="76b4f-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="76b4f-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="76b4f-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="76b4f-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="76b4f-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="76b4f-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="76b4f-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="76b4f-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-154">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-154">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="76b4f-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="76b4f-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-156">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-156">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="76b4f-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="76b4f-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-158">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-158">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="76b4f-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="76b4f-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="76b4f-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="76b4f-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-161">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-161">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="76b4f-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="76b4f-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-163">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="76b4f-163">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="76b4f-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="76b4f-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-165">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="76b4f-165">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="76b4f-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="76b4f-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-167">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-167">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="76b4f-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="76b4f-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-169">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="76b4f-169">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-170">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="76b4f-170">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-171">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="76b4f-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-173">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Videocontroller**".**Acceleratorfunktionen**")</span><span class="sxs-lookup"><span data-stu-id="76b4f-173">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-174">Freiform-Zeichen folgen, die ausführliche Beschreibungen der im **acceleratorforms** -Array angegebenen videoacceleratorfunktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-174">Free-form strings that provide detailed descriptions for the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="76b4f-175">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **acceleratorfunktionalitäten** -Array, das sich am gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-175">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="76b4f-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="76b4f-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-179">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="76b4f-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-180">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-180">Short textual description of the object.</span></span>

<span data-ttu-id="76b4f-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-182">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="76b4f-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-185">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="76b4f-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-186">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="76b4f-186">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="76b4f-187">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="76b4f-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="76b4f-189"> (0)</span><span class="sxs-lookup"><span data-stu-id="76b4f-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-190">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="76b4f-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="76b4f-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="76b4f-192">(1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-193">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="76b4f-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="76b4f-195">(2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="76b4f-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="76b4f-197">(3)</span><span class="sxs-lookup"><span data-stu-id="76b4f-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-198">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="76b4f-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="76b4f-200">(4)</span><span class="sxs-lookup"><span data-stu-id="76b4f-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-201">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="76b4f-201">Device is not working properly.</span></span> <span data-ttu-id="76b4f-202">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="76b4f-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="76b4f-204">(5)</span><span class="sxs-lookup"><span data-stu-id="76b4f-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-205">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="76b4f-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="76b4f-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="76b4f-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="76b4f-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-208">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="76b4f-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="76b4f-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="76b4f-210">(7)</span><span class="sxs-lookup"><span data-stu-id="76b4f-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="76b4f-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="76b4f-212">(8)</span><span class="sxs-lookup"><span data-stu-id="76b4f-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-213">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="76b4f-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="76b4f-215">(9)</span><span class="sxs-lookup"><span data-stu-id="76b4f-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-216">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="76b4f-216">Device is not working properly.</span></span> <span data-ttu-id="76b4f-217">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="76b4f-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="76b4f-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="76b4f-219">(10)</span><span class="sxs-lookup"><span data-stu-id="76b4f-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-220">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="76b4f-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="76b4f-222">(11)</span><span class="sxs-lookup"><span data-stu-id="76b4f-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-223">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="76b4f-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="76b4f-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="76b4f-225">(12)</span><span class="sxs-lookup"><span data-stu-id="76b4f-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-226">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="76b4f-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="76b4f-228">(13)</span><span class="sxs-lookup"><span data-stu-id="76b4f-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-229">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="76b4f-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="76b4f-231">(14)</span><span class="sxs-lookup"><span data-stu-id="76b4f-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-232">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="76b4f-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="76b4f-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="76b4f-234">(15)</span><span class="sxs-lookup"><span data-stu-id="76b4f-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-235">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="76b4f-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="76b4f-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="76b4f-237">(16)</span><span class="sxs-lookup"><span data-stu-id="76b4f-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-238">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="76b4f-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="76b4f-240">(17)</span><span class="sxs-lookup"><span data-stu-id="76b4f-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-241">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="76b4f-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="76b4f-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="76b4f-243">(18)</span><span class="sxs-lookup"><span data-stu-id="76b4f-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-244">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="76b4f-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="76b4f-246">(19)</span><span class="sxs-lookup"><span data-stu-id="76b4f-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="76b4f-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="76b4f-248">(20)</span><span class="sxs-lookup"><span data-stu-id="76b4f-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-249">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="76b4f-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="76b4f-251">(21)</span><span class="sxs-lookup"><span data-stu-id="76b4f-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-252">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="76b4f-252">System failure.</span></span> <span data-ttu-id="76b4f-253">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="76b4f-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="76b4f-254">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="76b4f-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="76b4f-256">(22)</span><span class="sxs-lookup"><span data-stu-id="76b4f-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-257">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="76b4f-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="76b4f-259">(23)</span><span class="sxs-lookup"><span data-stu-id="76b4f-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-260">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="76b4f-260">System failure.</span></span> <span data-ttu-id="76b4f-261">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="76b4f-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="76b4f-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="76b4f-263">(24)</span><span class="sxs-lookup"><span data-stu-id="76b4f-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-264">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="76b4f-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="76b4f-266">(25)</span><span class="sxs-lookup"><span data-stu-id="76b4f-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-267">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="76b4f-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="76b4f-269">(26)</span><span class="sxs-lookup"><span data-stu-id="76b4f-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-270">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="76b4f-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="76b4f-272">(27)</span><span class="sxs-lookup"><span data-stu-id="76b4f-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-273">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76b4f-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="76b4f-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="76b4f-275">(28)</span><span class="sxs-lookup"><span data-stu-id="76b4f-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-276">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="76b4f-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="76b4f-278">(29)</span><span class="sxs-lookup"><span data-stu-id="76b4f-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-279">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-279">Device is disabled.</span></span> <span data-ttu-id="76b4f-280">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="76b4f-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="76b4f-282">(30)</span><span class="sxs-lookup"><span data-stu-id="76b4f-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-283">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76b4f-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="76b4f-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="76b4f-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="76b4f-285">31,5</span><span class="sxs-lookup"><span data-stu-id="76b4f-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-286">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="76b4f-286">Device is not working properly.</span></span> <span data-ttu-id="76b4f-287">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-288">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="76b4f-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-289">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="76b4f-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-291">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="76b4f-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-292">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="76b4f-293">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-294">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="76b4f-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-297">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="76b4f-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-298">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76b4f-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="76b4f-299">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="76b4f-300">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-301">**Currentbitsperpixel**</span><span class="sxs-lookup"><span data-stu-id="76b4f-301">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-302">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-304">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,12 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-304">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-305">Anzahl von Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-305">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-306">**Ereignis Auflösung**</span><span class="sxs-lookup"><span data-stu-id="76b4f-306">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-307">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-309">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-309">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-310">Aktuelle Anzahl von horizontalen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="76b4f-310">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-311">**Currentzahlofcolors**</span><span class="sxs-lookup"><span data-stu-id="76b4f-311">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-312">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="76b4f-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-314">Anzahl von Farben, die bei der aktuellen Auflösung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-314">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="76b4f-315">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="76b4f-315">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-316">**Currentzahlofcolumns**</span><span class="sxs-lookup"><span data-stu-id="76b4f-316">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-317">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-319">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-320">Wenn im Zeichenmodus die Anzahl der Spalten für den Videocontroller. Andernfalls geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="76b4f-320">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-321">**Currentnumofrows**</span><span class="sxs-lookup"><span data-stu-id="76b4f-321">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-322">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-324">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-325">Im Zeichenmodus die Anzahl der Zeilen für den Videocontroller. Andernfalls geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="76b4f-325">If in character mode, number of rows for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-326">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="76b4f-326">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-327">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-329">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-330">Aktuelle Aktualisierungsrate in Hertz.</span><span class="sxs-lookup"><span data-stu-id="76b4f-330">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-331">**Currentscanmode**</span><span class="sxs-lookup"><span data-stu-id="76b4f-331">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-332">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76b4f-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-334">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-335">Aktueller Scanmodus.</span><span class="sxs-lookup"><span data-stu-id="76b4f-335">Current scan mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76b4f-336">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-336">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-337">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-337">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="76b4f-338">Zeilen **Sprung (3** )</span><span class="sxs-lookup"><span data-stu-id="76b4f-338">**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="76b4f-339">**Nicht** Zeilen Sprung (4)</span><span class="sxs-lookup"><span data-stu-id="76b4f-339">**Non Interlaced** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-340">**Currentverticalresolution**</span><span class="sxs-lookup"><span data-stu-id="76b4f-340">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-341">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-343">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-344">Aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="76b4f-344">Current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-345">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76b4f-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-348">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="76b4f-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-349">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-349">Textual description of the object.</span></span>

<span data-ttu-id="76b4f-350">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="76b4f-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-354">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="76b4f-354">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-355">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-355">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="76b4f-356">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-357">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="76b4f-357">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-358">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="76b4f-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-360">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="76b4f-360">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="76b4f-361">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-362">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="76b4f-362">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-363">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-365">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-365">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="76b4f-366">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-367">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="76b4f-367">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-368">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="76b4f-368">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-370">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-371">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-371">Date and time the object was installed.</span></span> <span data-ttu-id="76b4f-372">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="76b4f-372">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="76b4f-373">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-374">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="76b4f-374">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-375">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-377">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="76b4f-377">Last error code reported by the logical device.</span></span>

<span data-ttu-id="76b4f-378">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-379">**Maxmemorysupported**</span><span class="sxs-lookup"><span data-stu-id="76b4f-379">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-380">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-382">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="76b4f-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-383">Maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="76b4f-383">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-384">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="76b4f-384">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-385">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-386">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-387">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-388">Maximale Anzahl direkt Adressier barer Entitäten, die vom Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-388">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="76b4f-389">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-389">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="76b4f-390">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-391">**Maxfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="76b4f-391">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-392">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-394">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-395">Maximale Aktualisierungsrate des Video Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="76b4f-395">Maximum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-396">**Minfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="76b4f-396">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-397">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-397">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-399">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-400">Minimale Aktualisierungsrate des Video Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="76b4f-400">Minimum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-401">**Name**</span><span class="sxs-lookup"><span data-stu-id="76b4f-401">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-402">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-404">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="76b4f-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-405">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="76b4f-405">Label by which the object is known.</span></span> <span data-ttu-id="76b4f-406">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-406">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="76b4f-407">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-408">**Anzahl der videopages**</span><span class="sxs-lookup"><span data-stu-id="76b4f-408">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-409">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76b4f-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-411">Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="76b4f-411">Number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-412">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="76b4f-412">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-413">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-415">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="76b4f-415">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-416">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-416">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="76b4f-417">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="76b4f-418">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="76b4f-418">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-419">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="76b4f-419">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-420">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="76b4f-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-422">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-422">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="76b4f-423">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-423">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="76b4f-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="76b4f-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76b4f-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="76b4f-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="76b4f-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-428">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76b4f-428">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="76b4f-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="76b4f-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-430">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="76b4f-430">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="76b4f-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="76b4f-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-432">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-432">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="76b4f-433">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-433">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="76b4f-434">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="76b4f-434">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="76b4f-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="76b4f-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-436">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76b4f-436">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="76b4f-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="76b4f-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="76b4f-438">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76b4f-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-439">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="76b4f-439">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-440">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="76b4f-440">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-442">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="76b4f-442">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="76b4f-443">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="76b4f-443">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="76b4f-444">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-444">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="76b4f-445">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="76b4f-445">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="76b4f-446">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-447">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="76b4f-447">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-448">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76b4f-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-450">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-451">Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76b4f-451">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="76b4f-452">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-452">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="76b4f-453">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="76b4f-453">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76b4f-454">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-454">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-455">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-455">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="76b4f-456">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="76b4f-456">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="76b4f-457">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="76b4f-457">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="76b4f-458">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="76b4f-458">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="76b4f-459">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="76b4f-459">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="76b4f-460">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="76b4f-460">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="76b4f-461">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="76b4f-461">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="76b4f-462">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="76b4f-462">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="76b4f-463">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="76b4f-463">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="76b4f-464">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="76b4f-464">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="76b4f-465">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="76b4f-465">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="76b4f-466">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="76b4f-466">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="76b4f-467">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="76b4f-467">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="76b4f-468">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="76b4f-468">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="76b4f-469">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="76b4f-469">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="76b4f-470">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="76b4f-470">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="76b4f-471">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="76b4f-471">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="76b4f-472">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="76b4f-472">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="76b4f-473">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="76b4f-473">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="76b4f-474">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="76b4f-474">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="76b4f-475">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="76b4f-475">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="76b4f-476">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="76b4f-476">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="76b4f-477">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="76b4f-477">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="76b4f-478">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="76b4f-478">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="76b4f-479">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="76b4f-479">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="76b4f-480">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="76b4f-480">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="76b4f-481">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="76b4f-481">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="76b4f-482">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="76b4f-482">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="76b4f-483">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="76b4f-483">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="76b4f-484">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="76b4f-484">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="76b4f-485">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="76b4f-485">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="76b4f-486">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="76b4f-486">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="76b4f-487">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="76b4f-487">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="76b4f-488">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="76b4f-488">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="76b4f-489">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="76b4f-489">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="76b4f-490">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="76b4f-490">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="76b4f-491">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="76b4f-491">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="76b4f-492">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="76b4f-492">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="76b4f-493">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="76b4f-493">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="76b4f-494">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="76b4f-494">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="76b4f-495">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="76b4f-495">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="76b4f-496">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="76b4f-496">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="76b4f-497">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="76b4f-497">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="76b4f-498">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="76b4f-498">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="76b4f-499">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="76b4f-499">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="76b4f-500">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="76b4f-500">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-501">**Status**</span><span class="sxs-lookup"><span data-stu-id="76b4f-501">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-502">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-503">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-504">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="76b4f-504">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-505">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-505">Current status of the object.</span></span> <span data-ttu-id="76b4f-506">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-506">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="76b4f-507">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="76b4f-507">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="76b4f-508">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="76b4f-508">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="76b4f-509">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="76b4f-509">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="76b4f-510">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="76b4f-510">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-511">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="76b4f-511">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="76b4f-512">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="76b4f-512">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="76b4f-513">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="76b4f-513">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="76b4f-514">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-514">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="76b4f-515">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="76b4f-515">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="76b4f-516">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="76b4f-516">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="76b4f-517">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="76b4f-517">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="76b4f-518">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="76b4f-518">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="76b4f-519">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="76b4f-519">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-520">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="76b4f-520">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-521">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76b4f-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-522">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-523">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-524">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="76b4f-524">State of the logical device.</span></span> <span data-ttu-id="76b4f-525">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b4f-525">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="76b4f-526">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-526">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76b4f-527">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-527">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-528">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-528">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="76b4f-529">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="76b4f-529">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76b4f-530">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="76b4f-530">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="76b4f-531">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="76b4f-531">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-532">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="76b4f-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-533">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-534">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-535">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="76b4f-535">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-536">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="76b4f-536">Scoping system's creation class name.</span></span>

<span data-ttu-id="76b4f-537">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-537">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-538">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="76b4f-538">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-539">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-540">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-541">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="76b4f-541">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-542">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="76b4f-542">Scoping system's name.</span></span>

<span data-ttu-id="76b4f-543">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-543">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-544">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="76b4f-544">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-545">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="76b4f-545">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-546">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-546">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-547">Datum und Uhrzeit der letzten zurück setzung des Controllers, was bedeutet, dass der Controller heruntergefahren oder neu initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="76b4f-547">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="76b4f-548">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-548">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="76b4f-549">**Videomemorytype**</span><span class="sxs-lookup"><span data-stu-id="76b4f-549">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-550">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76b4f-550">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-551">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-552">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="76b4f-552">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-553">Typ des Video Speichers.</span><span class="sxs-lookup"><span data-stu-id="76b4f-553">Type of video memory.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76b4f-554">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="76b4f-554">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76b4f-555">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="76b4f-555">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="76b4f-556">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="76b4f-556">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="76b4f-557">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="76b4f-557">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="76b4f-558">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="76b4f-558">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="76b4f-559">**Wram** (6)</span><span class="sxs-lookup"><span data-stu-id="76b4f-559">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="76b4f-560">**EDO RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="76b4f-560">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="76b4f-561">**Burst synchroner DRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="76b4f-561">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="76b4f-562">**Pipelined Burst-SRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="76b4f-562">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="76b4f-563">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="76b4f-563">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="76b4f-564">**3dram** (11)</span><span class="sxs-lookup"><span data-stu-id="76b4f-564">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="76b4f-565">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="76b4f-565">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="76b4f-566">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="76b4f-566">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76b4f-567">**Videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="76b4f-567">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76b4f-568">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76b4f-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76b4f-569">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76b4f-569">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76b4f-570">Eine frei Form Zeichenfolge, die den Videoprozessor oder den Controller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="76b4f-570">Free-form string that describes the video processor or controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76b4f-571">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76b4f-571">Remarks</span></span>

<span data-ttu-id="76b4f-572">Die **CIM- \_ Videocontroller** -Klasse wird vom [**CIM- \_ Controller**](cim-controller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-572">The **CIM\_VideoController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="76b4f-573">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="76b4f-573">WMI does not implement this class.</span></span> <span data-ttu-id="76b4f-574">Informationen zu WMI-Klassen, die von **CIM \_ Videocontroller** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="76b4f-574">For WMI classes derived from **CIM\_VideoController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="76b4f-575">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="76b4f-575">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="76b4f-576">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="76b4f-576">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="76b4f-577">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76b4f-577">Requirements</span></span>



| <span data-ttu-id="76b4f-578">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76b4f-578">Requirement</span></span> | <span data-ttu-id="76b4f-579">Wert</span><span class="sxs-lookup"><span data-stu-id="76b4f-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76b4f-580">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76b4f-580">Minimum supported client</span></span><br/> | <span data-ttu-id="76b4f-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76b4f-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76b4f-582">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76b4f-582">Minimum supported server</span></span><br/> | <span data-ttu-id="76b4f-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76b4f-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76b4f-584">Namespace</span><span class="sxs-lookup"><span data-stu-id="76b4f-584">Namespace</span></span><br/>                | <span data-ttu-id="76b4f-585">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="76b4f-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="76b4f-586">MOF</span><span class="sxs-lookup"><span data-stu-id="76b4f-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76b4f-587"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="76b4f-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="76b4f-588">DLL</span><span class="sxs-lookup"><span data-stu-id="76b4f-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76b4f-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76b4f-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76b4f-590">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76b4f-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b4f-591">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="76b4f-591">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

