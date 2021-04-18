---
description: Die Run-Methode wechselt in den Modus "wird ausgeführt", sodass Befehle, die von der streamzeit verzögert werden, ausgeführt werden können.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Ccmdqueue. Run-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365901"
---
# <a name="ccmdqueuerun-method"></a><span data-ttu-id="cb06a-103">Ccmdqueue. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="cb06a-103">CCmdQueue.Run method</span></span>

<span data-ttu-id="cb06a-104">Die `Run` Methode wechselt in den Modus "wird ausgeführt", sodass Befehle, die von der streamzeit verzögert werden, ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="cb06a-104">The `Run` method switches to running mode so that commands that are deferred by the stream time can be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb06a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb06a-105">Syntax</span></span>


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a><span data-ttu-id="cb06a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb06a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb06a-107">*tstreamtimeoffset*</span><span class="sxs-lookup"><span data-stu-id="cb06a-107">*tStreamTimeOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="cb06a-108">Offset Zeit.</span><span class="sxs-lookup"><span data-stu-id="cb06a-108">Offset time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb06a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb06a-109">Return value</span></span>

<span data-ttu-id="cb06a-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="cb06a-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb06a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb06a-111">Remarks</span></span>

<span data-ttu-id="cb06a-112">Während des laufenden Modus ist die Zuordnung von streamzeit zu Präsentationszeit bekannt.</span><span class="sxs-lookup"><span data-stu-id="cb06a-112">During running mode, stream-time-to-presentation-time mapping is known.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb06a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb06a-113">Requirements</span></span>



| <span data-ttu-id="cb06a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb06a-114">Requirement</span></span> | <span data-ttu-id="cb06a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cb06a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb06a-116">Header</span><span class="sxs-lookup"><span data-stu-id="cb06a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cb06a-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb06a-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb06a-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cb06a-118">Library</span></span><br/> | <dl> <span data-ttu-id="cb06a-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cb06a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb06a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb06a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb06a-121">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cb06a-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




