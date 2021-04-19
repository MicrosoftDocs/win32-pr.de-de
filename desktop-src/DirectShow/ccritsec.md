---
description: Die ccritsec-Klasse stellt eine Thread Sperre bereit.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Ccritsec-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370641"
---
# <a name="ccritsec-class"></a><span data-ttu-id="f48f8-103">Ccritsec-Klasse</span><span class="sxs-lookup"><span data-stu-id="f48f8-103">CCritSec class</span></span>

<span data-ttu-id="f48f8-104">Die **ccritsec** -Klasse stellt eine Thread Sperre bereit.</span><span class="sxs-lookup"><span data-stu-id="f48f8-104">The **CCritSec** class provides a thread lock.</span></span>

<span data-ttu-id="f48f8-105">Diese Klasse ist ein schlanker Wrapper für ein kritisches Windows- **\_ Abschnitts** Objekt.</span><span class="sxs-lookup"><span data-stu-id="f48f8-105">This class is a thin wrapper for a Windows **CRITICAL\_SECTION** object.</span></span> <span data-ttu-id="f48f8-106">Sie können den Thread Sperren und entsperren, indem Sie die [**ccritsec:: Lock**](ccritsec-lock.md) -Methode und die [**ccritsec:: Unlock**](ccritsec-unlock.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f48f8-106">You can lock and unlock the thread by calling the [**CCritSec::Lock**](ccritsec-lock.md) and [**CCritSec::Unlock**](ccritsec-unlock.md) methods.</span></span> <span data-ttu-id="f48f8-107">Es ist jedoch sicherer, diese Klasse in Verbindung mit der [**cautolock**](cautolock.md) -Klasse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f48f8-107">However, it is safer to use this class in conjunction with the [**CAutoLock**](cautolock.md) class.</span></span> <span data-ttu-id="f48f8-108">Wenn die **cautolock** -Klasse den Gültigkeitsbereich verlässt, entsperrt Sie automatisch das **ccritsec** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f48f8-108">When the **CAutoLock** class goes out of scope, it automatically unlocks the **CCritSec** object.</span></span> <span data-ttu-id="f48f8-109">Außerdem wird es in effizienten Inline Code kompiliert.</span><span class="sxs-lookup"><span data-stu-id="f48f8-109">Moreover, it compiles to efficient inline code.</span></span>



| <span data-ttu-id="f48f8-110">Öffentliche Element Variablen</span><span class="sxs-lookup"><span data-stu-id="f48f8-110">Public Member Variables</span></span>                            | <span data-ttu-id="f48f8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f48f8-111">Description</span></span>                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="f48f8-112">**m \_ currentowner**</span><span class="sxs-lookup"><span data-stu-id="f48f8-112">**m\_currentOwner**</span></span>](ccritsec-m-currentowner.md) | <span data-ttu-id="f48f8-113">Thread Bezeichner des besitzenden Threads.</span><span class="sxs-lookup"><span data-stu-id="f48f8-113">Thread identifier of the owning thread.</span></span>                  |
| [<span data-ttu-id="f48f8-114">**m \_ Sperr Anzahl**</span><span class="sxs-lookup"><span data-stu-id="f48f8-114">**m\_lockCount**</span></span>](ccritsec-m-lockcount.md)       | <span data-ttu-id="f48f8-115">Anzahl der ausstehenden Sperren für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="f48f8-115">Number of outstanding locks on this object.</span></span>              |
| [<span data-ttu-id="f48f8-116">**m-nach \_ Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="f48f8-116">**m\_fTrace**</span></span>](ccritsec-m-ftrace.md)             | <span data-ttu-id="f48f8-117">Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f48f8-117">Boolean value that specifies whether to trace this lock.</span></span> |
| <span data-ttu-id="f48f8-118">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="f48f8-118">Public Methods</span></span>                                     | <span data-ttu-id="f48f8-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f48f8-119">Description</span></span>                                              |
| [<span data-ttu-id="f48f8-120">**Ccritsec**</span><span class="sxs-lookup"><span data-stu-id="f48f8-120">**CCritSec**</span></span>](ccritsec-ccritsec.md)              | <span data-ttu-id="f48f8-121">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f48f8-121">Constructor method.</span></span>                                      |
| [<span data-ttu-id="f48f8-122">**~ Ccritsec**</span><span class="sxs-lookup"><span data-stu-id="f48f8-122">**~CCritSec**</span></span>](ccritsec--ccritsec.md)            | <span data-ttu-id="f48f8-123">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f48f8-123">Destructor method.</span></span>                                       |
| [<span data-ttu-id="f48f8-124">**Sperre**</span><span class="sxs-lookup"><span data-stu-id="f48f8-124">**Lock**</span></span>](ccritsec-lock.md)                      | <span data-ttu-id="f48f8-125">Sperrt das kritische Abschnitts Objekt.</span><span class="sxs-lookup"><span data-stu-id="f48f8-125">Locks the critical section object.</span></span>                       |
| [<span data-ttu-id="f48f8-126">**Entsperren**</span><span class="sxs-lookup"><span data-stu-id="f48f8-126">**Unlock**</span></span>](ccritsec-unlock.md)                  | <span data-ttu-id="f48f8-127">Entsperrt das Objekt des kritischen Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="f48f8-127">Unlocks the critical section object.</span></span>                     |



 

## <a name="requirements"></a><span data-ttu-id="f48f8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f48f8-128">Requirements</span></span>



| <span data-ttu-id="f48f8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f48f8-129">Requirement</span></span> | <span data-ttu-id="f48f8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f48f8-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48f8-131">Header</span><span class="sxs-lookup"><span data-stu-id="f48f8-131">Header</span></span><br/>  | <dl> <span data-ttu-id="f48f8-132"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f48f8-132"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f48f8-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f48f8-133">Library</span></span><br/> | <dl> <span data-ttu-id="f48f8-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f48f8-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f48f8-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f48f8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48f8-136">Kritische Abschnitts Objekte</span><span class="sxs-lookup"><span data-stu-id="f48f8-136">Critical Section Objects</span></span>](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[<span data-ttu-id="f48f8-137">Referenz zur DirectShow-Basisklasse</span><span class="sxs-lookup"><span data-stu-id="f48f8-137">DirectShow Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

