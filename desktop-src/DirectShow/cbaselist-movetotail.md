---
description: Die Methode "muvedetail" teilt die Liste und fügt Sie an das Ende einer anderen Liste an.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Cbaselist. muvedetail-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370115"
---
# <a name="cbaselistmovetotail-method"></a><span data-ttu-id="fe2ee-103">Cbaselist. muvedetail-Methode</span><span class="sxs-lookup"><span data-stu-id="fe2ee-103">CBaseList.MoveToTail method</span></span>

<span data-ttu-id="fe2ee-104">Die `MoveToTail` -Methode teilt die Liste auf und fügt Sie an das Ende einer anderen Liste an.</span><span class="sxs-lookup"><span data-stu-id="fe2ee-104">The `MoveToTail` method splits the list and appends the head portion to the tail of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe2ee-105">Syntax</span></span>


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="fe2ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe2ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2ee-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="fe2ee-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="fe2ee-108">Positionsindikator, mit dem die Aufteilung in der Liste markiert wird.</span><span class="sxs-lookup"><span data-stu-id="fe2ee-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="fe2ee-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="fe2ee-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="fe2ee-110">Zeiger auf eine andere Liste.</span><span class="sxs-lookup"><span data-stu-id="fe2ee-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2ee-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe2ee-111">Return value</span></span>

<span data-ttu-id="fe2ee-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="fe2ee-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe2ee-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe2ee-113">Remarks</span></span>

<span data-ttu-id="fe2ee-114">Diese Methode teilt die Liste nach der durch den *POS* -Parameter angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="fe2ee-114">This method splits the list after the position specified by the *pos* parameter.</span></span> <span data-ttu-id="fe2ee-115">Der Teil Fragment verbleibt in der Liste.</span><span class="sxs-lookup"><span data-stu-id="fe2ee-115">The tail portion remains in the list.</span></span> <span data-ttu-id="fe2ee-116">Der Kopfteil wird an das Ende der anderen Liste angehängt.</span><span class="sxs-lookup"><span data-stu-id="fe2ee-116">The head portion is appended to the tail of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe2ee-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe2ee-117">Requirements</span></span>



| <span data-ttu-id="fe2ee-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe2ee-118">Requirement</span></span> | <span data-ttu-id="fe2ee-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fe2ee-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2ee-120">Header</span><span class="sxs-lookup"><span data-stu-id="fe2ee-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fe2ee-121"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe2ee-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fe2ee-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe2ee-122">Library</span></span><br/> | <dl> <span data-ttu-id="fe2ee-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fe2ee-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe2ee-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe2ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2ee-125">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fe2ee-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




