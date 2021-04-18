---
description: 'Die Cancel-Methode bricht eine zuvor in die Warteschlange eingereihte cdeferredcommand:: Aufrufen-Anforderung ab.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Cdeferredcommand. Cancel-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364475"
---
# <a name="cdeferredcommandcancel-method"></a><span data-ttu-id="d2886-103">Cdeferredcommand. Cancel-Methode</span><span class="sxs-lookup"><span data-stu-id="d2886-103">CDeferredCommand.Cancel method</span></span>

<span data-ttu-id="d2886-104">Die- `Cancel` Methode bricht eine zuvor in die Warteschlange eingereihte [**cdeferredcommand:: Aufrufen**](cdeferredcommand-invoke.md) -Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="d2886-104">The `Cancel` method cancels a previously queued [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2886-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2886-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="d2886-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2886-106">Parameters</span></span>

<span data-ttu-id="d2886-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d2886-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2886-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2886-108">Return value</span></span>

<span data-ttu-id="d2886-109">Gibt VFW E zurück, die \_ \_ bereits \_ abgebrochen wurde, wenn **m \_ pqueue** **null** ist.</span><span class="sxs-lookup"><span data-stu-id="d2886-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="d2886-110">Gibt ein **HRESULT** aus [**ccmdqueue:: Remove**](ccmdqueue-remove.md) zurück, wenn der-Befehl einen Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="d2886-110">Returns an **HRESULT** from [**CCmdQueue::Remove**](ccmdqueue-remove.md) if the call generates an error.</span></span> <span data-ttu-id="d2886-111">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="d2886-111">Returns S\_OK if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2886-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2886-112">Remarks</span></span>

<span data-ttu-id="d2886-113">Diese Member-Funktion implementiert die [**ideferredcommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d2886-113">This member function implements the [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2886-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2886-114">Requirements</span></span>



| <span data-ttu-id="d2886-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2886-115">Requirement</span></span> | <span data-ttu-id="d2886-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d2886-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2886-117">Header</span><span class="sxs-lookup"><span data-stu-id="d2886-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d2886-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2886-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2886-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2886-119">Library</span></span><br/> | <dl> <span data-ttu-id="d2886-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d2886-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2886-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2886-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2886-122">**Cdeferredcommand-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d2886-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




