---
description: Die getcommandduefor-Methode ruft einen verzögerten Befehl ab, der zu einem bestimmten Zeitpunkt geplant wird.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Ccmdqueue. getcommandduefor-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350770"
---
# <a name="ccmdqueuegetcommandduefor-method"></a><span data-ttu-id="69874-103">Ccmdqueue. getcommandduefor-Methode</span><span class="sxs-lookup"><span data-stu-id="69874-103">CCmdQueue.GetCommandDueFor method</span></span>

<span data-ttu-id="69874-104">Die- `GetCommandDueFor` Methode ruft einen verzögerten Befehl ab, der zu einem bestimmten Zeitpunkt geplant wird.</span><span class="sxs-lookup"><span data-stu-id="69874-104">The `GetCommandDueFor` method retrieves a deferred command that is scheduled at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="69874-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69874-105">Syntax</span></span>


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="69874-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69874-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69874-107">*tstream*</span><span class="sxs-lookup"><span data-stu-id="69874-107">*tStream*</span></span> 
</dt> <dd>

<span data-ttu-id="69874-108">Der Zeitpunkt, zu dem der Befehl geplant ist.</span><span class="sxs-lookup"><span data-stu-id="69874-108">Time for which the command is scheduled.</span></span>

</dd> <dt>

<span data-ttu-id="69874-109">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="69874-109">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="69874-110">Adresse eines Zeigers auf den verzögerten Befehl, der zu dem im *tstream* -Parameter angegebenen Zeitpunkt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="69874-110">Address of a pointer to the deferred command to be carried out at the time specified in the *tStream* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69874-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69874-111">Return value</span></span>

<span data-ttu-id="69874-112">Gibt VFW \_ E \_ nicht \_ gefunden zurück, wenn keine Befehle fällig sind; andernfalls gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="69874-112">Returns VFW\_E\_NOT\_FOUND if no commands are due; otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="69874-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69874-113">Remarks</span></span>

<span data-ttu-id="69874-114">Diese Member-Funktion nimmt eine streamzeit an und gibt den verzögerten Befehl zurück, der zu diesem Zeitpunkt geplant ist.</span><span class="sxs-lookup"><span data-stu-id="69874-114">This member function takes a stream time and returns the deferred command scheduled at that time.</span></span> <span data-ttu-id="69874-115">Der tatsächliche Offset der streamzeit wird berechnet, wenn die Befehls Warteschlange ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69874-115">The actual stream-time offset is calculated when the command queue is run.</span></span> <span data-ttu-id="69874-116">Befehle bleiben bis zum Ausführen oder Abbrechen in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="69874-116">Commands remain queued until run or canceled.</span></span> <span data-ttu-id="69874-117">Diese Member-Funktion wird nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="69874-117">This member function will not block.</span></span>

## <a name="requirements"></a><span data-ttu-id="69874-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69874-118">Requirements</span></span>



| <span data-ttu-id="69874-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69874-119">Requirement</span></span> | <span data-ttu-id="69874-120">Wert</span><span class="sxs-lookup"><span data-stu-id="69874-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69874-121">Header</span><span class="sxs-lookup"><span data-stu-id="69874-121">Header</span></span><br/>  | <dl> <span data-ttu-id="69874-122"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69874-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="69874-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="69874-123">Library</span></span><br/> | <dl> <span data-ttu-id="69874-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="69874-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69874-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69874-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69874-126">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="69874-126">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




