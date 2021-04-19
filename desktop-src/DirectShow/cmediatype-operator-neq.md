---
description: Dieser Operator testet auf Ungleichheit zwischen cmediatype-Objekten.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: 'Cmediatype. cmediatype:: Operator! =-Methode (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe3d5b60ed1990423d5ad9375ffdf192da313b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369622"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="f6f19-103">Cmediatype. cmediatype:: Operator! =-Methode</span><span class="sxs-lookup"><span data-stu-id="f6f19-103">CMediaType.CMediaType::operator!= method</span></span>

<span data-ttu-id="f6f19-104">Dieser Operator testet auf Ungleichheit zwischen [**cmediatype**](cmediatype.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="f6f19-104">This operator tests for inequality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6f19-105">Syntax</span></span>


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="f6f19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6f19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f19-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="f6f19-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f6f19-108">Verweis auf das zu vergleichende **cmediatype** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f6f19-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f19-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6f19-109">Return value</span></span>

<span data-ttu-id="f6f19-110">Gibt **true** zurück, wenn *RT* nicht gleich diesem-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="f6f19-110">Returns **TRUE** if *rt* is not equal to this object.</span></span> <span data-ttu-id="f6f19-111">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6f19-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f19-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6f19-112">Requirements</span></span>



| <span data-ttu-id="f6f19-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6f19-113">Requirement</span></span> | <span data-ttu-id="f6f19-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f6f19-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f19-115">Header</span><span class="sxs-lookup"><span data-stu-id="f6f19-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f6f19-116"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6f19-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f6f19-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6f19-117">Library</span></span><br/> | <dl> <span data-ttu-id="f6f19-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f6f19-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f19-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6f19-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f19-120">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6f19-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




