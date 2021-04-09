---
description: Die \_ WMI-Klasse "Win32 printerconfiguration" stellt die Konfiguration für ein Druckergerät dar. Dies umfasst Funktionen wie Auflösung, Farbe, Schriftarten und Ausrichtung.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Win32_PrinterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958509"
---
# <a name="win32_printerconfiguration-class"></a><span data-ttu-id="51c66-104">Win32- \_ Klasse "printerconfiguration"</span><span class="sxs-lookup"><span data-stu-id="51c66-104">Win32\_PrinterConfiguration class</span></span>

<span data-ttu-id="51c66-105">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ printerconfiguration** " stellt die Konfiguration für ein Druckergerät dar.</span><span class="sxs-lookup"><span data-stu-id="51c66-105">The **Win32\_PrinterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the configuration for a printer device.</span></span> <span data-ttu-id="51c66-106">Dies umfasst Funktionen wie Auflösung, Farbe, Schriftarten und Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="51c66-106">This includes capabilities such as resolution, color, fonts, and orientation.</span></span>

<span data-ttu-id="51c66-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51c66-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="51c66-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="51c66-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c66-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="51c66-109">Syntax</span></span>

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a><span data-ttu-id="51c66-110">Member</span><span class="sxs-lookup"><span data-stu-id="51c66-110">Members</span></span>

<span data-ttu-id="51c66-111">Die **Win32-Klasse \_ printerconfiguration** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51c66-111">The **Win32\_PrinterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="51c66-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51c66-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51c66-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51c66-113">Properties</span></span>

<span data-ttu-id="51c66-114">Die **Win32-Klasse \_ printerconfiguration** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51c66-114">The **Win32\_PrinterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51c66-115">**BitsPerPel**</span><span class="sxs-lookup"><span data-stu-id="51c66-115">**BitsPerPel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-116">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-118">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51c66-118">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-119">Anzahl von Bits, die zur Darstellung der Farbe in dieser Konfiguration verwendet werden (Bits pro Pixel).</span><span class="sxs-lookup"><span data-stu-id="51c66-119">Number of bits used to represent the color in this configuration (the bits per pixel).</span></span> <span data-ttu-id="51c66-120">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="51c66-120">This property is obsolete.</span></span> <span data-ttu-id="51c66-121">Verwenden Sie stattdessen die Eigenschaften in den [**Win32 \_ Videocontroller**](win32-videocontroller.md)-, [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)-oder [**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klassen, um zu bestimmen, wie Farbe dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="51c66-121">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes to determine how color is represented.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="51c66-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51c66-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-125">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="51c66-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-126">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="51c66-126">Short textual description of the current object.</span></span>

<span data-ttu-id="51c66-127">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51c66-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="51c66-128">**Sortieren**</span><span class="sxs-lookup"><span data-stu-id="51c66-128">**Collate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51c66-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-131">**True** gibt an, dass die gedruckten Seiten sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51c66-131">If **TRUE**, the pages that are printed should be collated.</span></span> <span data-ttu-id="51c66-132">Zum Sortieren muss das gesamte Dokument gedruckt werden, bevor die nächste Kopie gedruckt wird, anstatt jede Seite des Dokuments so oft wie erforderlich auszugeben.</span><span class="sxs-lookup"><span data-stu-id="51c66-132">To collate is to print out the entire document before printing the next copy, as opposed to printing out each page of the document the required number of times.</span></span>

<span data-ttu-id="51c66-133">Diese Eigenschaft wird ignoriert, es sei denn, der Druckertreiber gibt Unterstützung für die Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="51c66-133">This property is ignored unless the printer driver indicates support for collation.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-134">**Farbe**</span><span class="sxs-lookup"><span data-stu-id="51c66-134">**Color**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-137">Die Farbe des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="51c66-137">Color of the document.</span></span> <span data-ttu-id="51c66-138">Einige Farbdrucker können mit true Black und nicht mit einer Kombination aus Cyan, Magenta und gelb (CMY) gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="51c66-138">Some color printers have the capability to print using true black instead of a combination of cyan, magenta, and yellow (CMY).</span></span> <span data-ttu-id="51c66-139">Dies erzeugt in der Regel einen dunkleren und stärkeren Text für Dokumente.</span><span class="sxs-lookup"><span data-stu-id="51c66-139">This usually creates darker and sharper text for documents.</span></span> <span data-ttu-id="51c66-140">Diese Option ist nur bei Farbdruckern nützlich, die das echte schwarze Drucken unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51c66-140">This option is only useful for color printers that support true black printing.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="51c66-141"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="51c66-141"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-142">Monochrom (true schwarz)</span><span class="sxs-lookup"><span data-stu-id="51c66-142">Monochrome (true black)</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="51c66-143"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="51c66-143"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-144">Color</span><span class="sxs-lookup"><span data-stu-id="51c66-144">Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-145">**Exemplare**</span><span class="sxs-lookup"><span data-stu-id="51c66-145">**Copies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-148">Anzahl der zu druckenden Kopien.</span><span class="sxs-lookup"><span data-stu-id="51c66-148">Number of copies to be printed.</span></span> <span data-ttu-id="51c66-149">Der Druckertreiber muss das Drucken von mehrseitigen Kopien unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51c66-149">The printer driver must support printing multi-page copies.</span></span>

<span data-ttu-id="51c66-150">Beispiel: 2</span><span class="sxs-lookup"><span data-stu-id="51c66-150">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="51c66-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51c66-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51c66-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-154">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="51c66-154">Textual description of the current object.</span></span>

<span data-ttu-id="51c66-155">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51c66-155">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="51c66-156">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="51c66-156">**DeviceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51c66-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-159">Anzeige Name des Druckers.</span><span class="sxs-lookup"><span data-stu-id="51c66-159">Friendly name of the printer.</span></span> <span data-ttu-id="51c66-160">Dieser Name ist für den Druckertyp eindeutig und kann aufgrund der Einschränkungen der Zeichenfolge, von der er abgeleitet ist, abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="51c66-160">This name is unique to the type of printer and may be truncated because of the limitations of the string from which it is derived.</span></span>

<span data-ttu-id="51c66-161">Beispiel: "PCL/HP LaserJet"</span><span class="sxs-lookup"><span data-stu-id="51c66-161">Example: "PCL/HP LaserJet"</span></span>

</dd> <dt>

<span data-ttu-id="51c66-162">**DisplayFlags**</span><span class="sxs-lookup"><span data-stu-id="51c66-162">**DisplayFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-165">Gibt an, ob das Anzeigegerät Farb-oder monochrome ist und ob der Typ der Überprüfung nicht Zeilen Sprung oder Zeilen Sprung ist.</span><span class="sxs-lookup"><span data-stu-id="51c66-165">Indicates whether the display device is color or monochrome and whether the type of scanning is noninterlaced or interlaced.</span></span> <span data-ttu-id="51c66-166">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="51c66-166">This property is obsolete.</span></span> <span data-ttu-id="51c66-167">Verwenden Sie stattdessen Anzeigeeigenschaften, z. b. die **DisplayType** -Eigenschaft der **Win32 \_ Desktopmonitor** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="51c66-167">Instead, use display properties such as the **DisplayType** property of the **Win32\_DesktopMonitor** class.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-168">**Display Frequency**</span><span class="sxs-lookup"><span data-stu-id="51c66-168">**DisplayFrequency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-169">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-171">Zeigt die vertikale Aktualisierungsrate an.</span><span class="sxs-lookup"><span data-stu-id="51c66-171">Displays the vertical refresh rate.</span></span> <span data-ttu-id="51c66-172">Die Aktualisierungsrate für einen Monitor gibt an, wie oft der Bildschirm pro Sekunde neu gezeichnet wird (Häufigkeit).</span><span class="sxs-lookup"><span data-stu-id="51c66-172">The refresh rate for a monitor is the number of times the screen is redrawn per second (frequency).</span></span> <span data-ttu-id="51c66-173">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="51c66-173">This property is obsolete.</span></span> <span data-ttu-id="51c66-174">Verwenden Sie stattdessen die Eigenschaften in der [**Win32 \_ Videocontroller**](win32-videocontroller.md)-, [**Win32 \_ Desktopmonitor**](win32-desktopmonitor.md)-oder [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="51c66-174">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-175">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="51c66-175">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-176">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-178">Der Typ des Druckers.</span><span class="sxs-lookup"><span data-stu-id="51c66-178">Dither type of the printer.</span></span> <span data-ttu-id="51c66-179">Für diese Eigenschaft können vordefinierte Werte von 1 bis 5 oder Treiber definierte Werte von 6 bis 256 angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="51c66-179">This property can assume predefined values of 1 to 5, or driver-defined values from 6 to 256.</span></span> <span data-ttu-id="51c66-180">Linienart-Dithering ist eine spezielle Dithering-Methode, die gut definierte Rahmen zwischen Schwarzen, weißen und grauen Skalierungen erzeugt.</span><span class="sxs-lookup"><span data-stu-id="51c66-180">Line art dithering is a special dithering method that produces well defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="51c66-181">Sie eignet sich nicht für Images, die kontinuierliche Abschlüsse in Intensität und Farbton enthalten, wie z. b. gescannte Fotos.</span><span class="sxs-lookup"><span data-stu-id="51c66-181">It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="51c66-182"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="51c66-182"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-183">Keine Dithering</span><span class="sxs-lookup"><span data-stu-id="51c66-183">No Dithering</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="51c66-184"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="51c66-184"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-185">Grober Pinsel</span><span class="sxs-lookup"><span data-stu-id="51c66-185">Coarse Brush</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="51c66-186"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="51c66-186"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-187">Feiner Pinsel</span><span class="sxs-lookup"><span data-stu-id="51c66-187">Fine Brush</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="51c66-188"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="51c66-188"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-189">Linienart</span><span class="sxs-lookup"><span data-stu-id="51c66-189">Line Art</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="51c66-190"><span id="5"></span>**5@@**</span><span class="sxs-lookup"><span data-stu-id="51c66-190"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-191">Grayscale</span><span class="sxs-lookup"><span data-stu-id="51c66-191">Grayscale</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-192">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="51c66-192">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-193">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-195">Versionsnummer des Windows-basierten Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="51c66-195">Version number of the Windows-based printer driver.</span></span> <span data-ttu-id="51c66-196">Die Versionsnummern werden vom Treiber Hersteller erstellt und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="51c66-196">The version numbers are created and maintained by the driver manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-197">**Duplex**</span><span class="sxs-lookup"><span data-stu-id="51c66-197">**Duplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-198">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51c66-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-200">**True** gibt an, dass der Druckvorgang auf beiden Seiten erfolgt.</span><span class="sxs-lookup"><span data-stu-id="51c66-200">If **TRUE**, printing is done on both sides.</span></span> <span data-ttu-id="51c66-201">**False** gibt an, dass der Druckvorgang nur auf einer Seite des Mediums erfolgt.</span><span class="sxs-lookup"><span data-stu-id="51c66-201">If **FALSE**, printing is done on only one side of the media.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-202">**Formular Name**</span><span class="sxs-lookup"><span data-stu-id="51c66-202">**FormName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51c66-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-205">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51c66-205">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-206">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="51c66-206">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-207">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-209">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Punkte pro Zoll)</span><span class="sxs-lookup"><span data-stu-id="51c66-209">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-210">Druckauflösung in dpi (Punkte pro Zoll) entlang der x-Achse (Breite) des Druckauftrags (ähnlich der veralteten **XResolution** -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="51c66-210">Print resolution in dots per inch along the x-axis (width) of the print job (similar to the obsolete **XResolution** property).</span></span> <span data-ttu-id="51c66-211">Dieser Wert wird nur festgelegt, wenn die **PrintQuality** -Eigenschaft dieser Klasse positiv ist.</span><span class="sxs-lookup"><span data-stu-id="51c66-211">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-212">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="51c66-212">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-213">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-213">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-215">Spezifischer Wert einer der drei möglichen Farb Vergleichsmethoden (als Intents bezeichnet), die standardmäßig verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51c66-215">Specific value of one of the three possible color matching methods (called intents) that should be used by default.</span></span> <span data-ttu-id="51c66-216">ICM-Anwendungen stellen Intents mithilfe der ICM-Funktionen her.</span><span class="sxs-lookup"><span data-stu-id="51c66-216">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="51c66-217">Für diese Eigenschaft können vordefinierte Werte von 1 bis 3 oder Treiber definierte Werte von 4 bis 256 angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="51c66-217">This property can assume predefined values of 1 to 3, or driver-defined values from 4 to 256.</span></span> <span data-ttu-id="51c66-218">Nicht-ICM-Anwendungen können diesen Wert verwenden, um zu bestimmen, wie der Drucker Farbdruckaufträge verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="51c66-218">Non-ICM applications can use this value to determine how the printer handles color printing jobs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="51c66-219"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="51c66-219"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-220">Sättigung</span><span class="sxs-lookup"><span data-stu-id="51c66-220">Saturation</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="51c66-221"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="51c66-221"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-222">Vergleichen Sie</span><span class="sxs-lookup"><span data-stu-id="51c66-222">Contrast</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="51c66-223"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="51c66-223"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-224">Exakte Farbe</span><span class="sxs-lookup"><span data-stu-id="51c66-224">Exact Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-225">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="51c66-225">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-226">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-228">Wie ICM verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="51c66-228">How ICM is handled.</span></span> <span data-ttu-id="51c66-229">Für eine nicht-ICM-Anwendung bestimmt diese Eigenschaft, ob ICM aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="51c66-229">For a non-ICM application, this property determines if ICM is enabled or disabled.</span></span> <span data-ttu-id="51c66-230">Bei ICM-Anwendungen prüft das System diese Eigenschaft, um zu bestimmen, welcher Teil des Computer Systems die ICM-Unterstützung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="51c66-230">For ICM applications, the system examines this property to determine which part of the computer system handles ICM support.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="51c66-231"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="51c66-231"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="51c66-232">Disabled</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="51c66-233"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="51c66-233"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-234">Windows</span><span class="sxs-lookup"><span data-stu-id="51c66-234">Windows</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="51c66-235"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="51c66-235"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-236">Gerätetreiber</span><span class="sxs-lookup"><span data-stu-id="51c66-236">Device Driver</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="51c66-237"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="51c66-237"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-238">Sicherungsmedium</span><span class="sxs-lookup"><span data-stu-id="51c66-238">Device</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-239">**Logpixels**</span><span class="sxs-lookup"><span data-stu-id="51c66-239">**LogPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-240">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-242">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51c66-242">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-243">Anzahl der Pixel pro logischem Zoll.</span><span class="sxs-lookup"><span data-stu-id="51c66-243">Number of pixels per logical inch.</span></span> <span data-ttu-id="51c66-244">Diese veraltete Eigenschaft ist nur für Geräte gültig, die mit Pixeln arbeiten und Geräte wie Drucker ausschließen.</span><span class="sxs-lookup"><span data-stu-id="51c66-244">This obsolete property is valid only with devices that work with pixels, which excludes devices such as printers.</span></span> <span data-ttu-id="51c66-245">Es gibt keinen Ersatzwert, der für Drucker gilt.</span><span class="sxs-lookup"><span data-stu-id="51c66-245">There is no replacement value that applies to printers.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-246">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="51c66-246">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-247">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-249">Der Medientyp, auf dem der Drucker druckt.</span><span class="sxs-lookup"><span data-stu-id="51c66-249">Type of media on which the printer prints.</span></span> <span data-ttu-id="51c66-250">Die-Eigenschaft kann auf einen vordefinierten Wert oder einen Treiber definierten Wert größer oder gleich 256 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51c66-250">The property can be set to a predefined value or a driver-defined value greater than or equal to 256.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="51c66-251"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="51c66-251"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-252">Standard</span><span class="sxs-lookup"><span data-stu-id="51c66-252">Standard</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="51c66-253"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="51c66-253"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-254">Transparenz</span><span class="sxs-lookup"><span data-stu-id="51c66-254">Transparency</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="51c66-255"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="51c66-255"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-256">Glanz</span><span class="sxs-lookup"><span data-stu-id="51c66-256">Glossy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-257">**Name**</span><span class="sxs-lookup"><span data-stu-id="51c66-257">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51c66-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-260">Qualifizierer: [**Key**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="51c66-260">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-261">Der Name des Druckers, mit dem diese Konfiguration verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="51c66-261">Name of the printer with which this configuration is associated.</span></span> <span data-ttu-id="51c66-262">Dieser Wert entspricht der **Name** -Eigenschaft der zugeordneten [**Win32- \_ Drucker**](win32-printer.md) Instanz.</span><span class="sxs-lookup"><span data-stu-id="51c66-262">This value matches the **Name** property of the associated [**Win32\_Printer**](win32-printer.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-263">**Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="51c66-263">**Orientation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-264">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-266">Druck Ausrichtung des Papiers.</span><span class="sxs-lookup"><span data-stu-id="51c66-266">Printing orientation of the paper.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="51c66-267"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="51c66-267"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-268">Hochformat</span><span class="sxs-lookup"><span data-stu-id="51c66-268">Portrait</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="51c66-269"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="51c66-269"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-270">Querformat</span><span class="sxs-lookup"><span data-stu-id="51c66-270">Landscape</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-271">**Papier Länge**</span><span class="sxs-lookup"><span data-stu-id="51c66-271">**PaperLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-272">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-274">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Zehntel Millimeter)</span><span class="sxs-lookup"><span data-stu-id="51c66-274">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-275">Die Länge des Papiers.</span><span class="sxs-lookup"><span data-stu-id="51c66-275">Length of the paper.</span></span> <span data-ttu-id="51c66-276">Um die Größe des Papiers in Zoll zu ermitteln, teilen Sie diesen Wert durch 254.</span><span class="sxs-lookup"><span data-stu-id="51c66-276">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="51c66-277">Beispiel: 2794</span><span class="sxs-lookup"><span data-stu-id="51c66-277">Example: 2794</span></span>

</dd> <dt>

<span data-ttu-id="51c66-278">**Taschenbuchgröße**</span><span class="sxs-lookup"><span data-stu-id="51c66-278">**PaperSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51c66-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-281">Größe des Papiers.</span><span class="sxs-lookup"><span data-stu-id="51c66-281">Size of the paper.</span></span> <span data-ttu-id="51c66-282">Die möglichen Größen finden Sie in der **Eigenschaft "** Eigenschaft (Eigenschaft)" der zugeordneten [**Win32- \_ Drucker**](win32-printer.md) Klasse.</span><span class="sxs-lookup"><span data-stu-id="51c66-282">The possible sizes are found in the **PaperSizesSupported** property of the associated [**Win32\_Printer**](win32-printer.md) class.</span></span>

<span data-ttu-id="51c66-283">Beispiel: "A4 oder Buchstabe".</span><span class="sxs-lookup"><span data-stu-id="51c66-283">Example: "A4 or Letter".</span></span>

</dd> <dt>

<span data-ttu-id="51c66-284">**Taschen Breite**</span><span class="sxs-lookup"><span data-stu-id="51c66-284">**PaperWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-285">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-287">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Zehntel Millimeter)</span><span class="sxs-lookup"><span data-stu-id="51c66-287">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-288">Breite des Papiers.</span><span class="sxs-lookup"><span data-stu-id="51c66-288">Width of the paper.</span></span> <span data-ttu-id="51c66-289">Um die Größe des Papiers in Zoll zu ermitteln, teilen Sie diesen Wert durch 254.</span><span class="sxs-lookup"><span data-stu-id="51c66-289">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="51c66-290">Beispiel: 2159</span><span class="sxs-lookup"><span data-stu-id="51c66-290">Example: 2159</span></span>

</dd> <dt>

<span data-ttu-id="51c66-291">**PelsHeight**</span><span class="sxs-lookup"><span data-stu-id="51c66-291">**PelsHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-292">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-294">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51c66-294">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-295">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51c66-295">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-296">**PelsWidth**</span><span class="sxs-lookup"><span data-stu-id="51c66-296">**PelsWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-297">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-299">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51c66-299">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-300">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51c66-300">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-301">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="51c66-301">**PrintQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-302">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-304">Eine von vier Qualitätsstufen des Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="51c66-304">One of four quality levels of the print job.</span></span> <span data-ttu-id="51c66-305">Wenn ein positiver Wert angegeben wird, wird die Qualität in dpi (Punkte pro Zoll) gemessen.</span><span class="sxs-lookup"><span data-stu-id="51c66-305">If a positive value is specified, the quality is measured in dots per inch.</span></span>

<dt>

<span id="-1"></span>

<span data-ttu-id="51c66-306"><span id="-1"></span>**-1**</span><span class="sxs-lookup"><span data-stu-id="51c66-306"><span id="-1"></span>**-1**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-307">Entwurf</span><span class="sxs-lookup"><span data-stu-id="51c66-307">Draft</span></span>

</dd> <dt>

<span id="-2"></span>

<span data-ttu-id="51c66-308"><span id="-2"></span>**-2**</span><span class="sxs-lookup"><span data-stu-id="51c66-308"><span id="-2"></span>**-2**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-309">Niedrig</span><span class="sxs-lookup"><span data-stu-id="51c66-309">Low</span></span>

</dd> <dt>

<span id="-3"></span>

<span data-ttu-id="51c66-310"><span id="-3"></span>**1-3**</span><span class="sxs-lookup"><span data-stu-id="51c66-310"><span id="-3"></span>**-3**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-311">Medium</span><span class="sxs-lookup"><span data-stu-id="51c66-311">Medium</span></span>

</dd> <dt>

<span id="-4"></span>

<span data-ttu-id="51c66-312"><span id="-4"></span>**-4**</span><span class="sxs-lookup"><span data-stu-id="51c66-312"><span id="-4"></span>**-4**</span></span>


</dt> <dd>

<span data-ttu-id="51c66-313">High</span><span class="sxs-lookup"><span data-stu-id="51c66-313">High</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-314">**Skalieren**</span><span class="sxs-lookup"><span data-stu-id="51c66-314">**Scale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-315">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-317">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Prozent)</span><span class="sxs-lookup"><span data-stu-id="51c66-317">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Percent)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-318">Der Faktor, um den die gedruckte Ausgabe skaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="51c66-318">Factor by which the printed output is to be scaled.</span></span> <span data-ttu-id="51c66-319">Beispielsweise reduziert eine Skala von 75 die Druckausgabe auf 3/4 die ursprüngliche Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="51c66-319">For example, a scale of 75 reduces the print output to 3/4 its original height and width.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-320">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="51c66-320">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51c66-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-323">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="51c66-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-324">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="51c66-324">Identifier by which the current object is known.</span></span>

<span data-ttu-id="51c66-325">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51c66-325">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="51c66-326">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="51c66-326">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-327">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-329">Versionsnummer der Initialisierungs Daten für das Gerät, das mit dem Windows-basierten Drucker verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="51c66-329">Version number of the initialization data for the device associated with the Windows-based printer.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-330">**TTOption**</span><span class="sxs-lookup"><span data-stu-id="51c66-330">**TTOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-331">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51c66-333">Gibt an, wie TrueType-Schriftarten gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51c66-333">Indicates how TrueType fonts should be printed.</span></span>

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span data-ttu-id="51c66-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span><span class="sxs-lookup"><span data-stu-id="51c66-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span></span>


</dt> <dd>

<span data-ttu-id="51c66-335">Druckt TrueType-Schriftarten als Grafiken.</span><span class="sxs-lookup"><span data-stu-id="51c66-335">Prints TrueType fonts as graphics.</span></span> <span data-ttu-id="51c66-336">Dies ist die Standardaktion für Punkt-Matrix-Drucker.</span><span class="sxs-lookup"><span data-stu-id="51c66-336">This is the default action for dot-matrix printers.</span></span>

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span data-ttu-id="51c66-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span><span class="sxs-lookup"><span data-stu-id="51c66-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span></span>


</dt> <dd>

<span data-ttu-id="51c66-338">Lädt TrueType-Schriftarten als weiche Schriftarten herunter.</span><span class="sxs-lookup"><span data-stu-id="51c66-338">Downloads TrueType fonts as soft fonts.</span></span> <span data-ttu-id="51c66-339">Dies ist die Standardaktion für Drucker, die die druckersteuerungsprache (-PCL) verwenden.</span><span class="sxs-lookup"><span data-stu-id="51c66-339">This is the default action for printers that use the Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span data-ttu-id="51c66-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Ersatz** (3)</span><span class="sxs-lookup"><span data-stu-id="51c66-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span></span>


</dt> <dd>

<span data-ttu-id="51c66-341">Ersetzt Geräte Schriftarten für TrueType-Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="51c66-341">Substitutes device fonts for TrueType fonts.</span></span> <span data-ttu-id="51c66-342">Dies ist die Standardaktion für PostScript-Drucker.</span><span class="sxs-lookup"><span data-stu-id="51c66-342">This is the default action for PostScript printers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="51c66-343">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="51c66-343">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-344">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-346">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) (Punkte pro Zoll)</span><span class="sxs-lookup"><span data-stu-id="51c66-346">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-347">Druckauflösung entlang der y-Achse (Höhe) des Druckauftrags (ähnlich der veralteten **YResolution** -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="51c66-347">Print resolution along the y-axis (height) of the print job (similar to the obsolete **YResolution** property).</span></span> <span data-ttu-id="51c66-348">Dieser Wert wird nur festgelegt, wenn die **PrintQuality** -Eigenschaft dieser Klasse positiv ist.</span><span class="sxs-lookup"><span data-stu-id="51c66-348">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-349">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="51c66-349">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-350">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-350">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-352">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51c66-352">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-353">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="51c66-353">This property is obsolete.</span></span> <span data-ttu-id="51c66-354">Verwenden Sie stattdessen die **HorizontalResolution** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="51c66-354">Use the **HorizontalResolution** property instead.</span></span>

</dd> <dt>

<span data-ttu-id="51c66-355">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="51c66-355">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c66-356">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51c66-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51c66-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51c66-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51c66-358">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51c66-358">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51c66-359">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="51c66-359">This property is obsolete.</span></span> <span data-ttu-id="51c66-360">Verwenden Sie stattdessen die **VerticalResolution** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="51c66-360">Use the **VerticalResolution** property instead.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51c66-361">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51c66-361">Remarks</span></span>

<span data-ttu-id="51c66-362">Die **Win32-Klasse \_ printerconfiguration** wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="51c66-362">The **Win32\_PrinterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="51c66-363">**Übersicht**</span><span class="sxs-lookup"><span data-stu-id="51c66-363">**Overview**</span></span>

<span data-ttu-id="51c66-364">Bevor Sie bestimmen können, wie Sie Ihre Druck Ressourcen optimal verteilen und verwenden können, benötigen Sie ausführliche Informationen zu diesen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="51c66-364">Before you can determine how to best distribute and use your printing resources, you must have a detailed knowledge of those resources.</span></span> <span data-ttu-id="51c66-365">Beispielsweise kann Abteilung a im Vergleich zu fünf Druckern in Abteilung B nur drei Drucker enthalten. Wenn die Drucker in Abteilung a 20 Seiten pro Minute drucken können und die Drucker in Abteilung B nur 5 Seiten pro Minute drucken können, verfügen Benutzer in Abteilung a tatsächlich über mehr Druckkapazität.</span><span class="sxs-lookup"><span data-stu-id="51c66-365">For example, Department A might have only three printers compared with five printers in Department B. However, if the printers in Department A can print 20 pages per minute and the printers in Department B can print only 5 pages per minute, users in Department A actually have more printing capacity.</span></span> <span data-ttu-id="51c66-366">Wenn Sie sich nicht mit den detaillierten Funktionen dieser Drucker auskennen, können Sie fälschlicherweise feststellen, dass Abteilung A eine kurze Druckkapazität hat und somit zusätzliche Drucker kaufen, die letztendlich nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51c66-366">Without knowing the detailed capabilities of these printers, you might erroneously conclude that Department A is short on printing capacity and thus purchase additional printers that end up going unused.</span></span>

<span data-ttu-id="51c66-367">WMI umfasst zwei Klassen: [**Win32- \_ Drucker**](win32-printer.md) und **Win32- \_ printerconfiguration**, die verwendet werden können, um detaillierte Informationen zu allen Druckern zurückzugeben, die auf einem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="51c66-367">WMI includes two classes, [**Win32\_Printer**](win32-printer.md) and **Win32\_PrinterConfiguration**, which can be used to return detailed information about all the printers installed on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="51c66-368">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51c66-368">Examples</span></span>

<span data-ttu-id="51c66-369">Im folgenden Codebeispiel werden Drucker Informationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="51c66-369">The following code sample retrieves printer information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a><span data-ttu-id="51c66-370">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51c66-370">Requirements</span></span>



| <span data-ttu-id="51c66-371">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51c66-371">Requirement</span></span> | <span data-ttu-id="51c66-372">Wert</span><span class="sxs-lookup"><span data-stu-id="51c66-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51c66-373">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51c66-373">Minimum supported client</span></span><br/> | <span data-ttu-id="51c66-374">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51c66-374">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="51c66-375">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51c66-375">Minimum supported server</span></span><br/> | <span data-ttu-id="51c66-376">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51c66-376">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="51c66-377">Namespace</span><span class="sxs-lookup"><span data-stu-id="51c66-377">Namespace</span></span><br/>                | <span data-ttu-id="51c66-378">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="51c66-378">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="51c66-379">MOF</span><span class="sxs-lookup"><span data-stu-id="51c66-379">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51c66-380"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="51c66-380"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="51c66-381">DLL</span><span class="sxs-lookup"><span data-stu-id="51c66-381">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51c66-382"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51c66-382"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="51c66-383">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51c66-383">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c66-384">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="51c66-384">**CIM\_Setting**</span></span>](./cim-setting.md)
</dt> <dt>

[<span data-ttu-id="51c66-385">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="51c66-385">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
