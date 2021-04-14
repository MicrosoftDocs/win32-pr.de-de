---
description: Die Win32- \_ videoconfiguration-Klasse ist nicht aktiv. Es werden keine Instanzen zurückgegeben, da es von keinem Anbieter unterstützt wird.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Win32_VideoConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523195"
---
# <a name="win32_videoconfiguration-class"></a><span data-ttu-id="83ff9-104">Win32- \_ videoconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="83ff9-104">Win32\_VideoConfiguration class</span></span>

<span data-ttu-id="83ff9-105">Die **Win32- \_ videoconfiguration** -Klasse ist nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="83ff9-105">The **Win32\_VideoConfiguration** class is not active.</span></span> <span data-ttu-id="83ff9-106">Es werden keine Instanzen zurückgegeben, da es von keinem Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="83ff9-106">It will not return any instances as there is no provider backing it.</span></span>

<span data-ttu-id="83ff9-107">Die **Win32- \_ videoconfiguration** -Klasse stellt eine Konfiguration eines Video Subsystems dar.</span><span class="sxs-lookup"><span data-stu-id="83ff9-107">The **Win32\_VideoConfiguration** class represents a configuration of a video subsystem.</span></span> <span data-ttu-id="83ff9-108">Diese Klasse ist zugunsten der Eigenschaften in den [**Win32- \_ Videocontroller**](win32-videocontroller.md)-, [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)-und [**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klassen veraltet.</span><span class="sxs-lookup"><span data-stu-id="83ff9-108">This class has been deprecated in favor of the properties contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes</span></span>

<span data-ttu-id="83ff9-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="83ff9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ff9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="83ff9-110">Syntax</span></span>

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="83ff9-111">Member</span><span class="sxs-lookup"><span data-stu-id="83ff9-111">Members</span></span>

<span data-ttu-id="83ff9-112">Die **Win32- \_ videoconfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="83ff9-112">The **Win32\_VideoConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="83ff9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83ff9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83ff9-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83ff9-114">Properties</span></span>

<span data-ttu-id="83ff9-115">Die **Win32- \_ videoconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="83ff9-115">The **Win32\_VideoConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83ff9-116">**ActualColorResolution**</span><span class="sxs-lookup"><span data-stu-id="83ff9-116">**ActualColorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-117">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-119">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| colorres"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Pixel")</span><span class="sxs-lookup"><span data-stu-id="83ff9-119">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-120">Gibt die aktuelle Farbtiefe der Videoanzeige an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-120">Indicates the current color depth of the video display.</span></span>

<span data-ttu-id="83ff9-121">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-121">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-122">**AdapterChipType**</span><span class="sxs-lookup"><span data-stu-id="83ff9-122">**AdapterChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-125">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| chiptype")</span><span class="sxs-lookup"><span data-stu-id="83ff9-125">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|ChipType")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-126">Enthält den Namen des Adapter Chips.</span><span class="sxs-lookup"><span data-stu-id="83ff9-126">Contains the name of the adapter chip.</span></span>

<span data-ttu-id="83ff9-127">Beispiel: S3</span><span class="sxs-lookup"><span data-stu-id="83ff9-127">Example: s3</span></span>

<span data-ttu-id="83ff9-128">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-128">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-129">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="83ff9-129">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-132">Qualifizierer: [**deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="83ff9-132">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-133">Gibt den Namen des Herstellers des Adapters an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-133">Specifies the name of the manufacturer of the adapter.</span></span> <span data-ttu-id="83ff9-134">Dieser Name kann verwendet werden, um die Kompatibilität dieses Geräts mit den Anforderungen des Computer Systems zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-134">This name can be used to compare the compatibility of this device with the needs of the computer system.</span></span>

<span data-ttu-id="83ff9-135">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-135">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-136">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="83ff9-136">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-139">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| dactype")</span><span class="sxs-lookup"><span data-stu-id="83ff9-139">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|DACType")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-140">Gibt den Namen des im Adapter verwendeten Digital-to-Analog-Chips (DAC) an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-140">Indicates the name of the digital-to-analog chip (DAC) used in the adapter.</span></span>

<span data-ttu-id="83ff9-141">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-141">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-142">**AdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="83ff9-142">**AdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-145">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="83ff9-145">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-146">Enthält eine Beschreibung oder einen beschreibenden Namen der Grafikkarte.</span><span class="sxs-lookup"><span data-stu-id="83ff9-146">Contains a description or descriptive name of the video adapter.</span></span>

<span data-ttu-id="83ff9-147">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-147">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-148">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="83ff9-148">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-151">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| videomemory"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="83ff9-151">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-152">Gibt die Arbeitsspeicher Größe der Grafikkarte an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-152">Indicates the memory size of the video adapter.</span></span>

<span data-ttu-id="83ff9-153">Beispiel: 16777216</span><span class="sxs-lookup"><span data-stu-id="83ff9-153">Example: 16777216</span></span>

<span data-ttu-id="83ff9-154">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-154">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-155">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="83ff9-155">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-158">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ Description \\ \\ System \\ \\ Display Controller \\ \\ 0 \\ \\ Identifier")</span><span class="sxs-lookup"><span data-stu-id="83ff9-158">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\DisplayController\\\\0\\\\Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-159">Gibt den Typ der Grafikkarte an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-159">Indicates the type of video adapter.</span></span>

<span data-ttu-id="83ff9-160">Zeichensatz: Alphanumerisch</span><span class="sxs-lookup"><span data-stu-id="83ff9-160">Character Set: Alphanumeric</span></span>

<span data-ttu-id="83ff9-161">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-161">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-162">**Bitsper Pixel**</span><span class="sxs-lookup"><span data-stu-id="83ff9-162">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-165">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| bitspixel")</span><span class="sxs-lookup"><span data-stu-id="83ff9-165">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-166">Gibt die tatsächliche Anzahl von Bits pro Pixel an, die die Anzeige darstellt.</span><span class="sxs-lookup"><span data-stu-id="83ff9-166">Indicates the actual number of bits per pixel representing the display.</span></span> <span data-ttu-id="83ff9-167">Dies kann auf die aktuelle Video Einstellung (dargestellt durch die ActualColorResolution-Eigenschaft) des Benutzers skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="83ff9-167">This may be scaled to the current video setting (represented by the ActualColorResolution property) of the user.</span></span>

<span data-ttu-id="83ff9-168">Beispiel: 8</span><span class="sxs-lookup"><span data-stu-id="83ff9-168">Example: 8</span></span>

<span data-ttu-id="83ff9-169">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-169">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-170">**Caption**</span><span class="sxs-lookup"><span data-stu-id="83ff9-170">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-173">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="83ff9-173">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-174">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="83ff9-174">Short textual description of the current object.</span></span>

<span data-ttu-id="83ff9-175">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="83ff9-175">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-176">**Colorplane**</span><span class="sxs-lookup"><span data-stu-id="83ff9-176">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-179">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| Plane")</span><span class="sxs-lookup"><span data-stu-id="83ff9-179">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-180">Gibt die aktuelle Anzahl von Farbebenen an, die in der Videoanzeige verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83ff9-180">Indicates the current number of color planes used in the video display.</span></span> <span data-ttu-id="83ff9-181">Eine Farb Ebene ist eine andere Möglichkeit zur Darstellung von Pixel Farben. Anstatt jedem Pixel einen einzelnen RGB-Wert zuzuweisen, trennen Farbebenen die Grafik in jede der primären Farbkomponenten (rotes grünes blau) und speichern Sie in ihren eigenen Flächen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-181">A color plane is another way to represent pixel colors; instead of assigning a single RGB value to each a pixel, color planes separate the graphic into each of the primary color components (red green blue), and store them in their own planes.</span></span> <span data-ttu-id="83ff9-182">Dies ermöglicht eine höhere Farbtiefe auf 8-und 16-Bit-Videosystemen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-182">This allows for greater color depths on 8 and 16 bit video systems.</span></span> <span data-ttu-id="83ff9-183">Vorhandene Grafik Systeme verfügen über den bitwidth, der groß genug ist, um farbausführungsinformationen zu speichern, sodass nur eine Farb Ebene erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="83ff9-183">Present graphics systems have the bitwidth large enough to store color depth information, making only one color plane necessary.</span></span>

<span data-ttu-id="83ff9-184">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="83ff9-184">Example: 1</span></span>

<span data-ttu-id="83ff9-185">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-185">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-186">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="83ff9-186">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-189">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| numcolors")</span><span class="sxs-lookup"><span data-stu-id="83ff9-189">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-190">Gibt die Anzahl der Farbindizes in einer Farbtabelle für eine Videoanzeige an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-190">Indicates the number of color indexes in a color table for a video display.</span></span> <span data-ttu-id="83ff9-191">Diese Eigenschaft wird verwendet, wenn das Gerät über eine Farbtiefe von höchstens 8 Bits pro Pixel verfügt.</span><span class="sxs-lookup"><span data-stu-id="83ff9-191">This property is used if the device has a color depth of no more than 8 bits per pixel.</span></span> <span data-ttu-id="83ff9-192">Bei Geräten mit größerer Farbtiefe wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83ff9-192">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="83ff9-193">Beispiel: 256</span><span class="sxs-lookup"><span data-stu-id="83ff9-193">Example: 256</span></span>

<span data-ttu-id="83ff9-194">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-194">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-195">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83ff9-195">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-198">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="83ff9-198">Textual description of the current object.</span></span>

<span data-ttu-id="83ff9-199">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="83ff9-199">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-200">**Geräte Einstellungs Stifte**</span><span class="sxs-lookup"><span data-stu-id="83ff9-200">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-203">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| numpens")</span><span class="sxs-lookup"><span data-stu-id="83ff9-203">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-204">Gibt die aktuelle Anzahl von gerätespezifischen Stiften an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-204">Indicates the current number of device-specific pens.</span></span> <span data-ttu-id="83ff9-205">Der Wert 0xFFFFFFFF bedeutet, dass das Gerät keine Stifte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83ff9-205">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="83ff9-206">Stifte werden zum Zeichnen von Linien und Rändern von polygonalen Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="83ff9-206">Pens are used to draw lines and theborders of polygonal objects.</span></span>

<span data-ttu-id="83ff9-207">Beispiel: 3</span><span class="sxs-lookup"><span data-stu-id="83ff9-207">Example: 3</span></span>

<span data-ttu-id="83ff9-208">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-208">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-209">**Driverdate**</span><span class="sxs-lookup"><span data-stu-id="83ff9-209">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-210">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="83ff9-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-212">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| driverdate")</span><span class="sxs-lookup"><span data-stu-id="83ff9-212">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\AdapterDescription\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-213">Gibt das Datum und die Uhrzeit an, zu der der aktuelle Videotreiber installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="83ff9-213">Indicates the date and time the current video driver was installed.</span></span>

<span data-ttu-id="83ff9-214">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-214">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-215">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="83ff9-215">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-216">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-218">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| horzres")</span><span class="sxs-lookup"><span data-stu-id="83ff9-218">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-219">Gibt die aktuelle Anzahl der Pixel in der horizontalen Richtung (X-Achse) der Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-219">Indicates the current number of pixels in the horizontal direction (X axis) of the display.</span></span>

<span data-ttu-id="83ff9-220">Beispiel: 1024</span><span class="sxs-lookup"><span data-stu-id="83ff9-220">Example: 1024</span></span>

<span data-ttu-id="83ff9-221">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-221">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-222">**INFFILENAME**</span><span class="sxs-lookup"><span data-stu-id="83ff9-222">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-225">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| INFPath")</span><span class="sxs-lookup"><span data-stu-id="83ff9-225">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-226">Gibt den Pfad zur INF-Datei des Video Treibers an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-226">Specifies the path to the .inf file of the video driver.</span></span>

<span data-ttu-id="83ff9-227">Beispiel: C: \\ Windows \\ system32 \\ Drivers</span><span class="sxs-lookup"><span data-stu-id="83ff9-227">Example: C:\\Windows\\System32\\Drivers</span></span>

<span data-ttu-id="83ff9-228">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-228">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-229">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="83ff9-229">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-232">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="83ff9-232">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-233">Gibt den Abschnitt der INF-Datei an, in der sich die Win32-Videoinformationen befinden.</span><span class="sxs-lookup"><span data-stu-id="83ff9-233">Indicates the section of the .inf file where the Win32 video information resides.</span></span>

<span data-ttu-id="83ff9-234">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-234">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-235">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="83ff9-235">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-238">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ defaule \| drv")</span><span class="sxs-lookup"><span data-stu-id="83ff9-238">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Defaule\|drv")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-239">Gibt den Namen des installierten Video Treibers an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-239">Indicates the name of the installed video driver.</span></span>

<span data-ttu-id="83ff9-240">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-240">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-241">**Monitorhersteller**</span><span class="sxs-lookup"><span data-stu-id="83ff9-241">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-244">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="83ff9-244">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-245">Gibt den Namen des Herstellers des Anzeige Geräts an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-245">Indicates the name of the manufacturer of the display device.</span></span>

<span data-ttu-id="83ff9-246">Beispiel: NEC</span><span class="sxs-lookup"><span data-stu-id="83ff9-246">Example: NEC</span></span>

<span data-ttu-id="83ff9-247">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-247">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-248">**Monitortyp**</span><span class="sxs-lookup"><span data-stu-id="83ff9-248">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-251">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ Description \\ \\ System \\ \\ monitorperipherie \\ \\ 0 \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="83ff9-251">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\MonitorPeripheral\\\\0\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-252">Gibt den Modellnamen des Anzeige Geräts an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-252">Indicates the model name of the display device.</span></span>

<span data-ttu-id="83ff9-253">Beispiel: NEC 5F-GP</span><span class="sxs-lookup"><span data-stu-id="83ff9-253">Example: NEC 5FGp</span></span>

<span data-ttu-id="83ff9-254">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-254">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-255">**Name**</span><span class="sxs-lookup"><span data-stu-id="83ff9-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-258">Qualifizierer: [**deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="83ff9-258">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-259">Enthält einen identifizierenden Namen für die Video Konfigurationsklasse.</span><span class="sxs-lookup"><span data-stu-id="83ff9-259">Contains an identifying name for the video configuration class.</span></span>

<span data-ttu-id="83ff9-260">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-260">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-261">**Pixelsperxlogicalzoll**</span><span class="sxs-lookup"><span data-stu-id="83ff9-261">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-262">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-264">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| logpixelsx")</span><span class="sxs-lookup"><span data-stu-id="83ff9-264">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSX")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-265">Gibt die Anzahl der Pixel pro logischem Zoll entlang der X-Achse (horizontale Richtung) der Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-265">Indicates the number of pixels per logical inch along the X axis (horizontal direction) of the display.</span></span>

<span data-ttu-id="83ff9-266">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-266">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-267">**Pixelsperylogicalzoll**</span><span class="sxs-lookup"><span data-stu-id="83ff9-267">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-268">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-270">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| logpixelsy")</span><span class="sxs-lookup"><span data-stu-id="83ff9-270">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSY")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-271">Gibt die Anzahl der Pixel pro logischem Zoll entlang der Y-Achse (vertikale Richtung) der Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-271">Indicates the number of pixels per logical inch along the Y axis (vertical direction) of the display.</span></span>

<span data-ttu-id="83ff9-272">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-272">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-273">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="83ff9-273">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-274">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-276">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VRefresh")</span><span class="sxs-lookup"><span data-stu-id="83ff9-276">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VREFRESH")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-277">Gibt die Aktualisierungsrate der Video Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-277">Indicates the refresh rate of the video configuration.</span></span> <span data-ttu-id="83ff9-278">Der Wert 0 oder 1 gibt an, dass ein Standardsatz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83ff9-278">A value of 0 or 1 indicates a default rate is being used.</span></span>

<span data-ttu-id="83ff9-279">Beispiel: 72</span><span class="sxs-lookup"><span data-stu-id="83ff9-279">Example: 72</span></span>

<span data-ttu-id="83ff9-280">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-280">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-281">**Scanmode**</span><span class="sxs-lookup"><span data-stu-id="83ff9-281">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-284">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. interschnür")</span><span class="sxs-lookup"><span data-stu-id="83ff9-284">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Device0\|DefaultSettings.Interlaced")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-285">Gibt an, ob das Anzeigegerät mit Zeilen Sprung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="83ff9-285">Indicates whether the display device is interlaced.</span></span>

<span data-ttu-id="83ff9-286">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-286">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="83ff9-287">**Nicht** Zeilen Sprung ("nicht Zeilen Sprung")</span><span class="sxs-lookup"><span data-stu-id="83ff9-287">**Non Interlaced** ("Non Interlaced")</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="83ff9-288">Zeilen **Sprung ("** Zeilen Sprung")</span><span class="sxs-lookup"><span data-stu-id="83ff9-288">**Interlaced** ("Interlaced")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83ff9-289">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="83ff9-289">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-290">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-292">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| vertsize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millimeter")</span><span class="sxs-lookup"><span data-stu-id="83ff9-292">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-293">Gibt die Höhe des physischen Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-293">Specifies the height of the physical screen.</span></span>

<span data-ttu-id="83ff9-294">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-294">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-295">**Bildschirmbreite**</span><span class="sxs-lookup"><span data-stu-id="83ff9-295">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-296">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-298">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| horzsize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millimeter")</span><span class="sxs-lookup"><span data-stu-id="83ff9-298">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-299">Gibt die Breite des physischen Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-299">Specifies the width of the physical screen.</span></span>

<span data-ttu-id="83ff9-300">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-300">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-301">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="83ff9-301">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83ff9-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-304">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="83ff9-304">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-305">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="83ff9-305">Identifier by which the current object is known.</span></span>

<span data-ttu-id="83ff9-306">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="83ff9-306">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-307">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="83ff9-307">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-308">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-310">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")</span><span class="sxs-lookup"><span data-stu-id="83ff9-310">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|SIZEPALETTE")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-311">Gibt die aktuelle Anzahl von Farb Indexeinträgen an, die für die Verwendung durch das System reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="83ff9-311">Iindicates the current number of color index entries reserved for system use.</span></span> <span data-ttu-id="83ff9-312">Dieser Wert ist nur für Anzeigeeinstellungen gültig, die eine indizierte Palette verwenden.</span><span class="sxs-lookup"><span data-stu-id="83ff9-312">This value is only valid for display settings that use an indexed palette .</span></span> <span data-ttu-id="83ff9-313">Indizierte Paletten werden nicht für Farbtiefe verwendet, die größer als 8 Bits pro Pixel ist.</span><span class="sxs-lookup"><span data-stu-id="83ff9-313">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="83ff9-314">Wenn die Farbtiefe mehr als 8 Bits pro Pixel beträgt, wird dieser Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="83ff9-314">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="83ff9-315">Beispiel: 20</span><span class="sxs-lookup"><span data-stu-id="83ff9-315">Example: 20</span></span>

<span data-ttu-id="83ff9-316">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-316">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="83ff9-317">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="83ff9-317">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ff9-318">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83ff9-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="83ff9-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ff9-320">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| vertres")</span><span class="sxs-lookup"><span data-stu-id="83ff9-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES")</span></span>
</dt> </dl>

<span data-ttu-id="83ff9-321">Gibt die aktuelle Anzahl der Pixel in vertikaler Richtung (Y-Achse) der Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="83ff9-321">Indicates the current number of pixels in the vertical direction (Y axis) of the display.</span></span>

<span data-ttu-id="83ff9-322">Beispiel: 768</span><span class="sxs-lookup"><span data-stu-id="83ff9-322">Example: 768</span></span>

<span data-ttu-id="83ff9-323">Diese Eigenschaft wurde als veraltet markiert, um eine entsprechende Eigenschaft (en) im [**Win32- \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md) und//oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md)zu bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="83ff9-323">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83ff9-324">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83ff9-324">Requirements</span></span>



| <span data-ttu-id="83ff9-325">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83ff9-325">Requirement</span></span> | <span data-ttu-id="83ff9-326">Wert</span><span class="sxs-lookup"><span data-stu-id="83ff9-326">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83ff9-327">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83ff9-327">Minimum supported client</span></span><br/> | <span data-ttu-id="83ff9-328">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83ff9-328">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83ff9-329">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83ff9-329">Minimum supported server</span></span><br/> | <span data-ttu-id="83ff9-330">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83ff9-330">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83ff9-331">Namespace</span><span class="sxs-lookup"><span data-stu-id="83ff9-331">Namespace</span></span><br/>                | <span data-ttu-id="83ff9-332">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="83ff9-332">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83ff9-333">MOF</span><span class="sxs-lookup"><span data-stu-id="83ff9-333">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83ff9-334"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="83ff9-334"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83ff9-335">DLL</span><span class="sxs-lookup"><span data-stu-id="83ff9-335">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83ff9-336"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83ff9-336"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83ff9-337">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83ff9-337">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ff9-338">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="83ff9-338">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

 
