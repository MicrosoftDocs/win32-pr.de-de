---
description: Konstruktormethode.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Ccritsec. ccritsec-Konstruktor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374032"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="eeaec-103">Ccritsec. ccritsec-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="eeaec-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="eeaec-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="eeaec-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeaec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeaec-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="eeaec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eeaec-106">Parameters</span></span>

<span data-ttu-id="eeaec-107">Dieser Konstruktor weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="eeaec-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeaec-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eeaec-108">Remarks</span></span>

<span data-ttu-id="eeaec-109">Diese Methode ruft die [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) -Funktion auf, um den kritischen Abschnitt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="eeaec-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeaec-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eeaec-110">Requirements</span></span>



| <span data-ttu-id="eeaec-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eeaec-111">Requirement</span></span> | <span data-ttu-id="eeaec-112">Wert</span><span class="sxs-lookup"><span data-stu-id="eeaec-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeaec-113">Header</span><span class="sxs-lookup"><span data-stu-id="eeaec-113">Header</span></span><br/>  | <dl> <span data-ttu-id="eeaec-114"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eeaec-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="eeaec-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eeaec-115">Library</span></span><br/> | <dl> <span data-ttu-id="eeaec-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eeaec-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeaec-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eeaec-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeaec-118">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eeaec-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

