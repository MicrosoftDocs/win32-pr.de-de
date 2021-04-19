---
description: Konstruktormethode. Der Konstruktor sperrt das angegebene kritische Abschnitts Objekt.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Cautolock. cautolock-Konstruktor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366687"
---
# <a name="cautolockcautolock-constructor"></a><span data-ttu-id="6b2a5-104">Cautolock. cautolock-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="6b2a5-104">CAutoLock.CAutoLock constructor</span></span>

<span data-ttu-id="6b2a5-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="6b2a5-105">Constructor method.</span></span> <span data-ttu-id="6b2a5-106">Der Konstruktor sperrt das angegebene kritische Abschnitts Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b2a5-106">The constructor locks the specified critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b2a5-107">Syntax</span></span>


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a><span data-ttu-id="6b2a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b2a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2a5-109">*Plock*</span><span class="sxs-lookup"><span data-stu-id="6b2a5-109">*plock*</span></span> 
</dt> <dd>

<span data-ttu-id="6b2a5-110">Zeiger auf ein [**ccritsec**](ccritsec.md) -Objekt, das ein kritisches Abschnitts Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="6b2a5-110">Pointer to a [**CCritSec**](ccritsec.md) object, which contains a critical section object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b2a5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b2a5-111">Requirements</span></span>



| <span data-ttu-id="6b2a5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b2a5-112">Requirement</span></span> | <span data-ttu-id="6b2a5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6b2a5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2a5-114">Header</span><span class="sxs-lookup"><span data-stu-id="6b2a5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6b2a5-115"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b2a5-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6b2a5-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b2a5-116">Library</span></span><br/> | <dl> <span data-ttu-id="6b2a5-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6b2a5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2a5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b2a5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2a5-119">**Cautolock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6b2a5-119">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 




