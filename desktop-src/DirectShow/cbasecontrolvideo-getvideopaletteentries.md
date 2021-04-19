---
description: Die getvideopaletteentries-Methode ruft einen Bereich von paletteneinträgen für das Video ab.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Cbasecontrolvideo. getvideopaletteentries-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366866"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a><span data-ttu-id="87ce5-103">Cbasecontrolvideo. getvideopaletteentries-Methode</span><span class="sxs-lookup"><span data-stu-id="87ce5-103">CBaseControlVideo.GetVideoPaletteEntries method</span></span>

<span data-ttu-id="87ce5-104">Die- `GetVideoPaletteEntries` Methode ruft einen Bereich von paletteneinträgen für das Video ab.</span><span class="sxs-lookup"><span data-stu-id="87ce5-104">The `GetVideoPaletteEntries` method retrieves a range of palette entries for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ce5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87ce5-105">Syntax</span></span>


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a><span data-ttu-id="87ce5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87ce5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ce5-107">*Start Index*</span><span class="sxs-lookup"><span data-stu-id="87ce5-107">*StartIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="87ce5-108">Der null basierte Start Paletteneintrag.</span><span class="sxs-lookup"><span data-stu-id="87ce5-108">Zero-based start palette entry.</span></span>

</dd> <dt>

<span data-ttu-id="87ce5-109">*Gewinner*</span><span class="sxs-lookup"><span data-stu-id="87ce5-109">*Entries*</span></span> 
</dt> <dd>

<span data-ttu-id="87ce5-110">Anzahl der erforderlichen Einträge.</span><span class="sxs-lookup"><span data-stu-id="87ce5-110">Number of entries required.</span></span>

</dd> <dt>

<span data-ttu-id="87ce5-111">*vorab bereitgestellt*</span><span class="sxs-lookup"><span data-stu-id="87ce5-111">*pRetrieved*</span></span> 
</dt> <dd>

<span data-ttu-id="87ce5-112">Ein Zeiger auf die Anzahl der gewonnenen Farben.</span><span class="sxs-lookup"><span data-stu-id="87ce5-112">Pointer to the number of colors obtained.</span></span>

</dd> <dt>

<span data-ttu-id="87ce5-113">*pPalette*</span><span class="sxs-lookup"><span data-stu-id="87ce5-113">*pPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="87ce5-114">Zeiger auf den Ausgabepuffer für Farben.</span><span class="sxs-lookup"><span data-stu-id="87ce5-114">Pointer to output buffer for colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ce5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87ce5-115">Return value</span></span>

<span data-ttu-id="87ce5-116">Gibt noError zurück, wenn nicht genügend Arbeitsspeicher verfügbar ist, Vfw \_ e \_ keine \_ Palette \_ verfügbar ist, wenn die Videobeispiele keine Farbpalette haben, e \_ OutOfMemory, wenn nicht genügend Arbeitsspeicher verfügbar ist, e \_ invalidArg if *startIndex* ist ungültig, oder S \_ false, wenn die Palette keine Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="87ce5-116">Returns NOERROR if successful, VFW\_E\_NO\_PALETTE\_AVAILABLE if the video samples has no color palette, E\_OUTOFMEMORY if there is not enough memory available, E\_INVALIDARG if *StartIndex* is invalid, or S\_FALSE if there are no colors in the palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ce5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87ce5-117">Remarks</span></span>

<span data-ttu-id="87ce5-118">Diese Member-Funktion gibt die aktuelle Palette des Videos als Array zurück, das vom Benutzer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="87ce5-118">This member function returns the current palette of the video as an array allocated by the user.</span></span> <span data-ttu-id="87ce5-119">Um konsistent zu bleiben, verwenden Sie die Elemente in der Win32 **PaletteEntry** -Struktur, um die Farben anstelle der Elemente in der **rgbquad** -Struktur zurückzugeben (obwohl der-Parameter ein **Long**-Parameter ist).</span><span class="sxs-lookup"><span data-stu-id="87ce5-119">To remain consistent, use the members in the Win32 **PALETTEENTRY** structure to return the colors, rather than the members in the **RGBQUAD** structure (although the parameter is a **LONG**).</span></span> <span data-ttu-id="87ce5-120">Der Arbeitsspeicher wird vom Aufrufer zugeordnet. Kopieren Sie also alle nacheinander.</span><span class="sxs-lookup"><span data-stu-id="87ce5-120">The memory is allocated by the caller, so simply copy each in turn.</span></span> <span data-ttu-id="87ce5-121">Stellen Sie fest, dass die Anzahl der angeforderten Einträge und der Offset der Startposition gültig sind.</span><span class="sxs-lookup"><span data-stu-id="87ce5-121">Determine that the number of entries requested and the start position offset are both valid.</span></span> <span data-ttu-id="87ce5-122">Wenn die Anzahl der Einträge NULL ergibt, wird ein S false-Code zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="87ce5-122">If the number of entries evaluates to zero, return an S\_FALSE code.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ce5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87ce5-123">Requirements</span></span>



| <span data-ttu-id="87ce5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87ce5-124">Requirement</span></span> | <span data-ttu-id="87ce5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="87ce5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ce5-126">Header</span><span class="sxs-lookup"><span data-stu-id="87ce5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="87ce5-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87ce5-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87ce5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87ce5-128">Library</span></span><br/> | <dl> <span data-ttu-id="87ce5-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="87ce5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ce5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87ce5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ce5-131">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="87ce5-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




