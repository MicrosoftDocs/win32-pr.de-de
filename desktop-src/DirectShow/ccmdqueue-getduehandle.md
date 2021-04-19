---
description: Die getduehandle-Methode ruft das Ereignis Handle ab, das signalisiert werden soll.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Ccmdqueue. getduehandle-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350769"
---
# <a name="ccmdqueuegetduehandle-method"></a><span data-ttu-id="ce273-103">Ccmdqueue. getduehandle-Methode</span><span class="sxs-lookup"><span data-stu-id="ce273-103">CCmdQueue.GetDueHandle method</span></span>

<span data-ttu-id="ce273-104">Die- `GetDueHandle` Methode ruft das Ereignis Handle ab, das signalisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce273-104">The `GetDueHandle` method retrieves the event handle to be signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce273-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce273-105">Syntax</span></span>


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a><span data-ttu-id="ce273-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce273-106">Parameters</span></span>

<span data-ttu-id="ce273-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ce273-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce273-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce273-108">Return value</span></span>

<span data-ttu-id="ce273-109">Gibt das Ereignis Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="ce273-109">Returns the event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce273-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce273-110">Remarks</span></span>

<span data-ttu-id="ce273-111">Gibt das Ereignis Handle zurück, wenn verzögerte Befehle vorhanden sind, die für die Ausführung fällig sind (wenn [**ccmdqueue:: getduecommand**](ccmdqueue-getduecommand.md) nicht blockiert wird).</span><span class="sxs-lookup"><span data-stu-id="ce273-111">Return the event handle whenever there are deferred commands that are due for execution (when [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) will not block).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce273-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce273-112">Requirements</span></span>



| <span data-ttu-id="ce273-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce273-113">Requirement</span></span> | <span data-ttu-id="ce273-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ce273-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce273-115">Header</span><span class="sxs-lookup"><span data-stu-id="ce273-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ce273-116"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce273-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce273-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce273-117">Library</span></span><br/> | <dl> <span data-ttu-id="ce273-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce273-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce273-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce273-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce273-120">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ce273-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




