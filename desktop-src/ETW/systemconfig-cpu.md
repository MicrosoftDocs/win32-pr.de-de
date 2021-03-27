---
description: Diese Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse.
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
ms.openlocfilehash: d08d0eeac9aa2287576bbb6dfe0e8ce41f116e8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980072"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="d4322-103">SystemConfig- \_ CPU-Klasse</span><span class="sxs-lookup"><span data-stu-id="d4322-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="d4322-104">Diese Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d4322-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="d4322-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="d4322-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4322-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4322-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="d4322-107">Member</span><span class="sxs-lookup"><span data-stu-id="d4322-107">Members</span></span>

<span data-ttu-id="d4322-108">Die **System config- \_ CPU** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d4322-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="d4322-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4322-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4322-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4322-110">Properties</span></span>

<span data-ttu-id="d4322-111">Die **System config- \_ CPU** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4322-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4322-112">**"Zuweisung"-Granularität**</span><span class="sxs-lookup"><span data-stu-id="d4322-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4322-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4322-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-115">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="d4322-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="d4322-116">Die Granularität, mit der der virtuelle Arbeitsspeicher zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d4322-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="d4322-117">**Computername**</span><span class="sxs-lookup"><span data-stu-id="d4322-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-118">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="d4322-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4322-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-120">Qualifizierer: **wmidataid** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="d4322-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="d4322-121">Name des Computers</span><span class="sxs-lookup"><span data-stu-id="d4322-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d4322-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="d4322-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-123">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="d4322-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4322-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-125">Qualifizierer: **wmidataid** (7), **Max** (132), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="d4322-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="d4322-126">Der Name der Domäne, in der der Computer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="d4322-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="d4322-127">**Hyperthreadingflag**</span><span class="sxs-lookup"><span data-stu-id="d4322-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4322-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4322-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-130">Qualifizierer: **wmidataid** (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="d4322-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d4322-131">Gibt an, ob die Hyper-Threading-Option für einen Prozessor aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4322-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="d4322-132">Jedes Bit reflektiert den Hyperthreading Zustand einer CPU auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="d4322-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d4322-133">**Memsize**</span><span class="sxs-lookup"><span data-stu-id="d4322-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4322-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4322-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-136">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="d4322-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="d4322-137">Gesamtmenge des für das Betriebssystem verfügbaren physischen Speichers.</span><span class="sxs-lookup"><span data-stu-id="d4322-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d4322-138">**Suhr**</span><span class="sxs-lookup"><span data-stu-id="d4322-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4322-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4322-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-141">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="d4322-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="d4322-142">Maximale Geschwindigkeit des Prozessors in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="d4322-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="d4322-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="d4322-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4322-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4322-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-146">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="d4322-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="d4322-147">Anzahl der Prozessoren auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="d4322-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d4322-148">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="d4322-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4322-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4322-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4322-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4322-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4322-151">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="d4322-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="d4322-152">Größe einer Auslagerungs Seite (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="d4322-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4322-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d4322-153">Requirements</span></span>



| <span data-ttu-id="d4322-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4322-154">Requirement</span></span> | <span data-ttu-id="d4322-155">Wert</span><span class="sxs-lookup"><span data-stu-id="d4322-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4322-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4322-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d4322-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4322-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d4322-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4322-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d4322-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4322-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4322-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4322-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4322-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="d4322-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




