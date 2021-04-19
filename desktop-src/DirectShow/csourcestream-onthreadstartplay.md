---
description: Die onthreadstartplay-Methode wird am Anfang der csourcestream::D obufferprocessingloop-Methode aufgerufen.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Csourcestream. onthreadstartplay-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369144"
---
# <a name="csourcestreamonthreadstartplay-method"></a><span data-ttu-id="e8c54-103">Csourcestream. onthreadstartplay-Methode</span><span class="sxs-lookup"><span data-stu-id="e8c54-103">CSourceStream.OnThreadStartPlay method</span></span>

<span data-ttu-id="e8c54-104">Die- `OnThreadStartPlay` Methode wird zu Beginn der [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e8c54-104">The `OnThreadStartPlay` method is called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c54-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8c54-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a><span data-ttu-id="e8c54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8c54-106">Parameters</span></span>

<span data-ttu-id="e8c54-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e8c54-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8c54-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8c54-108">Return value</span></span>

<span data-ttu-id="e8c54-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e8c54-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c54-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8c54-110">Remarks</span></span>

<span data-ttu-id="e8c54-111">Diese Methode führt in der Basisklasse keine Aktion aus. Sie kann von der abgeleiteten Klasse außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="e8c54-111">This method does nothing in the base class; it is available for the derived class to override.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c54-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8c54-112">Requirements</span></span>



| <span data-ttu-id="e8c54-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8c54-113">Requirement</span></span> | <span data-ttu-id="e8c54-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e8c54-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c54-115">Header</span><span class="sxs-lookup"><span data-stu-id="e8c54-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e8c54-116"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8c54-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e8c54-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8c54-117">Library</span></span><br/> | <dl> <span data-ttu-id="e8c54-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e8c54-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c54-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8c54-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c54-120">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e8c54-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




