---
description: 'CBaseOutputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin aus einer Verbindung frei.'
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: CBaseOutputPin.BreakConnect-Methode (Amfilter.h)
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
ms.openlocfilehash: 746783a73892bc34273da4b020446f2668a19cd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096218"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="a2350-103">CBaseOutputPin.BreakConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="a2350-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="a2350-104">Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="a2350-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2350-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2350-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="a2350-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2350-106">Parameters</span></span>

<span data-ttu-id="a2350-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a2350-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2350-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2350-108">Return value</span></span>

<span data-ttu-id="a2350-109">Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="a2350-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2350-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2350-110">Remarks</span></span>

<span data-ttu-id="a2350-111">Diese Methode überschreibt die [**CBasePin::BreakConnect-Methode.**](cbasepin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="a2350-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="a2350-112">Er decommitiert die Zuweisung und gibt die [**Schnittstellen IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) und [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) frei.</span><span class="sxs-lookup"><span data-stu-id="a2350-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="a2350-113">Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a2350-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="a2350-114">Andernfalls können Speicherverlusten verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="a2350-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2350-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2350-115">Requirements</span></span>



| <span data-ttu-id="a2350-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2350-116">Requirement</span></span> | <span data-ttu-id="a2350-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a2350-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2350-118">Header</span><span class="sxs-lookup"><span data-stu-id="a2350-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a2350-119"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="a2350-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2350-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2350-120">Library</span></span><br/> | <dl> <span data-ttu-id="a2350-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a2350-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2350-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a2350-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2350-123">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a2350-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




