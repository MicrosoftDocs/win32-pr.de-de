---
description: Die PreparePalette-Methode richtet eine Palette basierend auf einem Medientyp des besitzenden Filters ein.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Cimagepalette. PreparePalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369404"
---
# <a name="cimagepalettepreparepalette-method"></a><span data-ttu-id="b9540-103">Cimagepalette. PreparePalette-Methode</span><span class="sxs-lookup"><span data-stu-id="b9540-103">CImagePalette.PreparePalette method</span></span>

<span data-ttu-id="b9540-104">Die- `PreparePalette` Methode richtet eine Palette auf der Grundlage eines Medientyps aus dem besitzenden Filter ein.</span><span class="sxs-lookup"><span data-stu-id="b9540-104">The `PreparePalette` method sets up a palette, based on a media type from the owning filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9540-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9540-105">Syntax</span></span>


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="b9540-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9540-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9540-107">*pmtnew*</span><span class="sxs-lookup"><span data-stu-id="b9540-107">*pmtNew*</span></span> 
</dt> <dd>

<span data-ttu-id="b9540-108">Zeiger auf den neuen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="b9540-108">Pointer to the new media type.</span></span> <span data-ttu-id="b9540-109">Der Format Block muss eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="b9540-109">The format block must be a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b9540-110">*pmtold*</span><span class="sxs-lookup"><span data-stu-id="b9540-110">*pmtOld*</span></span> 
</dt> <dd>

<span data-ttu-id="b9540-111">Zeiger auf den alten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="b9540-111">Pointer to the old media type.</span></span> <span data-ttu-id="b9540-112">Wenn der Medientyp zum ersten Mal festgelegt wird, kann dieser Parameter ein leerer Typ ohne Format Block sein.</span><span class="sxs-lookup"><span data-stu-id="b9540-112">If the media type is being set for the first time, this parameter can be an empty type with no format block.</span></span> <span data-ttu-id="b9540-113">Andernfalls muss der Format Block eine **videoinfoheader** -Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="b9540-113">Otherwise, the format block must be a **VIDEOINFOHEADER** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b9540-114">*szdevice*</span><span class="sxs-lookup"><span data-stu-id="b9540-114">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b9540-115">Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9540-115">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="b9540-116">Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9540-116">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9540-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9540-117">Return value</span></span>

<span data-ttu-id="b9540-118">Gibt s \_ OK zurück, wenn die Palette aktualisiert wurde, oder s \_ false, wenn sich die Palette nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b9540-118">Returns S\_OK if the palette was updated, or S\_FALSE if the palette did not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9540-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9540-119">Remarks</span></span>

<span data-ttu-id="b9540-120">Wenn die Palette aktualisiert werden muss, führt diese Methode die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="b9540-120">If the palette needs to be updated, this method performs the following actions:</span></span>

-   <span data-ttu-id="b9540-121">Ruft [**cimagepalette:: makepalette**](cimagepalette-makepalette.md) auf, um eine neue logische Palette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9540-121">Calls [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) to create a new logical palette.</span></span>
-   <span data-ttu-id="b9540-122">Sendet ein [**\_ \_ geändertes**](ec-palette-changed.md) Ereignis der EC-Palette an den Filter Diagramm-Manager.</span><span class="sxs-lookup"><span data-stu-id="b9540-122">Sends an [**EC\_PALETTE\_CHANGED**](ec-palette-changed.md) event to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="b9540-123">Ruft [**cbasewindow:: SetPalette**](cbasewindow-setpalette.md) für das **cbasewindow** -Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="b9540-123">Calls [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) on the **CBaseWindow** object.</span></span>
-   <span data-ttu-id="b9540-124">Ruft [**cdrawimage:: incrementpaletteversion**](cdrawimage-incrementpaletteversion.md) für das **cdrawimage** -Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="b9540-124">Calls [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) on the **CDrawImage** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9540-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9540-125">Requirements</span></span>



| <span data-ttu-id="b9540-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9540-126">Requirement</span></span> | <span data-ttu-id="b9540-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b9540-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9540-128">Header</span><span class="sxs-lookup"><span data-stu-id="b9540-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b9540-129"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9540-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9540-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9540-130">Library</span></span><br/> | <dl> <span data-ttu-id="b9540-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b9540-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9540-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9540-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9540-133">**Cimagepalette-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b9540-133">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




