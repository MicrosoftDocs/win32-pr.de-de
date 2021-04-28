---
description: 'CBaseList.CBaseList-Konstruktor: Konstruktormethode.'
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: CBaseList.CBaseList-Konstruktor (Wxlist.h)
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096327"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="ab98a-103">CBaseList.CBaseList-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ab98a-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="ab98a-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ab98a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab98a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab98a-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="ab98a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab98a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab98a-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ab98a-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ab98a-108">Zeiger auf den Namen der Liste.</span><span class="sxs-lookup"><span data-stu-id="ab98a-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab98a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab98a-109">Remarks</span></span>

<span data-ttu-id="ab98a-110">Zur Effizienz verwaltet `CBaseList` die -Klasse einen Cache von Listenknoten.</span><span class="sxs-lookup"><span data-stu-id="ab98a-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="ab98a-111">Diese Version des Konstruktors verwendet eine Standardcachegröße.</span><span class="sxs-lookup"><span data-stu-id="ab98a-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab98a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab98a-112">Requirements</span></span>



| <span data-ttu-id="ab98a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab98a-113">Requirement</span></span> | <span data-ttu-id="ab98a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ab98a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab98a-115">Header</span><span class="sxs-lookup"><span data-stu-id="ab98a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ab98a-116"><dt>Wxlist.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="ab98a-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ab98a-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab98a-117">Library</span></span><br/> | <dl> <span data-ttu-id="ab98a-118"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ab98a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab98a-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab98a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab98a-120">**CBaseList-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ab98a-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




