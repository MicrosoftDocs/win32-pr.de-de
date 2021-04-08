---
description: Stellt die analogen Videoeingabe Parameter eines Computermonitors dar.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Wmimonitoranalog gvideoinputparameams-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960100"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a><span data-ttu-id="95f4f-103">Wmimonitoranalog gvideoinputparameams-Klasse</span><span class="sxs-lookup"><span data-stu-id="95f4f-103">WmiMonitorAnalogVideoInputParams class</span></span>

<span data-ttu-id="95f4f-104">Die **wmimonitoranalog** -WMI-Klasse stellt die analogen Videoeingabe Parameter eines Computermonitors dar.</span><span class="sxs-lookup"><span data-stu-id="95f4f-104">The **WmiMonitorAnalogVideoInputParams** WMI class represents the analog video input parameters of a computer monitor.</span></span> <span data-ttu-id="95f4f-105">Die Daten in dieser Klasse entsprechen den Daten in der Videoeingabe Definition von "velectronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Standard".</span><span class="sxs-lookup"><span data-stu-id="95f4f-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="95f4f-106">Eine Instanz dieser Klasse ist nur verfügbar, wenn der Wert der **videoinputtype** -Eigenschaft der [**wmimonitorbasicdisplayparameyparameyparameyparameyparameyparameyparameyparameyparameyparamey**](wmimonitorbasicdisplayparams.md)</span><span class="sxs-lookup"><span data-stu-id="95f4f-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Analog".</span></span>

## <a name="syntax"></a><span data-ttu-id="95f4f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f4f-107">Syntax</span></span>

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a><span data-ttu-id="95f4f-108">Member</span><span class="sxs-lookup"><span data-stu-id="95f4f-108">Members</span></span>

<span data-ttu-id="95f4f-109">Die **wmimonitoranalog gvideoinputparameams** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="95f4f-109">The **WmiMonitorAnalogVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="95f4f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95f4f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95f4f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95f4f-111">Properties</span></span>

<span data-ttu-id="95f4f-112">Die **wmimonitoranalog gvideoinputparameams** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95f4f-112">The **WmiMonitorAnalogVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95f4f-113">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="95f4f-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-114">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-116">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="95f4f-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="95f4f-117">**Compositesyncsupported**</span><span class="sxs-lookup"><span data-stu-id="95f4f-117">**CompositeSyncSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-118">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="95f4f-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-120">Gibt an, ob die kombinierte Synchronisierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="95f4f-120">Indicates whether composite sync is supported.</span></span>



| <span data-ttu-id="95f4f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-121">Value</span></span>                                                                              | <span data-ttu-id="95f4f-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95f4f-122">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="95f4f-123"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-123"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95f4f-124">Zusammengesetzte Synchronisierung auf horizontaler Synchronisierungs Linie wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95f4f-124">Composite sync on horizontal sync line is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="95f4f-125"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-125"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="95f4f-126">Zusammengesetzte Synchronisierung auf horizontaler Synchronisierungs Linie wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95f4f-126">Composite sync on horizontal sync line is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="95f4f-127">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="95f4f-127">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="95f4f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="95f4f-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-131">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="95f4f-131">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="95f4f-132">**Separatesyncssupported**</span><span class="sxs-lookup"><span data-stu-id="95f4f-132">**SeparateSyncsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-133">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="95f4f-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-135">Gibt an, ob separate synchronisiert unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="95f4f-135">Indicates whether separate syncs are supported.</span></span>



| <span data-ttu-id="95f4f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-136">Value</span></span>                                                                              | <span data-ttu-id="95f4f-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95f4f-137">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="95f4f-138"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-138"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95f4f-139">Separate synchronisiert werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95f4f-139">Separate syncs are supported.</span></span><br/>     |
| <dl> <span data-ttu-id="95f4f-140"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-140"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="95f4f-141">Separate synchronisiert werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95f4f-141">Separate syncs are not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="95f4f-142">**Serrationofvsynkrequired**</span><span class="sxs-lookup"><span data-stu-id="95f4f-142">**SerrationOfVsyncRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-143">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="95f4f-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-145">Gibt an, ob die vertikale Synchronisierungs Pulse-serration erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="95f4f-145">Indicates whether vertical sync pulse serration is required.</span></span>



| <span data-ttu-id="95f4f-146">Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-146">Value</span></span>                                                                              | <span data-ttu-id="95f4f-147">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95f4f-147">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95f4f-148"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-148"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95f4f-149">Wenn ein zusammengesetztes synchronisieren oder ein on-Green-on-Green-Video verwendet wird, ist die serration des vertikalen Synchronisierungs Pulse erforderlich</span><span class="sxs-lookup"><span data-stu-id="95f4f-149">Serration of the vertical sync pulse is required when composite sync or sync-on-green video is used.</span></span><br/>     |
| <dl> <span data-ttu-id="95f4f-150"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-150"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="95f4f-151">Wenn ein zusammengesetztes synchronisieren oder ein on-Green-on-Green-Video verwendet wird, ist die serration des vertikalen Synchronisierungs Pulse nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95f4f-151">Serration of the vertical sync pulse is not required when composite sync or sync-on-green video is used.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="95f4f-152">**Setuperwartet**</span><span class="sxs-lookup"><span data-stu-id="95f4f-152">**SetupExpected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-153">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="95f4f-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-155">Gibt an, ob Setup erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="95f4f-155">Indicates whether setup is expected.</span></span>



| <span data-ttu-id="95f4f-156">Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-156">Value</span></span>                                                                              | <span data-ttu-id="95f4f-157">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95f4f-157">Meaning</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95f4f-158"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-158"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95f4f-159">Der Monitor erwartet eine leer-zu-leer-Einrichtung oder eine socksebene gemäß dem entsprechenden Signal Stufen Standard.</span><span class="sxs-lookup"><span data-stu-id="95f4f-159">Monitor expects a blank-to-blank setup or pedestal per appropriate Signal Level Standard.</span></span><br/>                      |
| <dl> <span data-ttu-id="95f4f-160"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-160"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="95f4f-161">Der Monitor erwartet nicht, dass ein Leerzeichen oder ein Bildschirm Bild entsprechend dem entsprechenden Signal Stufen Standard ist.</span><span class="sxs-lookup"><span data-stu-id="95f4f-161">Monitor does not expect a blank-to-blank setup or pedestal according to the appropriate signal level standard.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="95f4f-162">**Signallevelstandard**</span><span class="sxs-lookup"><span data-stu-id="95f4f-162">**SignalLevelStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-163">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="95f4f-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-165">Signal Level-Standard für eVC-Verbindungen (Enhanced Video Connector).</span><span class="sxs-lookup"><span data-stu-id="95f4f-165">Signal level standard for Enhanced video connector (EVC) connections.</span></span>



| <span data-ttu-id="95f4f-166">Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-166">Value</span></span>                                                                              | <span data-ttu-id="95f4f-167">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95f4f-167">Meaning</span></span>                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="95f4f-168"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-168"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95f4f-169">0,7, 0.3 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="95f4f-169">0.7,0.3\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="95f4f-170"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-170"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="95f4f-171">0.714, 0.286 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="95f4f-171">0.714,0.286\[V\]</span></span><br/> |
| <dl> <span data-ttu-id="95f4f-172"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-172"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="95f4f-173">1.0, 0,4 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="95f4f-173">1.0,0.4\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="95f4f-174"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-174"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="95f4f-175">0,7, 0,0 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="95f4f-175">0.7,0.0\[V\]</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="95f4f-176">**SYN-greenvideosupported**</span><span class="sxs-lookup"><span data-stu-id="95f4f-176">**SyncOnGreenVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f4f-177">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="95f4f-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="95f4f-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f4f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f4f-179">Gibt an, ob die Synchronisierung bei Grün unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="95f4f-179">Indicates whether sync on green is supported.</span></span>



| <span data-ttu-id="95f4f-180">Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-180">Value</span></span>                                                                              | <span data-ttu-id="95f4f-181">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95f4f-181">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="95f4f-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95f4f-183">Sync on Green Video wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95f4f-183">Sync on green video is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="95f4f-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="95f4f-185">Das Synchronisieren bei einem grünen Video wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95f4f-185">Sync on green video is not supported.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95f4f-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95f4f-186">Requirements</span></span>



| <span data-ttu-id="95f4f-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95f4f-187">Requirement</span></span> | <span data-ttu-id="95f4f-188">Wert</span><span class="sxs-lookup"><span data-stu-id="95f4f-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95f4f-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95f4f-189">Minimum supported client</span></span><br/> | <span data-ttu-id="95f4f-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95f4f-190">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="95f4f-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95f4f-191">Minimum supported server</span></span><br/> | <span data-ttu-id="95f4f-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95f4f-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="95f4f-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="95f4f-193">Namespace</span></span><br/>                | <span data-ttu-id="95f4f-194">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="95f4f-194">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="95f4f-195">MOF</span><span class="sxs-lookup"><span data-stu-id="95f4f-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95f4f-196"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-196"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="95f4f-197">DLL</span><span class="sxs-lookup"><span data-stu-id="95f4f-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95f4f-198"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95f4f-198"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95f4f-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95f4f-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f4f-200">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="95f4f-200">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




