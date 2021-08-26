---
description: Die PERFINFO \_ DSHOW \_ AUDIOBREAK-Struktur enthält Daten für ein Ablaufverfolgungsereignis vom Typ GUID \_ AUDIOBREAK. Der Filter DirectSound Renderer protokolliert dieses Ereignis, wenn im Audiostream eine Unterbrechung vorliegt.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: PERFINFO_DSHOW_AUDIOBREAK-Struktur (Perfstruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: c7b8f83fffaa718c27e0333d864a564282228c0943f4d77fb653dc1800a6ddd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928190"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>PERFINFO \_ DSHOW \_ AUDIOBREAK-Struktur

Die `PERFINFO_DSHOW_AUDIOBREAK` -Struktur enthält Daten für ein Ablaufverfolgungsereignis vom Typ GUID \_ AUDIOBREAK.

Der [Filter DirectSound Renderer](directsound-renderer-filter.md) protokolliert dieses Ereignis, wenn im Audiostream eine Unterbrechung vorliegt.

## <a name="syntax"></a>Syntax


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>Member

<dl> <dt>

**cycleCounter**
</dt> <dd>

Aktuelle Taktzyklusanzahl (RDTSC-Anweisung).

</dd> <dt>

**dshowClock**
</dt> <dd>

Aktuelle Schreibposition im DirectSound-Puffer.

</dd> <dt>

**sampleTime**
</dt> <dd>

Beginn der Audiounterbrechung im DirectSound-Puffer.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Dauer der Unterbrechung in Millisekunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um dieses Ereignis zu aktivieren, müssen Sie das AUDIOBREAK \_ BIT-Flag im *EnableFlag-Parameter* festlegen, wenn Sie **EnableTrace** aufrufen. Dieses Flag wird in der Headerdatei Dxmperf.h definiert, die in den DirectShow-Basisklassen enthalten ist.

Um dieses Ereignis aus einem DirectShow-Filter zu protokollieren, verwenden Sie das **PERFLOG \_ AUDIOBREAK-Makro,** das in Dxmperf.h definiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Perfstruct.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[Ereignisablaufverfolgung in DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUIDs für Ablaufverfolgungsereignisse](trace-guids.md)
</dt> </dl>

 

 




