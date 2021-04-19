---
description: Die perfinfo \_ DShow \_ streamtrace-Struktur enthält Daten für ein DirectShow-Ablauf Verfolgungs Ereignis vom Typ GUID \_ streamtrace.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: PERFINFO_DSHOW_STREAMTRACE-Struktur (perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_STREAMTRACE
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 2bee4f3c11cf8462c8292cc412a6da5d9f9bfa78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352887"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a><span data-ttu-id="f2520-103">Perfinfo \_ DShow \_ streamtrace-Struktur</span><span class="sxs-lookup"><span data-stu-id="f2520-103">PERFINFO\_DSHOW\_STREAMTRACE structure</span></span>

<span data-ttu-id="f2520-104">Die `PERFINFO_DSHOW_STREAMTRACE` Struktur enthält Daten für ein DirectShow-Ablauf Verfolgungs Ereignis vom Typ GUID \_ streamtrace.</span><span class="sxs-lookup"><span data-stu-id="f2520-104">The `PERFINFO_DSHOW_STREAMTRACE` structure contains data for a DirectShow trace event of type GUID\_STREAMTRACE.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2520-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2520-105">Syntax</span></span>


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a><span data-ttu-id="f2520-106">Member</span><span class="sxs-lookup"><span data-stu-id="f2520-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2520-107">**id**</span><span class="sxs-lookup"><span data-stu-id="f2520-107">**id**</span></span>
</dt> <dd>

<span data-ttu-id="f2520-108">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f2520-108">Event identifier.</span></span> <span data-ttu-id="f2520-109">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f2520-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f2520-110">**bleiben**</span><span class="sxs-lookup"><span data-stu-id="f2520-110">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f2520-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="f2520-111">Reserved.</span></span> <span data-ttu-id="f2520-112">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="f2520-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f2520-113">**dshowclock**</span><span class="sxs-lookup"><span data-stu-id="f2520-113">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="f2520-114">Streamzeit für dieses Ereignis in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="f2520-114">Stream time for this event, in 100-nanosecond units.</span></span> <span data-ttu-id="f2520-115">Dieser Wert ist optional und kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f2520-115">This value is optional and can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f2520-116">**data**</span><span class="sxs-lookup"><span data-stu-id="f2520-116">**data**</span></span>
</dt> <dd>

<span data-ttu-id="f2520-117">Optionale Ereignisdaten, die aus vier **ULONGLONG** -Werten bestehen.</span><span class="sxs-lookup"><span data-stu-id="f2520-117">Optional event data consisting of four **ULONGLONG** values.</span></span> <span data-ttu-id="f2520-118">Die Bedeutung dieser Daten hängt vom Ereignis Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="f2520-118">The meaning of this data depends on the event identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2520-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2520-119">Remarks</span></span>

<span data-ttu-id="f2520-120">Die folgenden Ereignis Bezeichner sind definiert.</span><span class="sxs-lookup"><span data-stu-id="f2520-120">The following event identifiers are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2520-121">Ereignis Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f2520-121">Event identifier</span></span></th>
<th><span data-ttu-id="f2520-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2520-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2520-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span><span class="sxs-lookup"><span data-stu-id="f2520-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span></span></td>
<td><span data-ttu-id="f2520-124">Wird protokolliert, wenn der <a href="mpeg-2-demultiplexer.md">MPEG-2-Demultiplexer-</a> Filter einen Präsentationszeit Stempel (PTS) in eine streamzeit konvertiert.</span><span class="sxs-lookup"><span data-stu-id="f2520-124">Logged when the <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer</a> filter converts a presentation time stamp (PTS) to stream time.</span></span>
<ul>
<li><span data-ttu-id="f2520-125"><strong>data</strong>[0]: Converted start time.</span><span class="sxs-lookup"><span data-stu-id="f2520-125"><strong>data</strong>[0]: Converted start time.</span></span></li>
<li><span data-ttu-id="f2520-126"><strong>data</strong>[1]: Converted stop time.</span><span class="sxs-lookup"><span data-stu-id="f2520-126"><strong>data</strong>[1]: Converted stop time.</span></span></li>
<li><span data-ttu-id="f2520-127"><strong>Daten</strong>[2].</span><span class="sxs-lookup"><span data-stu-id="f2520-127"><strong>data</strong>[2].</span></span> <span data-ttu-id="f2520-128">Datenstrom Bezeichner für die eingabepin.</span><span class="sxs-lookup"><span data-stu-id="f2520-128">Stream identifier for the input pin.</span></span></li>
<li><span data-ttu-id="f2520-129"><strong>data</strong>[3]: PTS that was converted.</span><span class="sxs-lookup"><span data-stu-id="f2520-129"><strong>data</strong>[3]: PTS that was converted.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2520-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="f2520-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span></span></td>
<td><span data-ttu-id="f2520-131">Wird protokolliert, wenn MPEG-2 Demultiplexer ein Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="f2520-131">Logged when MPEG-2 Demultiplexer receives a sample.</span></span>
<ul>
<li><span data-ttu-id="f2520-132"><strong>Daten</strong> [0]: Current time returned by  <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2520-132"><strong>data</strong>[0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2520-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span><span class="sxs-lookup"><span data-stu-id="f2520-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span></span></td>
<td><span data-ttu-id="f2520-134">Wird protokolliert, wenn der VMR ein Beispiel für das Rendering plant, unmittelbar bevor der VMR <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: advientime</strong></a>aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2520-134">Logged when the VMR schedules a sample for rendering, immediately before the VMR calls <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.</span></span>
<ul>
<li><span data-ttu-id="f2520-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span><span class="sxs-lookup"><span data-stu-id="f2520-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2520-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span><span class="sxs-lookup"><span data-stu-id="f2520-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span></span></td>
<td><span data-ttu-id="f2520-137">Wird protokolliert, wenn der VMR einen Decodierungs Vorgang startet – d. h., wenn der Decoder <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>iamvideoaccelerator:: beginFrame</strong></a>aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2520-137">Logged when the VMR begins a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>.</span></span> <span data-ttu-id="f2520-138">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f2520-138">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2520-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="f2520-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span></span></td>
<td><span data-ttu-id="f2520-140">Wird protokolliert, wenn der VMR einen Deinterlacing-oder Video Zusammensetzung-Vorgang startet.</span><span class="sxs-lookup"><span data-stu-id="f2520-140">Logged when the VMR begins a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="f2520-141">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f2520-141">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2520-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span><span class="sxs-lookup"><span data-stu-id="f2520-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span></span></td>
<td><span data-ttu-id="f2520-143">Wird protokolliert, wenn der VMR einen Frame löscht. beispielsweise, wenn ein Beispiel spät war.</span><span class="sxs-lookup"><span data-stu-id="f2520-143">Logged when the VMR drops a frame; for example, if a sample was late.</span></span>
<ul>
<li><span data-ttu-id="f2520-144"><strong>data</strong>[0]: Sample start time.</span><span class="sxs-lookup"><span data-stu-id="f2520-144"><strong>data</strong>[0]: Sample start time.</span></span></li>
<li><span data-ttu-id="f2520-145"><strong>data</strong>[1]: Sample end time.</span><span class="sxs-lookup"><span data-stu-id="f2520-145"><strong>data</strong>[1]: Sample end time.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2520-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span><span class="sxs-lookup"><span data-stu-id="f2520-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span></span></td>
<td><span data-ttu-id="f2520-147">Wird protokolliert, wenn der VMR eine Benachrichtigungs Benachrichtigung von der Referenzuhr empfängt.</span><span class="sxs-lookup"><span data-stu-id="f2520-147">Logged when the VMR receives an advise notification from the reference clock.</span></span> <span data-ttu-id="f2520-148">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f2520-148">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2520-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span><span class="sxs-lookup"><span data-stu-id="f2520-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span></span></td>
<td><span data-ttu-id="f2520-150">Wird protokolliert, wenn der VMR einen Decodierungs Vorgang beendet – d. h., wenn der Decoder <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>iamvideoaccelerator:: Endframe</strong></a>aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2520-150">Logged when the VMR ends a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>.</span></span> <span data-ttu-id="f2520-151">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f2520-151">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2520-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="f2520-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span></span></td>
<td><span data-ttu-id="f2520-153">Wird protokolliert, wenn der VMR einen Deinterlacing-oder Video Zusammensetzung-Vorgang abschließt.</span><span class="sxs-lookup"><span data-stu-id="f2520-153">Logged when the VMR completes a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="f2520-154">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f2520-154">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2520-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="f2520-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span></span></td>
<td><span data-ttu-id="f2520-156">Wird protokolliert, wenn der VMR ein neues Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="f2520-156">Logged when the VMR receives a new sample.</span></span> <span data-ttu-id="f2520-157">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f2520-157">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2520-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span><span class="sxs-lookup"><span data-stu-id="f2520-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span></span></td>
<td><span data-ttu-id="f2520-159">Wird protokolliert, wenn der VMR das Rendern eines Frames abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="f2520-159">Logged when the VMR finishes rendering a frame.</span></span>
<ul>
<li><span data-ttu-id="f2520-160"><strong>data</strong>[0]: Time that it took to render this frame.</span><span class="sxs-lookup"><span data-stu-id="f2520-160"><strong>data</strong>[0]: Time that it took to render this frame.</span></span></li>
<li><span data-ttu-id="f2520-161"><strong>data</strong>[1]: Running average of frame rendering times.</span><span class="sxs-lookup"><span data-stu-id="f2520-161"><strong>data</strong>[1]: Running average of frame rendering times.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f2520-162">Um dieses Ereignis von einem DirectShow-Filter zu protokollieren, verwenden Sie die Funktion " **Perflog \_ streamtrace** ", die in der Header Datei "dxmperf. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f2520-162">To log this event from a DirectShow filter, use the **PERFLOG\_STREAMTRACE** function, which is defined in the header file Dxmperf.h.</span></span> <span data-ttu-id="f2520-163">Dieser Header ist in den DirectShow-Basisklassen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f2520-163">This header is included in the DirectShow base classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2520-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2520-164">Requirements</span></span>



| <span data-ttu-id="f2520-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2520-165">Requirement</span></span> | <span data-ttu-id="f2520-166">Wert</span><span class="sxs-lookup"><span data-stu-id="f2520-166">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2520-167">Header</span><span class="sxs-lookup"><span data-stu-id="f2520-167">Header</span></span><br/> | <dl> <span data-ttu-id="f2520-168"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2520-168"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2520-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2520-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2520-170">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f2520-170">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="f2520-171">Ereignis Ablauf Verfolgung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2520-171">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f2520-172">GUIDs der Ablauf Verfolgungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="f2520-172">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 
