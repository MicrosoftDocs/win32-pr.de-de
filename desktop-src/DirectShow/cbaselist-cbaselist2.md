---
description: Konstruktormethode.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Cbaselist. cbaselist-Konstruktor (wxlist. h)
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
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358111"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="da570-103">Cbaselist. cbaselist-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="da570-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="da570-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="da570-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="da570-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da570-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="da570-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da570-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da570-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="da570-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="da570-108">Zeiger auf den Namen der Liste.</span><span class="sxs-lookup"><span data-stu-id="da570-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da570-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da570-109">Remarks</span></span>

<span data-ttu-id="da570-110">Aus Effizienzgründen verwaltet die- `CBaseList` Klasse einen Cache von Listen Knoten.</span><span class="sxs-lookup"><span data-stu-id="da570-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="da570-111">Für diese Version des Konstruktors wird eine Standard Cache Größe verwendet.</span><span class="sxs-lookup"><span data-stu-id="da570-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="da570-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da570-112">Requirements</span></span>



| <span data-ttu-id="da570-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da570-113">Requirement</span></span> | <span data-ttu-id="da570-114">Wert</span><span class="sxs-lookup"><span data-stu-id="da570-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da570-115">Header</span><span class="sxs-lookup"><span data-stu-id="da570-115">Header</span></span><br/>  | <dl> <span data-ttu-id="da570-116"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da570-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="da570-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da570-117">Library</span></span><br/> | <dl> <span data-ttu-id="da570-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="da570-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da570-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da570-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da570-120">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="da570-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




