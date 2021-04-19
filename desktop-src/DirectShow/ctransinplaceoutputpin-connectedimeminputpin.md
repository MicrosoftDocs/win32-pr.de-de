---
description: 'Die connectedimeminputpin-Methode ruft einen Zeiger auf die nachgelagerte Eingabe-PIN ab. Diese Methode gibt die cbaseoutputpin:: m \_ pinputpin-Member-Variable zurück.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Ctransinplaceoutputpin. connectedimeminputpin-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357595"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a><span data-ttu-id="d8be3-104">Ctransinplaceoutputpin. connectedimeminputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="d8be3-104">CTransInPlaceOutputPin.ConnectedIMemInputPin method</span></span>

<span data-ttu-id="d8be3-105">Die- `ConnectedIMemInputPin` Methode ruft einen Zeiger auf die nachgelagerte Eingabe-PIN ab.</span><span class="sxs-lookup"><span data-stu-id="d8be3-105">The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin.</span></span> <span data-ttu-id="d8be3-106">Diese Methode gibt die [**cbaseoutputpin:: m \_ pinputpin**](cbaseoutputpin-m-pinputpin.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="d8be3-106">This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8be3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8be3-107">Syntax</span></span>


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a><span data-ttu-id="d8be3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8be3-108">Parameters</span></span>

<span data-ttu-id="d8be3-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d8be3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8be3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8be3-110">Return value</span></span>

<span data-ttu-id="d8be3-111">Gibt einen Zeiger auf die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle der nachgeschalteten Eingabe-PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="d8be3-111">Returns a pointer to the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8be3-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8be3-112">Requirements</span></span>



| <span data-ttu-id="d8be3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8be3-113">Requirement</span></span> | <span data-ttu-id="d8be3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d8be3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8be3-115">Header</span><span class="sxs-lookup"><span data-stu-id="d8be3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d8be3-116"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8be3-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8be3-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8be3-117">Library</span></span><br/> | <dl> <span data-ttu-id="d8be3-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d8be3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8be3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8be3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8be3-120">**Ctransinplaceoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d8be3-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




