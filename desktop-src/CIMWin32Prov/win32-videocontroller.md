---
description: Stellt die Funktionen und die Verwaltungskapazität des Video Controllers auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Win32_VideoController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482771"
---
# <a name="win32_videocontroller-class"></a><span data-ttu-id="a0b99-103">Win32 \_ Videocontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="a0b99-103">Win32\_VideoController class</span></span>

<span data-ttu-id="a0b99-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) von **Win32 \_ Videocontroller** stellt die Funktionen und die Verwaltungskapazität des Video Controllers auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-104">The **Win32\_VideoController** [WMI class](../wmisdk/retrieving-a-class.md) represents the capabilities and management capacity of the video controller on a computer system running Windows.</span></span>

<span data-ttu-id="a0b99-105">Hardware, die nicht mit dem Windows-Anzeigetreiber Modell (WDDM) kompatibel ist, gibt falsche Eigenschaftswerte für Instanzen dieser Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="a0b99-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="a0b99-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a0b99-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a0b99-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b99-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0b99-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
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
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="a0b99-109">Member</span><span class="sxs-lookup"><span data-stu-id="a0b99-109">Members</span></span>

<span data-ttu-id="a0b99-110">Die **Win32 \_ Videocontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a0b99-110">The **Win32\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="a0b99-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a0b99-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0b99-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0b99-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0b99-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="a0b99-113">Methods</span></span>

<span data-ttu-id="a0b99-114">Die **Win32 \_ Videocontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-114">The **Win32\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="a0b99-115">Methode</span><span class="sxs-lookup"><span data-stu-id="a0b99-115">Method</span></span>            | <span data-ttu-id="a0b99-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0b99-116">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b99-117">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="a0b99-117">**Reset**</span></span>         | <span data-ttu-id="a0b99-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-118">Not implemented.</span></span> <span data-ttu-id="a0b99-119">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a0b99-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/>                 |
| <span data-ttu-id="a0b99-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a0b99-120">**SetPowerState**</span></span> | <span data-ttu-id="a0b99-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-121">Not implemented.</span></span> <span data-ttu-id="a0b99-122">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a0b99-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0b99-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0b99-123">Properties</span></span>

<span data-ttu-id="a0b99-124">Die **Win32 \_ Videocontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a0b99-124">The **Win32\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0b99-125">**Beschleuniger Funktionen**</span><span class="sxs-lookup"><span data-stu-id="a0b99-125">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-126">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a0b99-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-128">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="a0b99-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-129">Array von Grafiken und 3D-Funktionen des Video Controllers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-129">Array of graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="a0b99-130">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-130">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a0b99-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0b99-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="a0b99-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Grafikbeschleuniger** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="a0b99-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D-Accelerator** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-135">3D-Accelerator</span><span class="sxs-lookup"><span data-stu-id="a0b99-135">3-D Accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-136">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="a0b99-136">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-139">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="a0b99-139">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-140">Allgemeiner Chipsatz, der für diesen Controller zum Vergleichen von Kompatibilitäten mit dem System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-140">General chipset used for this controller to compare compatibilities with the system.</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-141">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="a0b99-141">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-144">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardwareinformation. dactype")</span><span class="sxs-lookup"><span data-stu-id="a0b99-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.DACType")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-145">Der Name oder Bezeichner des Digital-to-Analog Converter-Chips (DAC).</span><span class="sxs-lookup"><span data-stu-id="a0b99-145">Name or identifier of the digital-to-analog converter (DAC) chip.</span></span> <span data-ttu-id="a0b99-146">Der Zeichensatz dieser Eigenschaft ist alphanumerisch.</span><span class="sxs-lookup"><span data-stu-id="a0b99-146">The character set of this property is alphanumeric.</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-147">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="a0b99-147">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-150">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardwareinformation. MemorySize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="a0b99-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-151">Arbeitsspeicher Größe der Grafikkarte.</span><span class="sxs-lookup"><span data-stu-id="a0b99-151">Memory size of the video adapter.</span></span>

<span data-ttu-id="a0b99-152">Beispiel: 64000</span><span class="sxs-lookup"><span data-stu-id="a0b99-152">Example: 64000</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-153">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="a0b99-153">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-156">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-157">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-157">Availability and status of the device.</span></span>

<span data-ttu-id="a0b99-158">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-158">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0b99-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a0b99-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-162">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="a0b99-162">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a0b99-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a0b99-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="a0b99-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a0b99-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="a0b99-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a0b99-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="a0b99-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a0b99-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="a0b99-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-168">Offline</span><span class="sxs-lookup"><span data-stu-id="a0b99-168">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a0b99-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="a0b99-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a0b99-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="a0b99-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a0b99-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="a0b99-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a0b99-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="a0b99-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a0b99-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="a0b99-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-174">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-174">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a0b99-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="a0b99-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-176">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a0b99-176">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a0b99-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="a0b99-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-178">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-178">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a0b99-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="a0b99-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a0b99-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="a0b99-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-181">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-181">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a0b99-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="a0b99-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-183">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="a0b99-183">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a0b99-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="a0b99-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-185">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="a0b99-185">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a0b99-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="a0b99-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-187">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-187">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a0b99-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="a0b99-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-189">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="a0b99-189">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-190">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="a0b99-190">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-191">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a0b99-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-193">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Acceleratorfunktionen**")</span><span class="sxs-lookup"><span data-stu-id="a0b99-193">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-194">Freiform-Zeichen folgen, die Ausführlichere Erläuterungen zu den im **acceleratorforms** -Array aufgeführten Features der videoaccelerationsfunktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a0b99-194">Free-form strings providing more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="a0b99-195">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **acceleratorfunktionalitäten** -Array verknüpft ist, das sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-195">Note, each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

<span data-ttu-id="a0b99-196">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-196">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-197">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a0b99-197">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-200">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a0b99-200">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-201">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-201">Short description of the object.</span></span>

<span data-ttu-id="a0b99-202">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-202">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-203">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="a0b99-203">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-204">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-206">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="a0b99-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-207">Die Größe der Farbtabelle des Systems.</span><span class="sxs-lookup"><span data-stu-id="a0b99-207">Size of the system's color table.</span></span> <span data-ttu-id="a0b99-208">Das Gerät muss eine Farbtiefe von höchstens 8 Bits pro Pixel aufweisen. Andernfalls ist diese Eigenschaft nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-208">The device must have a color depth of no more than 8 bits per pixel; otherwise, this property is not set.</span></span>

<span data-ttu-id="a0b99-209">Beispiel: 256</span><span class="sxs-lookup"><span data-stu-id="a0b99-209">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-210">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="a0b99-210">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-211">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-213">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0b99-213">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-214">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a0b99-214">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a0b99-215">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-215">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a0b99-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a0b99-217"> (0)</span><span class="sxs-lookup"><span data-stu-id="a0b99-217">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-218">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a0b99-218">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a0b99-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a0b99-220">(1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-220">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-221">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-221">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0b99-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a0b99-223">(2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-223">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a0b99-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a0b99-225">(3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-225">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-226">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a0b99-226">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a0b99-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a0b99-228">(4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-228">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-229">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a0b99-229">Device is not working properly.</span></span> <span data-ttu-id="a0b99-230">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-230">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a0b99-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a0b99-232">(5)</span><span class="sxs-lookup"><span data-stu-id="a0b99-232">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-233">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0b99-233">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a0b99-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a0b99-235"> (6)</span><span class="sxs-lookup"><span data-stu-id="a0b99-235">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-236">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="a0b99-236">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a0b99-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a0b99-238">(7)</span><span class="sxs-lookup"><span data-stu-id="a0b99-238">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a0b99-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a0b99-240">(8)</span><span class="sxs-lookup"><span data-stu-id="a0b99-240">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-241">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-241">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a0b99-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a0b99-243">(9)</span><span class="sxs-lookup"><span data-stu-id="a0b99-243">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-244">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a0b99-244">Device is not working properly.</span></span> <span data-ttu-id="a0b99-245">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="a0b99-245">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a0b99-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a0b99-247">(10)</span><span class="sxs-lookup"><span data-stu-id="a0b99-247">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-248">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-248">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a0b99-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a0b99-250">(11)</span><span class="sxs-lookup"><span data-stu-id="a0b99-250">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-251">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="a0b99-251">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a0b99-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a0b99-253">(12)</span><span class="sxs-lookup"><span data-stu-id="a0b99-253">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-254">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-254">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a0b99-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a0b99-256">(13)</span><span class="sxs-lookup"><span data-stu-id="a0b99-256">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-257">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-257">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a0b99-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a0b99-259">(14)</span><span class="sxs-lookup"><span data-stu-id="a0b99-259">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-260">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-260">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a0b99-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a0b99-262">(15)</span><span class="sxs-lookup"><span data-stu-id="a0b99-262">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-263">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a0b99-263">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a0b99-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a0b99-265">(16)</span><span class="sxs-lookup"><span data-stu-id="a0b99-265">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-266">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-266">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a0b99-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a0b99-268">(17)</span><span class="sxs-lookup"><span data-stu-id="a0b99-268">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-269">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="a0b99-269">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0b99-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a0b99-271">(18)</span><span class="sxs-lookup"><span data-stu-id="a0b99-271">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-272">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-272">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a0b99-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a0b99-274">(19)</span><span class="sxs-lookup"><span data-stu-id="a0b99-274">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a0b99-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a0b99-276">(20)</span><span class="sxs-lookup"><span data-stu-id="a0b99-276">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-277">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-277">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a0b99-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a0b99-279">(21)</span><span class="sxs-lookup"><span data-stu-id="a0b99-279">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-280">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0b99-280">System failure.</span></span> <span data-ttu-id="a0b99-281">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a0b99-281">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a0b99-282">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-282">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a0b99-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a0b99-284">(22)</span><span class="sxs-lookup"><span data-stu-id="a0b99-284">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-285">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-285">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a0b99-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a0b99-287">(23)</span><span class="sxs-lookup"><span data-stu-id="a0b99-287">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-288">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0b99-288">System failure.</span></span> <span data-ttu-id="a0b99-289">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a0b99-289">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a0b99-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a0b99-291">(24)</span><span class="sxs-lookup"><span data-stu-id="a0b99-291">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-292">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-292">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a0b99-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a0b99-294">(25)</span><span class="sxs-lookup"><span data-stu-id="a0b99-294">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-295">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-295">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a0b99-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a0b99-297">(26)</span><span class="sxs-lookup"><span data-stu-id="a0b99-297">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-298">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a0b99-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a0b99-300">(27)</span><span class="sxs-lookup"><span data-stu-id="a0b99-300">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-301">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a0b99-301">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a0b99-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a0b99-303">(28)</span><span class="sxs-lookup"><span data-stu-id="a0b99-303">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-304">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-304">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a0b99-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a0b99-306">(29)</span><span class="sxs-lookup"><span data-stu-id="a0b99-306">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-307">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-307">Device is disabled.</span></span> <span data-ttu-id="a0b99-308">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-308">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a0b99-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a0b99-310">(30)</span><span class="sxs-lookup"><span data-stu-id="a0b99-310">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-311">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-311">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0b99-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="a0b99-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a0b99-313">31,5</span><span class="sxs-lookup"><span data-stu-id="a0b99-313">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-314">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a0b99-314">Device is not working properly.</span></span> <span data-ttu-id="a0b99-315">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-315">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-316">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="a0b99-316">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-317">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a0b99-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-319">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0b99-319">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-320">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-320">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a0b99-321">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-322">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a0b99-322">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-323">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-325">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a0b99-325">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-326">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-326">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a0b99-327">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-327">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a0b99-328">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-329">**Currentbitsperpixel**</span><span class="sxs-lookup"><span data-stu-id="a0b99-329">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-330">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-332">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,12 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-333">Anzahl von Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-333">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="a0b99-334">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-334">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-335">**Ereignis Auflösung**</span><span class="sxs-lookup"><span data-stu-id="a0b99-335">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-336">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-338">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,11 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-339">Aktuelle Anzahl von horizontalen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="a0b99-339">Current number of horizontal pixels.</span></span>

<span data-ttu-id="a0b99-340">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-340">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-341">**Currentzahlofcolors**</span><span class="sxs-lookup"><span data-stu-id="a0b99-341">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-342">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0b99-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-344">Anzahl von Farben, die bei der aktuellen Auflösung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-344">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="a0b99-345">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a0b99-345">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="a0b99-346">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-346">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-347">**Currentzahlofcolumns**</span><span class="sxs-lookup"><span data-stu-id="a0b99-347">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-348">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-350">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-351">Anzahl der Spalten für diesen Videocontroller (im Zeichenmodus).</span><span class="sxs-lookup"><span data-stu-id="a0b99-351">Number of columns for this video controller (if in character mode).</span></span> <span data-ttu-id="a0b99-352">Andernfalls geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="a0b99-352">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="a0b99-353">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-353">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-354">**Currentnumofrows**</span><span class="sxs-lookup"><span data-stu-id="a0b99-354">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-355">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-357">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-358">Anzahl der Zeilen für diesen Videocontroller (im Zeichenmodus).</span><span class="sxs-lookup"><span data-stu-id="a0b99-358">Number of rows for this video controller (if in character mode).</span></span> <span data-ttu-id="a0b99-359">Andernfalls geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="a0b99-359">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="a0b99-360">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-360">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-361">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="a0b99-361">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-362">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-364">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardwareinformation."), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="a0b99-364">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-365">Häufigkeit, mit der der Videocontroller das Bild für den Monitor aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a0b99-365">Frequency at which the video controller refreshes the image for the monitor.</span></span> <span data-ttu-id="a0b99-366">Der Wert 0 (null) gibt an, dass die Standard Rate verwendet wird, während 0xFFFFFFFF angibt, dass die optimale Rate verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-366">A value of 0 (zero) indicates the default rate is being used, while 0xFFFFFFFF indicates the optimal rate is being used.</span></span>

<span data-ttu-id="a0b99-367">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-367">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-368">**Currentscanmode**</span><span class="sxs-lookup"><span data-stu-id="a0b99-368">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-369">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-371">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-372">Aktueller Scanmodus.</span><span class="sxs-lookup"><span data-stu-id="a0b99-372">Current scan mode.</span></span>

<span data-ttu-id="a0b99-373">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-373">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0b99-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="a0b99-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>Zeilen **Sprung (3** )</span><span class="sxs-lookup"><span data-stu-id="a0b99-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="a0b99-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Nicht** Zeilen Sprung (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-378">Nicht Zeilen Sprung</span><span class="sxs-lookup"><span data-stu-id="a0b99-378">Noninterlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-379">**Currentverticalresolution**</span><span class="sxs-lookup"><span data-stu-id="a0b99-379">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-380">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-382">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,10 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-383">Aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="a0b99-383">Current number of vertical pixels.</span></span>

<span data-ttu-id="a0b99-384">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-384">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-385">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0b99-385">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-386">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-388">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a0b99-388">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-389">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-389">Description of the object.</span></span>

<span data-ttu-id="a0b99-390">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-390">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-391">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a0b99-391">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-392">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-394">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a0b99-394">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-395">Bezeichner (für das Computersystem eindeutig) für diesen Videocontroller.</span><span class="sxs-lookup"><span data-stu-id="a0b99-395">Identifier (unique to the computer system) for this video controller.</span></span>

<span data-ttu-id="a0b99-396">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-397">**Geräte Einstellungs Stifte**</span><span class="sxs-lookup"><span data-stu-id="a0b99-397">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-398">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-400">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="a0b99-400">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-401">Aktuelle Anzahl der gerätespezifischen Stifte.</span><span class="sxs-lookup"><span data-stu-id="a0b99-401">Current number of device-specific pens.</span></span> <span data-ttu-id="a0b99-402">Der Wert 0xFFFF bedeutet, dass das Gerät keine Stifte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-402">A value of 0xffff means that the device does not support pens.</span></span>

<span data-ttu-id="a0b99-403">Beispiel: 3</span><span class="sxs-lookup"><span data-stu-id="a0b99-403">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-404">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="a0b99-404">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-405">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-407">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| enumdisplaysettings")</span><span class="sxs-lookup"><span data-stu-id="a0b99-407">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|EnumDisplaySettings")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-408">Der Typ des Video Controllers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-408">Dither type of the video controller.</span></span> <span data-ttu-id="a0b99-409">Bei der Eigenschaft kann es sich um einen der vordefinierten Werte oder um einen von einem Treiber definierten Wert handeln, der größer oder gleich 256 ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-409">The property can be one of the predefined values, or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="a0b99-410">Wenn Linienart-Dithering ausgewählt wird, verwendet der Controller eine Dithering-Methode, die klar definierte Rahmen zwischen Schwarzen, weißen und grauen Skalierungen erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-410">If line art dithering is chosen, the controller uses a dithering method that produces well-defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="a0b99-411">Linienart-Dithering eignet sich nicht für Bilder, die kontinuierliche Abschlüsse in Intensität und Farbton enthalten, wie z. b. gescannte Fotos.</span><span class="sxs-lookup"><span data-stu-id="a0b99-411">Line art dithering is not suitable for images that include continuous graduations in intensity and hue such as scanned photographs.</span></span>

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

<span data-ttu-id="a0b99-412">**Keine Dithering** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-412">**No dithering** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

<span data-ttu-id="a0b99-413">**Dithering mit einem groben Pinsel** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-413">**Dithering with a coarse brush** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

<span data-ttu-id="a0b99-414">**Dithering mit einem Pinsel** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-414">**Dithering with a fine brush** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

<span data-ttu-id="a0b99-415">**Linienkunst Dithering** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-415">**Line art dithering** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

<span data-ttu-id="a0b99-416">**Das Gerät führt eine graue Skalierung** durch (5).</span><span class="sxs-lookup"><span data-stu-id="a0b99-416">**Device does gray scaling** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-417">**Driverdate**</span><span class="sxs-lookup"><span data-stu-id="a0b99-417">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-418">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0b99-418">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-420">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-420">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-421">Datum und Uhrzeit der letzten Änderung des aktuell installierten Video Treibers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-421">Last modification date and time of the currently installed video driver.</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-422">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="a0b99-422">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-423">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-425">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Installation Library Functions \| GetFileVersionInfo")</span><span class="sxs-lookup"><span data-stu-id="a0b99-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Installation Library Functions\|GetFileVersionInfo")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-426">Versionsnummer des Video Treibers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-426">Version number of the video driver.</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-427">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="a0b99-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-428">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a0b99-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-430">**True** gibt an, dass der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="a0b99-430">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a0b99-431">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-432">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a0b99-432">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-433">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-435">Frei Form Zeichenfolge, die weitere Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie Informationen zu eventuell durchgeführten Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="a0b99-435">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="a0b99-436">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-437">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="a0b99-437">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-438">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-440">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print Spooler Structures \| DEVMODE \| dmicmintent")</span><span class="sxs-lookup"><span data-stu-id="a0b99-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMIntent")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-441">Bestimmter Wert einer der drei möglichen Farb Vergleichsmethoden oder Intents, die standardmäßig verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a0b99-441">Specific value of one of the three possible color-matching methods or intents that should be used by default.</span></span> <span data-ttu-id="a0b99-442">Diese Eigenschaft wird hauptsächlich für nicht-ICM-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-442">This property is used primarily for non-ICM applications.</span></span> <span data-ttu-id="a0b99-443">ICM-Anwendungen stellen Intents mithilfe der ICM-Funktionen her.</span><span class="sxs-lookup"><span data-stu-id="a0b99-443">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="a0b99-444">Bei dieser Eigenschaft kann es sich um einen vordefinierten Wert oder einen Treiber definierten Wert handeln, der größer oder gleich 256 ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-444">This property can be a predefined value or a driver defined value greater than or equal to 256.</span></span> <span data-ttu-id="a0b99-445">Farb Vergleiche auf der Grundlage von Sättigung ist die geeignetste Wahl für Unternehmens Diagramme, wenn Dithering nicht gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-445">Color matching based on saturation is the most appropriate choice for business graphs when dithering is not desired.</span></span> <span data-ttu-id="a0b99-446">Farbabgleich auf der Grundlage von Kontrast ist die am besten geeignete Option für gescannte oder fotografische Bilder, wenn Dithering gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-446">Color matching based on contrast is the most appropriate choice for scanned or photographic images when dithering is desired.</span></span> <span data-ttu-id="a0b99-447">Die Farbe, die entsprechend der angeforderten Farbe optimiert ist, eignet sich am besten für die Verwendung mit Geschäfts Logos oder anderen Bildern, wenn eine exakte Farb Übereinstimmung gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-447">Color matching optimized to match the exact color requested is most appropriate for use with business logos or other images when an exact color match is desired.</span></span>

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

<span data-ttu-id="a0b99-448">**Sättigung** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-448">**Saturation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

<span data-ttu-id="a0b99-449">**Kontrast** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-449">**Contrast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

<span data-ttu-id="a0b99-450">**Exakte Farbe** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-450">**Exact Color** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-451">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="a0b99-451">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-452">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-454">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print Spooler Structures \| DEVMODE \| dmicmmethod")</span><span class="sxs-lookup"><span data-stu-id="a0b99-454">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMMethod")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-455">Methode der ICM-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a0b99-455">Method of handling ICM.</span></span> <span data-ttu-id="a0b99-456">Bei nicht-ICM-Anwendungen bestimmt diese Eigenschaft, ob ICM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-456">For non-ICM applications, this property determines if ICM is enabled.</span></span> <span data-ttu-id="a0b99-457">Für ICM-Anwendungen prüft das System diese Eigenschaft, um zu bestimmen, wie die ICM-Unterstützung behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0b99-457">For ICM applications, the system examines this property to determine how to handle ICM support.</span></span> <span data-ttu-id="a0b99-458">Bei dieser Eigenschaft kann es sich um einen vordefinierten Wert oder einen Treiber definierten Wert handeln, der größer oder gleich 256 ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-458">This property can be a predefined value or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="a0b99-459">Der-Wert bestimmt, welches System Abbild Farbabgleich behandelt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-459">The value determines which system handles image color matching.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0b99-460">**Deaktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-460">**Disabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

<span data-ttu-id="a0b99-461">**Windows** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-461">**Windows** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

<span data-ttu-id="a0b99-462">**Gerätetreiber** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-462">**Device Driver** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

<span data-ttu-id="a0b99-463">**Zielgerät** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-463">**Destination Device** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-464">**INFFILENAME**</span><span class="sxs-lookup"><span data-stu-id="a0b99-464">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-465">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-466">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-467">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4d36e968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="a0b99-467">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-468">Der Pfad zur INF-Datei des Video Adapters.</span><span class="sxs-lookup"><span data-stu-id="a0b99-468">Path to the video adapter's .inf file.</span></span>

<span data-ttu-id="a0b99-469">Beispiel: "C: \\ Windows \\ system32 \\ Drivers"</span><span class="sxs-lookup"><span data-stu-id="a0b99-469">Example: "C:\\Windows\\SYSTEM32\\DRIVERS"</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-470">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="a0b99-470">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-471">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-473">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4d36e968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="a0b99-473">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-474">Abschnitt der INF-Datei, in der sich die Windows-Videoinformationen befinden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-474">Section of the .inf file where the Windows video information resides.</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-475">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a0b99-475">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-476">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0b99-476">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-478">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-479">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-479">Date and time the object was installed.</span></span> <span data-ttu-id="a0b99-480">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-480">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a0b99-481">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-482">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="a0b99-482">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-483">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-484">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-485">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-485">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-486">Der Name des installierten Anzeigegeräte Treibers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-486">Name of the installed display device driver.</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-487">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a0b99-487">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-488">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-489">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-490">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a0b99-490">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a0b99-491">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-492">**Maxmemorysupported**</span><span class="sxs-lookup"><span data-stu-id="a0b99-492">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-493">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-494">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-495">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="a0b99-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-496">Maximal unterstützter Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a0b99-496">Maximum amount of memory supported in bytes.</span></span>

<span data-ttu-id="a0b99-497">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-497">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-498">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="a0b99-498">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-499">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-499">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-501">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-501">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-502">Maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-502">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="a0b99-503">Wenn die Zahl unbekannt ist, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-503">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="a0b99-504">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-504">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-505">**Maxfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="a0b99-505">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-506">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-508">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,5 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-508">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-509">Maximale Aktualisierungsrate des Video Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="a0b99-509">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="a0b99-510">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-510">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-511">**Minfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="a0b99-511">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-512">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-512">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-514">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,4 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-514">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-515">Minimale Aktualisierungsrate des Video Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="a0b99-515">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="a0b99-516">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-516">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-517">**Monochrom**</span><span class="sxs-lookup"><span data-stu-id="a0b99-517">**Monochrome**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-518">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a0b99-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-520">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a0b99-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-521">**True** gibt an, dass die graue Skala zum Anzeigen von Bildern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-521">If **TRUE**, gray scale is used to display images.</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-522">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0b99-522">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-525">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a0b99-525">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-526">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-526">Label by which the object is known.</span></span> <span data-ttu-id="a0b99-527">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-527">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a0b99-528">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-528">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-529">**Anzahl von colorplane**</span><span class="sxs-lookup"><span data-stu-id="a0b99-529">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-530">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-531">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-532">Aktuelle Anzahl von Farbebenen.</span><span class="sxs-lookup"><span data-stu-id="a0b99-532">Current number of color planes.</span></span> <span data-ttu-id="a0b99-533">Wenn dieser Wert für die aktuelle Video Konfiguration nicht anwendbar ist, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="a0b99-533">If this value is not applicable for the current video configuration, enter 0 (zero).</span></span>

<span data-ttu-id="a0b99-534">Diese Eigenschaft wird von [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-534">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-535">**Anzahl der videopages**</span><span class="sxs-lookup"><span data-stu-id="a0b99-535">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-536">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-536">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-537">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-538">Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-538">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="a0b99-539">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-539">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-540">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a0b99-540">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-541">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-543">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0b99-543">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-544">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-544">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a0b99-545">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a0b99-545">Example: "\*PNP030b"</span></span>

<span data-ttu-id="a0b99-546">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-546">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-547">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="a0b99-547">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-548">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a0b99-548">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-549">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-550">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-550">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a0b99-551">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-551">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a0b99-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a0b99-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0b99-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a0b99-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-556">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0b99-556">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a0b99-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-558">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="a0b99-558">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a0b99-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="a0b99-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-560">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-560">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a0b99-561">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-561">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="a0b99-562">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="a0b99-562">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a0b99-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="a0b99-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-564">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-564">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a0b99-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="a0b99-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-566">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-566">Timed Power-On Supported</span></span>

<span data-ttu-id="a0b99-567">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-567">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-568">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="a0b99-568">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-569">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a0b99-569">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-570">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-570">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-571">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="a0b99-571">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="a0b99-572">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-572">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="a0b99-573">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-574">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="a0b99-574">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-575">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-576">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-577">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-577">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-578">Protokoll, das vom Controller für den Zugriff auf "gesteuerte" Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b99-578">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="a0b99-579">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-579">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0b99-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="a0b99-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="a0b99-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="a0b99-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="a0b99-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="a0b99-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="a0b99-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a0b99-586">ATA oder ATAPI</span><span class="sxs-lookup"><span data-stu-id="a0b99-586">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="a0b99-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="a0b99-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="a0b99-588"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="a0b99-588"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="a0b99-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="a0b99-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="a0b99-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="a0b99-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="a0b99-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="a0b99-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="a0b99-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="a0b99-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="a0b99-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="a0b99-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="a0b99-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="a0b99-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="a0b99-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="a0b99-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="a0b99-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="a0b99-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="a0b99-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="a0b99-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="a0b99-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="a0b99-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="a0b99-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="a0b99-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="a0b99-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="a0b99-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="a0b99-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="a0b99-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="a0b99-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="a0b99-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="a0b99-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="a0b99-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="a0b99-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="a0b99-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="a0b99-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="a0b99-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="a0b99-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="a0b99-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="a0b99-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="a0b99-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="a0b99-608"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="a0b99-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="a0b99-609"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="a0b99-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="a0b99-610"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="a0b99-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="a0b99-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="a0b99-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="a0b99-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="a0b99-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="a0b99-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="a0b99-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="a0b99-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="a0b99-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="a0b99-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="a0b99-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="a0b99-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="a0b99-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="a0b99-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="a0b99-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="a0b99-618"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="a0b99-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="a0b99-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="a0b99-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="a0b99-620"><span id="DSSI"></span><span id="dssi"></span>**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="a0b99-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="a0b99-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="a0b99-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="a0b99-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="a0b99-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="a0b99-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="a0b99-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="a0b99-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="a0b99-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="a0b99-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="a0b99-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="a0b99-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="a0b99-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="a0b99-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="a0b99-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-628">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="a0b99-628">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-629">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-629">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-630">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-631">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="a0b99-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-632">Anzahl reservierter Einträge in der Systempalette.</span><span class="sxs-lookup"><span data-stu-id="a0b99-632">Number of reserved entries in the system palette.</span></span> <span data-ttu-id="a0b99-633">Das Betriebssystem kann Einträge reservieren, um Standardfarben für Task leisten und andere Desktop Anzeigeelemente zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a0b99-633">The operating system may reserve entries to support standard colors for task bars and other desktop display items.</span></span> <span data-ttu-id="a0b99-634">Dieser Index ist nur gültig, wenn der Gerätetreiber das **RC- \_ palettenbit** im RasterCaps-Index festlegt und nur verfügbar ist, wenn der Treiber mit 16-Bit-Windows kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-634">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="a0b99-635">Wenn das System keine Palette verwendet, ist **ReservedSystemPaletteEntries** nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-635">If the system is not using a palette, **ReservedSystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="a0b99-636">Beispiel: 20</span><span class="sxs-lookup"><span data-stu-id="a0b99-636">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-637">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="a0b99-637">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-638">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-638">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-639">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-639">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-640">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print Spooler Structures \| DEVMODE \| dmspecversion")</span><span class="sxs-lookup"><span data-stu-id="a0b99-640">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmSpecVersion")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-641">Die Versionsnummer der Initialisierungs Daten Spezifikation (auf der die Struktur basiert).</span><span class="sxs-lookup"><span data-stu-id="a0b99-641">Version number of the initialization data specification (upon which the structure is based).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-642">**Status**</span><span class="sxs-lookup"><span data-stu-id="a0b99-642">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-643">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-644">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-644">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-645">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a0b99-645">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-646">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-646">Current status of the object.</span></span> <span data-ttu-id="a0b99-647">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-647">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a0b99-648">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="a0b99-648">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a0b99-649">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="a0b99-649">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a0b99-650">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-650">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a0b99-651">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a0b99-651">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a0b99-652">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-652">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a0b99-653">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a0b99-653">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a0b99-654">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a0b99-654">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a0b99-655">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a0b99-655">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a0b99-656">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a0b99-656">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-657">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a0b99-657">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a0b99-658">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a0b99-658">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a0b99-659">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a0b99-659">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a0b99-660">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-660">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a0b99-661">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a0b99-661">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a0b99-662">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a0b99-662">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a0b99-663">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a0b99-663">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a0b99-664">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a0b99-664">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a0b99-665">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a0b99-665">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-666">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a0b99-666">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-667">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-667">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-668">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-668">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-669">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-669">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-670">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a0b99-670">State of the logical device.</span></span> <span data-ttu-id="a0b99-671">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0b99-671">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a0b99-672">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-672">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0b99-673">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-673">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-674">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-674">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a0b99-675">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-675">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0b99-676">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-676">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a0b99-677">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="a0b99-677">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-678">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="a0b99-678">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-679">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-679">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-680">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-681">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a0b99-681">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-682">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-682">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="a0b99-683">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-683">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-684">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="a0b99-684">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-685">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-685">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-686">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-687">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a0b99-687">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-688">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a0b99-688">Name of the scoping system.</span></span>

<span data-ttu-id="a0b99-689">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-689">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-690">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="a0b99-690">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-691">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b99-691">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-692">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-692">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-693">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="a0b99-693">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-694">Aktuelle Anzahl der Farb Indexeinträge in der Systempalette.</span><span class="sxs-lookup"><span data-stu-id="a0b99-694">Current number of color index entries in the system palette.</span></span> <span data-ttu-id="a0b99-695">Dieser Index ist nur gültig, wenn der Gerätetreiber das **RC- \_ palettenbit** im RasterCaps-Index festlegt und nur verfügbar ist, wenn der Treiber mit 16-Bit-Windows kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="a0b99-695">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="a0b99-696">Wenn das System keine Palette verwendet, ist **SystemPaletteEntries** nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-696">If the system is not using a palette, **SystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="a0b99-697">Beispiel: 20</span><span class="sxs-lookup"><span data-stu-id="a0b99-697">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-698">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="a0b99-698">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-699">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0b99-699">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-700">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-700">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-701">Datum und Uhrzeit des letzten zurück Setzens des Controllers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-701">Date and time this controller was last reset.</span></span> <span data-ttu-id="a0b99-702">Dies könnte bedeuten, dass der Controller heruntergefahren oder erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a0b99-702">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="a0b99-703">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-703">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-704">**Videoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="a0b99-704">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-705">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-705">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-706">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-706">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-707">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-707">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-708">Der Typ der Video Architektur.</span><span class="sxs-lookup"><span data-stu-id="a0b99-708">Type of video architecture.</span></span>

<span data-ttu-id="a0b99-709">Diese Eigenschaft wird von [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-709">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0b99-710">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-710">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-711">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-711">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="a0b99-712">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-712">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="a0b99-713">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-713">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="a0b99-714">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="a0b99-714">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="a0b99-715">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="a0b99-715">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="a0b99-716">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="a0b99-716">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="a0b99-717">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="a0b99-717">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="a0b99-718">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="a0b99-718">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="a0b99-719">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="a0b99-719">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="a0b99-720">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="a0b99-720">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="a0b99-721">**Linearer Rahmen Puffer** (12)</span><span class="sxs-lookup"><span data-stu-id="a0b99-721">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="a0b99-722">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="a0b99-722">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-723">**Videomemorytype**</span><span class="sxs-lookup"><span data-stu-id="a0b99-723">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-724">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-724">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-725">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-726">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-726">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-727">Typ des Video Speichers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-727">Type of video memory.</span></span>

<span data-ttu-id="a0b99-728">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-728">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0b99-729">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b99-729">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0b99-730">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b99-730">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="a0b99-731">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b99-731">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="a0b99-732">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b99-732">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="a0b99-733">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="a0b99-733">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="a0b99-734">**Wram** (6)</span><span class="sxs-lookup"><span data-stu-id="a0b99-734">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="a0b99-735">**EDO RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="a0b99-735">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="a0b99-736">**Burst synchroner DRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="a0b99-736">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="a0b99-737">**Pipelined Burst-SRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="a0b99-737">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="a0b99-738">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="a0b99-738">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="a0b99-739">**3dram** (11)</span><span class="sxs-lookup"><span data-stu-id="a0b99-739">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="a0b99-740">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="a0b99-740">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="a0b99-741">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="a0b99-741">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0b99-742">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="a0b99-742">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-743">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0b99-743">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-744">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-744">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-745">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Video \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a0b99-745">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-746">Aktueller Videomodus.</span><span class="sxs-lookup"><span data-stu-id="a0b99-746">Current video mode.</span></span>

<span data-ttu-id="a0b99-747">Diese Eigenschaft wird von [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-747">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-748">**Videomodecodescription**</span><span class="sxs-lookup"><span data-stu-id="a0b99-748">**VideoModeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-749">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-750">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-750">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-751">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="a0b99-751">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-752">Aktuelle Einstellungen für Auflösung, Farbe und Scanmodus des Video Controllers.</span><span class="sxs-lookup"><span data-stu-id="a0b99-752">Current resolution, color, and scan mode settings of the video controller.</span></span>

<span data-ttu-id="a0b99-753">Beispiel: "1024 x 768 x 256 Colors"</span><span class="sxs-lookup"><span data-stu-id="a0b99-753">Example: "1024 x 768 x 256 colors"</span></span>

</dd> <dt>

<span data-ttu-id="a0b99-754">**Videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="a0b99-754">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b99-755">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a0b99-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b99-756">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a0b99-756">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0b99-757">Frei Form Zeichenfolge, die den Videoprozessor beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-757">Free-form string describing the video processor.</span></span>

<span data-ttu-id="a0b99-758">Diese Eigenschaft wird von [**CIM \_ Videocontroller**](cim-videocontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a0b99-758">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0b99-759">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0b99-759">Remarks</span></span>

<span data-ttu-id="a0b99-760">Die **Win32 \_ Videocontroller** -Klasse wird von [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-760">The **Win32\_VideoController** class is derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<span data-ttu-id="a0b99-761">Weitere Informationen zur Verwendung dieser Klasse, z. b. zum Abrufen von Informationen von mehreren Monitoren, finden [Sie unter Verwenden von PowerShell zum Ermitteln von Multimonitor-Informationen](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0b99-761">For more information about using this class, such as retrieving information from multiple monitors, see [Use PowerShell to Discover Multi-Monitor Information](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="a0b99-762">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0b99-762">Examples</span></span>

<span data-ttu-id="a0b99-763">Im Listen [Videocontroller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript-Beispiel werden die Videocontroller Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-763">The [List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript sample lists the video controller properties.</span></span>

<span data-ttu-id="a0b99-764">Im folgenden PowerShell-Beispiel werden die Videocontroller Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a0b99-764">The following PowerShell example lists the video controller properties.</span></span>


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a><span data-ttu-id="a0b99-765">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0b99-765">Requirements</span></span>



| <span data-ttu-id="a0b99-766">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0b99-766">Requirement</span></span> | <span data-ttu-id="a0b99-767">Wert</span><span class="sxs-lookup"><span data-stu-id="a0b99-767">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b99-768">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0b99-768">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b99-769">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0b99-769">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0b99-770">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0b99-770">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b99-771">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0b99-771">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0b99-772">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0b99-772">Namespace</span></span><br/>                | <span data-ttu-id="a0b99-773">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a0b99-773">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a0b99-774">MOF</span><span class="sxs-lookup"><span data-stu-id="a0b99-774">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0b99-775"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a0b99-775"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0b99-776">DLL</span><span class="sxs-lookup"><span data-stu-id="a0b99-776">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0b99-777"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0b99-777"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b99-778">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0b99-778">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b99-779">**CIM \_ pcvideocontroller**</span><span class="sxs-lookup"><span data-stu-id="a0b99-779">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="a0b99-780">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a0b99-780">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
