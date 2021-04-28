---
description: 'CSeekingPassThru.CSeekingPassThru-Konstruktor : Konstruktormethode.'
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: CSeekingPassThru.CSeekingPassThru-Konstruktor (Seekpt.h)
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
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085378"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="1d5e8-103">CSeekingPassThru.CSeekingPassThru-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="1d5e8-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="1d5e8-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d5e8-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="1d5e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d5e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d5e8-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1d5e8-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1d5e8-108">Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-108">String containing the name of the object.</span></span> <span data-ttu-id="1d5e8-109">Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="1d5e8-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="1d5e8-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="1d5e8-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1d5e8-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="1d5e8-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="1d5e8-113">Legen Sie andernfalls diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1d5e8-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="1d5e8-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1d5e8-115">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="1d5e8-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d5e8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d5e8-117">Requirements</span></span>



| <span data-ttu-id="1d5e8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d5e8-118">Requirement</span></span> | <span data-ttu-id="1d5e8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1d5e8-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5e8-120">Header</span><span class="sxs-lookup"><span data-stu-id="1d5e8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1d5e8-121"><dt>Seekpt.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d5e8-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1d5e8-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d5e8-122">Library</span></span><br/> | <dl> <span data-ttu-id="1d5e8-123"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1d5e8-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d5e8-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1d5e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5e8-125">**CSeekingPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




