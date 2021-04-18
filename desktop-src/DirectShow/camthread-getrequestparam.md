---
description: Die getrequestparam-Methode ruft die aktuelle Anforderung ab.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Camthread. getrequestparam-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371239"
---
# <a name="camthreadgetrequestparam-method"></a><span data-ttu-id="943c8-103">Camthread. getrequestparam-Methode</span><span class="sxs-lookup"><span data-stu-id="943c8-103">CAMThread.GetRequestParam method</span></span>

<span data-ttu-id="943c8-104">Die- `GetRequestParam` Methode ruft die aktuelle Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="943c8-104">The `GetRequestParam` method retrieves the latest request.</span></span>

## <a name="syntax"></a><span data-ttu-id="943c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="943c8-105">Syntax</span></span>


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a><span data-ttu-id="943c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="943c8-106">Parameters</span></span>

<span data-ttu-id="943c8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="943c8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="943c8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="943c8-108">Return value</span></span>

<span data-ttu-id="943c8-109">Gibt den Wert des-Parameters zurück, der zuletzt an die Methode " [**camthread:: callworker**](camthread-callworker.md) " übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="943c8-109">Returns the value of the parameter that was passed most recently to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="943c8-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="943c8-110">Requirements</span></span>



| <span data-ttu-id="943c8-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="943c8-111">Requirement</span></span> | <span data-ttu-id="943c8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="943c8-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943c8-113">Header</span><span class="sxs-lookup"><span data-stu-id="943c8-113">Header</span></span><br/>  | <dl> <span data-ttu-id="943c8-114"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="943c8-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="943c8-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="943c8-115">Library</span></span><br/> | <dl> <span data-ttu-id="943c8-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="943c8-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943c8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="943c8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943c8-118">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="943c8-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




