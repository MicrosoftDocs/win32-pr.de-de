---
description: Stellt die Initialisierung für einen Thread bereit.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Cmsgthread. onthreadinit-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367592"
---
# <a name="cmsgthreadonthreadinit-method"></a><span data-ttu-id="e796f-103">Cmsgthread. onthreadinit-Methode</span><span class="sxs-lookup"><span data-stu-id="e796f-103">CMsgThread.OnThreadInit method</span></span>

<span data-ttu-id="e796f-104">Stellt die Initialisierung für einen Thread bereit.</span><span class="sxs-lookup"><span data-stu-id="e796f-104">Provides initialization on a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="e796f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e796f-105">Syntax</span></span>


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a><span data-ttu-id="e796f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e796f-106">Parameters</span></span>

<span data-ttu-id="e796f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e796f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e796f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e796f-108">Return value</span></span>

<span data-ttu-id="e796f-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e796f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e796f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e796f-110">Remarks</span></span>

<span data-ttu-id="e796f-111">Überschreiben Sie diese Funktion, wenn Sie eine eigene spezifische Initialisierung beim Starten des Threads durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="e796f-111">Override this function if you want to do your own specific initialization on thread startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="e796f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e796f-112">Requirements</span></span>



| <span data-ttu-id="e796f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e796f-113">Requirement</span></span> | <span data-ttu-id="e796f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e796f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e796f-115">Header</span><span class="sxs-lookup"><span data-stu-id="e796f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e796f-116"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e796f-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e796f-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e796f-117">Library</span></span><br/> | <dl> <span data-ttu-id="e796f-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e796f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e796f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e796f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e796f-120">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e796f-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




