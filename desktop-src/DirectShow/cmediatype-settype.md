---
description: Die settype-Methode gibt den Haupttyp an.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Cmediatype. SetType-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371301"
---
# <a name="cmediatypesettype-method"></a><span data-ttu-id="88aa4-103">Cmediatype. SetType-Methode</span><span class="sxs-lookup"><span data-stu-id="88aa4-103">CMediaType.SetType method</span></span>

<span data-ttu-id="88aa4-104">Die- `SetType` Methode gibt den Haupttyp an.</span><span class="sxs-lookup"><span data-stu-id="88aa4-104">The `SetType` method specifies the major type.</span></span>

## <a name="syntax"></a><span data-ttu-id="88aa4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88aa4-105">Syntax</span></span>


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a><span data-ttu-id="88aa4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88aa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88aa4-107">*pType*</span><span class="sxs-lookup"><span data-stu-id="88aa4-107">*ptype*</span></span> 
</dt> <dd>

<span data-ttu-id="88aa4-108">Zeiger auf eine **GUID** , die den Haupttyp angibt.</span><span class="sxs-lookup"><span data-stu-id="88aa4-108">Pointer to a **GUID** that specifies the major type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88aa4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88aa4-109">Return value</span></span>

<span data-ttu-id="88aa4-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="88aa4-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="88aa4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88aa4-111">Requirements</span></span>



| <span data-ttu-id="88aa4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88aa4-112">Requirement</span></span> | <span data-ttu-id="88aa4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="88aa4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88aa4-114">Header</span><span class="sxs-lookup"><span data-stu-id="88aa4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="88aa4-115"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88aa4-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="88aa4-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88aa4-116">Library</span></span><br/> | <dl> <span data-ttu-id="88aa4-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="88aa4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88aa4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88aa4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88aa4-119">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="88aa4-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




