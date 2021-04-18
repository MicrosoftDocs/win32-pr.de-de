---
description: Die AddBefore-Methode fügt eine Liste vor der angegebenen Position ein.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Cbaselist. AddBefore-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372415"
---
# <a name="cbaselistaddbefore-method"></a><span data-ttu-id="9663f-103">Cbaselist. AddBefore-Methode</span><span class="sxs-lookup"><span data-stu-id="9663f-103">CBaseList.AddBefore method</span></span>

<span data-ttu-id="9663f-104">Die- `AddBefore` Methode fügt eine Liste vor der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="9663f-104">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="9663f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9663f-105">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="9663f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9663f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9663f-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="9663f-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="9663f-108">Die Position, an der die Liste eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9663f-108">Position before which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="9663f-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="9663f-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="9663f-110">Ein Zeiger auf die einzufügende Liste.</span><span class="sxs-lookup"><span data-stu-id="9663f-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9663f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9663f-111">Return value</span></span>

<span data-ttu-id="9663f-112">Gibt **true** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9663f-112">Returns **TRUE** if successful.</span></span> <span data-ttu-id="9663f-113">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9663f-113">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9663f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9663f-114">Remarks</span></span>

<span data-ttu-id="9663f-115">Vorhandene positionsindikatoren, einschließlich der im *POS* -Parameter angegebenen, bleiben gültig.</span><span class="sxs-lookup"><span data-stu-id="9663f-115">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="9663f-116">Wenn die Methode fehlschlägt, wurden möglicherweise einige der Elemente hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9663f-116">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="9663f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9663f-117">Requirements</span></span>



| <span data-ttu-id="9663f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9663f-118">Requirement</span></span> | <span data-ttu-id="9663f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9663f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9663f-120">Header</span><span class="sxs-lookup"><span data-stu-id="9663f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9663f-121"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9663f-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9663f-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9663f-122">Library</span></span><br/> | <dl> <span data-ttu-id="9663f-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9663f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9663f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9663f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9663f-125">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9663f-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




