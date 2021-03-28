---
description: Die Ereignistyp Klasse für das Header Ereignis der Protokolldatei. Diese Klasse enthält Informationen über die Ereignis Ablauf Verfolgungs Sitzung.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: EventTrace_Header-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526864"
---
# <a name="eventtrace_header-class"></a><span data-ttu-id="1640d-104">EventTrace- \_ Header Klasse</span><span class="sxs-lookup"><span data-stu-id="1640d-104">EventTrace\_Header class</span></span>

<span data-ttu-id="1640d-105">Die Ereignistyp Klasse für das Header Ereignis der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="1640d-105">The event type class for the log file header event.</span></span> <span data-ttu-id="1640d-106">Diese Klasse enthält Informationen über die Ereignis Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1640d-106">This class contains information about the event tracing session.</span></span>

<span data-ttu-id="1640d-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1640d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1640d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1640d-108">Syntax</span></span>

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a><span data-ttu-id="1640d-109">Member</span><span class="sxs-lookup"><span data-stu-id="1640d-109">Members</span></span>

<span data-ttu-id="1640d-110">Die **EventTrace- \_ Header** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1640d-110">The **EventTrace\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="1640d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1640d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1640d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1640d-112">Properties</span></span>

<span data-ttu-id="1640d-113">Die **EventTrace- \_ Header** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1640d-113">The **EventTrace\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1640d-114">**BootTime**</span><span class="sxs-lookup"><span data-stu-id="1640d-114">**BootTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-115">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1640d-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-117">Qualifizierer: **wmidataid** (17)</span><span class="sxs-lookup"><span data-stu-id="1640d-117">Qualifiers: **WmiDataId** (17)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-118">Der Zeitpunkt, zu dem das System gestartet wurde, in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="1640d-118">Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-119">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="1640d-119">**BufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-122">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="1640d-122">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-123">Größe der Puffer der Ereignis Ablauf Verfolgungs Sitzung in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="1640d-123">Size of the event tracing session's buffers, in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-124">**Bufferslost**</span><span class="sxs-lookup"><span data-stu-id="1640d-124">**BuffersLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-127">Qualifizierer: **wmidataid** (21)</span><span class="sxs-lookup"><span data-stu-id="1640d-127">Qualifiers: **WmiDataId** (21)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-128">Gesamtanzahl verlorener Puffer.</span><span class="sxs-lookup"><span data-stu-id="1640d-128">Total number of buffers lost.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-129">**Bufferswritten**</span><span class="sxs-lookup"><span data-stu-id="1640d-129">**BuffersWritten**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-132">Qualifizierer: **wmidataid** (9)</span><span class="sxs-lookup"><span data-stu-id="1640d-132">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-133">Die Gesamtanzahl der Puffer, die von der Ereignis Ablauf Verfolgungs Sitzung geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="1640d-133">Total number of buffers written by the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-134">**Cpuspeed**</span><span class="sxs-lookup"><span data-stu-id="1640d-134">**CPUSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-137">Qualifizierer: **wmidataid** (13)</span><span class="sxs-lookup"><span data-stu-id="1640d-137">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-138">CPU-Geschwindigkeit in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="1640d-138">CPU speed, in megahertz.</span></span>

<span data-ttu-id="1640d-139">**Windows 2000:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1640d-139">**Windows 2000:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-140">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="1640d-140">**EndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1640d-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-143">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="1640d-143">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-144">Der Zeitpunkt, zu dem die Ereignis Ablauf Verfolgungs Sitzung beendet wurde (in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601).</span><span class="sxs-lookup"><span data-stu-id="1640d-144">Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span> <span data-ttu-id="1640d-145">Dieser Wert kann 0 sein, wenn Sie Ereignisse in Echtzeit oder über eine Protokolldatei, für die die Bereitstellung weiterhin Ereignisse protokolliert, verbrauchen.</span><span class="sxs-lookup"><span data-stu-id="1640d-145">This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-146">**Eventslost**</span><span class="sxs-lookup"><span data-stu-id="1640d-146">**EventsLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-149">Qualifizierer: **wmidataid** (12)</span><span class="sxs-lookup"><span data-stu-id="1640d-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-150">Anzahl von Ereignissen, die während der Ereignis Ablauf Verfolgungs Sitzung verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="1640d-150">Number of events lost during the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-151">**Logfilemode**</span><span class="sxs-lookup"><span data-stu-id="1640d-151">**LogFileMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-154">Qualifizierer: **wmidataid** (8), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="1640d-154">Qualifiers: **WmiDataId** (8), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="1640d-155">Aktueller Protokollierungs Modus für die Ereignis Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1640d-155">Current logging mode for the event tracing session.</span></span> <span data-ttu-id="1640d-156">Eine Liste der Werte finden Sie unter Protokollierungs Modus-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="1640d-156">For a list of values, see Logging Mode Constants.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-157">**Protokoll Dateiname**</span><span class="sxs-lookup"><span data-stu-id="1640d-157">**LogFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-158">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-160">Qualifizierer: **wmidataid** (15), **Zeiger**</span><span class="sxs-lookup"><span data-stu-id="1640d-160">Qualifiers: **WmiDataId** (15), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="1640d-161">Der Name der Ereignis Ablauf Verfolgungs Protokoll-Datei, die die Ereignisse enthält.</span><span class="sxs-lookup"><span data-stu-id="1640d-161">Name of the event tracing log file that contains the events.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-162">**Loggername**</span><span class="sxs-lookup"><span data-stu-id="1640d-162">**LoggerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-165">Qualifizierer: **wmidataid** (14), **Zeiger**</span><span class="sxs-lookup"><span data-stu-id="1640d-165">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="1640d-166">Name der Ereignis Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1640d-166">Name of the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-167">**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="1640d-167">**MaxFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-170">Qualifizierer: **wmidataid** (7)</span><span class="sxs-lookup"><span data-stu-id="1640d-170">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-171">Maximale Größe der Protokolldatei in Megabytes.</span><span class="sxs-lookup"><span data-stu-id="1640d-171">Maximum size of the log file, in megabytes.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-172">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="1640d-172">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-173">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-175">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="1640d-175">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-176">Anzahl der Prozessoren im System.</span><span class="sxs-lookup"><span data-stu-id="1640d-176">Number of processors on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-177">**PerfFreq**</span><span class="sxs-lookup"><span data-stu-id="1640d-177">**PerfFreq**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-178">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1640d-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-180">Qualifizierer: **wmidataid** (18)</span><span class="sxs-lookup"><span data-stu-id="1640d-180">Qualifiers: **WmiDataId** (18)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-181">Häufigkeit des hochauflösenden Leistungs Zählers, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1640d-181">Frequency of the high-resolution performance counter, if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-182">**Pointersize**</span><span class="sxs-lookup"><span data-stu-id="1640d-182">**PointerSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-185">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="1640d-185">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-186">Größe eines Zeiger Datentyps in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1640d-186">Size of a pointer data type, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-187">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="1640d-187">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-188">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-190">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="1640d-190">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-191">Buildnummer des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="1640d-191">Build number of the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-192">**Reservedflags**</span><span class="sxs-lookup"><span data-stu-id="1640d-192">**ReservedFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-193">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-195">Qualifizierer: **wmidataid** (20)</span><span class="sxs-lookup"><span data-stu-id="1640d-195">Qualifiers: **WmiDataId** (20)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-196">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1640d-196">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-197">**Startbuffers**</span><span class="sxs-lookup"><span data-stu-id="1640d-197">**StartBuffers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-198">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-200">Qualifizierer: **wmidataid** (10)</span><span class="sxs-lookup"><span data-stu-id="1640d-200">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-201">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1640d-201">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-202">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="1640d-202">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-203">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1640d-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-205">Qualifizierer: **wmidataid** (19)</span><span class="sxs-lookup"><span data-stu-id="1640d-205">Qualifiers: **WmiDataId** (19)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-206">Der Zeitpunkt, zu dem die Ereignis Ablauf Verfolgungs Sitzung in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601, gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="1640d-206">Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-207">**TimerResolution**</span><span class="sxs-lookup"><span data-stu-id="1640d-207">**TimerResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-210">Qualifizierer: **wmidataid** (6)</span><span class="sxs-lookup"><span data-stu-id="1640d-210">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-211">Auflösung des Hardware Zeit Gebers in Einheiten von 100 Nanosekunden.</span><span class="sxs-lookup"><span data-stu-id="1640d-211">Resolution of the hardware timer, in units of 100 nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-212">**TimeZoneInformation**</span><span class="sxs-lookup"><span data-stu-id="1640d-212">**TimeZoneInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-213">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="1640d-213">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1640d-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-215">Qualifizierer: **wmidataid** (16), **Extension ("noprint")**, **Max** (176)</span><span class="sxs-lookup"><span data-stu-id="1640d-215">Qualifiers: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-216">Eine [**Zeit \_ Zonen \_ Informations**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) Struktur, die die Zeitzone für die Member " **Boottime**", " **EndTime** " und " **StartTime** " enthält.</span><span class="sxs-lookup"><span data-stu-id="1640d-216">A [**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) structure that contains the time zone for the **BootTime**, **EndTime** and **StartTime** members.</span></span>

</dd> <dt>

<span data-ttu-id="1640d-217">**Version**</span><span class="sxs-lookup"><span data-stu-id="1640d-217">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1640d-218">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1640d-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1640d-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1640d-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1640d-220">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="1640d-220">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="1640d-221">Versionsnummer des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="1640d-221">Version number of the operating system.</span></span> <span data-ttu-id="1640d-222">Beginnend mit den nieder wertigen Bytes enthalten die ersten zwei Bytes die Hauptversion, die nächsten zwei Bytes enthalten eine neben Version, die nächsten zwei Bytes enthalten Service Pack Hauptversion, und die letzten zwei Bytes enthalten Service Pack neben Version.</span><span class="sxs-lookup"><span data-stu-id="1640d-222">Starting with the low-order bytes, the first two bytes contain major version, the next two bytes contain minor version, the next two bytes contain service pack major version, and the last two bytes contain service pack minor version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1640d-223">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1640d-223">Remarks</span></span>

<span data-ttu-id="1640d-224">Normalerweise möchten Sie die Werte für die folgenden Eigenschaften speichern, damit Sie später bei der Verarbeitung von Ereignissen aus der Protokolldatei verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1640d-224">Typically, you want to save the values for the following properties for use later when processing events from the log file.</span></span>

-   <span data-ttu-id="1640d-225">**Timerresolution**– verwenden Sie diese mit den **kerneltime** -und **usertime** -Membern der [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur, um die CPU-Kosten für eine Reihe von Anweisungen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1640d-225">**TimerResolution**—use with the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to determine the CPU cost for a set of instructions.</span></span> <span data-ttu-id="1640d-226">Weitere Informationen finden Sie im Abschnitt "Hinweise" im [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span><span class="sxs-lookup"><span data-stu-id="1640d-226">For details, see the Remarks section of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span>
-   <span data-ttu-id="1640d-227">**Pointersize**– verwenden Sie diesen Wert für Eigenschaften, die den **Zeiger** Qualifizierer enthalten, um die Größe des Zeigers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1640d-227">**PointerSize**—for properties that contain the **Pointer** qualifier, use this value to determine the size of the pointer.</span></span> <span data-ttu-id="1640d-228">Beachten Sie, dass dieser Wert möglicherweise nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="1640d-228">Note that this value may not be accurate.</span></span> <span data-ttu-id="1640d-229">Auf einem 64-Bit-Computer protokolliert z. b. eine 32-Bit-Anwendung 4-Byte-Zeiger. in der Sitzung wird jedoch " **pointersize** " auf 8 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1640d-229">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set **PointerSize** to 8.</span></span>
-   <span data-ttu-id="1640d-230">**Logfilemode**– verwenden Sie, um zu bestimmen, ob diese Sitzung eine private Protokollierungs Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="1640d-230">**LogFileMode**—use to determine if this session is a private logger session.</span></span> <span data-ttu-id="1640d-231">Es gibt einige Eigenschaften, die keine Daten für private Protokollierungs Sitzungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1640d-231">There are some properties that do not contain data for private logger sessions.</span></span> <span data-ttu-id="1640d-232">Beispielsweise die **kerneltime** -und **usertime** -Member der [**Ereignis-Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1640d-232">For example, the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1640d-233">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1640d-233">Requirements</span></span>



| <span data-ttu-id="1640d-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1640d-234">Requirement</span></span> | <span data-ttu-id="1640d-235">Wert</span><span class="sxs-lookup"><span data-stu-id="1640d-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1640d-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1640d-236">Minimum supported client</span></span><br/> | <span data-ttu-id="1640d-237">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1640d-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1640d-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1640d-238">Minimum supported server</span></span><br/> | <span data-ttu-id="1640d-239">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1640d-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1640d-240">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1640d-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1640d-241">**Eventtraceevent**</span><span class="sxs-lookup"><span data-stu-id="1640d-241">**EventTraceEvent**</span></span>](eventtraceevent.md)
</dt> <dt>

[<span data-ttu-id="1640d-242">**\_logfile-Header der Ablauf Verfolgung \_**</span><span class="sxs-lookup"><span data-stu-id="1640d-242">**TRACE\_LOGFILE\_HEADER**</span></span>](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
