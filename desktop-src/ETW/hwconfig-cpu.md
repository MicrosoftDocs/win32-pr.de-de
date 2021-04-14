---
description: Die hwconfig- \_ CPU-Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: HWConfig_CPU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978273"
---
# <a name="hwconfig_cpu-class"></a><span data-ttu-id="3d36c-104">Hwconfig- \_ CPU-Klasse</span><span class="sxs-lookup"><span data-stu-id="3d36c-104">HWConfig\_CPU class</span></span>

<span data-ttu-id="3d36c-105">Die **hwconfig- \_ CPU** -Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="3d36c-105">The **HWConfig\_CPU** class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="3d36c-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="3d36c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d36c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d36c-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a><span data-ttu-id="3d36c-108">Member</span><span class="sxs-lookup"><span data-stu-id="3d36c-108">Members</span></span>

<span data-ttu-id="3d36c-109">Die **hwconfig- \_ CPU** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3d36c-109">The **HWConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="3d36c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d36c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d36c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d36c-111">Properties</span></span>

<span data-ttu-id="3d36c-112">Die **hwconfig- \_ CPU** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3d36c-112">The **HWConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d36c-113">"Zuweisung"-Granularität</span><span class="sxs-lookup"><span data-stu-id="3d36c-113">AllocationGranularity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36c-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d36c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d36c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-116">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="3d36c-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="3d36c-117">Die Granularität, mit der der virtuelle Arbeitsspeicher zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3d36c-117">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="3d36c-118">Computername</span><span class="sxs-lookup"><span data-stu-id="3d36c-118">ComputerName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36c-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3d36c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d36c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-121">Qualifizierer: wmidataid (6), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="3d36c-121">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="3d36c-122">Name des Computers</span><span class="sxs-lookup"><span data-stu-id="3d36c-122">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3d36c-123">Memsize</span><span class="sxs-lookup"><span data-stu-id="3d36c-123">MemSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36c-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d36c-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d36c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-126">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="3d36c-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="3d36c-127">Gesamtmenge des für das Betriebssystem verfügbaren physischen Speichers.</span><span class="sxs-lookup"><span data-stu-id="3d36c-127">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="3d36c-128">Suhr</span><span class="sxs-lookup"><span data-stu-id="3d36c-128">MHz</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36c-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d36c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d36c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-131">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="3d36c-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="3d36c-132">Maximale Geschwindigkeit des Prozessors in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="3d36c-132">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="3d36c-133">NumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="3d36c-133">NumberOfProcessors</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36c-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d36c-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d36c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-136">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="3d36c-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="3d36c-137">Anzahl der Prozessoren auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="3d36c-137">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3d36c-138">PageSize</span><span class="sxs-lookup"><span data-stu-id="3d36c-138">PageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36c-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d36c-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d36c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d36c-141">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="3d36c-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="3d36c-142">Größe einer Auslagerungs Seite (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="3d36c-142">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d36c-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3d36c-143">Requirements</span></span>



| <span data-ttu-id="3d36c-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d36c-144">Requirement</span></span> | <span data-ttu-id="3d36c-145">Wert</span><span class="sxs-lookup"><span data-stu-id="3d36c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="3d36c-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d36c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3d36c-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d36c-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3d36c-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d36c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3d36c-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3d36c-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="3d36c-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d36c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d36c-151">**Hwconfig**</span><span class="sxs-lookup"><span data-stu-id="3d36c-151">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




