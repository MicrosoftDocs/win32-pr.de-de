---
description: Die getsourcerect-Methode ruft das aktuelle Quell Rechteck ab.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Cdrawimage. getsourcerect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366735"
---
# <a name="cdrawimagegetsourcerect-method"></a><span data-ttu-id="87841-103">Cdrawimage. getsourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="87841-103">CDrawImage.GetSourceRect method</span></span>

<span data-ttu-id="87841-104">Die- `GetSourceRect` Methode ruft das aktuelle Quell Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="87841-104">The `GetSourceRect` method retrieves the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="87841-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87841-105">Syntax</span></span>


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="87841-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87841-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87841-107">*psourcerect*</span><span class="sxs-lookup"><span data-stu-id="87841-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="87841-108">Ein Zeiger auf eine **Rect** -Struktur, die das Quell Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="87841-108">Pointer to a **RECT** structure that receives the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87841-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87841-109">Return value</span></span>

<span data-ttu-id="87841-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="87841-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="87841-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87841-111">Requirements</span></span>



| <span data-ttu-id="87841-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87841-112">Requirement</span></span> | <span data-ttu-id="87841-113">Wert</span><span class="sxs-lookup"><span data-stu-id="87841-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87841-114">Header</span><span class="sxs-lookup"><span data-stu-id="87841-114">Header</span></span><br/>  | <dl> <span data-ttu-id="87841-115"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87841-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87841-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87841-116">Library</span></span><br/> | <dl> <span data-ttu-id="87841-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="87841-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87841-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87841-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87841-119">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="87841-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




