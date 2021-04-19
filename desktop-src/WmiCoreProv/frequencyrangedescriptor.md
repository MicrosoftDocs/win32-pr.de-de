---
description: Stellt einen Container für Merkmale eines unterstützten Häufigkeits Bereichs dar.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: Frequencyrangedescriptor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345099"
---
# <a name="frequencyrangedescriptor-class"></a><span data-ttu-id="cd83c-103">Frequencyrangedescriptor-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd83c-103">FrequencyRangeDescriptor class</span></span>

<span data-ttu-id="cd83c-104">Die WMI-Klasse **frequencyrangedescriptor** stellt einen Container für Merkmale eines unterstützten Häufigkeits Bereichs dar.</span><span class="sxs-lookup"><span data-stu-id="cd83c-104">The **FrequencyRangeDescriptor** WMI class represents a container for characteristics of a supported frequency range.</span></span> <span data-ttu-id="cd83c-105">Instanzen dieser Klasse sind Elemente des **monitorfreqranges** -Arrays in [**wmimonitorlistedfrequencyranges**](wmimonitorlistedfrequencyranges.md).</span><span class="sxs-lookup"><span data-stu-id="cd83c-105">Instances of this class are elements of the **MonitorFreqRanges** array in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd83c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd83c-106">Syntax</span></span>

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a><span data-ttu-id="cd83c-107">Member</span><span class="sxs-lookup"><span data-stu-id="cd83c-107">Members</span></span>

<span data-ttu-id="cd83c-108">Die **frequencyrangedescriptor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cd83c-108">The **FrequencyRangeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="cd83c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd83c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd83c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd83c-110">Properties</span></span>

<span data-ttu-id="cd83c-111">Die **frequencyrangedescriptor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd83c-111">The **FrequencyRangeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd83c-112">**Activeheight**</span><span class="sxs-lookup"><span data-stu-id="cd83c-112">**ActiveHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-115">Die Höhe des aktiven Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="cd83c-115">Height, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-116">**Activewidth**</span><span class="sxs-lookup"><span data-stu-id="cd83c-116">**ActiveWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-117">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-119">Breite des aktiven Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="cd83c-119">Width, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-120">**ConstraintType**</span><span class="sxs-lookup"><span data-stu-id="cd83c-120">**ConstraintType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-121">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-123">Einschränkungstyp für den Häufigkeits Bereich.</span><span class="sxs-lookup"><span data-stu-id="cd83c-123">Constraint type for the frequency range.</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-124">**Maxhsyncnenner**</span><span class="sxs-lookup"><span data-stu-id="cd83c-124">**MaxHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-127">Maximaler horizontaler Synchronisierungs Nenner.</span><span class="sxs-lookup"><span data-stu-id="cd83c-127">Maximum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-128">**Maxhsyncnumerator**</span><span class="sxs-lookup"><span data-stu-id="cd83c-128">**MaxHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-131">Maximaler horizontaler Synchronisierungs Zähler in Kilohertz (kHz).</span><span class="sxs-lookup"><span data-stu-id="cd83c-131">Maximum horizontal sync numerator in kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-132">**Maxpixelrate**</span><span class="sxs-lookup"><span data-stu-id="cd83c-132">**MaxPixelRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-135">Maximale Pixelrate in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="cd83c-135">Maximum pixel rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-136">**Maxvsyncnenner**</span><span class="sxs-lookup"><span data-stu-id="cd83c-136">**MaxVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-139">Maximaler vertikaler Synchronisierungs Nenner.</span><span class="sxs-lookup"><span data-stu-id="cd83c-139">Maximum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-140">**Maxvsyncnumerator**</span><span class="sxs-lookup"><span data-stu-id="cd83c-140">**MaxVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-143">Maximaler vertikaler Synchronisierungs Zähler in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="cd83c-143">Maximum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-144">**Minhsyncnenner**</span><span class="sxs-lookup"><span data-stu-id="cd83c-144">**MinHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-147">Der minimale horizontale Synchronisierungs Nenner.</span><span class="sxs-lookup"><span data-stu-id="cd83c-147">Minimum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-148">**Minhsyncnumerator**</span><span class="sxs-lookup"><span data-stu-id="cd83c-148">**MinHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-151">Minimaler horizontaler Synchronisierungs Zähler in, Kilohertz (kHz).</span><span class="sxs-lookup"><span data-stu-id="cd83c-151">Minimum horizontal sync numerator in, kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-152">**Minvsyncnenner**</span><span class="sxs-lookup"><span data-stu-id="cd83c-152">**MinVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-153">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-155">Minimaler vertikaler Synchronisierungs Nenner.</span><span class="sxs-lookup"><span data-stu-id="cd83c-155">Minimum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-156">**Minvsyncnumerator**</span><span class="sxs-lookup"><span data-stu-id="cd83c-156">**MinVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd83c-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-159">Minimaler vertikaler Synchronisierungs Zähler in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="cd83c-159">Minimum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="cd83c-160">**Ursprung**</span><span class="sxs-lookup"><span data-stu-id="cd83c-160">**Origin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd83c-161">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cd83c-161">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cd83c-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd83c-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd83c-163">Entstehungs.</span><span class="sxs-lookup"><span data-stu-id="cd83c-163">Origin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd83c-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd83c-164">Requirements</span></span>



| <span data-ttu-id="cd83c-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd83c-165">Requirement</span></span> | <span data-ttu-id="cd83c-166">Wert</span><span class="sxs-lookup"><span data-stu-id="cd83c-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd83c-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd83c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="cd83c-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd83c-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cd83c-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd83c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="cd83c-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd83c-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cd83c-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd83c-171">Namespace</span></span><br/>                | <span data-ttu-id="cd83c-172">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="cd83c-172">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="cd83c-173">MOF</span><span class="sxs-lookup"><span data-stu-id="cd83c-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd83c-174"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cd83c-174"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd83c-175">DLL</span><span class="sxs-lookup"><span data-stu-id="cd83c-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd83c-176"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd83c-176"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd83c-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd83c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd83c-178">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="cd83c-178">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




