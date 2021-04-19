---
description: Stellt die unterstützten Anzeigefunktionen des Monitors dar.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Supporteddisplayfeaturesdescriptor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356836"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a><span data-ttu-id="88e50-103">Supporteddisplayfeaturesdescriptor-Klasse</span><span class="sxs-lookup"><span data-stu-id="88e50-103">SupportedDisplayFeaturesDescriptor class</span></span>

<span data-ttu-id="88e50-104">Der **supporteddisplayfeaturesdescriptor** stellt die unterstützten Anzeigefunktionen des Monitors dar.</span><span class="sxs-lookup"><span data-stu-id="88e50-104">The **SupportedDisplayFeaturesDescriptor** represents the supported display features of the monitor.</span></span> <span data-ttu-id="88e50-105">Die Informationen in dieser Klasse entsprechen den Daten in der Videoeingabe Definition des standardmäßigen Enhanced Display Identification Data (E-EDID)-Standards von Video Electronics Standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="88e50-105">The information in this class corresponds to data in the Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e50-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="88e50-106">Syntax</span></span>

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a><span data-ttu-id="88e50-107">Member</span><span class="sxs-lookup"><span data-stu-id="88e50-107">Members</span></span>

<span data-ttu-id="88e50-108">Die **supporteddisplayfeaturesdescriptor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="88e50-108">The **SupportedDisplayFeaturesDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="88e50-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88e50-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88e50-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88e50-110">Properties</span></span>

<span data-ttu-id="88e50-111">Die **supporteddisplayfeaturesdescriptor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88e50-111">The **SupportedDisplayFeaturesDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88e50-112">**Activeoffsupported**</span><span class="sxs-lookup"><span data-stu-id="88e50-112">**ActiveOffSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e50-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88e50-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88e50-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e50-115">Unterstützung für aktive und sehr geringe Leistung.</span><span class="sxs-lookup"><span data-stu-id="88e50-115">Support for active off and very low power.</span></span> <span data-ttu-id="88e50-116">Die Anzeige beansprucht weniger Leistung, wenn Sie ein Zeit Steuerungs Signal empfängt, das außerhalb des deklarierten aktiven Betriebsbereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="88e50-116">The display consumes less power when it receives a timing signal that is outside the declared active operating range.</span></span> <span data-ttu-id="88e50-117">Die Anzeige wird auf den normalen Vorgang zurückgesetzt, wenn das Zeit Steuerungs Signal in den normalen Betriebsbereich zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="88e50-117">The display will revert to normal operation if the timing signal returns to the normal operating range.</span></span> <span data-ttu-id="88e50-118">Beispiele für Zeit Steuerungs Signale außerhalb des normalen Betriebsbereichs sind keine Synchronisierungs Signale oder kein Signal.</span><span class="sxs-lookup"><span data-stu-id="88e50-118">Examples of timing signals outside the normal operating range are no sync signals or no DE signal.</span></span>

</dd> <dt>

<span data-ttu-id="88e50-119">**Display Type**</span><span class="sxs-lookup"><span data-stu-id="88e50-119">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e50-120">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="88e50-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="88e50-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88e50-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e50-122">Der Typ der Anzeige für den Monitor.</span><span class="sxs-lookup"><span data-stu-id="88e50-122">Type of display for the monitor.</span></span> <span data-ttu-id="88e50-123">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="88e50-123">The following table lists possible values.</span></span>



| <span data-ttu-id="88e50-124">Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-124">Value</span></span>                                                                              | <span data-ttu-id="88e50-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="88e50-125">Meaning</span></span>                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="88e50-126"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="88e50-126"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="88e50-127">Monochrome/Graustufen Anzeige</span><span class="sxs-lookup"><span data-stu-id="88e50-127">Monochrome/grayscale display</span></span><br/> |
| <dl> <span data-ttu-id="88e50-128"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="88e50-128"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="88e50-129">RGB-Farbanzeige</span><span class="sxs-lookup"><span data-stu-id="88e50-129">RGB color display</span></span><br/>            |
| <dl> <span data-ttu-id="88e50-130"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="88e50-130"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="88e50-131">Nicht-RGB-multifarbanzeige</span><span class="sxs-lookup"><span data-stu-id="88e50-131">Non-RGB multicolor display</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="88e50-132">**Unterstützt**</span><span class="sxs-lookup"><span data-stu-id="88e50-132">**GTFSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e50-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88e50-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88e50-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e50-135">Gibt an, ob die Anzeige über eine Unterstützung von GTF verfügt</span><span class="sxs-lookup"><span data-stu-id="88e50-135">Indicates whether the display has GTF support.</span></span> <span data-ttu-id="88e50-136">**True** gibt an, dass die Anzeigezeit Angaben unterstützt, die auf dem standardmäßigen GTF-Parameter basieren.</span><span class="sxs-lookup"><span data-stu-id="88e50-136">If **True**, the display supports timings based on the GTF standard using default GTF parameter values.</span></span>

</dd> <dt>

<span data-ttu-id="88e50-137">**Haspreferredtimingmode**</span><span class="sxs-lookup"><span data-stu-id="88e50-137">**HasPreferredTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e50-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88e50-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88e50-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e50-140">Gibt an, ob die Anzeige über einen bevorzugten Zeit Steuerungs Modus verfügt.</span><span class="sxs-lookup"><span data-stu-id="88e50-140">Indicates whether the display has has a preferred timing mode.</span></span> <span data-ttu-id="88e50-141">**True** gibt an, dass der erste ausführliche Zeit Steuerungs Block den bevorzugten Zeit Steuerungs Modus des Monitors enthält.</span><span class="sxs-lookup"><span data-stu-id="88e50-141">If **True**, the first detailed timing block contains the preferred timing mode of the monitor.</span></span> <span data-ttu-id="88e50-142">Die Verwendung des bevorzugten Zeit Steuerungs Modus ist für EDID v. 1.3 und höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88e50-142">Use of preferred timing mode is required by EDID v.1.3 and higher.</span></span>

</dd> <dt>

<span data-ttu-id="88e50-143">**srgbsupported**</span><span class="sxs-lookup"><span data-stu-id="88e50-143">**sRGBSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e50-144">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88e50-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88e50-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e50-146">**True** gibt an, dass die Anzeige sRGB unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88e50-146">If **True**, the display supports sRGB.</span></span>

</dd> <dt>

<span data-ttu-id="88e50-147">**Standbysupported**</span><span class="sxs-lookup"><span data-stu-id="88e50-147">**StandbySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e50-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88e50-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88e50-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e50-150">Gibt an, ob die Anzeige den VESA-Display-/DPMS-Standbymodus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88e50-150">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) standby.</span></span> <span data-ttu-id="88e50-151">**True** gibt an, dass DPMS Standby unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="88e50-151">If **True**, DPMS standby is supported.</span></span>

</dd> <dt>

<span data-ttu-id="88e50-152">**Suspendsupported**</span><span class="sxs-lookup"><span data-stu-id="88e50-152">**SuspendSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e50-153">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88e50-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88e50-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e50-155">Gibt an, ob die Anzeige das anbrechen der VESA-Anzeige Energie Verwaltung (DPMS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88e50-155">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) suspend.</span></span> <span data-ttu-id="88e50-156">**True** gibt an, dass DPMS Suspend unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="88e50-156">If **True**, DPMS suspend is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88e50-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88e50-157">Requirements</span></span>



| <span data-ttu-id="88e50-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88e50-158">Requirement</span></span> | <span data-ttu-id="88e50-159">Wert</span><span class="sxs-lookup"><span data-stu-id="88e50-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88e50-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88e50-160">Minimum supported client</span></span><br/> | <span data-ttu-id="88e50-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88e50-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="88e50-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88e50-162">Minimum supported server</span></span><br/> | <span data-ttu-id="88e50-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88e50-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="88e50-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="88e50-164">Namespace</span></span><br/>                | <span data-ttu-id="88e50-165">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="88e50-165">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="88e50-166">MOF</span><span class="sxs-lookup"><span data-stu-id="88e50-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88e50-167"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="88e50-167"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="88e50-168">DLL</span><span class="sxs-lookup"><span data-stu-id="88e50-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88e50-169"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88e50-169"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e50-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88e50-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e50-171">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="88e50-171">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




