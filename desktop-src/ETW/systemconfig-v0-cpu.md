---
description: Diese Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: SystemConfig_V0_CPU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6963201f76afa40e9b1741dc2936fa2ab4433a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960576"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="251ed-103">System config \_ v0- \_ CPU-Klasse</span><span class="sxs-lookup"><span data-stu-id="251ed-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="251ed-104">Diese Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="251ed-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="251ed-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="251ed-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="251ed-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="251ed-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a><span data-ttu-id="251ed-107">Member</span><span class="sxs-lookup"><span data-stu-id="251ed-107">Members</span></span>

<span data-ttu-id="251ed-108">Die **\_ \_ CPU-Klasse "SystemConfig v0** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="251ed-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="251ed-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="251ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="251ed-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="251ed-110">Properties</span></span>

<span data-ttu-id="251ed-111">Die **System config \_ v0- \_ CPU** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="251ed-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="251ed-112">**"Zuweisung"-Granularität**</span><span class="sxs-lookup"><span data-stu-id="251ed-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251ed-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="251ed-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="251ed-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="251ed-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251ed-115">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="251ed-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="251ed-116">Die Granularität, mit der der virtuelle Arbeitsspeicher zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="251ed-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="251ed-117">**Computername**</span><span class="sxs-lookup"><span data-stu-id="251ed-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251ed-118">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="251ed-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="251ed-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="251ed-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251ed-120">Qualifizierer: **wmidataid** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="251ed-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="251ed-121">Name des Computers</span><span class="sxs-lookup"><span data-stu-id="251ed-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="251ed-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="251ed-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251ed-123">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="251ed-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="251ed-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="251ed-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251ed-125">Qualifizierer: **wmidataid** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="251ed-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="251ed-126">Der Name der Domäne, in der der Computer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="251ed-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="251ed-127">**Memsize**</span><span class="sxs-lookup"><span data-stu-id="251ed-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251ed-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="251ed-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="251ed-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="251ed-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251ed-130">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="251ed-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="251ed-131">Gesamtmenge des für das Betriebssystem verfügbaren physischen Speichers.</span><span class="sxs-lookup"><span data-stu-id="251ed-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="251ed-132">**Suhr**</span><span class="sxs-lookup"><span data-stu-id="251ed-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251ed-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="251ed-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="251ed-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="251ed-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251ed-135">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="251ed-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="251ed-136">Maximale Geschwindigkeit des Prozessors in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="251ed-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="251ed-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="251ed-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251ed-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="251ed-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="251ed-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="251ed-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251ed-140">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="251ed-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="251ed-141">Anzahl der Prozessoren auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="251ed-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="251ed-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="251ed-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251ed-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="251ed-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="251ed-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="251ed-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251ed-145">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="251ed-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="251ed-146">Größe einer Auslagerungs Seite (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="251ed-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="251ed-147">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="251ed-147">Requirements</span></span>



| <span data-ttu-id="251ed-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="251ed-148">Requirement</span></span> | <span data-ttu-id="251ed-149">Wert</span><span class="sxs-lookup"><span data-stu-id="251ed-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="251ed-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="251ed-150">Minimum supported client</span></span><br/> | <span data-ttu-id="251ed-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="251ed-151">None supported</span></span><br/>                            |
| <span data-ttu-id="251ed-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="251ed-152">Minimum supported server</span></span><br/> | <span data-ttu-id="251ed-153">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="251ed-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="251ed-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="251ed-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251ed-155">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="251ed-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




