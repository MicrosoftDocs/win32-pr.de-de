---
description: Die dbgend-Funktion bereinigt die Debug-Bibliothek. Wird in Einzelhandels Builds ignoriert.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Dbgend-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358018"
---
# <a name="dbgterminate-function"></a><span data-ttu-id="7f93b-104">Dbgend-Funktion</span><span class="sxs-lookup"><span data-stu-id="7f93b-104">DbgTerminate function</span></span>

<span data-ttu-id="7f93b-105">Die **dbgend** -Funktion bereinigt die Debug-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="7f93b-105">The **DbgTerminate** function cleans up the debug library.</span></span> <span data-ttu-id="7f93b-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7f93b-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f93b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f93b-107">Syntax</span></span>


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a><span data-ttu-id="7f93b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f93b-108">Parameters</span></span>

<span data-ttu-id="7f93b-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7f93b-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f93b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f93b-110">Return value</span></span>

<span data-ttu-id="7f93b-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7f93b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f93b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f93b-112">Remarks</span></span>

<span data-ttu-id="7f93b-113">Wenn Sie die [**dbginitialise**](dbginitialise.md) -Funktion aufzurufen, wird diese Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7f93b-113">Call this function if you call the [**DbgInitialise**](dbginitialise.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f93b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f93b-114">Requirements</span></span>



| <span data-ttu-id="7f93b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f93b-115">Requirement</span></span> | <span data-ttu-id="7f93b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7f93b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f93b-117">Header</span><span class="sxs-lookup"><span data-stu-id="7f93b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7f93b-118"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f93b-118"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f93b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f93b-119">Library</span></span><br/> | <dl> <span data-ttu-id="7f93b-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7f93b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f93b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f93b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f93b-122">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="7f93b-122">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




