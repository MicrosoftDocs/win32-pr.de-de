---
description: Die equalpins-Funktion überprüft, ob sich zwei Pins auf demselben Objekt befinden.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Equalpins-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357950"
---
# <a name="equalpins-function"></a><span data-ttu-id="8af31-103">Equalpins-Funktion</span><span class="sxs-lookup"><span data-stu-id="8af31-103">EqualPins function</span></span>

<span data-ttu-id="8af31-104">Die equalpins-Funktion überprüft, ob sich zwei Pins auf demselben Objekt befinden.</span><span class="sxs-lookup"><span data-stu-id="8af31-104">The EqualPins function checks if two pins are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8af31-105">Syntax</span></span>


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a><span data-ttu-id="8af31-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8af31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af31-107">*pPin1*</span><span class="sxs-lookup"><span data-stu-id="8af31-107">*pPin1*</span></span> 
</dt> <dd>

<span data-ttu-id="8af31-108">Zeiger auf eine PIN.</span><span class="sxs-lookup"><span data-stu-id="8af31-108">Pointer to one pin.</span></span>

</dd> <dt>

<span data-ttu-id="8af31-109">*pPin2*</span><span class="sxs-lookup"><span data-stu-id="8af31-109">*pPin2*</span></span> 
</dt> <dd>

<span data-ttu-id="8af31-110">Zeiger auf die andere PIN.</span><span class="sxs-lookup"><span data-stu-id="8af31-110">Pointer to the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af31-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8af31-111">Return value</span></span>

<span data-ttu-id="8af31-112">Gibt **true** zurück, wenn sich beide Pins auf demselben Objekt befinden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8af31-112">Returns **TRUE** if both pins are on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af31-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8af31-113">Requirements</span></span>



| <span data-ttu-id="8af31-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8af31-114">Requirement</span></span> | <span data-ttu-id="8af31-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8af31-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af31-116">Header</span><span class="sxs-lookup"><span data-stu-id="8af31-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8af31-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8af31-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8af31-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8af31-118">Library</span></span><br/> | <dl> <span data-ttu-id="8af31-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8af31-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af31-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8af31-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af31-121">Diverse Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="8af31-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




