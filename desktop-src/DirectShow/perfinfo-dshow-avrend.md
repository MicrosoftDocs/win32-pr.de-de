---
description: Die PERFINFO \_ \_ DSHOW-A ADRND-Struktur enthält Daten für ein Ablaufverfolgungsereignis vom Typ GUID \_ VIDEOREND. Die VMR protokolliert dieses Ereignis unmittelbar vor dem Rendern eines Frames.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: PERFINFO_DSHOW_AVREND-Struktur (Perfstruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 49cc76f4db1a5fae76678ee2d81f3e2fff0a6c5ca3d5c5532adebaec23f48215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050710"
---
# <a name="perfinfo_dshow_avrend-structure"></a>PERFINFO \_ \_ DSHOW-AMILLND-Struktur

Die `PERFINFO_DSHOW_AVREND` -Struktur enthält Daten für ein Ablaufverfolgungsereignis vom Typ GUID \_ VIDEOREND.

Die VMR protokolliert dieses Ereignis unmittelbar vor dem Rendern eines Frames.

## <a name="syntax"></a>Syntax


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a>Member

<dl> <dt>

**cycleCounter**
</dt> <dd>

Aktuelle Taktzyklusanzahl (RDTSC-Anweisung).

</dd> <dt>

**dshowClock**
</dt> <dd>

Aktuelle Referenzzeit, wie von der [**IReferenceClock::GetTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) zurückgegeben.

</dd> <dt>

**sampleTime**
</dt> <dd>

Startzeit des Beispiels.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um dieses Ereignis zu aktivieren, müssen Sie das DXMPERF \_ VIDEOREND-Flag im *EnableFlag-Parameter* festlegen, wenn Sie **EnableTrace** aufrufen. Dieses Flag wird in der Headerdatei Dxmperf.h definiert, die in den DirectShow-Basisklassen enthalten ist.

Um dieses Ereignis aus einem DirectShow-Filter zu protokollieren, verwenden Sie das **PERFLOG \_ VIDEOREND-Makro,** das in Dxmperf.h definiert ist.

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

 

 




