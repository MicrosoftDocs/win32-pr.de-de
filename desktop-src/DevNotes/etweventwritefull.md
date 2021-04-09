---
description: Schreibt ein vollständiges Ereignis in eine Sitzung.
title: Etweventschreitefull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958491"
---
# <a name="etweventwritefull-function"></a><span data-ttu-id="51a5b-103">Etweventschreitefull-Funktion</span><span class="sxs-lookup"><span data-stu-id="51a5b-103">EtwEventWriteFull function</span></span>

<span data-ttu-id="51a5b-104">[Die etweventwrite tefull-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.]</span><span class="sxs-lookup"><span data-stu-id="51a5b-104">[The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="51a5b-105">Schreibt ein vollständiges Ereignis in eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="51a5b-105">Writes a full event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a5b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="51a5b-106">Syntax</span></span>

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="51a5b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51a5b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51a5b-108">*Reghandle*</span><span class="sxs-lookup"><span data-stu-id="51a5b-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="51a5b-109">Reghandle für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="51a5b-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="51a5b-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="51a5b-110">*EventDescriptor*</span></span> 
</dt> <dd>

<span data-ttu-id="51a5b-111">Der Ereignis Deskriptor des Ereignisses, das protokolliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="51a5b-111">Event Descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="51a5b-112">*EventProperty*</span><span class="sxs-lookup"><span data-stu-id="51a5b-112">*EventProperty*</span></span>
</dt> <dd>

<span data-ttu-id="51a5b-113">Das Flag, das vom Benutzer angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="51a5b-113">Flag given by the user.</span></span>

</dd> <dt>

<span data-ttu-id="51a5b-114">*ActivityId*</span><span class="sxs-lookup"><span data-stu-id="51a5b-114">*ActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="51a5b-115">Aktivitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="51a5b-115">Activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="51a5b-116">*RelatedActivityId*</span><span class="sxs-lookup"><span data-stu-id="51a5b-116">*RelatedActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="51a5b-117">Zugehörige Aktivitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="51a5b-117">Related activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="51a5b-118">*Userdatacount*</span><span class="sxs-lookup"><span data-stu-id="51a5b-118">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="51a5b-119">Die Anzahl der Benutzerdaten Elemente.</span><span class="sxs-lookup"><span data-stu-id="51a5b-119">The number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="51a5b-120">*UserData*</span><span class="sxs-lookup"><span data-stu-id="51a5b-120">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="51a5b-121">Zeiger auf ein Array von Benutzerdaten Elementen.</span><span class="sxs-lookup"><span data-stu-id="51a5b-121">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51a5b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51a5b-122">Return value</span></span>

<span data-ttu-id="51a5b-123">Ein Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="51a5b-123">A Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a5b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51a5b-124">Remarks</span></span>

<span data-ttu-id="51a5b-125">Die etweventwrite tefull-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.</span><span class="sxs-lookup"><span data-stu-id="51a5b-125">The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="51a5b-126">Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="51a5b-126">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>


## <a name="requirements"></a><span data-ttu-id="51a5b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51a5b-127">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="51a5b-128">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="51a5b-128">**Target Platform**</span></span> | <span data-ttu-id="51a5b-129">Windows</span><span class="sxs-lookup"><span data-stu-id="51a5b-129">Windows</span></span> |
| <span data-ttu-id="51a5b-130">**Header**</span><span class="sxs-lookup"><span data-stu-id="51a5b-130">**Header**</span></span> | <span data-ttu-id="51a5b-131">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="51a5b-131">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="51a5b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51a5b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a5b-133">EventWrite</span><span class="sxs-lookup"><span data-stu-id="51a5b-133">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="51a5b-134">EventWrite-Ex</span><span class="sxs-lookup"><span data-stu-id="51a5b-134">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
