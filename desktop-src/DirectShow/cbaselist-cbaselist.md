---
description: 'CBaseList.CBaseList(TCHAR, \* INT)-Konstruktor : Konstruktormethode.'
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: CBaseList.CBaseList(TCHAR*, INT)-Konstruktor (Wxlist.h)
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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099638"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="de040-103">CBaseList.CBaseList(TCHAR, \* INT)-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="de040-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="de040-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="de040-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de040-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de040-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="de040-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de040-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de040-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="de040-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="de040-108">Zeiger auf den Namen der Liste.</span><span class="sxs-lookup"><span data-stu-id="de040-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="de040-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="de040-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="de040-110">Größe des Knotencaches.</span><span class="sxs-lookup"><span data-stu-id="de040-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de040-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de040-111">Remarks</span></span>

<span data-ttu-id="de040-112">Zur Effizienz verwaltet `CBaseList` die -Klasse einen Cache von Listenknoten.</span><span class="sxs-lookup"><span data-stu-id="de040-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="de040-113">Wenn Sie ungefähr wissen, wie viele Elemente die Liste enthalten wird, verwenden Sie diese Version des Konstruktors.</span><span class="sxs-lookup"><span data-stu-id="de040-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="de040-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de040-114">Requirements</span></span>



| <span data-ttu-id="de040-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de040-115">Requirement</span></span> | <span data-ttu-id="de040-116">Wert</span><span class="sxs-lookup"><span data-stu-id="de040-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de040-117">Header</span><span class="sxs-lookup"><span data-stu-id="de040-117">Header</span></span><br/>  | <dl> <span data-ttu-id="de040-118"><dt>Wxlist.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="de040-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="de040-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de040-119">Library</span></span><br/> | <dl> <span data-ttu-id="de040-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="de040-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de040-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="de040-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de040-122">**CBaseList-Klasse**</span><span class="sxs-lookup"><span data-stu-id="de040-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




