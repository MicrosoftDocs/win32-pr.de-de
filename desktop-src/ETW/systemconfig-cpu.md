---
description: 'SystemConfig_CPU-Klasse: Diese Klasse ist die Ereignistypklasse für CPU-Konfigurationsereignisse.'
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: SystemConfig_CPU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 07efa01bf58aeadfdfe12cd5db4d010a7f6dbca0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106118"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="d36c7-103">\_SystemConfig-CPU-Klasse</span><span class="sxs-lookup"><span data-stu-id="d36c7-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="d36c7-104">Diese Klasse ist die Ereignistypklasse für CPU-Konfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="d36c7-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="d36c7-105">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="d36c7-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d36c7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d36c7-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a><span data-ttu-id="d36c7-107">Member</span><span class="sxs-lookup"><span data-stu-id="d36c7-107">Members</span></span>

<span data-ttu-id="d36c7-108">Die **\_ SystemConfig-CPU-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d36c7-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="d36c7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d36c7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d36c7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d36c7-110">Properties</span></span>

<span data-ttu-id="d36c7-111">Die **\_ SystemConfig-CPU-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d36c7-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d36c7-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="d36c7-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-113">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d36c7-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-115">Qualifizierer: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="d36c7-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-116">Granularität, mit der virtueller Arbeitsspeicher zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="d36c7-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="d36c7-117">**Computername**</span><span class="sxs-lookup"><span data-stu-id="d36c7-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-118">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="d36c7-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-120">Qualifizierer: **WmiDataId** (6), **Max** (256), **Format(s)**</span><span class="sxs-lookup"><span data-stu-id="d36c7-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-121">Name des Computers</span><span class="sxs-lookup"><span data-stu-id="d36c7-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d36c7-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="d36c7-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-123">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="d36c7-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-125">Qualifizierer: **WmiDataId** (7), **Max** (132), **Format(s)**</span><span class="sxs-lookup"><span data-stu-id="d36c7-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-126">Name der Domäne, in der der Computer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="d36c7-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="d36c7-127">**HyperThreadingFlag**</span><span class="sxs-lookup"><span data-stu-id="d36c7-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-128">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d36c7-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-130">Qualifizierer: **WmiDataId** (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="d36c7-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-131">Gibt an, ob die Hyperthreadingoption für einen Prozessor ein- oder ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="d36c7-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="d36c7-132">Jedes Bit spiegelt den Hyperthreadingstatus einer CPU auf dem Computer wider.</span><span class="sxs-lookup"><span data-stu-id="d36c7-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d36c7-133">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="d36c7-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d36c7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-136">Qualifizierer: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="d36c7-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-137">Gesamtmenge des für das Betriebssystem verfügbaren physischen Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="d36c7-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d36c7-138">**Mhz**</span><span class="sxs-lookup"><span data-stu-id="d36c7-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-139">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d36c7-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-141">Qualifizierer: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="d36c7-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-142">Maximale Geschwindigkeit des Prozessors in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="d36c7-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="d36c7-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="d36c7-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-144">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d36c7-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-146">Qualifizierer: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="d36c7-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-147">Anzahl der Prozessoren auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="d36c7-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d36c7-148">**Pagesize**</span><span class="sxs-lookup"><span data-stu-id="d36c7-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d36c7-149">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="d36c7-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d36c7-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d36c7-151">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="d36c7-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="d36c7-152">Größe einer Auslagerungsseite in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d36c7-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d36c7-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d36c7-153">Requirements</span></span>



| <span data-ttu-id="d36c7-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d36c7-154">Requirement</span></span> | <span data-ttu-id="d36c7-155">Wert</span><span class="sxs-lookup"><span data-stu-id="d36c7-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d36c7-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d36c7-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d36c7-157">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d36c7-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d36c7-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d36c7-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d36c7-159">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d36c7-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d36c7-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d36c7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36c7-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="d36c7-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




