---
description: Konstruktormethode.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Cbaselist. cbaselist (TCHAR *, int)-Konstruktor (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355904"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="47383-103">Cbaselist. cbaselist (TCHAR \* , int)-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="47383-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="47383-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="47383-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47383-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47383-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="47383-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47383-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47383-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="47383-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="47383-108">Zeiger auf den Namen der Liste.</span><span class="sxs-lookup"><span data-stu-id="47383-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="47383-109">*IItems*</span><span class="sxs-lookup"><span data-stu-id="47383-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="47383-110">Größe des Knoten Caches.</span><span class="sxs-lookup"><span data-stu-id="47383-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47383-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47383-111">Remarks</span></span>

<span data-ttu-id="47383-112">Aus Effizienzgründen verwaltet die- `CBaseList` Klasse einen Cache von Listen Knoten.</span><span class="sxs-lookup"><span data-stu-id="47383-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="47383-113">Wenn Sie ungefähr wissen, wie viele Elemente in der Liste enthalten sein werden, verwenden Sie diese Version des Konstruktors.</span><span class="sxs-lookup"><span data-stu-id="47383-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="47383-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47383-114">Requirements</span></span>



| <span data-ttu-id="47383-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47383-115">Requirement</span></span> | <span data-ttu-id="47383-116">Wert</span><span class="sxs-lookup"><span data-stu-id="47383-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47383-117">Header</span><span class="sxs-lookup"><span data-stu-id="47383-117">Header</span></span><br/>  | <dl> <span data-ttu-id="47383-118"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47383-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="47383-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47383-119">Library</span></span><br/> | <dl> <span data-ttu-id="47383-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="47383-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47383-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47383-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47383-122">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="47383-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




