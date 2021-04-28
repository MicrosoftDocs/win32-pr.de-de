---
description: 'CCritSec.CCritSec-Konstruktor : Konstruktormethode.'
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: CCritSec.CCritSec-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119798"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="f195c-103">CCritSec.CCritSec-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="f195c-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="f195c-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f195c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f195c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f195c-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="f195c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f195c-106">Parameters</span></span>

<span data-ttu-id="f195c-107">Dieser Konstruktor verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f195c-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f195c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f195c-108">Remarks</span></span>

<span data-ttu-id="f195c-109">Diese Methode ruft die [**InitializeCriticalSection-Funktion auf,**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) um den kritischen Abschnitt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="f195c-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="f195c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f195c-110">Requirements</span></span>



| <span data-ttu-id="f195c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f195c-111">Requirement</span></span> | <span data-ttu-id="f195c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f195c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f195c-113">Header</span><span class="sxs-lookup"><span data-stu-id="f195c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f195c-114"><dt>Wxutil.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="f195c-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f195c-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f195c-115">Library</span></span><br/> | <dl> <span data-ttu-id="f195c-116"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f195c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f195c-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f195c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f195c-118">**CCritSec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f195c-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

