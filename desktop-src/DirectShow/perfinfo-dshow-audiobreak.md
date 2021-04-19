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
# <a name="perfinfo_dshow_audiobreak-structure"></a><span data-ttu-id="41de3-103">Perfinfo \_ DShow \_ audiobreak-Struktur</span><span class="sxs-lookup"><span data-stu-id="41de3-103">PERFINFO\_DSHOW\_AUDIOBREAK structure</span></span>

<span data-ttu-id="41de3-104">Die `PERFINFO_DSHOW_AUDIOBREAK` Struktur enthält Daten für ein Ablauf Verfolgungs Ereignis vom Typ GUID \_ audiobreak.</span><span class="sxs-lookup"><span data-stu-id="41de3-104">The `PERFINFO_DSHOW_AUDIOBREAK` structure contains data for a trace event of type GUID\_AUDIOBREAK.</span></span>

<span data-ttu-id="41de3-105">Der [DirectSound](directsound-renderer-filter.md) -rendererfilter protokolliert dieses Ereignis, wenn im Audiodatenstrom eine Unterbrechung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="41de3-105">The [DirectSound Renderer](directsound-renderer-filter.md) filter logs this event when there is a break in the audio stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="41de3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="41de3-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a><span data-ttu-id="41de3-107">Member</span><span class="sxs-lookup"><span data-stu-id="41de3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="41de3-108">**CycleCounter**</span><span class="sxs-lookup"><span data-stu-id="41de3-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="41de3-109">Letzte Anzahl von Uhrzyklen (RDTSC-Anweisung).</span><span class="sxs-lookup"><span data-stu-id="41de3-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="41de3-110">**dshowclock**</span><span class="sxs-lookup"><span data-stu-id="41de3-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="41de3-111">Aktuelle Schreibposition im DirectSound-Puffer.</span><span class="sxs-lookup"><span data-stu-id="41de3-111">Current write position in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="41de3-112">**sampletime**</span><span class="sxs-lookup"><span data-stu-id="41de3-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="41de3-113">Start der audiopause im DirectSound-Puffer.</span><span class="sxs-lookup"><span data-stu-id="41de3-113">Start of the audio break in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="41de3-114">**sampleduration**</span><span class="sxs-lookup"><span data-stu-id="41de3-114">**sampleDuration**</span></span>
</dt> <dd>

<span data-ttu-id="41de3-115">Dauer der Unterbrechung in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="41de3-115">Duration of the break, in milliseconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41de3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41de3-116">Remarks</span></span>

<span data-ttu-id="41de3-117">Um dieses Ereignis zu aktivieren, müssen Sie beim \_ Aufrufen von **EnableTrace** das audiobreak-Bitflag im *EnableFlag* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="41de3-117">To enable this event, you must set the AUDIOBREAK\_BIT flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="41de3-118">Dieses Flag ist in der Header Datei dxmperf. h definiert, die in den DirectShow-Basisklassen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="41de3-118">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="41de3-119">Um dieses Ereignis von einem DirectShow-Filter zu protokollieren, verwenden Sie das **Perflog \_ audiobreak** -Makro, das in "dxmperf. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="41de3-119">To log this event from a DirectShow filter, use the **PERFLOG\_AUDIOBREAK** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="41de3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41de3-120">Requirements</span></span>



| <span data-ttu-id="41de3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41de3-121">Requirement</span></span> | <span data-ttu-id="41de3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="41de3-122">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41de3-123">Header</span><span class="sxs-lookup"><span data-stu-id="41de3-123">Header</span></span><br/> | <dl> <span data-ttu-id="41de3-124"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="41de3-124"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41de3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41de3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41de3-126">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="41de3-126">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="41de3-127">Ereignis Ablauf Verfolgung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="41de3-127">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="41de3-128">GUIDs der Ablauf Verfolgungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="41de3-128">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




