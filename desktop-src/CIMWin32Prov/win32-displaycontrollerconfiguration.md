---
description: Die Win32 \_ displaycontrollerconfiguration-WMI-Klasse stellt die Grafikkarten-Konfigurationsinformationen eines Computer Systems dar, auf dem Windows ausgeführt wird.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Win32_DisplayControllerConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127336"
---
# <a name="win32_displaycontrollerconfiguration-class"></a><span data-ttu-id="b104c-103">Win32 \_ displaycontrollerconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="b104c-103">Win32\_DisplayControllerConfiguration class</span></span>

<span data-ttu-id="b104c-104">Die **Win32 \_ displaycontrollerconfiguration** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Grafikkarten-Konfigurationsinformationen eines Computer Systems dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b104c-104">The **Win32\_DisplayControllerConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the video adapter configuration information of a computer system running Windows.</span></span>

<span data-ttu-id="b104c-105">Diese Klasse ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="b104c-105">This class is obsolete.</span></span> <span data-ttu-id="b104c-106">Anstelle dieser Klasse sollten Sie die Eigenschaften in den Klassen [**Win32 \_ Videocontroller**](win32-videocontroller.md), [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)und [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b104c-106">In place of this class, you should use the properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes.</span></span>

<span data-ttu-id="b104c-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b104c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b104c-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b104c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b104c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b104c-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a><span data-ttu-id="b104c-110">Member</span><span class="sxs-lookup"><span data-stu-id="b104c-110">Members</span></span>

<span data-ttu-id="b104c-111">Die **Win32-Klasse \_ displaycontrollerconfiguration** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b104c-111">The **Win32\_DisplayControllerConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="b104c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b104c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b104c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b104c-113">Properties</span></span>

<span data-ttu-id="b104c-114">Die **Win32-Klasse \_ displaycontrollerconfiguration** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b104c-114">The **Win32\_DisplayControllerConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b104c-115">**Bitsper Pixel**</span><span class="sxs-lookup"><span data-stu-id="b104c-115">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-116">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-118">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| bitspixel")</span><span class="sxs-lookup"><span data-stu-id="b104c-118">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-119">Entweder die Anzahl der Bits, die zur Darstellung der Farbe in dieser Konfiguration verwendet werden, oder die Bits in jedem Pixel.</span><span class="sxs-lookup"><span data-stu-id="b104c-119">Either the number of bits used to represent the color in this configuration, or the bits in each pixel.</span></span>

<span data-ttu-id="b104c-120">Beispiel: 8</span><span class="sxs-lookup"><span data-stu-id="b104c-120">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="b104c-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b104c-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b104c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-124">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b104c-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b104c-125">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b104c-125">Short textual description of the current object.</span></span>

<span data-ttu-id="b104c-126">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b104c-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b104c-127">**Colorplane**</span><span class="sxs-lookup"><span data-stu-id="b104c-127">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-130">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| Plane")</span><span class="sxs-lookup"><span data-stu-id="b104c-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-131">Aktuelle Anzahl von Farbebenen, die in der Anzeige Konfiguration verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b104c-131">Current number of color planes used in the display configuration.</span></span> <span data-ttu-id="b104c-132">Eine Farb Ebene ist eine andere Möglichkeit zur Darstellung von Pixel Farben.</span><span class="sxs-lookup"><span data-stu-id="b104c-132">A color plane is another way to represent pixel colors.</span></span> <span data-ttu-id="b104c-133">Anstatt jedem Pixel einen einzelnen RGB-Wert zuzuweisen, trennen Farbebenen die Grafik in jede der primären Farbkomponenten (rot, grün, blau) und speichern Sie in ihren eigenen Ebenen.</span><span class="sxs-lookup"><span data-stu-id="b104c-133">Instead of assigning a single RGB value to each pixel, color planes separate the graphic into each of the primary color components (red, green, blue), and stores them in their own planes.</span></span> <span data-ttu-id="b104c-134">Dies ermöglicht eine höhere Farbtiefe auf 8-Bit-und 16-Bit-Videosystemen.</span><span class="sxs-lookup"><span data-stu-id="b104c-134">This allows for greater color depths on 8-bit and 16-bit video systems.</span></span> <span data-ttu-id="b104c-135">Vorhandene Grafik Systeme verfügen über den bitwidth, der groß genug ist, um Detailinformationen zu speichern, was bedeutet, dass nur eine Farbebene erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b104c-135">Present graphics systems have the bitwidth large enough to store color depth information, meaning only one color plane is needed.</span></span>

<span data-ttu-id="b104c-136">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="b104c-136">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="b104c-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b104c-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b104c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b104c-140">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b104c-140">Textual description of the current object.</span></span>

<span data-ttu-id="b104c-141">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b104c-141">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b104c-142">**DeviceEntriesInAColorTable**</span><span class="sxs-lookup"><span data-stu-id="b104c-142">**DeviceEntriesInAColorTable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-145">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numcolors")</span><span class="sxs-lookup"><span data-stu-id="b104c-145">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-146">Anzahl der Farbindizes in einer Farbtabelle eines Anzeige Geräts (wenn das Gerät eine Farbtiefe von höchstens 8 Bits pro Pixel aufweist).</span><span class="sxs-lookup"><span data-stu-id="b104c-146">Number of color indexes in a color table of a display device (if the device has a color depth of no more than 8 bits per pixel).</span></span> <span data-ttu-id="b104c-147">Bei Geräten mit größerer Farbtiefe wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b104c-147">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="b104c-148">Beispiel: 256</span><span class="sxs-lookup"><span data-stu-id="b104c-148">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="b104c-149">**Geräte Einstellungs Stifte**</span><span class="sxs-lookup"><span data-stu-id="b104c-149">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-152">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numpens")</span><span class="sxs-lookup"><span data-stu-id="b104c-152">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-153">Aktuelle Anzahl der gerätespezifischen Stifte.</span><span class="sxs-lookup"><span data-stu-id="b104c-153">Current number of device-specific pens.</span></span> <span data-ttu-id="b104c-154">Der Wert 0xFFFFFFFF bedeutet, dass das Gerät keine Stifte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b104c-154">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="b104c-155">Stifte sind logische Eigenschaften, die vom Anzeige Controller zum Anzeigen von Geräten zugewiesen werden können und zum Zeichnen von Linien, Rahmen von Polygonen und Text verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b104c-155">Pens are logical properties that can be assigned by the display controller to display devices, and are used to draw lines, borders of polygons, and text.</span></span>

<span data-ttu-id="b104c-156">Beispiel: 3</span><span class="sxs-lookup"><span data-stu-id="b104c-156">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="b104c-157">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="b104c-157">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-158">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-160">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| horzres"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel")</span><span class="sxs-lookup"><span data-stu-id="b104c-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-161">Aktuelle Anzahl der Pixel in der horizontalen Richtung (x-Achse) der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="b104c-161">Current number of pixels in the horizontal direction (x-axis) of the display.</span></span>

<span data-ttu-id="b104c-162">Beispiel: 1024</span><span class="sxs-lookup"><span data-stu-id="b104c-162">Example: 1024</span></span>

</dd> <dt>

<span data-ttu-id="b104c-163">**Name**</span><span class="sxs-lookup"><span data-stu-id="b104c-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b104c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-166">Qualifizierer: [**deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b104c-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-167">Der Name des Adapters, der in dieser Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b104c-167">Name of the adapter used in this configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b104c-168">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="b104c-168">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-169">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b104c-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-171">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| horzresvrefresh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="b104c-171">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-172">Aktualisierungsrate der Grafikkarte.</span><span class="sxs-lookup"><span data-stu-id="b104c-172">Refresh rate of the video adapter.</span></span> <span data-ttu-id="b104c-173">Der Wert 0 (null) oder 1 (eins) gibt an, dass ein Standardsatz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b104c-173">A value of 0 (zero) or 1 (one) indicates a default rate is being used.</span></span> <span data-ttu-id="b104c-174">Der Wert-1 gibt an, dass eine optimale Rate verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b104c-174">A value of -1 indicates that an optimal rate is being used.</span></span>

<span data-ttu-id="b104c-175">Beispiel: 72</span><span class="sxs-lookup"><span data-stu-id="b104c-175">Example: 72</span></span>

</dd> <dt>

<span data-ttu-id="b104c-176">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="b104c-176">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-179">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numreserved")</span><span class="sxs-lookup"><span data-stu-id="b104c-179">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-180">Aktuelle Anzahl der Farb Indexeinträge, die für die System Verwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="b104c-180">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="b104c-181">Dieser Wert ist nur für Anzeigeeinstellungen gültig, die eine indizierte Palette verwenden.</span><span class="sxs-lookup"><span data-stu-id="b104c-181">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="b104c-182">Indizierte Paletten werden nicht für Farbtiefe verwendet, die größer als 8 Bits pro Pixel ist.</span><span class="sxs-lookup"><span data-stu-id="b104c-182">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="b104c-183">Wenn die Farbtiefe mehr als 8 Bits pro Pixel beträgt, wird dieser Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b104c-183">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="b104c-184">Beispiel: 20</span><span class="sxs-lookup"><span data-stu-id="b104c-184">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="b104c-185">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="b104c-185">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b104c-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-188">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b104c-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b104c-189">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b104c-189">Identifier by which the current object is known.</span></span>

<span data-ttu-id="b104c-190">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b104c-190">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b104c-191">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="b104c-191">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-192">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-194">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| numreserved")</span><span class="sxs-lookup"><span data-stu-id="b104c-194">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-195">Aktuelle Anzahl der Farb Indexeinträge, die für die System Verwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="b104c-195">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="b104c-196">Dieser Wert ist nur für Anzeigeeinstellungen gültig, die eine indizierte Palette verwenden.</span><span class="sxs-lookup"><span data-stu-id="b104c-196">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="b104c-197">Indizierte Paletten werden nicht für Farbtiefe verwendet, die größer als 8 Bits pro Pixel ist.</span><span class="sxs-lookup"><span data-stu-id="b104c-197">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="b104c-198">Wenn die Farbtiefe mehr als 8 Bits pro Pixel beträgt, wird dieser Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b104c-198">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="b104c-199">Beispiel: 20</span><span class="sxs-lookup"><span data-stu-id="b104c-199">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="b104c-200">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="b104c-200">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b104c-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-203">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| vertres"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel")</span><span class="sxs-lookup"><span data-stu-id="b104c-203">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-204">Aktuelle Anzahl der Pixel in vertikaler Richtung (y-Achse) der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="b104c-204">Current number of pixels in the vertical direction (y-axis) of the display.</span></span>

<span data-ttu-id="b104c-205">Beispiel: 768</span><span class="sxs-lookup"><span data-stu-id="b104c-205">Example: 768</span></span>

</dd> <dt>

<span data-ttu-id="b104c-206">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="b104c-206">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b104c-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b104c-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b104c-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b104c-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b104c-209">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b104c-209">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b104c-210">Benutzer lesbare Beschreibung der aktuellen Bildschirmauflösung und der Farbeinstellung der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="b104c-210">User-readable description of the current screen resolution and color setting of the display.</span></span>

<span data-ttu-id="b104c-211">Beispiel: "1024 768 mit 256 Farben"</span><span class="sxs-lookup"><span data-stu-id="b104c-211">Example: "1024   768 with 256 colors"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b104c-212">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b104c-212">Remarks</span></span>

<span data-ttu-id="b104c-213">Die **Win32-Klasse \_ displaycontrollerconfiguration** wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b104c-213">The **Win32\_DisplayControllerConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b104c-214">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b104c-214">Requirements</span></span>



| <span data-ttu-id="b104c-215">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b104c-215">Requirement</span></span> | <span data-ttu-id="b104c-216">Wert</span><span class="sxs-lookup"><span data-stu-id="b104c-216">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b104c-217">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b104c-217">Minimum supported client</span></span><br/> | <span data-ttu-id="b104c-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b104c-218">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b104c-219">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b104c-219">Minimum supported server</span></span><br/> | <span data-ttu-id="b104c-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b104c-220">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b104c-221">Namespace</span><span class="sxs-lookup"><span data-stu-id="b104c-221">Namespace</span></span><br/>                | <span data-ttu-id="b104c-222">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b104c-222">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b104c-223">MOF</span><span class="sxs-lookup"><span data-stu-id="b104c-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b104c-224"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b104c-224"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b104c-225">DLL</span><span class="sxs-lookup"><span data-stu-id="b104c-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b104c-226"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b104c-226"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b104c-227">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b104c-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b104c-228">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="b104c-228">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="b104c-229">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="b104c-229">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

