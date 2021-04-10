---
description: Berechnet die Menge an Video Arbeitsspeicher, der für einen virtuellen remotefx-Computer erforderlich ist.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Calculatevideomemoryrequirements-Methode der Msvm_Synth3dVideoPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129745"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a><span data-ttu-id="bd96c-103">Calculatevideomemoryrequirements-Methode der MSVM \_ Synth3dVideoPool-Klasse</span><span class="sxs-lookup"><span data-stu-id="bd96c-103">CalculateVideoMemoryRequirements method of the Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="bd96c-104">Berechnet die Menge an Video Arbeitsspeicher, der für einen virtuellen remotefx-Computer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bd96c-104">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd96c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd96c-105">Syntax</span></span>


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a><span data-ttu-id="bd96c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd96c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd96c-107">*Monitorauflösung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd96c-107">*monitorResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd96c-108">Die maximale Monitor Auflösung für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="bd96c-108">The maximum monitor resolution for the virtual machine.</span></span> <span data-ttu-id="bd96c-109">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="bd96c-109">This must be one of the following values.</span></span>



| <span data-ttu-id="bd96c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bd96c-110">Value</span></span>                                                                        | <span data-ttu-id="bd96c-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bd96c-111">Meaning</span></span>                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="bd96c-112"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-112"><dt>0</dt></span></span> </dl> | <span data-ttu-id="bd96c-113">Die maximale Auflösung beträgt 1024 768.</span><span class="sxs-lookup"><span data-stu-id="bd96c-113">The maximum resolution is 1024   768.</span></span><br/>  |
| <dl> <span data-ttu-id="bd96c-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-114"><dt>1</dt></span></span> </dl> | <span data-ttu-id="bd96c-115">Die maximale Auflösung beträgt 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="bd96c-115">The maximum resolution is 1280   1024.</span></span><br/> |
| <dl> <span data-ttu-id="bd96c-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-116"><dt>2</dt></span></span> </dl> | <span data-ttu-id="bd96c-117">Die maximale Auflösung beträgt 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="bd96c-117">The maximum resolution is 1600   1200.</span></span><br/> |
| <dl> <span data-ttu-id="bd96c-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="bd96c-119">Die maximale Auflösung beträgt 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="bd96c-119">The maximum resolution is 1920   1200.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bd96c-120">*anzahlüberwachungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd96c-120">*numberOfMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd96c-121">Die maximale Anzahl von Monitoren für die virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="bd96c-121">The maximum number of monitors for the virtual machine.</span></span> <span data-ttu-id="bd96c-122">Die Mindestanzahl von Monitoren ist 1, und der Höchstwert hängt von der maximalen Bildschirmauflösung ab.</span><span class="sxs-lookup"><span data-stu-id="bd96c-122">The minimum number of monitors is one and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="bd96c-123">In der folgenden Tabelle ist die maximale Anzahl von Monitoren definiert, die für unterschiedliche Auflösungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bd96c-123">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="bd96c-124">Lösung</span><span class="sxs-lookup"><span data-stu-id="bd96c-124">Resolution</span></span>             | <span data-ttu-id="bd96c-125">Maximale Anzahl von Monitoren</span><span class="sxs-lookup"><span data-stu-id="bd96c-125">Maximum monitors</span></span> |
|------------------------|------------------|
| <span data-ttu-id="bd96c-126">1024 768</span><span class="sxs-lookup"><span data-stu-id="bd96c-126">1024   768</span></span><br/>  | <span data-ttu-id="bd96c-127">4</span><span class="sxs-lookup"><span data-stu-id="bd96c-127">4</span></span><br/>     |
| <span data-ttu-id="bd96c-128">1280 1024</span><span class="sxs-lookup"><span data-stu-id="bd96c-128">1280   1024</span></span><br/> | <span data-ttu-id="bd96c-129">4</span><span class="sxs-lookup"><span data-stu-id="bd96c-129">4</span></span><br/>     |
| <span data-ttu-id="bd96c-130">1600 1200</span><span class="sxs-lookup"><span data-stu-id="bd96c-130">1600   1200</span></span><br/> | <span data-ttu-id="bd96c-131">3</span><span class="sxs-lookup"><span data-stu-id="bd96c-131">3</span></span><br/>     |
| <span data-ttu-id="bd96c-132">1920 1200</span><span class="sxs-lookup"><span data-stu-id="bd96c-132">1920   1200</span></span><br/> | <span data-ttu-id="bd96c-133">2</span><span class="sxs-lookup"><span data-stu-id="bd96c-133">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="bd96c-134">Requirements *dvideomemory* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd96c-134">*requiredVideoMemory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd96c-135">Empfängt die erforderliche Menge an Videospeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bd96c-135">Receives the required amount of video memory, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd96c-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd96c-136">Return value</span></span>

<span data-ttu-id="bd96c-137">Gibt einen Statuscode zurück, bei dem es sich um einen der folgenden Werte handeln kann.</span><span class="sxs-lookup"><span data-stu-id="bd96c-137">Returns a status code, which can be one of the following values.</span></span>



| <span data-ttu-id="bd96c-138">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bd96c-138">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="bd96c-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd96c-139">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="bd96c-140"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-140"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="bd96c-141">Erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bd96c-141">Successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="bd96c-142"><dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="bd96c-143">Der Auftrag wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="bd96c-143">Job started.</span></span><br/>                               |
| <dl> <span data-ttu-id="bd96c-144"><dt></dt> Fehler <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-144"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="bd96c-145">Fehler.</span><span class="sxs-lookup"><span data-stu-id="bd96c-145">Failed.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bd96c-146"><dt>**Zugriff verweigert**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-146"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="bd96c-147">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="bd96c-147">Access denied.</span></span><br/>                             |
| <dl> <span data-ttu-id="bd96c-148"><dt>**Nicht unterstützt**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-148"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="bd96c-149">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd96c-149">Not supported.</span></span><br/>                             |
| <dl> <span data-ttu-id="bd96c-150"><dt>**Status ist unbekannt**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-150"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="bd96c-151">Der Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="bd96c-151">Status is unknown.</span></span><br/>                         |
| <dl> <span data-ttu-id="bd96c-152"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-152"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="bd96c-153">Timeout</span><span class="sxs-lookup"><span data-stu-id="bd96c-153">Timeout.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bd96c-154"><dt>**Ungültiger Parameter**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-154"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="bd96c-155">Ein Parameter ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="bd96c-155">A parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="bd96c-156">Das <dt>**System wird in**</dt> <dt>32774</dt> verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd96c-156"><dt>**System is in used**</dt> <dt>32774</dt></span></span> </dl>                      | <span data-ttu-id="bd96c-157">Das System wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd96c-157">System is in use.</span></span><br/>                          |
| <dl> <span data-ttu-id="bd96c-158"><dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-158"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="bd96c-159">Der Status ist für diesen Vorgang ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd96c-159">The state is not valid for this operation.</span></span><br/> |
| <dl> <span data-ttu-id="bd96c-160"><dt>**Falscher Datentyp**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-160"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="bd96c-161">Falscher Datentyp.</span><span class="sxs-lookup"><span data-stu-id="bd96c-161">Incorrect data type.</span></span><br/>                       |
| <dl> <span data-ttu-id="bd96c-162"><dt>**System ist nicht verfügbar**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-162"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="bd96c-163">Das System ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd96c-163">System is not available.</span></span><br/>                   |
| <dl> <span data-ttu-id="bd96c-164"><dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-164"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="bd96c-165">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bd96c-165">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="bd96c-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd96c-166">Remarks</span></span>

<span data-ttu-id="bd96c-167">Diese Methode wird in der Regel auf dem Host System aufgerufen, um zu bestimmen, ob der Host über ausreichend verfügbaren Videospeicher zum Hosten eines virtuellen remotefx-Computers verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd96c-167">This method is typically called on the host system to determine if the host has enough available video memory to host a RemoteFX virtual machine.</span></span> <span data-ttu-id="bd96c-168">Zu diesem Zweck vergleichen Sie die von dieser Methode berechnete Menge an Videospeicher mit der Eigenschaft [**MSVM \_ physicalgpuinfo. availablevideomemory**](msvm-physicalgpuinfo.md) , um zu bestimmen, ob der Host Computer über ausreichend verfügbaren Videospeicher verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd96c-168">To do this, you compare the amount of video memory calculated by this method with the [**Msvm\_PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) property to determine if the host machine has enough available video memory.</span></span> <span data-ttu-id="bd96c-169">Anhand dieser Informationen können Sie feststellen, ob eine virtuelle Maschine auf das Host System verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="bd96c-169">You can use this information to determine if a virtual machine can be moved to the host system.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd96c-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd96c-170">Requirements</span></span>



| <span data-ttu-id="bd96c-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd96c-171">Requirement</span></span> | <span data-ttu-id="bd96c-172">Wert</span><span class="sxs-lookup"><span data-stu-id="bd96c-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd96c-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd96c-173">Minimum supported client</span></span><br/> | <span data-ttu-id="bd96c-174">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd96c-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bd96c-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd96c-175">Minimum supported server</span></span><br/> | <span data-ttu-id="bd96c-176">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd96c-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd96c-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd96c-177">Namespace</span></span><br/>                | <span data-ttu-id="bd96c-178">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bd96c-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bd96c-179">MOF</span><span class="sxs-lookup"><span data-stu-id="bd96c-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd96c-180"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd96c-181">DLL</span><span class="sxs-lookup"><span data-stu-id="bd96c-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd96c-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bd96c-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bd96c-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd96c-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd96c-184">**MSVM \_ physicalgpuinfo**</span><span class="sxs-lookup"><span data-stu-id="bd96c-184">**Msvm\_PhysicalGPUInfo**</span></span>](msvm-physicalgpuinfo.md)
</dt> <dt>

[<span data-ttu-id="bd96c-185">**MSVM \_ Synth3dVideoPool**</span><span class="sxs-lookup"><span data-stu-id="bd96c-185">**Msvm\_Synth3dVideoPool**</span></span>](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




