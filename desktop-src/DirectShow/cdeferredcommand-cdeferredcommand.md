---
description: Konstruktormethode.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Cdeferredcommand. cdeferredcommand-Konstruktor (ctlutil. h)
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
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371560"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="ec3a6-103">Cdeferredcommand. cdeferredcommand-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ec3a6-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="ec3a6-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec3a6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ec3a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec3a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec3a6-107">*PQ*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-108">Zeiger auf ein Objekt, das die [**iqueuecommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-110">Zeiger auf die äußere **IUnknown** -Schnittstelle für die Aggregation.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-112">Zeiger auf einen zurückgegebenen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-113">*punkexecutor*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-114">Zeiger auf das-Objekt, das diesen Befehl ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-115">*time*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-116">Der Zeitpunkt, zu dem der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-117">*IID*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-118">Ein Zeiger auf die Globally Unique Identifier (**GUID**) der Schnittstelle, die die Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-119">*dispidmethod*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-120">-Methode für die aufzurufende Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-121">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-122">Der Kontext des aufaufruf.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-123">*kargs*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-124">Anzahl der über gebenen Argumente.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-125">*pdispparameams*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-126">Zeiger auf eine Liste von Argument Variant-Typen.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-127">*pVarResult*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-128">Zeiger auf eine zurückgegebene Varianttyp Liste, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-129">*gibt puArgErr*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-130">Zeiger auf das letzte Argument in der *pDispParams* -Parameterliste mit einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="ec3a6-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="ec3a6-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3a6-132">Ein Wert, der angibt, ob die verzögerte Befehls Zeit in der streamzeit (**true**) oder in der Präsentationszeit (**false**) liegt.</span><span class="sxs-lookup"><span data-stu-id="ec3a6-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec3a6-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec3a6-133">Requirements</span></span>



| <span data-ttu-id="ec3a6-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec3a6-134">Requirement</span></span> | <span data-ttu-id="ec3a6-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ec3a6-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3a6-136">Header</span><span class="sxs-lookup"><span data-stu-id="ec3a6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ec3a6-137"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec3a6-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec3a6-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ec3a6-138">Library</span></span><br/> | <dl> <span data-ttu-id="ec3a6-139">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ec3a6-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec3a6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec3a6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3a6-141">**Cdeferredcommand-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ec3a6-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




