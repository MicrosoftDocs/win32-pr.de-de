---
description: Die Find-Methode ruft die erste Position ab, die das angegebene Element enthält.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: Cgenericlist. Find-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355953"
---
# <a name="cgenericlistfind-method"></a><span data-ttu-id="86cd6-103">Cgenericlist. Find-Methode</span><span class="sxs-lookup"><span data-stu-id="86cd6-103">CGenericList.Find method</span></span>

<span data-ttu-id="86cd6-104">Die- `Find` Methode ruft die erste Position ab, die das angegebene Element enthält.</span><span class="sxs-lookup"><span data-stu-id="86cd6-104">The `Find` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cd6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86cd6-105">Syntax</span></span>


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="86cd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86cd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86cd6-107">*pobj*</span><span class="sxs-lookup"><span data-stu-id="86cd6-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="86cd6-108">Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).</span><span class="sxs-lookup"><span data-stu-id="86cd6-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86cd6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86cd6-109">Return value</span></span>

<span data-ttu-id="86cd6-110">Gibt einen Positionswert oder **null** zurück, wenn das Element nicht in der Liste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="86cd6-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="86cd6-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86cd6-111">Requirements</span></span>



| <span data-ttu-id="86cd6-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86cd6-112">Requirement</span></span> | <span data-ttu-id="86cd6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="86cd6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86cd6-114">Header</span><span class="sxs-lookup"><span data-stu-id="86cd6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="86cd6-115"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86cd6-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="86cd6-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86cd6-116">Library</span></span><br/> | <dl> <span data-ttu-id="86cd6-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="86cd6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86cd6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86cd6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cd6-119">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="86cd6-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




