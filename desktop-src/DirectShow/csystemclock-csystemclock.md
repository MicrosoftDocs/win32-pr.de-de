---
description: Konstruktormethode.
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: Csystemclock. csystemclock-Konstruktor (sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fea99d95aa4c1b1cadefbb95384fb871374362f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371222"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="5eb49-103">Csystemclock. csystemclock-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="5eb49-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="5eb49-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="5eb49-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eb49-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="5eb49-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5eb49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb49-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="5eb49-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5eb49-108">Zeichenfolge, die den debugnamen des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="5eb49-108">String containing the debug name of the object.</span></span> <span data-ttu-id="5eb49-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="5eb49-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="5eb49-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="5eb49-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="5eb49-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="5eb49-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="5eb49-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="5eb49-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="5eb49-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="5eb49-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5eb49-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="5eb49-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5eb49-115">Zeiger auf den **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="5eb49-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="5eb49-116">Wenn ein Fehler auftritt, gibt die Methode einen Fehlercode in diesem Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="5eb49-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5eb49-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5eb49-117">Requirements</span></span>



| <span data-ttu-id="5eb49-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eb49-118">Requirement</span></span> | <span data-ttu-id="5eb49-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5eb49-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb49-120">Header</span><span class="sxs-lookup"><span data-stu-id="5eb49-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5eb49-121"><dt>Sysclock. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5eb49-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5eb49-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5eb49-122">Library</span></span><br/> | <dl> <span data-ttu-id="5eb49-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5eb49-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




