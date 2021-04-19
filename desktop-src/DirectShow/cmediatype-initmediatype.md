---
description: Die initmediatype-Methode initialisiert den Medientyp.
ms.assetid: 141ced68-11ed-4567-b2e1-82c040d3b4a4
title: CMediaType.Initmediatype-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.InitMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3bbe170c6d896f3b28d9b85cf49f18269341d50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350750"
---
# <a name="cmediatypeinitmediatype-method"></a><span data-ttu-id="e4ca2-103">CMediaType.Initmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="e4ca2-103">CMediaType.InitMediaType method</span></span>

<span data-ttu-id="e4ca2-104">Die- `InitMediaType` Methode initialisiert den Medientyp.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-104">The `InitMediaType` method initializes the media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ca2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ca2-105">Syntax</span></span>


```C++
void InitMediaType();
```



## <a name="parameters"></a><span data-ttu-id="e4ca2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4ca2-106">Parameters</span></span>

<span data-ttu-id="e4ca2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4ca2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4ca2-108">Return value</span></span>

<span data-ttu-id="e4ca2-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ca2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4ca2-110">Remarks</span></span>

<span data-ttu-id="e4ca2-111">Mit dieser Methode wird der Arbeitsspeicher des Objekts Nullen, die Eigenschaft Fixed-sample-size auf **true** festgelegt und die Stichprobengröße auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-111">This method zeroes the object's memory, sets the fixed-sample-size property to **TRUE**, and sets the sample size to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ca2-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4ca2-112">Requirements</span></span>



| <span data-ttu-id="e4ca2-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4ca2-113">Requirement</span></span> | <span data-ttu-id="e4ca2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e4ca2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ca2-115">Header</span><span class="sxs-lookup"><span data-stu-id="e4ca2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e4ca2-116"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ca2-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e4ca2-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4ca2-117">Library</span></span><br/> | <dl> <span data-ttu-id="e4ca2-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ca2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ca2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4ca2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ca2-120">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e4ca2-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




