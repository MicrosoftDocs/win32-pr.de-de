---
description: Diese Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869288"
---
# <a name="systemconfig-class"></a><span data-ttu-id="1bcba-104">SystemConfig-Klasse</span><span class="sxs-lookup"><span data-stu-id="1bcba-104">SystemConfig class</span></span>

<span data-ttu-id="1bcba-105">Diese Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="1bcba-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="1bcba-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1bcba-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bcba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bcba-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1bcba-108">Member</span><span class="sxs-lookup"><span data-stu-id="1bcba-108">Members</span></span>

<span data-ttu-id="1bcba-109">Die **SystemConfig** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="1bcba-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bcba-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bcba-110">Remarks</span></span>

<span data-ttu-id="1bcba-111">Diese Ereignisse stellen die Hardwarekonfiguration des Computers bereit.</span><span class="sxs-lookup"><span data-stu-id="1bcba-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="1bcba-112">Im Gegensatz zu anderen NT-Kernel Protokollierungs Ereignissen werden von der Kernel Sitzung automatisch Hardware Konfigurations Ereignisse generiert. Sie aktivieren diese Ereignisse nicht, wenn Sie die NT Kernel Logger-Sitzung starten.</span><span class="sxs-lookup"><span data-stu-id="1bcba-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="1bcba-113">Informationen zu Hardware Konfigurations Ereignissen unter Windows XP finden Sie in der [hwconfig](hwconfig.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="1bcba-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="1bcba-114">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Hardware Konfigurations Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**eventtraceconfigguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="1bcba-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="1bcba-115">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Hardware Konfigurations Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1bcba-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="1bcba-116">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="1bcba-116">Event type</span></span>                                                                      | <span data-ttu-id="1bcba-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bcba-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bcba-118">**Ereignis \_ Configuration \_ \_ \_ CPU**-Ablaufverfolgungstyp (Ereignistyp Wert ist 10)</span><span class="sxs-lookup"><span data-stu-id="1bcba-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="1bcba-119">CPU-Konfigurations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-119">CPU configuration event.</span></span> <span data-ttu-id="1bcba-120">Die MOF-Klassen der [**SystemConfig- \_ CPU**](systemconfig-cpu.md) definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="1bcba-121">**Ereignis \_ \_Parametertyp \_ config- \_ idechannel**(Ereignistyp Wert ist 23)</span><span class="sxs-lookup"><span data-stu-id="1bcba-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="1bcba-122">Konfigurations Ereignis für primäres und sekundäres IDE-Channel</span><span class="sxs-lookup"><span data-stu-id="1bcba-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="1bcba-123">Die MOF-Klasse der [**SystemConfig- \_ idechannel**](systemconfig-idechannel.md) -MOF-Klassen definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1bcba-124">**Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ UNQ**(Ereignistyp Wert ist 21)</span><span class="sxs-lookup"><span data-stu-id="1bcba-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="1bcba-125">UNQ-Ereignis (Interrupt Request).</span><span class="sxs-lookup"><span data-stu-id="1bcba-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="1bcba-126">Die MOF-Klasse [**SystemConfig \_ UNQ**](systemconfig-irq.md) MOF-Klassen definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="1bcba-127">**Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ LogicalDisk**(Ereignistyp Wert ist 12)</span><span class="sxs-lookup"><span data-stu-id="1bcba-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="1bcba-128">Konfigurations Ereignis des logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="1bcba-128">Logical disk configuration event.</span></span> <span data-ttu-id="1bcba-129">Die MOF-Klasse " [**SystemConfig \_ logdisk**](systemconfig-logdisk.md) MOF Classes" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="1bcba-130">**Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ NetInfo**(Ereignistyp Wert ist 17)</span><span class="sxs-lookup"><span data-stu-id="1bcba-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="1bcba-131">Netzwerk-Informationen-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-131">Network iformation event.</span></span> <span data-ttu-id="1bcba-132">Die MOF-Klasse [**SystemConfig \_ Network**](systemconfig-network.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="1bcba-133">**Ereignis \_ \_Konfigurations- \_ \_ NIC des Ablauf Verfolgungs Typs**(Ereignistyp Wert ist 13)</span><span class="sxs-lookup"><span data-stu-id="1bcba-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="1bcba-134">Nic-Konfigurations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-134">NIC configuration event.</span></span> <span data-ttu-id="1bcba-135">Die MOF-Klassen der [**SystemConfig- \_ NIC**](systemconfig-nic.md) definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="1bcba-136">**Ereignis \_ Typ der Ablaufverfolgungstyp \_ \_ config \_ PhysicalDisk**(Ereignistyp Wert ist 11)</span><span class="sxs-lookup"><span data-stu-id="1bcba-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="1bcba-137">Ereignis für die Konfiguration des physischen Datenträgers</span><span class="sxs-lookup"><span data-stu-id="1bcba-137">Physical disk configuration event.</span></span> <span data-ttu-id="1bcba-138">Die MOF-Klassen von [**SystemConfig \_ phydisk**](systemconfig-phydisk.md) definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="1bcba-139">**Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ PnP**(Ereignistyp Wert ist 22)</span><span class="sxs-lookup"><span data-stu-id="1bcba-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="1bcba-140">Plug & amp; Play-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-140">Plug and play event.</span></span> <span data-ttu-id="1bcba-141">Die MOF-Klasse der [**SystemConfig \_ PnP**](systemconfig-pnp.md) MOF-Klassen definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="1bcba-142">**Ereignis \_ Konfiguration des Ablaufverfolgungstyp \_ \_ config \_**(Ereignistyp Wert ist 16)</span><span class="sxs-lookup"><span data-stu-id="1bcba-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="1bcba-143">Power Configuration-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-143">Power configuration event.</span></span> <span data-ttu-id="1bcba-144">Die " [**SystemConfig \_ Power**](systemconfig-power.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="1bcba-145">**Ereignis \_ \_ \_ Konfigurations \_ Dienste des Ablauf Verfolgungs Typs**(Ereignistyp Wert ist 15)</span><span class="sxs-lookup"><span data-stu-id="1bcba-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="1bcba-146">Dienst Konfigurations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-146">Services configuration event.</span></span> <span data-ttu-id="1bcba-147">Die MOF-Klasse der [**SystemConfig- \_ Dienste**](systemconfig-services.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="1bcba-148">**Ereignis \_ \_ \_ Konfigurationstyp config \_ Video**(Ereignistyp Wert ist 14)</span><span class="sxs-lookup"><span data-stu-id="1bcba-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="1bcba-149">Konfigurations Ereignis des Grafikadapters.</span><span class="sxs-lookup"><span data-stu-id="1bcba-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="1bcba-150">Die [**SystemConfig \_ Video**](systemconfig-video.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1bcba-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="1bcba-151">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1bcba-151">Requirements</span></span>



| <span data-ttu-id="1bcba-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bcba-152">Requirement</span></span> | <span data-ttu-id="1bcba-153">Wert</span><span class="sxs-lookup"><span data-stu-id="1bcba-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1bcba-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1bcba-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1bcba-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bcba-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1bcba-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1bcba-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1bcba-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bcba-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1bcba-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1bcba-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bcba-159">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="1bcba-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="1bcba-160">**SystemConfig- \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="1bcba-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="1bcba-161">**SystemConfig- \_ idechannel**</span><span class="sxs-lookup"><span data-stu-id="1bcba-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="1bcba-162">**SystemConfig \_ UNQ**</span><span class="sxs-lookup"><span data-stu-id="1bcba-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="1bcba-163">**SystemConfig- \_ logdisk**</span><span class="sxs-lookup"><span data-stu-id="1bcba-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="1bcba-164">**SystemConfig- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="1bcba-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="1bcba-165">**SystemConfig- \_ NIC**</span><span class="sxs-lookup"><span data-stu-id="1bcba-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="1bcba-166">**SystemConfig- \_ phydisk**</span><span class="sxs-lookup"><span data-stu-id="1bcba-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="1bcba-167">**SystemConfig \_ PnP**</span><span class="sxs-lookup"><span data-stu-id="1bcba-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="1bcba-168">**\_Systemkonfigurationsstrom**</span><span class="sxs-lookup"><span data-stu-id="1bcba-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="1bcba-169">**SystemConfig- \_ Dienste**</span><span class="sxs-lookup"><span data-stu-id="1bcba-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="1bcba-170">**SystemConfig- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="1bcba-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="1bcba-171">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="1bcba-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 
