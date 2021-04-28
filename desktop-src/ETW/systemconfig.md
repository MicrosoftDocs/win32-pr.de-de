---
description: 'SystemConfig-Klasse: Diese Klasse ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: SystemConfig-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 232214aa2c33485d909525d54965f59fdc891a29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105868"
---
# <a name="systemconfig-class"></a><span data-ttu-id="50aa5-104">SystemConfig-Klasse</span><span class="sxs-lookup"><span data-stu-id="50aa5-104">SystemConfig class</span></span>

<span data-ttu-id="50aa5-105">Diese Klasse ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="50aa5-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="50aa5-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="50aa5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="50aa5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50aa5-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="50aa5-108">Member</span><span class="sxs-lookup"><span data-stu-id="50aa5-108">Members</span></span>

<span data-ttu-id="50aa5-109">Die **SystemConfig-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="50aa5-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="50aa5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50aa5-110">Remarks</span></span>

<span data-ttu-id="50aa5-111">Diese Ereignisse stellen die Hardwarekonfiguration des Computers bereit.</span><span class="sxs-lookup"><span data-stu-id="50aa5-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="50aa5-112">Im Gegensatz zu anderen NT-Kernelprotokollierungsereignissen generiert die Kernelsitzung automatisch Hardwarekonfigurationsereignisse. Sie aktivieren diese Ereignisse nicht, wenn Sie die NT-Kernelprotokollierungssitzung starten.</span><span class="sxs-lookup"><span data-stu-id="50aa5-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="50aa5-113">Informationen zu Hardwarekonfigurationsereignissen unter Windows XP finden Sie in der [HWConfig-Klasse.](hwconfig.md)</span><span class="sxs-lookup"><span data-stu-id="50aa5-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="50aa5-114">Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für Hardwarekonfigurationsereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="50aa5-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="50aa5-115">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Hardwarekonfigurationsereignis beim Nutzen von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="50aa5-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="50aa5-116">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="50aa5-116">Event type</span></span>                                                                      | <span data-ttu-id="50aa5-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50aa5-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50aa5-118">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(Ereignistypwert ist 10)</span><span class="sxs-lookup"><span data-stu-id="50aa5-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="50aa5-119">CPU-Konfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-119">CPU configuration event.</span></span> <span data-ttu-id="50aa5-120">Die [**\_ MOF-Klassen der SystemConfig-CPU**](systemconfig-cpu.md) definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="50aa5-121">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ IDECHANNEL**(Ereignistypwert ist 23)</span><span class="sxs-lookup"><span data-stu-id="50aa5-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="50aa5-122">Primäres und sekundäres IDE-Kanalkonfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="50aa5-123">Die [**MOF-Klasse der SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) MOF-Klassen definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="50aa5-124">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ IRQ**(Ereignistypwert ist 21)</span><span class="sxs-lookup"><span data-stu-id="50aa5-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="50aa5-125">IrQ-Ereignis (Interrupt Request).</span><span class="sxs-lookup"><span data-stu-id="50aa5-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="50aa5-126">Die [**MOF-Klasse \_ "SystemConfig IRQ**](systemconfig-irq.md) MOF" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="50aa5-127">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(Ereignistypwert ist 12)</span><span class="sxs-lookup"><span data-stu-id="50aa5-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="50aa5-128">Logisches Datenträgerkonfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-128">Logical disk configuration event.</span></span> <span data-ttu-id="50aa5-129">Die [**MOF-Klasse der SystemConfig LogDisk-MOF-Klasse \_**](systemconfig-logdisk.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="50aa5-130">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NETINFO**(Ereignistypwert ist 17)</span><span class="sxs-lookup"><span data-stu-id="50aa5-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="50aa5-131">Netzwerk-iformationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-131">Network iformation event.</span></span> <span data-ttu-id="50aa5-132">Die [**SystemConfig \_ Network**](systemconfig-network.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="50aa5-133">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NIC**(Ereignistypwert ist 13)</span><span class="sxs-lookup"><span data-stu-id="50aa5-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="50aa5-134">NIC-Konfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-134">NIC configuration event.</span></span> <span data-ttu-id="50aa5-135">Die [**MOF-Klassen \_ der SystemConfig-NIC**](systemconfig-nic.md) definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="50aa5-136">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(Ereignistypwert ist 11)</span><span class="sxs-lookup"><span data-stu-id="50aa5-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="50aa5-137">Physisches Datenträgerkonfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-137">Physical disk configuration event.</span></span> <span data-ttu-id="50aa5-138">Die [**MOF-Klassen von SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="50aa5-139">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PNP**(Ereignistypwert ist 22)</span><span class="sxs-lookup"><span data-stu-id="50aa5-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="50aa5-140">Plug &amp; Play-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-140">Plug and play event.</span></span> <span data-ttu-id="50aa5-141">Die [**MOF-Klasse \_ der SystemConfig-PNP-MOF-Klasse**](systemconfig-pnp.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="50aa5-142">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ POWER**(Ereignistypwert ist 16)</span><span class="sxs-lookup"><span data-stu-id="50aa5-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="50aa5-143">Energiekonfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-143">Power configuration event.</span></span> <span data-ttu-id="50aa5-144">Die [**SystemConfig \_ Power**](systemconfig-power.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="50aa5-145">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ SERVICES**(Ereignistypwert ist 15)</span><span class="sxs-lookup"><span data-stu-id="50aa5-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="50aa5-146">Dienstkonfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-146">Services configuration event.</span></span> <span data-ttu-id="50aa5-147">Die [**MOF-Klasse von SystemConfig \_ Services**](systemconfig-services.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="50aa5-148">**EVENT \_ TRACE \_ TYPE \_ CONFIG \_ VIDEO**(Ereignistypwert ist 14)</span><span class="sxs-lookup"><span data-stu-id="50aa5-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="50aa5-149">Grafikadapterkonfigurationsereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="50aa5-150">Die [**SystemConfig \_ Video**](systemconfig-video.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="50aa5-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="50aa5-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50aa5-151">Requirements</span></span>



| <span data-ttu-id="50aa5-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50aa5-152">Requirement</span></span> | <span data-ttu-id="50aa5-153">Wert</span><span class="sxs-lookup"><span data-stu-id="50aa5-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50aa5-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50aa5-154">Minimum supported client</span></span><br/> | <span data-ttu-id="50aa5-155">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50aa5-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50aa5-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50aa5-156">Minimum supported server</span></span><br/> | <span data-ttu-id="50aa5-157">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50aa5-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50aa5-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50aa5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50aa5-159">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="50aa5-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="50aa5-160">**\_SystemConfig-CPU**</span><span class="sxs-lookup"><span data-stu-id="50aa5-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="50aa5-161">**SystemConfig \_ IDEChannel**</span><span class="sxs-lookup"><span data-stu-id="50aa5-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="50aa5-162">**SystemConfig \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="50aa5-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="50aa5-163">**SystemConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="50aa5-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="50aa5-164">**SystemConfig \_ Network**</span><span class="sxs-lookup"><span data-stu-id="50aa5-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="50aa5-165">**\_SystemConfig-NIC**</span><span class="sxs-lookup"><span data-stu-id="50aa5-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="50aa5-166">**SystemConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="50aa5-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="50aa5-167">**\_SystemConfig-PNP**</span><span class="sxs-lookup"><span data-stu-id="50aa5-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="50aa5-168">**SystemConfig \_ Power**</span><span class="sxs-lookup"><span data-stu-id="50aa5-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="50aa5-169">**SystemConfig \_ Services**</span><span class="sxs-lookup"><span data-stu-id="50aa5-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="50aa5-170">**\_SystemConfig-Video**</span><span class="sxs-lookup"><span data-stu-id="50aa5-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="50aa5-171">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="50aa5-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 
