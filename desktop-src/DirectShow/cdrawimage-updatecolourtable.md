---
description: Die updatecolourtable-Methode aktualisiert die Farbtabelle mit einer neuen Palette.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Cdrawimage. updatecolourtable-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360442"
---
# <a name="cdrawimageupdatecolourtable-method"></a><span data-ttu-id="7624d-103">Cdrawimage. updatecolourtable-Methode</span><span class="sxs-lookup"><span data-stu-id="7624d-103">CDrawImage.UpdateColourTable method</span></span>

<span data-ttu-id="7624d-104">Die- `UpdateColourTable` Methode aktualisiert die Farbtabelle mit einer neuen Palette.</span><span class="sxs-lookup"><span data-stu-id="7624d-104">The `UpdateColourTable` method updates the color table with a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="7624d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7624d-105">Syntax</span></span>


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a><span data-ttu-id="7624d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7624d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7624d-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="7624d-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="7624d-108">Gerätekontext, der das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="7624d-108">Device context containing the image.</span></span>

</dd> <dt>

<span data-ttu-id="7624d-109">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="7624d-109">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="7624d-110">Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur, die die neue Palette enthält.</span><span class="sxs-lookup"><span data-stu-id="7624d-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure containing the new palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7624d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7624d-111">Return value</span></span>

<span data-ttu-id="7624d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7624d-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7624d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7624d-113">Requirements</span></span>



| <span data-ttu-id="7624d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7624d-114">Requirement</span></span> | <span data-ttu-id="7624d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7624d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7624d-116">Header</span><span class="sxs-lookup"><span data-stu-id="7624d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7624d-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7624d-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7624d-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7624d-118">Library</span></span><br/> | <dl> <span data-ttu-id="7624d-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7624d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7624d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7624d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7624d-121">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7624d-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




