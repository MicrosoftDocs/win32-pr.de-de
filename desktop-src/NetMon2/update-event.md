---
description: Die Update- \_ Ereignis Struktur aktualisiert Ereignisse. Diese Struktur wird über die Ereignis Status-Rückruf Prozedur vom NPP an die aufrufenden Anwendung zurückgegeben.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: UPDATE_EVENT Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348328"
---
# <a name="update_event-structure"></a><span data-ttu-id="6abe0-104">Aktualisieren der \_ Ereignis Struktur</span><span class="sxs-lookup"><span data-stu-id="6abe0-104">UPDATE\_EVENT structure</span></span>

<span data-ttu-id="6abe0-105">Die **Update- \_ Ereignis** Struktur aktualisiert Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6abe0-105">The **UPDATE\_EVENT** structure updates events.</span></span> <span data-ttu-id="6abe0-106">Diese Struktur wird über die Ereignis Status-Rückruf Prozedur vom NPP an die aufrufenden Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6abe0-106">This structure is passed back to the calling application via the event status callback procedure by the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abe0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6abe0-107">Syntax</span></span>


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a><span data-ttu-id="6abe0-108">Member</span><span class="sxs-lookup"><span data-stu-id="6abe0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6abe0-109">**Event**</span><span class="sxs-lookup"><span data-stu-id="6abe0-109">**Event**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-110">Tatsächliches Ereignis, das aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6abe0-110">Actual event being recorded.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-111">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="6abe0-111">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-112">Die ausgeführte Aktion.</span><span class="sxs-lookup"><span data-stu-id="6abe0-112">The action taken.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-113">**Status**</span><span class="sxs-lookup"><span data-stu-id="6abe0-113">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-114">Netzwerkstatus Anzeige.</span><span class="sxs-lookup"><span data-stu-id="6abe0-114">Network status indication.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6abe0-115">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-116">Zusätzliche Counter-Variable.</span><span class="sxs-lookup"><span data-stu-id="6abe0-116">Auxiliary counter variable.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-117">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="6abe0-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-118">Die markierten Ereignisse in Mikrosekunden.</span><span class="sxs-lookup"><span data-stu-id="6abe0-118">The marked events, in microseconds.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-119">**lpusercontext**</span><span class="sxs-lookup"><span data-stu-id="6abe0-119">**lpUserContext**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-120">Der Benutzer Kontext, der von der Anwendung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6abe0-120">User context given by the application.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-121">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="6abe0-121">**lpReserved**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-122">Treiber-oder nal-Verwendung.</span><span class="sxs-lookup"><span data-stu-id="6abe0-122">Driver or NAL use.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-123">**Framesdrop**</span><span class="sxs-lookup"><span data-stu-id="6abe0-123">**FramesDropped**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-124">RTF-Frames wurden im angegebenen Puffer abgelegt.</span><span class="sxs-lookup"><span data-stu-id="6abe0-124">RTF frames dropped in the specified buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="6abe0-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-126">Diese Switch-Option gibt keine Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="6abe0-126">No data comes back with this switch option.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-127">**lpframetable**</span><span class="sxs-lookup"><span data-stu-id="6abe0-127">**lpFrameTable**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-128">Nur RTF.</span><span class="sxs-lookup"><span data-stu-id="6abe0-128">RTF only.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-129">**lppacketqueue**</span><span class="sxs-lookup"><span data-stu-id="6abe0-129">**lpPacketQueue**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-130">Für überträgt.</span><span class="sxs-lookup"><span data-stu-id="6abe0-130">For transmits.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-131">**Securityresponse**</span><span class="sxs-lookup"><span data-stu-id="6abe0-131">**SecurityResponse**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-132">Antwort des Remote Sicherheits Monitors.</span><span class="sxs-lookup"><span data-stu-id="6abe0-132">Remote security monitor response.</span></span>

</dd> <dt>

<span data-ttu-id="6abe0-133">**lpfinalstats**</span><span class="sxs-lookup"><span data-stu-id="6abe0-133">**lpFinalStats**</span></span>
</dt> <dd>

<span data-ttu-id="6abe0-134">Dies wird nur bei nicht sicherheitsbezogenen Stopps (z. b. Triggern) ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6abe0-134">This is only filled in on non-security related stops (for example, triggers).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6abe0-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6abe0-135">Remarks</span></span>

<span data-ttu-id="6abe0-136">C++ Benutzer sollten beachten, dass sich die Deklaration für diesen Rückruf im öffentlichen Teil der Header Datei befinden sollte:</span><span class="sxs-lookup"><span data-stu-id="6abe0-136">C++ users should note that the declaration for this callback should be in the public part of the header file:</span></span>

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

<span data-ttu-id="6abe0-137">Die Implementierung sollte sich im geschützten Abschnitt der CPP-Datei befinden:</span><span class="sxs-lookup"><span data-stu-id="6abe0-137">The implementation should be in the protected section of the .cpp file:</span></span>

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a><span data-ttu-id="6abe0-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6abe0-138">Requirements</span></span>



| <span data-ttu-id="6abe0-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6abe0-139">Requirement</span></span> | <span data-ttu-id="6abe0-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6abe0-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6abe0-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6abe0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6abe0-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6abe0-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6abe0-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6abe0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6abe0-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6abe0-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6abe0-145">Header</span><span class="sxs-lookup"><span data-stu-id="6abe0-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6abe0-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6abe0-146"><dt>Netmon.h</dt></span></span> </dl> |



 

 




