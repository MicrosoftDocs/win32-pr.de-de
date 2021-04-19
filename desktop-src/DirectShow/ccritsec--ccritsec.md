---
description: Dekonstruktormethode.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Ccritsec. ~ ccritsec-debugtor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371671"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="06e17-103">Ccritsec. ~ ccritsec-Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="06e17-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="06e17-104">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="06e17-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e17-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="06e17-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06e17-106">Remarks</span></span>

<span data-ttu-id="06e17-107">Diese Methode ruft die [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) -Funktion auf, um den kritischen Abschnitt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="06e17-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e17-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06e17-108">Requirements</span></span>



| <span data-ttu-id="06e17-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06e17-109">Requirement</span></span> | <span data-ttu-id="06e17-110">Wert</span><span class="sxs-lookup"><span data-stu-id="06e17-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e17-111">Header</span><span class="sxs-lookup"><span data-stu-id="06e17-111">Header</span></span><br/>  | <dl> <span data-ttu-id="06e17-112"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06e17-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="06e17-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06e17-113">Library</span></span><br/> | <dl> <span data-ttu-id="06e17-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="06e17-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e17-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06e17-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e17-116">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="06e17-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

