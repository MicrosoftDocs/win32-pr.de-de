---
description: Die Methode "kreateinstance" erstellt eine Instanz des-Objekts. Diese Methode unterstützt die Erstellung des Objekts über eine Klassenfactory. Weitere Informationen finden Sie unter cfactoriytemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Cseekingpassthru. kreateinzustance-Methode (seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359360"
---
# <a name="cseekingpassthrucreateinstance-method"></a><span data-ttu-id="e7fb6-105">Cseekingpassthru. kreateinzustance-Methode</span><span class="sxs-lookup"><span data-stu-id="e7fb6-105">CSeekingPassThru.CreateInstance method</span></span>

<span data-ttu-id="e7fb6-106">Die- `CreateInstance` Methode erstellt eine Instanz des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-106">The `CreateInstance` method creates an instance of the object.</span></span> <span data-ttu-id="e7fb6-107">Diese Methode unterstützt die Erstellung des Objekts über eine Klassenfactory.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-107">This method supports creation of the object through a class factory.</span></span> <span data-ttu-id="e7fb6-108">Weitere Informationen finden Sie unter [**cfactoriytemplate**](cfactorytemplate.md).</span><span class="sxs-lookup"><span data-stu-id="e7fb6-108">For more information, see [**CFactoryTemplate**](cfactorytemplate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7fb6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7fb6-109">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="e7fb6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7fb6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7fb6-111">*Kro*</span><span class="sxs-lookup"><span data-stu-id="e7fb6-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e7fb6-112">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="e7fb6-113">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="e7fb6-114">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7fb6-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="e7fb6-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e7fb6-116">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-116">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="e7fb6-117">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-117">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7fb6-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7fb6-118">Return value</span></span>

<span data-ttu-id="e7fb6-119">Gibt einen Zeiger auf ein neues **cseekingpassthru** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e7fb6-119">Returns a pointer to a new **CSeekingPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7fb6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7fb6-120">Requirements</span></span>



| <span data-ttu-id="e7fb6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7fb6-121">Requirement</span></span> | <span data-ttu-id="e7fb6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e7fb6-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fb6-123">Header</span><span class="sxs-lookup"><span data-stu-id="e7fb6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e7fb6-124"><dt>Seekpt. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7fb6-124"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e7fb6-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7fb6-125">Library</span></span><br/> | <dl> <span data-ttu-id="e7fb6-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e7fb6-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7fb6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7fb6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fb6-128">**Cseekingpassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e7fb6-128">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




