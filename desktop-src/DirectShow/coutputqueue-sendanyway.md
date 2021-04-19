---
description: Die sendanyway-Methode liefert alle ausstehenden Beispiele.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Coutputqueue. sendanyway-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373600"
---
# <a name="coutputqueuesendanyway-method"></a><span data-ttu-id="5e8ef-103">Coutputqueue. sendanyway-Methode</span><span class="sxs-lookup"><span data-stu-id="5e8ef-103">COutputQueue.SendAnyway method</span></span>

<span data-ttu-id="5e8ef-104">Die- `SendAnyway` Methode stellt alle ausstehenden Beispiele bereit.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-104">The `SendAnyway` method delivers any pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e8ef-105">Syntax</span></span>


```C++
void SendAnyway();
```



## <a name="parameters"></a><span data-ttu-id="5e8ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e8ef-106">Parameters</span></span>

<span data-ttu-id="5e8ef-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e8ef-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e8ef-108">Return value</span></span>

<span data-ttu-id="5e8ef-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e8ef-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e8ef-110">Remarks</span></span>

<span data-ttu-id="5e8ef-111">Wenn die Element Variable [**coutputqueue:: m \_ bbatchexact**](coutputqueue-m-bbatchexact.md) den Wert **true** hat, füllt das Objekt das [**coutputqueue:: m \_ ppsamples**](coutputqueue-m-ppsamples.md) -Array aus, bevor es einen Batch von Beispielen liefert.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-111">If the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) member variable is **TRUE**, the object fills the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array before it delivers a batch of samples.</span></span> <span data-ttu-id="5e8ef-112">Mit dieser Methode können Sie einen partiellen Batch bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-112">Call this method to deliver a partial batch.</span></span> <span data-ttu-id="5e8ef-113">Beispielsweise ruft die [**coutputqueue:: EOS**](coutputqueue-eos.md) -Methode `SendAnyway` auf, um Streamende-Nachrichten zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-113">For example, the [**COutputQueue::EOS**](coutputqueue-eos.md) method calls `SendAnyway` to serialize end-of-stream messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e8ef-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e8ef-114">Requirements</span></span>



| <span data-ttu-id="5e8ef-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e8ef-115">Requirement</span></span> | <span data-ttu-id="5e8ef-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5e8ef-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8ef-117">Header</span><span class="sxs-lookup"><span data-stu-id="5e8ef-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5e8ef-118"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e8ef-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e8ef-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e8ef-119">Library</span></span><br/> | <dl> <span data-ttu-id="5e8ef-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5e8ef-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e8ef-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e8ef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8ef-122">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5e8ef-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




