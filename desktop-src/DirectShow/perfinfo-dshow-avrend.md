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
# <a name="perfinfo_dshow_avrend-structure"></a><span data-ttu-id="4df39-103">Perfinfo \_ DShow- \_ avrend-Struktur</span><span class="sxs-lookup"><span data-stu-id="4df39-103">PERFINFO\_DSHOW\_AVREND structure</span></span>

<span data-ttu-id="4df39-104">Die `PERFINFO_DSHOW_AVREND` Struktur enthält Daten für ein Ablauf Verfolgungs Ereignis vom Typ GUID \_ videorend.</span><span class="sxs-lookup"><span data-stu-id="4df39-104">The `PERFINFO_DSHOW_AVREND` structure contains data for a trace event of type GUID\_VIDEOREND.</span></span>

<span data-ttu-id="4df39-105">VMR protokolliert dieses Ereignis unmittelbar vor dem Rendern eines Frames.</span><span class="sxs-lookup"><span data-stu-id="4df39-105">The VMR logs this event immediately before rendering a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df39-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4df39-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a><span data-ttu-id="4df39-107">Member</span><span class="sxs-lookup"><span data-stu-id="4df39-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4df39-108">**CycleCounter**</span><span class="sxs-lookup"><span data-stu-id="4df39-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="4df39-109">Letzte Anzahl von Uhrzyklen (RDTSC-Anweisung).</span><span class="sxs-lookup"><span data-stu-id="4df39-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="4df39-110">**dshowclock**</span><span class="sxs-lookup"><span data-stu-id="4df39-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="4df39-111">Aktuelle Verweis Zeit, wie von der [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4df39-111">Current reference time, as returned by the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

</dd> <dt>

<span data-ttu-id="4df39-112">**sampletime**</span><span class="sxs-lookup"><span data-stu-id="4df39-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="4df39-113">Die Startzeit des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="4df39-113">Start time of the sample.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4df39-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4df39-114">Remarks</span></span>

<span data-ttu-id="4df39-115">Um dieses Ereignis zu aktivieren, müssen Sie beim Aufrufen von EnableTrace das Flag "dxmperf \_ videorend" im  *EnableFlag* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="4df39-115">To enable this event, you must set the DXMPERF\_VIDEOREND flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="4df39-116">Dieses Flag ist in der Header Datei dxmperf. h definiert, die in den DirectShow-Basisklassen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4df39-116">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="4df39-117">Um dieses Ereignis von einem DirectShow-Filter zu protokollieren, verwenden Sie das **Perflog \_ videorend** -Makro, das in "dxmperf. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4df39-117">To log this event from a DirectShow filter, use the **PERFLOG\_VIDEOREND** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df39-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4df39-118">Requirements</span></span>



| <span data-ttu-id="4df39-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4df39-119">Requirement</span></span> | <span data-ttu-id="4df39-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4df39-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df39-121">Header</span><span class="sxs-lookup"><span data-stu-id="4df39-121">Header</span></span><br/> | <dl> <span data-ttu-id="4df39-122"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df39-122"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df39-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4df39-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df39-124">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4df39-124">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="4df39-125">Ereignis Ablauf Verfolgung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4df39-125">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="4df39-126">GUIDs der Ablauf Verfolgungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="4df39-126">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




