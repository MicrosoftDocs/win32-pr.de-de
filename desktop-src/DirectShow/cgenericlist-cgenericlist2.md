---
description: Erfahren Sie mehr über die Konstruktormethode für cgenericlist. cgenericlist (wxlist. h). Diese Methode verwendet den pName-Parameter.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Cgenericlist. cgenericlist-Konstruktor (wxlist. h)-pName-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103870216"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a><span data-ttu-id="0c481-104">Cgenericlist. cgenericlist-Konstruktor (wxlist. h)-pName-Parameter</span><span class="sxs-lookup"><span data-stu-id="0c481-104">CGenericList.CGenericList constructor (Wxlist.h) - pName parameter</span></span>

<span data-ttu-id="0c481-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0c481-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c481-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c481-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="0c481-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c481-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c481-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="0c481-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0c481-109">Zeiger auf den Namen der Liste.</span><span class="sxs-lookup"><span data-stu-id="0c481-109">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c481-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c481-110">Remarks</span></span>

<span data-ttu-id="0c481-111">Aus Effizienzgründen verwaltet die- `CGenericList` Klasse einen Cache von Listen Knoten.</span><span class="sxs-lookup"><span data-stu-id="0c481-111">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="0c481-112">Für diese Version des Konstruktors wird eine Standard Cache Größe verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c481-112">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c481-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c481-113">Requirements</span></span>

| <span data-ttu-id="0c481-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c481-114">Requirement</span></span> | <span data-ttu-id="0c481-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0c481-115">Value</span></span> |
|-|-|
| <span data-ttu-id="0c481-116">Header</span><span class="sxs-lookup"><span data-stu-id="0c481-116">Header</span></span> | <span data-ttu-id="0c481-117">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="0c481-117">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="0c481-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c481-118">Library</span></span>| <span data-ttu-id="0c481-119">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="0c481-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="0c481-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c481-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c481-121">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0c481-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




