---
description: Diese Klasse ist die Ereignistyp Klasse für Video Konfigurations Ereignisse.
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: SystemConfig_Video-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 370c67501b75f0fd4ac88488744280f1e0065bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980944"
---
# <a name="systemconfig_video-class"></a><span data-ttu-id="ddb0e-103">SystemConfig- \_ Video Klasse</span><span class="sxs-lookup"><span data-stu-id="ddb0e-103">SystemConfig\_Video class</span></span>

<span data-ttu-id="ddb0e-104">Diese Klasse ist die Ereignistyp Klasse für Video Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="ddb0e-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb0e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb0e-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a><span data-ttu-id="ddb0e-107">Member</span><span class="sxs-lookup"><span data-stu-id="ddb0e-107">Members</span></span>

<span data-ttu-id="ddb0e-108">Die **SystemConfig- \_ Video** Klasse enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ddb0e-108">The **SystemConfig\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="ddb0e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ddb0e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddb0e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ddb0e-110">Properties</span></span>

<span data-ttu-id="ddb0e-111">Die **SystemConfig- \_ Video** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-111">The **SystemConfig\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddb0e-112">**Adapterstring**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-113">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="ddb0e-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-115">Qualifizierer: **wmidataid** (8), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-115">Qualifiers: **WmiDataId** (8), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-116">Der Name oder die Beschreibung des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-117">**Biosstring**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-118">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="ddb0e-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-120">Qualifizierer: **wmidataid** (9), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-120">Qualifiers: **WmiDataId** (9), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-121">BIOS-Name des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-122">**Bitsper Pixel**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-125">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-126">Anzahl von Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-127">**Chiptyp**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-128">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="ddb0e-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-130">Qualifizierer: **wmidataid** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-130">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-131">Der Chip Name des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-132">**' Dactype '**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-133">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="ddb0e-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-135">Qualifizierer: **wmidataid** (7), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-135">Qualifiers: **WmiDataId** (7), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-136">Der DAC-Chip Name (Digital-to-Analog Converter) des Adapters.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-138">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="ddb0e-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-140">Qualifizierer: **wmidataid** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-140">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-141">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-145">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-146">Maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-147">**Stateflags**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-150">Qualifizierer: **wmidataid** (11), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-150">Qualifiers: **WmiDataId** (11), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-151">Gerätestatusflags.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-151">Device state flags.</span></span> <span data-ttu-id="ddb0e-152">Dabei kann es sich um eine beliebige Kombination der folgenden handelt.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="ddb0e-153">Wert</span><span class="sxs-lookup"><span data-stu-id="ddb0e-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="ddb0e-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ddb0e-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="ddb0e-155"><dt>**Anzeigen \_ \_ \_ An \_ Desktop angefügtes Gerät**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb0e-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="ddb0e-156">Das Gerät ist Teil des Desktops.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="ddb0e-157"><dt>**Anzeigen \_ Geräte \_ Spiegelungs \_ Treiber**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb0e-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="ddb0e-158">Stellt ein Pseudo Gerät dar, das verwendet wird, um die Anwendungs Zeichnung für die Verbindung mit einem Remote Computer oder anderen Zwecken zu spiegeln.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="ddb0e-159">Diesem Gerät ist ein unsichtbarer Pseudo Monitor zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="ddb0e-160">Beispielsweise verwendet NetMeeting Sie.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="ddb0e-161"><dt>**Anzeigen \_ Gerät \_ modespruned**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb0e-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="ddb0e-162">Das Gerät verfügt über mehr Anzeigemodi als von seinen Ausgabegeräten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="ddb0e-163"><dt>**Anzeigen \_ \_Primäres \_**</dt> Gerät <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb0e-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="ddb0e-164">Der primäre Desktop befindet sich auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-164">The primary desktop is on the device.</span></span> <span data-ttu-id="ddb0e-165">Bei einem System mit einer einzelnen Anzeigekarte wird dies immer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="ddb0e-166">Bei einem System mit mehreren Anzeige Karten kann dieser Satz nur von einem Gerät festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="ddb0e-167"><dt>**Anzeigen \_ Gerät \_**</dt> Wechsel <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb0e-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="ddb0e-168">Das Gerät ist austauschbar. Dies kann nicht die primäre Anzeige sein.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="ddb0e-169"><dt>**Anzeigen \_ Gerät \_ VGA- \_ kompatibel**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb0e-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="ddb0e-170">Das Gerät ist VGA-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="ddb0e-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-174">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-175">Aktuelle Aktualisierungsrate in Hertz.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-179">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-180">Aktuelle Anzahl von horizontalen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ddb0e-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb0e-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ddb0e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb0e-184">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="ddb0e-185">Aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddb0e-186">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-186">Requirements</span></span>



| <span data-ttu-id="ddb0e-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddb0e-187">Requirement</span></span> | <span data-ttu-id="ddb0e-188">Wert</span><span class="sxs-lookup"><span data-stu-id="ddb0e-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ddb0e-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-189">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb0e-190">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddb0e-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ddb0e-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddb0e-191">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb0e-192">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddb0e-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddb0e-193">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ddb0e-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb0e-194">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="ddb0e-194">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




