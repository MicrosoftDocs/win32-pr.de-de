---
description: 'CSource.CSource-Konstruktor : Konstruktormethode.'
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: CSource.CSource-Konstruktor (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fab398f3f4e3fdd8c23ce1e1c08f5c130478dfb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085358"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="6973c-103">CSource.CSource-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="6973c-103">CSource.CSource constructor</span></span>

<span data-ttu-id="6973c-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="6973c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6973c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6973c-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="6973c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6973c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6973c-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6973c-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6973c-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="6973c-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="6973c-109">Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="6973c-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6973c-110">*lpunk*</span><span class="sxs-lookup"><span data-stu-id="6973c-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="6973c-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="6973c-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="6973c-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="6973c-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6973c-113">Legen Sie andernfalls diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="6973c-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6973c-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="6973c-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="6973c-115">Klassenbezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="6973c-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6973c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6973c-116">Requirements</span></span>



| <span data-ttu-id="6973c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6973c-117">Requirement</span></span> | <span data-ttu-id="6973c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6973c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6973c-119">Header</span><span class="sxs-lookup"><span data-stu-id="6973c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6973c-120"><dt>Source.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6973c-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6973c-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6973c-121">Library</span></span><br/> | <dl> <span data-ttu-id="6973c-122"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6973c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6973c-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6973c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6973c-124">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6973c-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




