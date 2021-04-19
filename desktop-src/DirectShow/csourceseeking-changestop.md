---
description: Die changestoppt-Methode wird aufgerufen, wenn die Position des Stopps geändert wird.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Csourceseeking. changestoppt-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366049"
---
# <a name="csourceseekingchangestop-method"></a><span data-ttu-id="4ad72-103">Csourceseeking. changestoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="4ad72-103">CSourceSeeking.ChangeStop method</span></span>

<span data-ttu-id="4ad72-104">Die- `ChangeStop` Methode wird aufgerufen, wenn die Position des Stopps geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4ad72-104">The `ChangeStop` method is called when the stop position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ad72-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a><span data-ttu-id="4ad72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ad72-106">Parameters</span></span>

<span data-ttu-id="4ad72-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4ad72-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ad72-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ad72-108">Return value</span></span>

<span data-ttu-id="4ad72-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4ad72-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad72-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ad72-110">Remarks</span></span>

<span data-ttu-id="4ad72-111">Die [**csourceseeking:: setpositions**](csourceseeking-setpositions.md) -Methode ruft diese Methode auf, wenn sich die Position des Stopps ändert.</span><span class="sxs-lookup"><span data-stu-id="4ad72-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the stop position changes.</span></span> <span data-ttu-id="4ad72-112">Diese Methode ist rein virtuell. Diese Klasse muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ad72-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="4ad72-113">Das folgende Beispiel zeigt eine mögliche Implementierung:</span><span class="sxs-lookup"><span data-stu-id="4ad72-113">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="4ad72-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ad72-114">Requirements</span></span>



| <span data-ttu-id="4ad72-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ad72-115">Requirement</span></span> | <span data-ttu-id="4ad72-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4ad72-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad72-117">Header</span><span class="sxs-lookup"><span data-stu-id="4ad72-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4ad72-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ad72-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ad72-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ad72-119">Library</span></span><br/> | <dl> <span data-ttu-id="4ad72-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4ad72-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad72-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ad72-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad72-122">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4ad72-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




