---
description: Konstruktormethode.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Cimagepalette. cimagepalette-Konstruktor (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366875"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="563e2-103">Cimagepalette. cimagepalette-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="563e2-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="563e2-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="563e2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="563e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="563e2-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="563e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="563e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="563e2-107">*pbasefilter*</span><span class="sxs-lookup"><span data-stu-id="563e2-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="563e2-108">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="563e2-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="563e2-109">*pbasewindow*</span><span class="sxs-lookup"><span data-stu-id="563e2-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="563e2-110">Zeiger auf ein **cbasewindow** -Objekt, das das Fenster verwaltet, in dem die Palette realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="563e2-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="563e2-111">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="563e2-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="563e2-112">*pdrawimage*</span><span class="sxs-lookup"><span data-stu-id="563e2-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="563e2-113">Zeiger auf ein **cdrawimage** -Objekt, das das Videobild zeichnet.</span><span class="sxs-lookup"><span data-stu-id="563e2-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="563e2-114">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="563e2-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="563e2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="563e2-115">Requirements</span></span>



| <span data-ttu-id="563e2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="563e2-116">Requirement</span></span> | <span data-ttu-id="563e2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="563e2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="563e2-118">Header</span><span class="sxs-lookup"><span data-stu-id="563e2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="563e2-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="563e2-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="563e2-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="563e2-120">Library</span></span><br/> | <dl> <span data-ttu-id="563e2-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="563e2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="563e2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="563e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563e2-123">**Cimagepalette-Klasse**</span><span class="sxs-lookup"><span data-stu-id="563e2-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




