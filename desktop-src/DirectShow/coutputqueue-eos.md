---
description: Die EOS-Methode übermittelt einen streamingdatenstrom für den eingabepin.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Coutputqueue. EOS-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365529"
---
# <a name="coutputqueueeos-method"></a><span data-ttu-id="230ad-103">Coutputqueue. EOS-Methode</span><span class="sxs-lookup"><span data-stu-id="230ad-103">COutputQueue.EOS method</span></span>

<span data-ttu-id="230ad-104">Die- `EOS` Methode stellt einen End-of-Stream-Rückruf für die Eingabe-PIN bereit.</span><span class="sxs-lookup"><span data-stu-id="230ad-104">The `EOS` method delivers an end-of-stream call to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="230ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="230ad-105">Syntax</span></span>


```C++
void EOS();
```



## <a name="parameters"></a><span data-ttu-id="230ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="230ad-106">Parameters</span></span>

<span data-ttu-id="230ad-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="230ad-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="230ad-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="230ad-108">Return value</span></span>

<span data-ttu-id="230ad-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="230ad-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="230ad-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="230ad-110">Remarks</span></span>

<span data-ttu-id="230ad-111">Wenn das Objekt einen Thread verwendet, wird eine EOS-Paket Steuerungs Meldung in die Warteschlange eingereiht \_ .</span><span class="sxs-lookup"><span data-stu-id="230ad-111">If the object is using a thread, it queues an EOS\_PACKET control message.</span></span> <span data-ttu-id="230ad-112">Der Thread liefert alle ausstehenden Beispiele und ruft die [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="230ad-112">The thread delivers any pending samples and calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

<span data-ttu-id="230ad-113">Wenn das Objekt keinen Thread verwendet, ruft es die [**coutputqueue:: sendanyway**](coutputqueue-sendanyway.md) -Methode auf, um alle ausstehenden Beispiele bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="230ad-113">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="230ad-114">Anschließend wird **IPin:: EndOf Stream** für die Eingabe-PIN aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="230ad-114">Then it calls **IPin::EndOfStream** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="230ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="230ad-115">Requirements</span></span>



| <span data-ttu-id="230ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="230ad-116">Requirement</span></span> | <span data-ttu-id="230ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="230ad-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="230ad-118">Header</span><span class="sxs-lookup"><span data-stu-id="230ad-118">Header</span></span><br/>  | <dl> <span data-ttu-id="230ad-119"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="230ad-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="230ad-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="230ad-120">Library</span></span><br/> | <dl> <span data-ttu-id="230ad-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="230ad-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="230ad-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="230ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230ad-123">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="230ad-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




