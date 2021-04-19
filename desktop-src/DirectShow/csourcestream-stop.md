---
description: Die Methode zum Abbrechen signalisiert dem streamingthread, den Vorgang anzuhalten.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Csourcestream. stopmethode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44c9f845c092280ef5fafa808036654bd868a796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369678"
---
# <a name="csourcestreamstop-method"></a><span data-ttu-id="56c0d-103">Csourcestream. stopmethode</span><span class="sxs-lookup"><span data-stu-id="56c0d-103">CSourceStream.Stop method</span></span>

<span data-ttu-id="56c0d-104">Die- `Stop` Methode signalisiert dem Streaminginhalt das Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="56c0d-104">The `Stop` method signals the streaming thread to stop.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56c0d-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="56c0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56c0d-106">Parameters</span></span>

<span data-ttu-id="56c0d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="56c0d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56c0d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56c0d-108">Return value</span></span>

<span data-ttu-id="56c0d-109">Gibt \_ OK oder E \_ unerwartet zurück.</span><span class="sxs-lookup"><span data-stu-id="56c0d-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c0d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56c0d-110">Remarks</span></span>

<span data-ttu-id="56c0d-111">Die [**csourcestream:: inaktive**](csourcestream-inactive.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="56c0d-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c0d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56c0d-112">Requirements</span></span>



| <span data-ttu-id="56c0d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56c0d-113">Requirement</span></span> | <span data-ttu-id="56c0d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="56c0d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c0d-115">Header</span><span class="sxs-lookup"><span data-stu-id="56c0d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="56c0d-116"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56c0d-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="56c0d-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56c0d-117">Library</span></span><br/> | <dl> <span data-ttu-id="56c0d-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="56c0d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c0d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56c0d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c0d-120">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="56c0d-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




