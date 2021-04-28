---
description: 'SystemConfig_V0_CPU-Klasse: Diese Klasse ist die Ereignistypklasse für CPU-Konfigurationsereignisse.'
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
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105988"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="abd97-103">SystemConfig \_ V0 \_ CPU-Klasse</span><span class="sxs-lookup"><span data-stu-id="abd97-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="abd97-104">Diese Klasse ist die Ereignistypklasse für CPU-Konfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="abd97-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="abd97-105">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="abd97-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd97-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="abd97-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="abd97-107">Member</span><span class="sxs-lookup"><span data-stu-id="abd97-107">Members</span></span>

<span data-ttu-id="abd97-108">Die **SystemConfig \_ \_ V0-CPU-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="abd97-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="abd97-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abd97-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abd97-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abd97-110">Properties</span></span>

<span data-ttu-id="abd97-111">Die **SystemConfig \_ \_ V0-CPU-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abd97-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abd97-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="abd97-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd97-113">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="abd97-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abd97-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd97-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd97-115">Qualifizierer: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="abd97-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="abd97-116">Granularität, mit der virtueller Arbeitsspeicher zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="abd97-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="abd97-117">**Computername**</span><span class="sxs-lookup"><span data-stu-id="abd97-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd97-118">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="abd97-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="abd97-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd97-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd97-120">Qualifizierer: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="abd97-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="abd97-121">Name des Computers</span><span class="sxs-lookup"><span data-stu-id="abd97-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="abd97-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="abd97-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd97-123">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="abd97-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="abd97-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd97-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd97-125">Qualifizierer: **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="abd97-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="abd97-126">Name der Domäne, in der der Computer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="abd97-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="abd97-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="abd97-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd97-128">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="abd97-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abd97-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd97-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd97-130">Qualifizierer: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="abd97-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="abd97-131">Gesamtmenge des für das Betriebssystem verfügbaren physischen Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="abd97-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="abd97-132">**Mhz**</span><span class="sxs-lookup"><span data-stu-id="abd97-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd97-133">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="abd97-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abd97-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd97-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd97-135">Qualifizierer: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="abd97-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="abd97-136">Maximale Geschwindigkeit des Prozessors in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="abd97-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="abd97-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="abd97-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd97-138">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="abd97-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abd97-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd97-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd97-140">Qualifizierer: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="abd97-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="abd97-141">Anzahl der Prozessoren auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="abd97-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="abd97-142">**Pagesize**</span><span class="sxs-lookup"><span data-stu-id="abd97-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd97-143">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="abd97-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abd97-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd97-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd97-145">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="abd97-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="abd97-146">Größe einer Auslagerungsseite in Bytes.</span><span class="sxs-lookup"><span data-stu-id="abd97-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abd97-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd97-147">Requirements</span></span>



| <span data-ttu-id="abd97-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd97-148">Requirement</span></span> | <span data-ttu-id="abd97-149">Wert</span><span class="sxs-lookup"><span data-stu-id="abd97-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="abd97-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abd97-150">Minimum supported client</span></span><br/> | <span data-ttu-id="abd97-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="abd97-151">None supported</span></span><br/>                            |
| <span data-ttu-id="abd97-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abd97-152">Minimum supported server</span></span><br/> | <span data-ttu-id="abd97-153">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abd97-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abd97-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="abd97-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd97-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="abd97-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




