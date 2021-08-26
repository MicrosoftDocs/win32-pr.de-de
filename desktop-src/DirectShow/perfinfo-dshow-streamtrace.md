---
description: Die PERFINFO \_ DSHOW \_ STREAMTRACE-Struktur enthält Daten für ein DirectShow-Ablaufverfolgungsereignis vom Typ GUID \_ STREAMTRACE.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: PERFINFO_DSHOW_STREAMTRACE-Struktur (Perfstruct.h)
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
ms.openlocfilehash: e17d013d90b133f9c6819b8d9ddf4b5970582cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477005"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>PERFINFO \_ DSHOW \_ STREAMTRACE-Struktur

Die `PERFINFO_DSHOW_STREAMTRACE` -Struktur enthält Daten für ein DirectShow-Ablaufverfolgungsereignis vom Typ GUID \_ STREAMTRACE.

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

Ereignisbezeichner. Siehe Hinweise.

</dd> <dt>

**reserved**
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

**dshowClock**
</dt> <dd>

Streamzeit für dieses Ereignis in Einheiten von 100 Nanosekunden. Dieser Wert ist optional und kann 0 (null) sein.

</dd> <dt>

**data**
</dt> <dd>

Optionale Ereignisdaten, die aus vier **ULONGLONG-Werten** bestehen. Die Bedeutung dieser Daten hängt vom Ereignisbezeichner ab.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die folgenden Ereignisbezeichner werden definiert.




| Ereignisbezeichner | BESCHREIBUNG | 
|------------------|-------------|
| PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION | Wird protokolliert, wenn der <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer-Filter</a> einen Präsentationszeitstempel (PTS) in die Streamzeit konvertiert.<ul><li><strong>data</strong>[0]: Konvertierte Startzeit.</li><li><strong>data</strong>[1]: Konvertierte Beendigungszeit.</li><li><strong>data</strong>[2]. Streambezeichner für den Eingabepin.</li><li><strong>data</strong>[3]: PTS, der konvertiert wurde.</li></ul> | 
| PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE | Wird protokolliert, wenn MPEG-2 Demultiplexer ein Beispiel empfängt.<ul><li><strong>data</strong>[0]: Aktuelle Zeit, die von <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>zurückgegeben wird.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE | Wird protokolliert, wenn die VMR ein Beispiel für das Rendering plant, unmittelbar bevor die VMR <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime aufruft.</strong></a><ul><li><strong>data</strong>[0]: Referenzzeit zum Beginn des Streamings, was der Streamzeit 0 (null) entspricht.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE | Wird protokolliert, wenn die VMR einen Decodierungsvorgang startet, d. h., wenn der Decoder <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>aufruft. Keine Ereignisdaten. | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE | Wird protokolliert, wenn die VMR einen Deinterlacing- oder Video-Compositingvorgang startet. Keine Ereignisdaten. | 
| PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME | Protokolliert, wenn die VMR einen Frame löscht; Beispielsweise, wenn ein Beispiel zu spät war.<ul><li><strong>data</strong>[0]: Beispielstartzeit.</li><li><strong>data</strong>[1]: Beispielendzeit.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_END_ADVISE | Wird protokolliert, wenn die VMR eine Empfehlungsbenachrichtigung von der Referenzuhr empfängt. Keine Ereignisdaten. | 
| PERFINFO_STREAMTRACE_VMR_END_DECODE | Wird protokolliert, wenn die VMR einen Decodierungsvorgang beendet, d. h., wenn der Decoder <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>aufruft. Keine Ereignisdaten. | 
| PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE | Wird protokolliert, wenn die VMR einen Deinterlacing- oder Video-Compositingvorgang abschließt. Keine Ereignisdaten. | 
| PERFINFO_STREAMTRACE_VMR_RECEIVE | Wird protokolliert, wenn die VMR ein neues Beispiel empfängt. Keine Ereignisdaten. | 
| PERFINFO_STREAMTRACE_VMR_RENDER_TIME | Wird protokolliert, wenn die VMR das Rendern eines Frames beendet.<ul><li><strong>data</strong>[0]: Zeit, die zum Rendern dieses Frames gedauert hat.</li><li><strong>data</strong>[1]: Durchschnittliche Ausführung der Framerenderingzeiten.</li></ul> | 




 

Verwenden Sie zum Protokollieren dieses Ereignisses aus einem DirectShow-Filter die **PERFLOG \_ STREAMTRACE-Funktion,** die in der Headerdatei Dxmperf.h definiert ist. Dieser Header ist in den DirectShow-Basisklassen enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Perfstruct.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[Ereignisablaufverfolgung in DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUIDs für Ablaufverfolgungsereignisse](trace-guids.md)
</dt> </dl>

 

 
