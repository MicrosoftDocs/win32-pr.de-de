---
description: 'CImagePalette.CImagePalette-Konstruktor: Konstruktormethode.'
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: CImagePalette.CImagePalette-Konstruktor (Winutil.h)
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
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085678"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="600c7-103">CImagePalette.CImagePalette-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="600c7-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="600c7-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="600c7-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="600c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="600c7-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="600c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="600c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="600c7-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="600c7-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="600c7-108">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="600c7-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="600c7-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="600c7-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="600c7-110">Zeiger auf ein **CBaseWindow-Objekt,** das das Fenster verwaltet, in dem die Palette realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="600c7-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="600c7-111">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="600c7-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="600c7-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="600c7-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="600c7-113">Zeiger auf ein **CDrawImage-Objekt,** das das Videobild zeichnet.</span><span class="sxs-lookup"><span data-stu-id="600c7-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="600c7-114">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="600c7-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="600c7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="600c7-115">Requirements</span></span>



| <span data-ttu-id="600c7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="600c7-116">Requirement</span></span> | <span data-ttu-id="600c7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="600c7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600c7-118">Header</span><span class="sxs-lookup"><span data-stu-id="600c7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="600c7-119"><dt>Winutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="600c7-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="600c7-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="600c7-120">Library</span></span><br/> | <dl> <span data-ttu-id="600c7-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="600c7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="600c7-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="600c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600c7-123">**CImagePalette-Klasse**</span><span class="sxs-lookup"><span data-stu-id="600c7-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




