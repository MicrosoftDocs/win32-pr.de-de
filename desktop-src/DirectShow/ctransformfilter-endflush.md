---
description: 'CTransformFilter.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang.'
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: CTransformFilter.EndFlush-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085059"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="eb1b3-103">CTransformFilter.EndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="eb1b3-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="eb1b3-104">Die `EndFlush` -Methode beendet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="eb1b3-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb1b3-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="eb1b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb1b3-106">Parameters</span></span>

<span data-ttu-id="eb1b3-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eb1b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb1b3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb1b3-108">Return value</span></span>

<span data-ttu-id="eb1b3-109">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="eb1b3-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1b3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb1b3-110">Remarks</span></span>

<span data-ttu-id="eb1b3-111">Am Ende eines Leerungsvorgang ruft die [**CTransformInputPin::EndFlush-Methode**](ctransforminputpin-endflush.md) des Eingabepins diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="eb1b3-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="eb1b3-112">Diese Methode übergibt den `EndFlush` Aufruf downstream.</span><span class="sxs-lookup"><span data-stu-id="eb1b3-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="eb1b3-113">Wenn die abgeleitete Klasse einen Arbeitsthread zum Senden von Beispielen verwendet, muss sie alle Daten in der Warteschlange verwerfen, bevor der Aufruf `EndFlush` nachgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="eb1b3-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="eb1b3-114">Weitere Informationen finden Sie unter [Datenfluss für Filterentwickler.](data-flow-for-filter-developers.md)</span><span class="sxs-lookup"><span data-stu-id="eb1b3-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1b3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb1b3-115">Requirements</span></span>



| <span data-ttu-id="eb1b3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb1b3-116">Requirement</span></span> | <span data-ttu-id="eb1b3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="eb1b3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1b3-118">Header</span><span class="sxs-lookup"><span data-stu-id="eb1b3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="eb1b3-119"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="eb1b3-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb1b3-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb1b3-120">Library</span></span><br/> | <dl> <span data-ttu-id="eb1b3-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eb1b3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb1b3-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb1b3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1b3-123">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb1b3-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




