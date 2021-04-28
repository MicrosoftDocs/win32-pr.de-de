---
description: 'SystemConfig_V0_Video-Klasse: Diese Klasse ist die Ereignistypklasse für Videokonfigurationsereignisse.'
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
ms.openlocfilehash: 94fb9e50344cfbdde4be67815b80e4074ab1a878
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105918"
---
# <a name="systemconfig_v0_video-class"></a><span data-ttu-id="61eb7-103">SystemConfig \_ V0 \_ Video-Klasse</span><span class="sxs-lookup"><span data-stu-id="61eb7-103">SystemConfig\_V0\_Video class</span></span>

<span data-ttu-id="61eb7-104">Diese Klasse ist die Ereignistypklasse für Videokonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="61eb7-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="61eb7-105">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="61eb7-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="61eb7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="61eb7-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="61eb7-107">Member</span><span class="sxs-lookup"><span data-stu-id="61eb7-107">Members</span></span>

<span data-ttu-id="61eb7-108">Die **SystemConfig \_ V0 \_ Video-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="61eb7-108">The **SystemConfig\_V0\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="61eb7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61eb7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61eb7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61eb7-110">Properties</span></span>

<span data-ttu-id="61eb7-111">Die **SystemConfig \_ V0 \_ Video-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="61eb7-111">The **SystemConfig\_V0\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61eb7-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="61eb7-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-113">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="61eb7-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-115">Qualifizierer: **WmiDataId** (8), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="61eb7-115">Qualifiers: **WmiDataId** (8), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-116">Name oder Beschreibung des Adapters.</span><span class="sxs-lookup"><span data-stu-id="61eb7-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="61eb7-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-118">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="61eb7-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-120">Qualifizierer: **WmiDataId** (9), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="61eb7-120">Qualifiers: **WmiDataId** (9), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-121">BIOS-Name des Adapters.</span><span class="sxs-lookup"><span data-stu-id="61eb7-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="61eb7-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-123">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="61eb7-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-125">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="61eb7-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-126">Anzahl der Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61eb7-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="61eb7-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-128">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="61eb7-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-130">Qualifizierer: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="61eb7-130">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-131">Chipname des Adapters.</span><span class="sxs-lookup"><span data-stu-id="61eb7-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="61eb7-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-133">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="61eb7-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-135">Qualifizierer: **WmiDataId** (7), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="61eb7-135">Qualifiers: **WmiDataId** (7), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-136">Der Name des DAC-Chips (Digital-to-Analog Converter) des Adapters.</span><span class="sxs-lookup"><span data-stu-id="61eb7-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="61eb7-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-138">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="61eb7-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-140">Qualifizierer: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="61eb7-140">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-141">Adresse oder andere identifizierende Informationen zum eindeutigen Benennen des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="61eb7-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="61eb7-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-143">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="61eb7-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-145">Qualifizierer: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="61eb7-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-146">Maximal unterstützter Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="61eb7-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="61eb7-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-148">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="61eb7-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-150">Qualifizierer: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="61eb7-150">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-151">Gerätestatusflags.</span><span class="sxs-lookup"><span data-stu-id="61eb7-151">Device state flags.</span></span> <span data-ttu-id="61eb7-152">Dies kann eine beliebige kombination der folgenden Punkte sein.</span><span class="sxs-lookup"><span data-stu-id="61eb7-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="61eb7-153">Wert</span><span class="sxs-lookup"><span data-stu-id="61eb7-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="61eb7-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="61eb7-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="61eb7-155"><dt>**DISPLAY \_ AN DESKTOP 1 \_ \_ \_ ANGESCHLOSSENES GERÄT**</dt> <dt>(0X1)</dt></span><span class="sxs-lookup"><span data-stu-id="61eb7-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="61eb7-156">Das Gerät ist Teil des Desktops.</span><span class="sxs-lookup"><span data-stu-id="61eb7-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="61eb7-157"><dt>**DISPLAY \_ \_GERÄTESPIEGELUNGSTREIBER \_**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="61eb7-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="61eb7-158">Stellt ein Pseudogerät dar, das zum Spiegeln von Anwendungszeichnungen zum Herstellen einer Verbindung mit einem Remotecomputer oder anderen Zwecken verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61eb7-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="61eb7-159">Diesem Gerät ist ein unsichtbarer Pseudomonitor zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="61eb7-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="61eb7-160">NetMeeting verwendet sie beispielsweise.</span><span class="sxs-lookup"><span data-stu-id="61eb7-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="61eb7-161"><dt>**DISPLAY \_ \_GERÄTEMODUSSPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="61eb7-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="61eb7-162">Das Gerät verfügt über mehr Anzeigemodi als die Ausgabegeräte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="61eb7-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="61eb7-163"><dt>**DISPLAY \_ \_PRIMÄRES \_ GERÄT**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="61eb7-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="61eb7-164">Der primäre Desktop befindet sich auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="61eb7-164">The primary desktop is on the device.</span></span> <span data-ttu-id="61eb7-165">Für ein System mit einer einzelnen Anzeigekarte ist dies immer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61eb7-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="61eb7-166">Für ein System mit mehreren Grafikkarten kann diese Einstellung nur auf einem Gerät festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61eb7-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="61eb7-167"><dt>**DISPLAY \_ DEVICE \_ REMOVABLE**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="61eb7-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="61eb7-168">Das Gerät ist wechselbar. es kann nicht die primäre Anzeige sein.</span><span class="sxs-lookup"><span data-stu-id="61eb7-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="61eb7-169"><dt>**DISPLAY \_ \_ \_ GERÄTE-VGA-KOMPATIBEL**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="61eb7-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="61eb7-170">Das Gerät ist VGA-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="61eb7-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="61eb7-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="61eb7-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-172">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="61eb7-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-174">Qualifizierer: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="61eb7-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-175">Aktuelle Aktualisierungsrate in Hertz.</span><span class="sxs-lookup"><span data-stu-id="61eb7-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="61eb7-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-177">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="61eb7-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-179">Qualifizierer: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="61eb7-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-180">Aktuelle Anzahl horizontaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="61eb7-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="61eb7-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="61eb7-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61eb7-182">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="61eb7-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61eb7-184">Qualifizierer: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="61eb7-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="61eb7-185">Aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="61eb7-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61eb7-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61eb7-186">Requirements</span></span>



| <span data-ttu-id="61eb7-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61eb7-187">Requirement</span></span> | <span data-ttu-id="61eb7-188">Wert</span><span class="sxs-lookup"><span data-stu-id="61eb7-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61eb7-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61eb7-189">Minimum supported client</span></span><br/> | <span data-ttu-id="61eb7-190">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="61eb7-190">None supported</span></span><br/>                            |
| <span data-ttu-id="61eb7-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61eb7-191">Minimum supported server</span></span><br/> | <span data-ttu-id="61eb7-192">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61eb7-192">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61eb7-193">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="61eb7-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61eb7-194">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="61eb7-194">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




