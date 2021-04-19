---
description: Die perfinfo \_ DShow \_ audiobreak-Struktur enthält Daten für ein Ablauf Verfolgungs Ereignis vom Typ GUID \_ audiobreak. Der DirectSound-rendererfilter protokolliert dieses Ereignis, wenn im Audiodatenstrom eine Unterbrechung vorliegt.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: PERFINFO_DSHOW_AUDIOBREAK-Struktur (perfstruct. h)
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
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370792"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>Perfinfo \_ DShow \_ audiobreak-Struktur

Die `PERFINFO_DSHOW_AUDIOBREAK` Struktur enthält Daten für ein Ablauf Verfolgungs Ereignis vom Typ GUID \_ audiobreak.

Der [DirectSound](directsound-renderer-filter.md) -rendererfilter protokolliert dieses Ereignis, wenn im Audiodatenstrom eine Unterbrechung vorliegt.

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

**CycleCounter**
</dt> <dd>

Letzte Anzahl von Uhrzyklen (RDTSC-Anweisung).

</dd> <dt>

**dshowclock**
</dt> <dd>

Aktuelle Schreibposition im DirectSound-Puffer.

</dd> <dt>

**sampletime**
</dt> <dd>

Start der audiopause im DirectSound-Puffer.

</dd> <dt>

**sampleduration**
</dt> <dd>

Dauer der Unterbrechung in Millisekunden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um dieses Ereignis zu aktivieren, müssen Sie beim \_ Aufrufen von **EnableTrace** das audiobreak-Bitflag im *EnableFlag* -Parameter festlegen. Dieses Flag ist in der Header Datei dxmperf. h definiert, die in den DirectShow-Basisklassen enthalten ist.

Um dieses Ereignis von einem DirectShow-Filter zu protokollieren, verwenden Sie das **Perflog \_ audiobreak** -Makro, das in "dxmperf. h" definiert ist.

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

 

 




