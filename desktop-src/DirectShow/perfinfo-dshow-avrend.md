---
description: Die perfinfo \_ DShow \_ avrend-Struktur enthält Daten für ein Ablauf Verfolgungs Ereignis vom Typ GUID \_ videorend. VMR protokolliert dieses Ereignis unmittelbar vor dem Rendern eines Frames.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: PERFINFO_DSHOW_AVREND-Struktur (perfstruct. h)
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
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372452"
---
# <a name="perfinfo_dshow_avrend-structure"></a>Perfinfo \_ DShow- \_ avrend-Struktur

Die `PERFINFO_DSHOW_AVREND` Struktur enthält Daten für ein Ablauf Verfolgungs Ereignis vom Typ GUID \_ videorend.

VMR protokolliert dieses Ereignis unmittelbar vor dem Rendern eines Frames.

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

**CycleCounter**
</dt> <dd>

Letzte Anzahl von Uhrzyklen (RDTSC-Anweisung).

</dd> <dt>

**dshowclock**
</dt> <dd>

Aktuelle Verweis Zeit, wie von der [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode zurückgegeben.

</dd> <dt>

**sampletime**
</dt> <dd>

Die Startzeit des Beispiels.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um dieses Ereignis zu aktivieren, müssen Sie beim Aufrufen von EnableTrace das Flag "dxmperf \_ videorend" im  *EnableFlag* -Parameter festlegen. Dieses Flag ist in der Header Datei dxmperf. h definiert, die in den DirectShow-Basisklassen enthalten ist.

Um dieses Ereignis von einem DirectShow-Filter zu protokollieren, verwenden Sie das **Perflog \_ videorend** -Makro, das in "dxmperf. h" definiert ist.

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

 

 




