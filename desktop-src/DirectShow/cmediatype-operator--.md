---
description: Dieser Operator testet auf Gleichheit zwischen cmediatype-Objekten.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'Cmediatype. cmediatype:: Operator = =-Methode (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362027"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="b8872-103">Cmediatype. cmediatype:: Operator = =-Methode</span><span class="sxs-lookup"><span data-stu-id="b8872-103">CMediaType.CMediaType::operator== method</span></span>

<span data-ttu-id="b8872-104">Dieser Operator testet auf Gleichheit zwischen [**cmediatype**](cmediatype.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="b8872-104">This operator tests for equality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8872-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8872-105">Syntax</span></span>


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="b8872-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8872-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="b8872-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b8872-108">Verweis auf das zu vergleichende **cmediatype** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b8872-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8872-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8872-109">Return value</span></span>

<span data-ttu-id="b8872-110">Gibt **true** zurück, wenn *RT* gleich diesem-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="b8872-110">Returns **TRUE** if *rt* is equal to this object.</span></span> <span data-ttu-id="b8872-111">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b8872-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8872-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8872-112">Requirements</span></span>



| <span data-ttu-id="b8872-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8872-113">Requirement</span></span> | <span data-ttu-id="b8872-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b8872-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8872-115">Header</span><span class="sxs-lookup"><span data-stu-id="b8872-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b8872-116"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8872-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b8872-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8872-117">Library</span></span><br/> | <dl> <span data-ttu-id="b8872-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b8872-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8872-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8872-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8872-120">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b8872-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




