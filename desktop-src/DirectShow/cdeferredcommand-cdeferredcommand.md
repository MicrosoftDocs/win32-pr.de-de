---
description: CDeferredCommand.CDeferredCommand-Konstruktor – Konstruktormethode.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: CDeferredCommand.CDeferredCommand-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119788"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="f2efc-103">CDeferredCommand.CDeferredCommand-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="f2efc-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="f2efc-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f2efc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2efc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2efc-105">Syntax</span></span>


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a><span data-ttu-id="f2efc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2efc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2efc-107">*Pq*</span><span class="sxs-lookup"><span data-stu-id="f2efc-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-108">Zeiger auf ein Objekt, das die [**IQueueCommand-Schnittstelle verfügbar**](/windows/desktop/api/Control/nn-control-iqueuecommand) macht.</span><span class="sxs-lookup"><span data-stu-id="f2efc-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="f2efc-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-110">Zeiger auf die äußere **IUnknown-Schnittstelle** für die Aggregation.</span><span class="sxs-lookup"><span data-stu-id="f2efc-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="f2efc-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-112">Zeiger auf einen zurückgegebenen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="f2efc-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-113">*pUnkExecutor*</span><span class="sxs-lookup"><span data-stu-id="f2efc-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-114">Zeiger auf das Objekt, von dem dieser Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2efc-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-115">*time*</span><span class="sxs-lookup"><span data-stu-id="f2efc-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-116">Zeitpunkt, zu dem der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2efc-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-117">*Iid*</span><span class="sxs-lookup"><span data-stu-id="f2efc-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-118">Zeiger auf den global eindeutigen Bezeichner **(GUID)** der Schnittstelle, die die -Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="f2efc-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-119">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="f2efc-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-120">Methode für die aufrufende Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f2efc-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-121">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="f2efc-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-122">Kontext des Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="f2efc-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-123">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="f2efc-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-124">Anzahl der übergebenen Argumente.</span><span class="sxs-lookup"><span data-stu-id="f2efc-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-125">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="f2efc-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-126">Zeiger auf eine Liste von Argumentvariantentypen.</span><span class="sxs-lookup"><span data-stu-id="f2efc-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-127">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="f2efc-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-128">Zeiger auf eine zurückgegebene Liste von Variantentypen, sofern diese enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f2efc-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-129">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="f2efc-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-130">Zeiger auf das letzte Argument in der *pDispParams-Parameterliste* mit einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2efc-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="f2efc-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="f2efc-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="f2efc-132">Wert, der angibt, ob die verzögerte Befehlszeit in der Streamzeit (**TRUE**) oder in der Präsentationszeit ( FALSE )**liegt.**</span><span class="sxs-lookup"><span data-stu-id="f2efc-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2efc-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2efc-133">Requirements</span></span>



| <span data-ttu-id="f2efc-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2efc-134">Requirement</span></span> | <span data-ttu-id="f2efc-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f2efc-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2efc-136">Header</span><span class="sxs-lookup"><span data-stu-id="f2efc-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f2efc-137"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2efc-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2efc-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2efc-138">Library</span></span><br/> | <dl> <span data-ttu-id="f2efc-139"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f2efc-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2efc-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f2efc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2efc-141">**CDeferredCommand-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2efc-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




