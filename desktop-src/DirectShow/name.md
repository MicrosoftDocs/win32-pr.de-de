---
description: Das Name-Makro generiert eine reine debugzeichenfolge.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: Name (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373760"
---
# <a name="name"></a><span data-ttu-id="3f187-103">NAME</span><span class="sxs-lookup"><span data-stu-id="3f187-103">NAME</span></span>

<span data-ttu-id="3f187-104">Das **Name** -Makro generiert eine reine debugzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3f187-104">The **NAME** macro generates a debug-only string.</span></span>

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="3f187-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f187-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f187-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*"Straume"*</span><span class="sxs-lookup"><span data-stu-id="3f187-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="3f187-107">Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3f187-107">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f187-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f187-108">Remarks</span></span>

<span data-ttu-id="3f187-109">In Debugbuilds entspricht dieses Makro dem **Text** Makro.</span><span class="sxs-lookup"><span data-stu-id="3f187-109">In debug builds, this macro is equivalent to the **TEXT** macro.</span></span> <span data-ttu-id="3f187-110">In Einzelhandels Builds wird Sie in (TCHAR \* ) **null** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="3f187-110">In retail builds, it resolves to (TCHAR\*) **NULL**.</span></span> <span data-ttu-id="3f187-111">Dieses Makro ist hilfreich beim Deklarieren des Namens eines Objekts, das von der [**cbaseobject**](cbaseobject.md) -Klasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3f187-111">This macro is useful when declaring the name of an object that derives from the [**CBaseObject**](cbaseobject.md) class.</span></span>


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a><span data-ttu-id="3f187-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f187-112">Requirements</span></span>



| <span data-ttu-id="3f187-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f187-113">Requirement</span></span> | <span data-ttu-id="3f187-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3f187-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f187-115">Header</span><span class="sxs-lookup"><span data-stu-id="3f187-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3f187-116"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f187-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f187-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f187-117">Library</span></span><br/> | <dl> <span data-ttu-id="3f187-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3f187-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f187-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f187-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f187-120">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="3f187-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




