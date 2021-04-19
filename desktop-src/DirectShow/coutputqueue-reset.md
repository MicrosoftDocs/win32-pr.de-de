---
description: Die Reset-Methode setzt das-Objekt zurück, sodass mehr Daten empfangen werden können.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Coutputqueue. Reset-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356324"
---
# <a name="coutputqueuereset-method"></a><span data-ttu-id="b58e8-103">Coutputqueue. Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="b58e8-103">COutputQueue.Reset method</span></span>

<span data-ttu-id="b58e8-104">Die- `Reset` Methode setzt das-Objekt zurück, sodass mehr Daten empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="b58e8-104">The `Reset` method resets the object so that it can receive more data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b58e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b58e8-105">Syntax</span></span>


```C++
void Reset();
```



## <a name="parameters"></a><span data-ttu-id="b58e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b58e8-106">Parameters</span></span>

<span data-ttu-id="b58e8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b58e8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b58e8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b58e8-108">Return value</span></span>

<span data-ttu-id="b58e8-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b58e8-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b58e8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b58e8-110">Remarks</span></span>

<span data-ttu-id="b58e8-111">Diese Methode setzt die Element Variable [**coutputqueue:: m \_ HR**](coutputqueue-m-hr.md) auf S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b58e8-111">This method resets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_OK.</span></span> <span data-ttu-id="b58e8-112">Das Objekt kann erneut Medien Beispiele empfangen. beispielsweise nach einem Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="b58e8-112">The object can receive media samples again; for example, after a flush operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b58e8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b58e8-113">Requirements</span></span>



| <span data-ttu-id="b58e8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b58e8-114">Requirement</span></span> | <span data-ttu-id="b58e8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b58e8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58e8-116">Header</span><span class="sxs-lookup"><span data-stu-id="b58e8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b58e8-117"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b58e8-117"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b58e8-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b58e8-118">Library</span></span><br/> | <dl> <span data-ttu-id="b58e8-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b58e8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b58e8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b58e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58e8-121">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b58e8-121">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




