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
# <a name="perfinfo_dshow_streamtrace-structure"></a>Perfinfo \_ DShow \_ streamtrace-Struktur

Die `PERFINFO_DSHOW_STREAMTRACE` Struktur enthält Daten für ein DirectShow-Ablauf Verfolgungs Ereignis vom Typ GUID \_ streamtrace.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>Member

<dl> <dt>

**id**
</dt> <dd>

Ereignis Bezeichner. Siehe Hinweise.

</dd> <dt>

**bleiben**
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

**dshowclock**
</dt> <dd>

Streamzeit für dieses Ereignis in 100-Nanosecond-Einheiten. Dieser Wert ist optional und kann NULL sein.

</dd> <dt>

**data**
</dt> <dd>

Optionale Ereignisdaten, die aus vier **ULONGLONG** -Werten bestehen. Die Bedeutung dieser Daten hängt vom Ereignis Bezeichner ab.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die folgenden Ereignis Bezeichner sind definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ereignis Bezeichner</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</td>
<td>Wird protokolliert, wenn der <a href="mpeg-2-demultiplexer.md">MPEG-2-Demultiplexer-</a> Filter einen Präsentationszeit Stempel (PTS) in eine streamzeit konvertiert.
<ul>
<li><strong>data</strong>[0]: Converted start time.</li>
<li><strong>data</strong>[1]: Converted stop time.</li>
<li><strong>Daten</strong>[2]. Datenstrom Bezeichner für die eingabepin.</li>
<li><strong>data</strong>[3]: PTS that was converted.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</td>
<td>Wird protokolliert, wenn MPEG-2 Demultiplexer ein Beispiel empfängt.
<ul>
<li><strong>Daten</strong> [0]: Current time returned by  <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</td>
<td>Wird protokolliert, wenn der VMR ein Beispiel für das Rendering plant, unmittelbar bevor der VMR <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: advientime</strong></a>aufruft.
<ul>
<li><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</td>
<td>Wird protokolliert, wenn der VMR einen Decodierungs Vorgang startet – d. h., wenn der Decoder <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>iamvideoaccelerator:: beginFrame</strong></a>aufruft. Keine Ereignisdaten.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</td>
<td>Wird protokolliert, wenn der VMR einen Deinterlacing-oder Video Zusammensetzung-Vorgang startet. Keine Ereignisdaten.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</td>
<td>Wird protokolliert, wenn der VMR einen Frame löscht. beispielsweise, wenn ein Beispiel spät war.
<ul>
<li><strong>data</strong>[0]: Sample start time.</li>
<li><strong>data</strong>[1]: Sample end time.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_ADVISE</td>
<td>Wird protokolliert, wenn der VMR eine Benachrichtigungs Benachrichtigung von der Referenzuhr empfängt. Keine Ereignisdaten.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_END_DECODE</td>
<td>Wird protokolliert, wenn der VMR einen Decodierungs Vorgang beendet – d. h., wenn der Decoder <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>iamvideoaccelerator:: Endframe</strong></a>aufruft. Keine Ereignisdaten.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</td>
<td>Wird protokolliert, wenn der VMR einen Deinterlacing-oder Video Zusammensetzung-Vorgang abschließt. Keine Ereignisdaten.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_RECEIVE</td>
<td>Wird protokolliert, wenn der VMR ein neues Beispiel empfängt. Keine Ereignisdaten.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_RENDER_TIME</td>
<td>Wird protokolliert, wenn der VMR das Rendern eines Frames abgeschlossen hat.
<ul>
<li><strong>data</strong>[0]: Time that it took to render this frame.</li>
<li><strong>data</strong>[1]: Running average of frame rendering times.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Um dieses Ereignis von einem DirectShow-Filter zu protokollieren, verwenden Sie die Funktion " **Perflog \_ streamtrace** ", die in der Header Datei "dxmperf. h" definiert ist. Dieser Header ist in den DirectShow-Basisklassen enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Perfstruct. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[Ereignis Ablauf Verfolgung in DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUIDs der Ablauf Verfolgungs Ereignisse](trace-guids.md)
</dt> </dl>

 

 
