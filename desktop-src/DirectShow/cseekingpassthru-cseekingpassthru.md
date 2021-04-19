---
description: Konstruktormethode.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Cseekingpassthru. cseekingpassthru-Konstruktor (seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a93ed9706762b9a1672bfae85550ee4c2aceeead
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352834"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="20374-103">Cseekingpassthru. cseekingpassthru-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="20374-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="20374-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="20374-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20374-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20374-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="20374-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20374-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20374-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="20374-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="20374-108">Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="20374-108">String containing the name of the object.</span></span> <span data-ttu-id="20374-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="20374-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="20374-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="20374-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="20374-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="20374-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="20374-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="20374-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="20374-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="20374-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="20374-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="20374-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="20374-115">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="20374-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="20374-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="20374-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20374-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20374-117">Requirements</span></span>



| <span data-ttu-id="20374-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20374-118">Requirement</span></span> | <span data-ttu-id="20374-119">Wert</span><span class="sxs-lookup"><span data-stu-id="20374-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20374-120">Header</span><span class="sxs-lookup"><span data-stu-id="20374-120">Header</span></span><br/>  | <dl> <span data-ttu-id="20374-121"><dt>Seekpt. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20374-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="20374-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="20374-122">Library</span></span><br/> | <dl> <span data-ttu-id="20374-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="20374-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20374-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20374-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20374-125">**Cseekingpassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="20374-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




