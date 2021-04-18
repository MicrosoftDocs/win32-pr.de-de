---
description: Handle für den Thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Camthread:: m_hThread Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358796"
---
# <a name="camthreadm_hthread-member"></a><span data-ttu-id="88deb-103">Camthread:: m- \_ hThread-Member</span><span class="sxs-lookup"><span data-stu-id="88deb-103">CAMThread::m\_hThread member</span></span>

<span data-ttu-id="88deb-104">Handle für den Thread.</span><span class="sxs-lookup"><span data-stu-id="88deb-104">Handle to the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="88deb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88deb-105">Syntax</span></span>


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a><span data-ttu-id="88deb-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88deb-106">Remarks</span></span>

<span data-ttu-id="88deb-107">Diese Variable wird als **null** initialisiert.</span><span class="sxs-lookup"><span data-stu-id="88deb-107">This variable is initialized as **NULL**.</span></span> <span data-ttu-id="88deb-108">Die Methode " [**camthread:: Create**](camthread-create.md) " legt diese Variable auf das Thread Handle fest.</span><span class="sxs-lookup"><span data-stu-id="88deb-108">The [**CAMThread::Create**](camthread-create.md) method sets this variable to the thread handle.</span></span> <span data-ttu-id="88deb-109">Um zu ermitteln, ob der Thread vorhanden ist, müssen Sie die Methode " [**camthread:: threadexists**](camthread-threadexists.md) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="88deb-109">To determine whether the thread exists, call the [**CAMThread::ThreadExists**](camthread-threadexists.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="88deb-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88deb-110">Requirements</span></span>



| <span data-ttu-id="88deb-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88deb-111">Requirement</span></span> | <span data-ttu-id="88deb-112">Wert</span><span class="sxs-lookup"><span data-stu-id="88deb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88deb-113">Header</span><span class="sxs-lookup"><span data-stu-id="88deb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="88deb-114"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88deb-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="88deb-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88deb-115">Library</span></span><br/> | <dl> <span data-ttu-id="88deb-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="88deb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88deb-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88deb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88deb-118">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="88deb-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




