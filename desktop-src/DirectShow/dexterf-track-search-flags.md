---
description: Die dexterf \_ - \_ \_ Suchflags-Enumeration gibt die begrenzungsbedingungen bei einer Suche nach einem Objekt in der Zeitachse an.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: DEXTERF_TRACK_SEARCH_FLAGS-Enumeration (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365699"
---
# <a name="dexterf_track_search_flags-enumeration"></a><span data-ttu-id="0e076-103">Dexterf \_ - \_ \_ Suchflags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0e076-103">DEXTERF\_TRACK\_SEARCH\_FLAGS enumeration</span></span>

> [!Note]  
> <span data-ttu-id="0e076-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0e076-104">\[Deprecated.</span></span> <span data-ttu-id="0e076-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="0e076-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e076-106">Die- `DEXTERF_TRACK_SEARCH_FLAGS` Enumeration gibt die begrenzungsbedingungen bei einer Suche nach einem Objekt in der Zeitachse an.</span><span class="sxs-lookup"><span data-stu-id="0e076-106">The `DEXTERF_TRACK_SEARCH_FLAGS` enumeration specifies the boundary conditions on a search for an object in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e076-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e076-107">Syntax</span></span>


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="0e076-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0e076-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0e076-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**dexterf- \_ Begrenzungs Zeichen**</span><span class="sxs-lookup"><span data-stu-id="0e076-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF\_BOUNDING**</span></span>
</dt> <dd>

<span data-ttu-id="0e076-110">Sucht nach einem Objekt, das die angegebene Zeitspanne überspannt.</span><span class="sxs-lookup"><span data-stu-id="0e076-110">Search for an object that spans the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="0e076-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**dexterf \_ genau \_ um**</span><span class="sxs-lookup"><span data-stu-id="0e076-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF\_EXACTLY\_AT**</span></span>
</dt> <dd>

<span data-ttu-id="0e076-112">Suchen Sie nach einem Objekt, das genau zum angegebenen Zeitpunkt gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0e076-112">Search for an object that starts exactly at the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="0e076-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**dexterf \_ weiterleiten**</span><span class="sxs-lookup"><span data-stu-id="0e076-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF\_FORWARDS**</span></span>
</dt> <dd>

<span data-ttu-id="0e076-114">Suchen Sie nach einem Objekt, das zum angegebenen Zeitpunkt oder später gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0e076-114">Search for an object that starts at the specified time or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e076-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e076-115">Remarks</span></span>

<span data-ttu-id="0e076-116">Diese begrenzungsbedingungen werden in der folgenden Tabelle zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="0e076-116">These boundary conditions are summarized in the following table.</span></span>



| <span data-ttu-id="0e076-117">Enumerationswert</span><span class="sxs-lookup"><span data-stu-id="0e076-117">Enumeration value</span></span>    | <span data-ttu-id="0e076-118">Begrenzungs Bedingung</span><span class="sxs-lookup"><span data-stu-id="0e076-118">Boundary condition</span></span>                        |
|----------------------|-------------------------------------------|
| <span data-ttu-id="0e076-119">dexterf- \_ Begrenzungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="0e076-119">DEXTERF\_BOUNDING</span></span>    | <span data-ttu-id="0e076-120">Start <= timestoppt > Zeit</span><span class="sxs-lookup"><span data-stu-id="0e076-120">Start <= TimeStop > Time</span></span><br/> |
| <span data-ttu-id="0e076-121">dexterf \_ genau \_ um</span><span class="sxs-lookup"><span data-stu-id="0e076-121">DEXTERF\_EXACTLY\_AT</span></span> | <span data-ttu-id="0e076-122">Start = = Zeit</span><span class="sxs-lookup"><span data-stu-id="0e076-122">Start == Time</span></span>                             |
| <span data-ttu-id="0e076-123">dexterf \_ weiterleiten</span><span class="sxs-lookup"><span data-stu-id="0e076-123">DEXTERF\_FORWARDS</span></span>    | <span data-ttu-id="0e076-124">Start >= Zeit</span><span class="sxs-lookup"><span data-stu-id="0e076-124">Start >= Time</span></span>                          |



 

-   <span data-ttu-id="0e076-125">Start: Startzeit des abgerufenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="0e076-125">Start: start time of the retrieved object.</span></span>
-   <span data-ttu-id="0e076-126">Beendigung: die Endzeit des abgerufenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="0e076-126">Stop: stop time of the retrieved object.</span></span>
-   <span data-ttu-id="0e076-127">Time: angegebene Suchzeit.</span><span class="sxs-lookup"><span data-stu-id="0e076-127">Time: specified search time.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e076-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e076-128">Requirements</span></span>



| <span data-ttu-id="0e076-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e076-129">Requirement</span></span> | <span data-ttu-id="0e076-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0e076-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e076-131">Header</span><span class="sxs-lookup"><span data-stu-id="0e076-131">Header</span></span><br/> | <dl> <span data-ttu-id="0e076-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0e076-132"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e076-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e076-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e076-134">**Iamtimelinetrack:: gezr| Time**</span><span class="sxs-lookup"><span data-stu-id="0e076-134">**IAMTimelineTrack::GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




