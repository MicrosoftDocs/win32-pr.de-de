---
description: Die isequalobject-Funktion überprüft, ob sich zwei Schnittstellen auf demselben Objekt befinden.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Isequalobject-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370018"
---
# <a name="isequalobject-function"></a><span data-ttu-id="75207-103">Isequalobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="75207-103">IsEqualObject function</span></span>

<span data-ttu-id="75207-104">Die- `IsEqualObject` Funktion überprüft, ob sich zwei Schnittstellen auf demselben Objekt befinden.</span><span class="sxs-lookup"><span data-stu-id="75207-104">The `IsEqualObject` function checks if two interfaces are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75207-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75207-105">Syntax</span></span>


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a><span data-ttu-id="75207-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75207-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75207-107">*pfirst*</span><span class="sxs-lookup"><span data-stu-id="75207-107">*pFirst*</span></span> 
</dt> <dd>

<span data-ttu-id="75207-108">Zeiger auf eine-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="75207-108">Pointer to one interface.</span></span>

</dd> <dt>

<span data-ttu-id="75207-109">*psecond*</span><span class="sxs-lookup"><span data-stu-id="75207-109">*pSecond*</span></span> 
</dt> <dd>

<span data-ttu-id="75207-110">Zeiger auf die andere-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="75207-110">Pointer to the other interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75207-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75207-111">Return value</span></span>

<span data-ttu-id="75207-112">Gibt " **true** " zurück, wenn sich die Schnittstellen im selben Objekt befinden, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="75207-112">Returns **TRUE** if the interfaces are both on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="75207-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75207-113">Requirements</span></span>



| <span data-ttu-id="75207-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75207-114">Requirement</span></span> | <span data-ttu-id="75207-115">Wert</span><span class="sxs-lookup"><span data-stu-id="75207-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75207-116">Header</span><span class="sxs-lookup"><span data-stu-id="75207-116">Header</span></span><br/>  | <dl> <span data-ttu-id="75207-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75207-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="75207-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75207-118">Library</span></span><br/> | <dl> <span data-ttu-id="75207-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="75207-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75207-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75207-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75207-121">Diverse Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="75207-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




