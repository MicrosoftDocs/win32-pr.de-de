---
description: Die Pause-Methode hält den Filter an. Diese Methode implementiert die imediafilter::P ause-Methode.
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Ctransformfilter. Pause-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5408b9a39f92fd68eacb83474a18da0acda6b961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365572"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="6821b-104">Ctransformfilter. Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="6821b-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="6821b-105">Die `Pause` Methode hält den Filter an.</span><span class="sxs-lookup"><span data-stu-id="6821b-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="6821b-106">Diese Methode implementiert die [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6821b-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6821b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6821b-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="6821b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6821b-108">Parameters</span></span>

<span data-ttu-id="6821b-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6821b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6821b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6821b-110">Return value</span></span>

<span data-ttu-id="6821b-111">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6821b-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6821b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6821b-112">Remarks</span></span>

<span data-ttu-id="6821b-113">Diese Methode ruft die [**startstreaming**](ctransformfilter-startstreaming.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6821b-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="6821b-114">Die **startstreaming** -Methode führt in der Basisklasse keine Aktion aus, die abgeleitete Klasse kann Sie jedoch überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6821b-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6821b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6821b-115">Requirements</span></span>



| <span data-ttu-id="6821b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6821b-116">Requirement</span></span> | <span data-ttu-id="6821b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6821b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6821b-118">Header</span><span class="sxs-lookup"><span data-stu-id="6821b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6821b-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6821b-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6821b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6821b-120">Library</span></span><br/> | <dl> <span data-ttu-id="6821b-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6821b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6821b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6821b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6821b-123">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6821b-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




