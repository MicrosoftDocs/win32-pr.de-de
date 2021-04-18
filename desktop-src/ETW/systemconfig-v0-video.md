---
description: Diese Klasse ist die Ereignistyp Klasse für Video Konfigurations Ereignisse.
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: SystemConfig_V0_Video-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: b840e3c06e74f8acbd1e43550559385e78c9a638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978873"
---
# <a name="systemconfig_v0_video-class"></a><span data-ttu-id="35e46-103">SystemConfig \_ v0- \_ Video Klasse</span><span class="sxs-lookup"><span data-stu-id="35e46-103">SystemConfig\_V0\_Video class</span></span>

<span data-ttu-id="35e46-104">Diese Klasse ist die Ereignistyp Klasse für Video Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="35e46-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="35e46-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="35e46-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e46-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="35e46-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
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

## <a name="members"></a><span data-ttu-id="35e46-107">Member</span><span class="sxs-lookup"><span data-stu-id="35e46-107">Members</span></span>

<span data-ttu-id="35e46-108">Die **\_ \_ Video Klasse "SystemConfig v0** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="35e46-108">The **SystemConfig\_V0\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="35e46-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35e46-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35e46-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35e46-110">Properties</span></span>

<span data-ttu-id="35e46-111">Die **\_ \_ Video Klasse "SystemConfig v0** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="35e46-111">The **SystemConfig\_V0\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35e46-112">**Adapterstring**</span><span class="sxs-lookup"><span data-stu-id="35e46-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-113">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="35e46-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35e46-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-115">Qualifizierer: **wmidataid** (8), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="35e46-115">Qualifiers: **WmiDataId** (8), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-116">Der Name oder die Beschreibung des Adapters.</span><span class="sxs-lookup"><span data-stu-id="35e46-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-117">**Biosstring**</span><span class="sxs-lookup"><span data-stu-id="35e46-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-118">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="35e46-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35e46-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-120">Qualifizierer: **wmidataid** (9), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="35e46-120">Qualifiers: **WmiDataId** (9), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-121">BIOS-Name des Adapters.</span><span class="sxs-lookup"><span data-stu-id="35e46-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-122">**Bitsper Pixel**</span><span class="sxs-lookup"><span data-stu-id="35e46-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e46-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e46-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-125">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="35e46-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-126">Anzahl von Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35e46-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-127">**Chiptyp**</span><span class="sxs-lookup"><span data-stu-id="35e46-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-128">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="35e46-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35e46-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-130">Qualifizierer: **wmidataid** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="35e46-130">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-131">Der Chip Name des Adapters.</span><span class="sxs-lookup"><span data-stu-id="35e46-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-132">**' Dactype '**</span><span class="sxs-lookup"><span data-stu-id="35e46-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-133">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="35e46-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35e46-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-135">Qualifizierer: **wmidataid** (7), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="35e46-135">Qualifiers: **WmiDataId** (7), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-136">Der DAC-Chip Name (Digital-to-Analog Converter) des Adapters.</span><span class="sxs-lookup"><span data-stu-id="35e46-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="35e46-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-138">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="35e46-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35e46-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-140">Qualifizierer: **wmidataid** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="35e46-140">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-141">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="35e46-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="35e46-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e46-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e46-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-145">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="35e46-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-146">Maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="35e46-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-147">**Stateflags**</span><span class="sxs-lookup"><span data-stu-id="35e46-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e46-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e46-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-150">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="35e46-150">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-151">Gerätestatusflags.</span><span class="sxs-lookup"><span data-stu-id="35e46-151">Device state flags.</span></span> <span data-ttu-id="35e46-152">Dabei kann es sich um eine beliebige Kombination der folgenden handelt.</span><span class="sxs-lookup"><span data-stu-id="35e46-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="35e46-153">Wert</span><span class="sxs-lookup"><span data-stu-id="35e46-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="35e46-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="35e46-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="35e46-155"><dt>**Anzeigen \_ \_ \_ An \_ Desktop angefügtes Gerät**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="35e46-156">Das Gerät ist Teil des Desktops.</span><span class="sxs-lookup"><span data-stu-id="35e46-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="35e46-157"><dt>**Anzeigen \_ Geräte \_ Spiegelungs \_ Treiber**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="35e46-158">Stellt ein Pseudo Gerät dar, das verwendet wird, um die Anwendungs Zeichnung für die Verbindung mit einem Remote Computer oder anderen Zwecken zu spiegeln.</span><span class="sxs-lookup"><span data-stu-id="35e46-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="35e46-159">Diesem Gerät ist ein unsichtbarer Pseudo Monitor zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="35e46-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="35e46-160">Beispielsweise verwendet NetMeeting Sie.</span><span class="sxs-lookup"><span data-stu-id="35e46-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="35e46-161"><dt>**Anzeigen \_ Gerät \_ modespruned**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="35e46-162">Das Gerät verfügt über mehr Anzeigemodi als von seinen Ausgabegeräten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="35e46-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="35e46-163"><dt>**Anzeigen \_ \_Primäres \_**</dt> Gerät <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="35e46-164">Der primäre Desktop befindet sich auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="35e46-164">The primary desktop is on the device.</span></span> <span data-ttu-id="35e46-165">Bei einem System mit einer einzelnen Anzeigekarte wird dies immer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="35e46-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="35e46-166">Bei einem System mit mehreren Anzeige Karten kann dieser Satz nur von einem Gerät festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="35e46-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="35e46-167"><dt>**Anzeigen \_ Gerät \_**</dt> Wechsel <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="35e46-168">Das Gerät ist austauschbar. Dies kann nicht die primäre Anzeige sein.</span><span class="sxs-lookup"><span data-stu-id="35e46-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="35e46-169"><dt>**Anzeigen \_ Gerät \_ VGA- \_ kompatibel**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="35e46-170">Das Gerät ist VGA-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="35e46-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="35e46-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="35e46-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e46-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e46-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-174">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="35e46-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-175">Aktuelle Aktualisierungsrate in Hertz.</span><span class="sxs-lookup"><span data-stu-id="35e46-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="35e46-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e46-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e46-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-179">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="35e46-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-180">Aktuelle Anzahl von horizontalen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="35e46-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="35e46-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="35e46-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e46-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e46-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e46-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="35e46-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e46-184">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="35e46-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="35e46-185">Aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="35e46-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35e46-186">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="35e46-186">Requirements</span></span>



| <span data-ttu-id="35e46-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35e46-187">Requirement</span></span> | <span data-ttu-id="35e46-188">Wert</span><span class="sxs-lookup"><span data-stu-id="35e46-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35e46-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35e46-189">Minimum supported client</span></span><br/> | <span data-ttu-id="35e46-190">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="35e46-190">None supported</span></span><br/>                            |
| <span data-ttu-id="35e46-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35e46-191">Minimum supported server</span></span><br/> | <span data-ttu-id="35e46-192">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35e46-192">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35e46-193">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35e46-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e46-194">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="35e46-194">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




