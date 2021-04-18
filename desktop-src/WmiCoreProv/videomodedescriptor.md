---
description: Enthält modusdeskriptorelemente für das monitorsourcemodes-Array in der wmimonitorlistedsupportedsourcemodes-Klasse.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Videomodedescriptor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348428"
---
# <a name="videomodedescriptor-class"></a><span data-ttu-id="0fe3b-103">Videomodedescriptor-Klasse</span><span class="sxs-lookup"><span data-stu-id="0fe3b-103">VideoModeDescriptor class</span></span>

<span data-ttu-id="0fe3b-104">Die **videomodedescriptorvideo** -WMI-Klasse enthält modusdeskriptorelemente für das **monitorsourcemodes** -Array in der [**wmimonitorlistedsupportedsourcemodes**](wmimonitorlistedsupportedsourcemodes.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-104">The **VideoModeDescriptorVideo** WMI class contains mode descriptor elements for the **MonitorSourceModes** array in the [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) class.</span></span> <span data-ttu-id="0fe3b-105">Zu diesen Elementen gehören Monitor Features wie Aktualisierungsrate, Pixel Merkmale oder die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-105">These elements include monitor features such as refresh rate, pixel characteristics, or image size.</span></span> <span data-ttu-id="0fe3b-106">Die **videomodedescriptorvideo** -Klasse enthält Informationen, die eine übergeordnete Menge der Daten sind, die aus eingerichteten, standardmäßigen und detaillierten Zeit Steuerungs Blöcken verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-106">The **VideoModeDescriptorVideo** class contains information that is a superset of the data available from established, standard, and detailed timing blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe3b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fe3b-107">Syntax</span></span>

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a><span data-ttu-id="0fe3b-108">Member</span><span class="sxs-lookup"><span data-stu-id="0fe3b-108">Members</span></span>

<span data-ttu-id="0fe3b-109">Die **videomodedescriptor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0fe3b-109">The **VideoModeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="0fe3b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fe3b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fe3b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fe3b-111">Properties</span></span>

<span data-ttu-id="0fe3b-112">Die **videomodedescriptor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-112">The **VideoModeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fe3b-113">**Compositepolaritytype**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-113">**CompositePolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-114">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-116">Zusammengesetzter poltyp.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-116">Composite polarity type.</span></span> <span data-ttu-id="0fe3b-117">Dies ist eine Polarität von horizontalen Synchronisierungs Impulsen außerhalb der vertikalen Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-117">This is polarity of horizontal sync pulses outside of vertical sync.</span></span>



| <span data-ttu-id="0fe3b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-118">Value</span></span>                                                                              | <span data-ttu-id="0fe3b-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-119">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fe3b-120"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-120"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-121">Die zusammengesetzte Polarität ist positiv.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-121">Composite polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0fe3b-122"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-122"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-123">Die zusammengesetzte Polarität ist negativ.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-123">Composite polarity is negative.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0fe3b-124"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-124"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-125">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fe3b-125">Not applicable.</span></span> <span data-ttu-id="0fe3b-126">Der Signal Synchronisierungstyp muss Digital Composite sein.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-126">The signal sync type must be digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0fe3b-127">**Horizontalactivepixels**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-127">**HorizontalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-130">Anzahl von horizontal aktiven Pixeln.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-130">Number of horizontally active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-131">**Horizontalblankingpixels**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-131">**HorizontalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-132">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-134">Anzahl der horizontal leere Pixel</span><span class="sxs-lookup"><span data-stu-id="0fe3b-134">Number of horizontally blanking pixels</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-135">**Horizontalborder**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-135">**HorizontalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-136">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-138">Horizontaler Rahmen.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-138">Horizontal border.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-139">**Horizontalimagesize**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-139">**HorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-142">Horizontale Bildgröße in Millimeter (mm).</span><span class="sxs-lookup"><span data-stu-id="0fe3b-142">Horizontal image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-143">**Horizontalpolaritytype**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-143">**HorizontalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-144">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-146">Horizontaler poltyp.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-146">Horizontal polarity type.</span></span>



| <span data-ttu-id="0fe3b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-147">Value</span></span>                                                                              | <span data-ttu-id="0fe3b-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-148">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fe3b-149"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-149"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-150">Die horizontale Polarität ist positiv.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-150">Horizontal polarity is positive.</span></span><br/>                               |
| <dl> <span data-ttu-id="0fe3b-151"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-151"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-152">Die horizontale Polarität ist negativ.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-152">Horizontal polarity is negative.</span></span><br/>                               |
| <dl> <span data-ttu-id="0fe3b-153"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-153"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-154">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fe3b-154">Not applicable.</span></span> <span data-ttu-id="0fe3b-155">Der Signal Synchronisierungstyp muss Digital getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-155">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0fe3b-156">**Horizontalfreshshratenenner**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-156">**HorizontalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-159">Der Nenner der horizontalen Aktualisierungsrate.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-159">Horizontal refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-160">**Horizontalfreshshratenumschlag**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-160">**HorizontalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-163">Horizontaler Aktualisierungs Raten Zähler in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="0fe3b-163">Horizontal refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-164">**Horizontalsyncoffset**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-164">**HorizontalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-167">Horizontaler Synchronisierungs Offset.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-167">Horizontal sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-168">**Horizontalsyncpull Width**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-168">**HorizontalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-169">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-171">Breite der horizontalen Synchronisierungs Pulse.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-171">Horizontal sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-172">**Isinterschnür**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-172">**IsInterlaced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-173">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-175">Gibt an, ob der Anzeigemodus mit Zeilen Sprung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-175">Indicates whether the display mode is interlaced.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-176">**Isserrationrequired**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-176">**IsSerrationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-177">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-179">Gibt ggf. an, welche Art von Server erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-179">Indicates what type of serration is required, if appropriate.</span></span>



| <span data-ttu-id="0fe3b-180">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-180">Value</span></span>                                                                              | <span data-ttu-id="0fe3b-181">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-181">Meaning</span></span>                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fe3b-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-183">Der Controller muss während der vertikalen Synchronisierung eine horizontale Synchronisierung angeben.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-183">Controller shall supply horizontal sync during vertical sync.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0fe3b-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-185">Der Controller darf während der vertikalen Synchronisierung keine horizontale Synchronisierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-185">Controller shall not supply horizontal sync during vertical sync.</span></span><br/>                             |
| <dl> <span data-ttu-id="0fe3b-186"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-186"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-187">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fe3b-187">Not applicable.</span></span> <span data-ttu-id="0fe3b-188">Der Signal Synchronisierungstyp muss ein Bipolar, ein Analog zusammengesetzter oder ein digitaler Verbund sein.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-188">The signal sync type must be bipolar, analog composite, or digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0fe3b-189">**Issynconfiguration**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-189">**IsSyncOnRGB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-190">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-192">Gibt ggf. an, welche Videosignal Linien synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-192">Indicates which video signal lines should be synchronized, if appropriate.</span></span>



| <span data-ttu-id="0fe3b-193">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-193">Value</span></span>                                                                              | <span data-ttu-id="0fe3b-194">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-194">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fe3b-195"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-195"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-196">Der Synchronisierungs Impuls sollte in allen drei Videosignal Zeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-196">Sync pulse should appear on all 3 video signal lines.</span></span><br/>                  |
| <dl> <span data-ttu-id="0fe3b-197"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-197"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-198">Der Synchronisierungs Impuls sollte nur in der grünen Videosignal Linie angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-198">Sync pulse should only appear on the green video signal line.</span></span><br/>          |
| <dl> <span data-ttu-id="0fe3b-199"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-199"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-200">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fe3b-200">Not applicable.</span></span> <span data-ttu-id="0fe3b-201">Der Signal Synchronisierungstyp muss eine bipolare, zusammengesetzte Zeichen</span><span class="sxs-lookup"><span data-stu-id="0fe3b-201">The signal sync type must be bipolar analog composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0fe3b-202">**Pixelclockrate**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-202">**PixelClockRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-203">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-205">Pixel Taktfrequenz in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="0fe3b-205">Pixel clock rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-206">**Stereomodetype**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-206">**StereoModeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-207">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-207">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-209">Typ des Stereo-Modus.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-209">Stereo mode type.</span></span> <span data-ttu-id="0fe3b-210">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-210">The following table lists the possible values.</span></span>



| <span data-ttu-id="0fe3b-211">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-211">Value</span></span>                                                                              | <span data-ttu-id="0fe3b-212">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-212">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fe3b-213"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-213"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-214">Keine Stereo-.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-214">No stereo.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0fe3b-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-215"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-216">Feld sequenzielles Stereo mit dem richtigen Bild bei der Stereo Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-216">Field sequential stereo with right image on stereo sync.</span></span><br/> |
| <dl> <span data-ttu-id="0fe3b-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-217"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-218">Feld sequenzielles Stereo mit Links Bild bei der Stereo-Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-218">Field sequential stereo with left image on stereo sync.</span></span><br/>  |
| <dl> <span data-ttu-id="0fe3b-219"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-219"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-220">bidirektionale verschachtelte Stereo-Stereo-Datei mit dem rechten Bild in geraden Linien.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-220">2-way Interleaved Stereo with Right Image on Even Lines.</span></span><br/> |
| <dl> <span data-ttu-id="0fe3b-221"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-221"><dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-222">bidirektionale verschachtelte Stereo-Stereo-Datei mit dem linken Bild in geraden Linien.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-222">2-way Interleaved Stereo with Left Image on Even Lines.</span></span><br/>  |
| <dl> <span data-ttu-id="0fe3b-223"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-223"><dt>5 (0x5)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-224">vier Wege verschachtelte Stereo</span><span class="sxs-lookup"><span data-stu-id="0fe3b-224">4-way Interleaved Stereo.</span></span><br/>                                |
| <dl> <span data-ttu-id="0fe3b-225"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-225"><dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-226">Paralleles Interleaved Stereo.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-226">Side-by-Side Interleaved Stereo.</span></span><br/>                         |



 

</dd> <dt>

<span data-ttu-id="0fe3b-227">**Syncsignaltype**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-227">**SyncSignalType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-228">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-228">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-230">Signal Synchronisierungstyp.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-230">Signal sync type.</span></span> <span data-ttu-id="0fe3b-231">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-231">The following table lists the possible values.</span></span>



| <span data-ttu-id="0fe3b-232">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-232">Value</span></span>                                                                              | <span data-ttu-id="0fe3b-233">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-233">Meaning</span></span>                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="0fe3b-234"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-234"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-235">Analog zusammengesetzter</span><span class="sxs-lookup"><span data-stu-id="0fe3b-235">Analog Composite</span></span><br/>         |
| <dl> <span data-ttu-id="0fe3b-236"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-236"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-237">Bipolar Analog Composite</span><span class="sxs-lookup"><span data-stu-id="0fe3b-237">Bipolar Analog Composite</span></span><br/> |
| <dl> <span data-ttu-id="0fe3b-238"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-238"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-239">Digitaler Verbund</span><span class="sxs-lookup"><span data-stu-id="0fe3b-239">Digital Composite</span></span><br/>        |
| <dl> <span data-ttu-id="0fe3b-240"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-240"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-241">Digitaler separater</span><span class="sxs-lookup"><span data-stu-id="0fe3b-241">Digital Separate</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="0fe3b-242">**Verticalactivepixels**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-242">**VerticalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-243">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-245">Anzahl von vertikal aktiven Pixeln.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-245">Number of vertically active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-246">**Verticalblankingpixels**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-246">**VerticalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-247">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-249">Anzahl von vertikal Leerlauf enden Pixeln.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-249">Number of vertically blanking pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-250">**Verticalborder**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-250">**VerticalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-251">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-253">Vertikaler Rahmen.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-253">Vertical border.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-254">**Vertikalimagesize**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-254">**VerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-255">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-257">Vertikale Bildgröße in Millimeter (mm).</span><span class="sxs-lookup"><span data-stu-id="0fe3b-257">Vertical image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-258">**Verticalpolaritytype**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-258">**VerticalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-259">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-259">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-261">Vertikaler poltyp.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-261">Vertical polarity type.</span></span>



| <span data-ttu-id="0fe3b-262">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-262">Value</span></span>                                                                              | <span data-ttu-id="0fe3b-263">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-263">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fe3b-264"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-264"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-265">Die vertikale Polarität ist positiv.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-265">Vertical polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0fe3b-266"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-266"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-267">Vertikale Polarität ist negativ.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-267">Vertical polarity is negative</span></span><br/>                                  |
| <dl> <span data-ttu-id="0fe3b-268"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-268"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-269">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fe3b-269">Not applicable.</span></span> <span data-ttu-id="0fe3b-270">Der Signal Synchronisierungstyp muss Digital getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-270">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0fe3b-271">**Verticalfreshshratenenner**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-271">**VerticalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-272">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-274">Vertikaler Aktualisierungs Raten Nenner.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-274">Vertical refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-275">**Verticalcalfreshatenumschlag**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-275">**VerticalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-276">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-278">Vertikaler Aktualisierungs Raten Zähler in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="0fe3b-278">Vertical refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-279">**Verticalsyncoffset**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-279">**VerticalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-280">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-282">Vertikaler Synchronisierungs Offset.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-282">Vertical sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-283">**Verticalsyncpulcalwidth**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-283">**VerticalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-284">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-286">Breite der vertikalen Synchronisierungs Pulse.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-286">Vertical sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="0fe3b-287">Videostandardtype</span><span class="sxs-lookup"><span data-stu-id="0fe3b-287">VideoStandardType</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe3b-288">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-288">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0fe3b-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fe3b-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe3b-290">Video-Standardtyp.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-290">Video standard type.</span></span>



| <span data-ttu-id="0fe3b-291">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-291">Value</span></span>                                                                                | <span data-ttu-id="0fe3b-292">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-292">Meaning</span></span>                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fe3b-293"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-293"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-294">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0fe3b-294">Other</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-295"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-295"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-296">VESA-DMT.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-296">VESA DMT.</span></span> <span data-ttu-id="0fe3b-297">Von der Grafik zur Anzeige des Monitor Zeit Monitors für die Video-Electronics Standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="0fe3b-297">From Video Electronics Standard Association (VESA) Display Monitor Timings specification.</span></span><br/> |
| <dl> <span data-ttu-id="0fe3b-298"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-298"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-299">VESA-GTF.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-299">VESA GTF.</span></span> <span data-ttu-id="0fe3b-300">Von VESA verallgemeinerter Zeit Formel Standard.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-300">From VESA Generalized Timing Formula standard.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0fe3b-301"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-301"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-302">VESA CVT/von VESA koordinierte Video Zeitstandard.</span><span class="sxs-lookup"><span data-stu-id="0fe3b-302">VESA CVT/ From VESA Coordinated Video Timings standard.</span></span><br/>                                             |
| <dl> <span data-ttu-id="0fe3b-303"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-303"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-304">IBM</span><span class="sxs-lookup"><span data-stu-id="0fe3b-304">IBM</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="0fe3b-305"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-305"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-306">Apples</span><span class="sxs-lookup"><span data-stu-id="0fe3b-306">APPLE</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-307"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-307"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-308">NTSC M</span><span class="sxs-lookup"><span data-stu-id="0fe3b-308">NTSC M</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0fe3b-309"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-309"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-310">NTSC J</span><span class="sxs-lookup"><span data-stu-id="0fe3b-310">NTSC J</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0fe3b-311"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-311"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-312">NTSC 433</span><span class="sxs-lookup"><span data-stu-id="0fe3b-312">NTSC 433</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="0fe3b-313"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-313"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="0fe3b-314">PAL B</span><span class="sxs-lookup"><span data-stu-id="0fe3b-314">PAL B</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-315"><dt>10 (0xa)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-315"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="0fe3b-316">PAL B1</span><span class="sxs-lookup"><span data-stu-id="0fe3b-316">PAL B1</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0fe3b-317"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-317"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="0fe3b-318">PAL G</span><span class="sxs-lookup"><span data-stu-id="0fe3b-318">PAL G</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-319"><dt>12 (0xc)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-319"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="0fe3b-320">PAL H</span><span class="sxs-lookup"><span data-stu-id="0fe3b-320">PAL H</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-321"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-321"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="0fe3b-322">PAL I</span><span class="sxs-lookup"><span data-stu-id="0fe3b-322">PAL I</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-323"><dt>14 (0xe)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-323"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="0fe3b-324">PAL-ID</span><span class="sxs-lookup"><span data-stu-id="0fe3b-324">PAL D</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-325"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-325"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="0fe3b-326">PAL N</span><span class="sxs-lookup"><span data-stu-id="0fe3b-326">PAL N</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0fe3b-327"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-327"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-328">PAL-NC</span><span class="sxs-lookup"><span data-stu-id="0fe3b-328">PAL NC</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0fe3b-329"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-329"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-330">SECAM B</span><span class="sxs-lookup"><span data-stu-id="0fe3b-330">SECAM B</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0fe3b-331"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-331"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-332">SECAM D</span><span class="sxs-lookup"><span data-stu-id="0fe3b-332">SECAM D</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0fe3b-333"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-333"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-334">SECAM G</span><span class="sxs-lookup"><span data-stu-id="0fe3b-334">SECAM G</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0fe3b-335"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-335"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-336">SECAM H</span><span class="sxs-lookup"><span data-stu-id="0fe3b-336">SECAM H</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0fe3b-337"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-337"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-338">SECAM-K</span><span class="sxs-lookup"><span data-stu-id="0fe3b-338">SECAM K</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0fe3b-339"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-339"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-340">SECAM K1</span><span class="sxs-lookup"><span data-stu-id="0fe3b-340">SECAM K1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="0fe3b-341"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-341"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-342">SECAM L</span><span class="sxs-lookup"><span data-stu-id="0fe3b-342">SECAM L</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0fe3b-343"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-343"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-344">SECAM L1</span><span class="sxs-lookup"><span data-stu-id="0fe3b-344">SECAM L1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="0fe3b-345"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-345"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-346">EIA861</span><span class="sxs-lookup"><span data-stu-id="0fe3b-346">EIA861</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0fe3b-347"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-347"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-348">EIA861A</span><span class="sxs-lookup"><span data-stu-id="0fe3b-348">EIA861A</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0fe3b-349"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-349"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="0fe3b-350">EIA861B</span><span class="sxs-lookup"><span data-stu-id="0fe3b-350">EIA861B</span></span><br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fe3b-351">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fe3b-351">Requirements</span></span>



| <span data-ttu-id="0fe3b-352">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fe3b-352">Requirement</span></span> | <span data-ttu-id="0fe3b-353">Wert</span><span class="sxs-lookup"><span data-stu-id="0fe3b-353">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe3b-354">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fe3b-354">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe3b-355">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fe3b-355">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0fe3b-356">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fe3b-356">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe3b-357">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fe3b-357">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0fe3b-358">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fe3b-358">Namespace</span></span><br/>                | <span data-ttu-id="0fe3b-359">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="0fe3b-359">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="0fe3b-360">MOF</span><span class="sxs-lookup"><span data-stu-id="0fe3b-360">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fe3b-361"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-361"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fe3b-362">DLL</span><span class="sxs-lookup"><span data-stu-id="0fe3b-362">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fe3b-363"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fe3b-363"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe3b-364">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fe3b-364">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe3b-365">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="0fe3b-365">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




