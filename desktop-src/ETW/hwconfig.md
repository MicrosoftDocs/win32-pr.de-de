---
description: Die hwconfig-Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse unter Windows XP. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Hwconfig-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868919"
---
# <a name="hwconfig-class"></a><span data-ttu-id="10f70-104">Hwconfig-Klasse</span><span class="sxs-lookup"><span data-stu-id="10f70-104">HWConfig class</span></span>

<span data-ttu-id="10f70-105">Die **hwconfig** -Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse unter Windows XP.</span><span class="sxs-lookup"><span data-stu-id="10f70-105">The **HWConfig** class is the parent class for hardware configuration events on Windows XP.</span></span>

<span data-ttu-id="10f70-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="10f70-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f70-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10f70-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="10f70-108">Member</span><span class="sxs-lookup"><span data-stu-id="10f70-108">Members</span></span>

<span data-ttu-id="10f70-109">Die **hwconfig** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="10f70-109">The **HWConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="10f70-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10f70-110">Remarks</span></span>

<span data-ttu-id="10f70-111">Diese Ereignisse stellen die Hardwarekonfiguration des Computers bereit.</span><span class="sxs-lookup"><span data-stu-id="10f70-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="10f70-112">Im Gegensatz zu anderen NT-Kernel Protokollierungs Ereignissen werden von der Kernel Sitzung automatisch Hardware Konfigurations Ereignisse generiert. Sie aktivieren diese Ereignisse nicht, wenn Sie die NT Kernel Logger-Sitzung starten.</span><span class="sxs-lookup"><span data-stu-id="10f70-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="10f70-113">**Windows 2000:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10f70-113">**Windows 2000:** Not supported.</span></span>

<span data-ttu-id="10f70-114">Informationen zu Hardware Konfigurations Ereignissen unter Windows Vista und Windows Server 2003 finden Sie in der [SystemConfig](systemconfig.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="10f70-114">For hardware configuration events on Windows Vista and Windows Server 2003, see the [SystemConfig](systemconfig.md) class.</span></span>

<span data-ttu-id="10f70-115">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Hardware Konfigurations Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**eventtraceconfigguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="10f70-115">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="10f70-116">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Hardware Konfigurations Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="10f70-116">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="10f70-117">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="10f70-117">Event type</span></span>                                                                      | <span data-ttu-id="10f70-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10f70-118">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f70-119">**Ereignis \_ Configuration \_ \_ \_ CPU**-Ablaufverfolgungstyp (Ereignistyp Wert ist 10)</span><span class="sxs-lookup"><span data-stu-id="10f70-119">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="10f70-120">CPU-Konfigurations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="10f70-120">CPU configuration event.</span></span> <span data-ttu-id="10f70-121">Die [**hwconfig \_ CPU**](hwconfig-cpu.md) MOF-Klassen definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="10f70-121">The [**HWConfig\_CPU**](hwconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="10f70-122">**Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ LogicalDisk**(Ereignistyp Wert ist 12)</span><span class="sxs-lookup"><span data-stu-id="10f70-122">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="10f70-123">Konfigurations Ereignis des logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="10f70-123">Logical disk configuration event.</span></span> <span data-ttu-id="10f70-124">Die MOF-Klasse " [**hwconfig \_ logdisk**](hwconfig-logdisk.md) MOF Classes" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="10f70-124">The [**HWConfig\_LogDisk**](hwconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="10f70-125">**Ereignis \_ \_Konfigurations- \_ \_ NIC des Ablauf Verfolgungs Typs**(Ereignistyp Wert ist 13)</span><span class="sxs-lookup"><span data-stu-id="10f70-125">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="10f70-126">Nic-Konfigurations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="10f70-126">NIC configuration event.</span></span> <span data-ttu-id="10f70-127">Die MOF-Klassen der [**hwconfig- \_ NIC**](hwconfig-nic.md) definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="10f70-127">The [**HWConfig\_NIC**](hwconfig-nic.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="10f70-128">**Ereignis \_ Typ der Ablaufverfolgungstyp \_ \_ config \_ PhysicalDisk**(Ereignistyp Wert ist 11)</span><span class="sxs-lookup"><span data-stu-id="10f70-128">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="10f70-129">Ereignis für die Konfiguration des physischen Datenträgers</span><span class="sxs-lookup"><span data-stu-id="10f70-129">Physical disk configuration event.</span></span> <span data-ttu-id="10f70-130">Die [**hwconfig \_ phydisk**](hwconfig-phydisk.md) -MOF-Klassen definieren die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="10f70-130">The [**HWConfig\_PhyDisk**](hwconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="10f70-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="10f70-131">Requirements</span></span>



| <span data-ttu-id="10f70-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10f70-132">Requirement</span></span> | <span data-ttu-id="10f70-133">Wert</span><span class="sxs-lookup"><span data-stu-id="10f70-133">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="10f70-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10f70-134">Minimum supported client</span></span><br/> | <span data-ttu-id="10f70-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10f70-135">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="10f70-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10f70-136">Minimum supported server</span></span><br/> | <span data-ttu-id="10f70-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="10f70-137">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="10f70-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="10f70-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f70-139">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="10f70-139">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="10f70-140">**Hwconfig- \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="10f70-140">**HWConfig\_CPU**</span></span>](hwconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="10f70-141">**Hwconfig- \_ logdisk**</span><span class="sxs-lookup"><span data-stu-id="10f70-141">**HWConfig\_LogDisk**</span></span>](hwconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="10f70-142">**Hwconfig- \_ NIC**</span><span class="sxs-lookup"><span data-stu-id="10f70-142">**HWConfig\_NIC**</span></span>](hwconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="10f70-143">**Hwconfig- \_ phydisk**</span><span class="sxs-lookup"><span data-stu-id="10f70-143">**HWConfig\_PhyDisk**</span></span>](hwconfig-phydisk.md)
</dt> </dl>

 

 
