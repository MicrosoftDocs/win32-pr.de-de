---
description: Die breakconnect-Methode gibt die PIN von einer Verbindung frei.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Cbaseoutputpin. breakconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372574"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="bbd47-103">Cbaseoutputpin. breakconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="bbd47-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="bbd47-104">Die- `BreakConnect` Methode gibt die PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="bbd47-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbd47-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="bbd47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbd47-106">Parameters</span></span>

<span data-ttu-id="bbd47-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bbd47-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbd47-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbd47-108">Return value</span></span>

<span data-ttu-id="bbd47-109">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="bbd47-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd47-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbd47-110">Remarks</span></span>

<span data-ttu-id="bbd47-111">Diese Methode überschreibt die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bbd47-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="bbd47-112">Er debugt die Zuweisung und gibt die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -und [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen frei.</span><span class="sxs-lookup"><span data-stu-id="bbd47-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="bbd47-113">Wenn Sie diese Methode überschreiben, müssen Sie die Basisklassen Methode aus der über schreibenden Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="bbd47-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="bbd47-114">Andernfalls können Sie Speicher Verluste verursachen.</span><span class="sxs-lookup"><span data-stu-id="bbd47-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd47-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbd47-115">Requirements</span></span>



| <span data-ttu-id="bbd47-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbd47-116">Requirement</span></span> | <span data-ttu-id="bbd47-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd47-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd47-118">Header</span><span class="sxs-lookup"><span data-stu-id="bbd47-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bbd47-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd47-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bbd47-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bbd47-120">Library</span></span><br/> | <dl> <span data-ttu-id="bbd47-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd47-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd47-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbd47-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd47-123">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bbd47-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




