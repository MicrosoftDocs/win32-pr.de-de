---
description: Die Methode "schuldupdate" bestimmt, ob eine neue Palette erstellt werden muss.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Cimagepalette. Schulter Dupdate-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373621"
---
# <a name="cimagepaletteshouldupdate-method"></a><span data-ttu-id="c861f-103">Cimagepalette. schuldupdate-Methode</span><span class="sxs-lookup"><span data-stu-id="c861f-103">CImagePalette.ShouldUpdate method</span></span>

<span data-ttu-id="c861f-104">Die- `ShouldUpdate` Methode bestimmt, ob eine neue Palette erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c861f-104">The `ShouldUpdate` method determines whether it is necessary to create a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="c861f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c861f-105">Syntax</span></span>


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c861f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c861f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c861f-107">*pnetwinfo*</span><span class="sxs-lookup"><span data-stu-id="c861f-107">*pNewInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c861f-108">Ein Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur, die die neue Farbtabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c861f-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure containing the new color table.</span></span>

</dd> <dt>

<span data-ttu-id="c861f-109">*poldinfo*</span><span class="sxs-lookup"><span data-stu-id="c861f-109">*pOldInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c861f-110">Zeiger auf eine **videoinfoheader** -Struktur, die die alte Farbtabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c861f-110">Pointer to a **VIDEOINFOHEADER** structure containing the old color table.</span></span> <span data-ttu-id="c861f-111">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="c861f-111">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c861f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c861f-112">Return value</span></span>

<span data-ttu-id="c861f-113">Gibt **true** zurück, wenn die Palette aktualisiert werden muss, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c861f-113">Returns **TRUE** if the palette needs to be updated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c861f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c861f-114">Remarks</span></span>

-   <span data-ttu-id="c861f-115">Wenn keine **videoinfoheader** -Struktur eine Farbtabelle enthält, gibt die Methode **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c861f-115">If neither **VIDEOINFOHEADER** structure contains a color table, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="c861f-116">Wenn nur eine Struktur eine Farbtabelle enthält oder *poldinfo* **null** ist, gibt die Methode **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="c861f-116">If only one structure contains a color table, or if *pOldInfo* is **NULL**, the method returns **TRUE**.</span></span>
-   <span data-ttu-id="c861f-117">Wenn beide Strukturen Farbtabellen enthalten und die Farbeinträge Stimmen, gibt die Methode **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c861f-117">If both structures contain color tables, and the color entries match, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="c861f-118">Wenn beide Strukturen Farbtabellen enthalten, die Farbeinträge jedoch nicht stimmen, gibt die Methode **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="c861f-118">If both structures contain color tables, but the color entries do not match, the method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c861f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c861f-119">Requirements</span></span>



| <span data-ttu-id="c861f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c861f-120">Requirement</span></span> | <span data-ttu-id="c861f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c861f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c861f-122">Header</span><span class="sxs-lookup"><span data-stu-id="c861f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c861f-123"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c861f-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c861f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c861f-124">Library</span></span><br/> | <dl> <span data-ttu-id="c861f-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c861f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c861f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c861f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c861f-127">**Cimagepalette-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c861f-127">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




