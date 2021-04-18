---
description: Die getColorMask-Methode ruft die Farb Masken für das aktuelle Anzeige Format ab.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Cimagedisplay. getColorMask-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365810"
---
# <a name="cimagedisplaygetcolourmask-method"></a><span data-ttu-id="1848b-103">Cimagedisplay. getColorMask-Methode</span><span class="sxs-lookup"><span data-stu-id="1848b-103">CImageDisplay.GetColourMask method</span></span>

<span data-ttu-id="1848b-104">Die- `GetColourMask` Methode ruft die Farb Masken für das aktuelle Anzeige Format ab.</span><span class="sxs-lookup"><span data-stu-id="1848b-104">The `GetColourMask` method retrieves the color masks for the current display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="1848b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1848b-105">Syntax</span></span>


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a><span data-ttu-id="1848b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1848b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1848b-107">*pmaskred*</span><span class="sxs-lookup"><span data-stu-id="1848b-107">*pMaskRed*</span></span> 
</dt> <dd>

<span data-ttu-id="1848b-108">Ein Zeiger auf eine Variable, die die rote Komponenten Maske empfängt.</span><span class="sxs-lookup"><span data-stu-id="1848b-108">Pointer to a variable that receives the red-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="1848b-109">*pmaskgreen*</span><span class="sxs-lookup"><span data-stu-id="1848b-109">*pMaskGreen*</span></span> 
</dt> <dd>

<span data-ttu-id="1848b-110">Ein Zeiger auf eine Variable, die die grüne Komponenten Maske empfängt.</span><span class="sxs-lookup"><span data-stu-id="1848b-110">Pointer to a variable that receives the green-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="1848b-111">*pmaskblue*</span><span class="sxs-lookup"><span data-stu-id="1848b-111">*pMaskBlue*</span></span> 
</dt> <dd>

<span data-ttu-id="1848b-112">Ein Zeiger auf eine Variable, die die blaue Komponenten Maske empfängt.</span><span class="sxs-lookup"><span data-stu-id="1848b-112">Pointer to a variable that receives the blue-component mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1848b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1848b-113">Return value</span></span>

<span data-ttu-id="1848b-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1848b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1848b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1848b-115">Requirements</span></span>



| <span data-ttu-id="1848b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1848b-116">Requirement</span></span> | <span data-ttu-id="1848b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1848b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1848b-118">Header</span><span class="sxs-lookup"><span data-stu-id="1848b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1848b-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1848b-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1848b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1848b-120">Library</span></span><br/> | <dl> <span data-ttu-id="1848b-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1848b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1848b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1848b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1848b-123">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1848b-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




