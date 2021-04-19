---
description: Die cimagedisplay-Klasse ist eine Hilfsklasse für GDI-Videorenderer, um das Anzeige Format zu verwalten.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Cimagedisplay-Klasse (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373965"
---
# <a name="cimagedisplay-class"></a><span data-ttu-id="5d7c7-103">Cimagedisplay-Klasse</span><span class="sxs-lookup"><span data-stu-id="5d7c7-103">CImageDisplay class</span></span>

![cimagedisplayclasshierarchy](images/wutil06.png)

<span data-ttu-id="5d7c7-105">Die- `CImageDisplay` Klasse ist eine Hilfsklasse für GDI-Videorenderer, um das Anzeige Format zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-105">The `CImageDisplay` class is a helper class for GDI video renderers to manage the display format.</span></span> <span data-ttu-id="5d7c7-106">Das-Objekt speichert eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur, die den aktuellen Anzeigemodus beschreibt, der in der Konstruktormethode des-Objekts initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-106">The object stores a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that describes the current display mode, which is initialized in the object's constructor method.</span></span> <span data-ttu-id="5d7c7-107">Die **checkmediatype** -Methode des Objekts überprüft, ob ein vorgeschlagene Medientyp mithilfe von GDI effizient gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-107">The object's **CheckMediaType** method checks whether a proposed media type can be rendered efficiently using GDI.</span></span>



| <span data-ttu-id="5d7c7-108">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="5d7c7-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="5d7c7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d7c7-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d7c7-110">**m- \_ Anzeige**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-110">**m\_Display**</span></span>](cimagedisplay-m-display.md)                    | <span data-ttu-id="5d7c7-111">**Videoinfo** -Struktur, die das aktuelle Anzeige Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-111">**VIDEOINFO** structure that describes the current display format.</span></span>                     |
| <span data-ttu-id="5d7c7-112">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="5d7c7-112">Protected Methods</span></span>                                                | <span data-ttu-id="5d7c7-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d7c7-113">Description</span></span>                                                                            |
| [<span data-ttu-id="5d7c7-114">**Checkbitfields**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-114">**CheckBitFields**</span></span>](cimagedisplay-checkbitfields.md)           | <span data-ttu-id="5d7c7-115">Überprüft die Farb Masken in einer **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-115">Validates the color masks in a **VIDEOINFO** structure.</span></span>                                |
| [<span data-ttu-id="5d7c7-116">**"Count prefixbits"**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-116">**CountPrefixBits**</span></span>](cimagedisplay-countprefixbits.md)         | <span data-ttu-id="5d7c7-117">Berechnet die Anzahl der Bits (0) am Anfang eines angegebenen Bitfelds.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-117">Calculates the number of zero bits at the start of a specified bit field.</span></span>              |
| [<span data-ttu-id="5d7c7-118">**Count-setbits**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-118">**CountSetBits**</span></span>](cimagedisplay-countsetbits.md)               | <span data-ttu-id="5d7c7-119">Gibt die Anzahl der Bits zurück, die in einem angegebenen Bitfeld auf 1 festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-119">Returns the number of bits set to 1 in a specified bit field.</span></span>                          |
| <span data-ttu-id="5d7c7-120">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="5d7c7-120">Public Methods</span></span>                                                   | <span data-ttu-id="5d7c7-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d7c7-121">Description</span></span>                                                                            |
| [<span data-ttu-id="5d7c7-122">**Checkheadergültigkeit**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-122">**CheckHeaderValidity**</span></span>](cimagedisplay-checkheadervalidity.md) | <span data-ttu-id="5d7c7-123">Überprüft eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-123">Validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>                    |
| [<span data-ttu-id="5d7c7-124">**Checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-124">**CheckMediaType**</span></span>](cimagedisplay-checkmediatype.md)           | <span data-ttu-id="5d7c7-125">Bestimmt, ob ein vorgeschlagene Medientyp mit dem Anzeige Format kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-125">Determines whether a proposed media type is compatible with the display format.</span></span>        |
| [<span data-ttu-id="5d7c7-126">**Checkpaletteheader**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-126">**CheckPaletteHeader**</span></span>](cimagedisplay-checkpaletteheader.md)   | <span data-ttu-id="5d7c7-127">Überprüft die Paletteneinträge in einer **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-127">Validates the palette entries in a **VIDEOINFO** structure.</span></span>                            |
| [<span data-ttu-id="5d7c7-128">**Checkvideotype**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-128">**CheckVideoType**</span></span>](cimagedisplay-checkvideotype.md)           | <span data-ttu-id="5d7c7-129">Überprüft, ob ein angegebenes **videoinfo** -Format mit dem Anzeige Format kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-129">Checks whether a specified **VIDEOINFO** format is compatible with the display format.</span></span> |
| [<span data-ttu-id="5d7c7-130">**Cimagedisplay**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-130">**CImageDisplay**</span></span>](cimagedisplay-cimagedisplay.md)             | <span data-ttu-id="5d7c7-131">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-131">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="5d7c7-132">**GetBitMasks**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-132">**GetBitMasks**</span></span>](cimagedisplay-getbitmasks.md)                 | <span data-ttu-id="5d7c7-133">Ruft die Farb Masken für ein angegebenes **videoinfo** -Format ab.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-133">Retrieves the color masks for a specified **VIDEOINFO** format.</span></span>                        |
| [<span data-ttu-id="5d7c7-134">**GetColorMask**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-134">**GetColourMask**</span></span>](cimagedisplay-getcolourmask.md)             | <span data-ttu-id="5d7c7-135">Ruft die Farb Masken für das aktuelle Anzeige Format ab.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-135">Retrieves the color masks for the current display format.</span></span>                              |
| [<span data-ttu-id="5d7c7-136">**Getdisplaytiefe**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-136">**GetDisplayDepth**</span></span>](cimagedisplay-getdisplaydepth.md)         | <span data-ttu-id="5d7c7-137">Ruft die Bittiefe des aktuellen Anzeigemodus ab.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-137">Retrieves the bit depth of the current display mode.</span></span>                                   |
| [<span data-ttu-id="5d7c7-138">**Getdisplayformat**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-138">**GetDisplayFormat**</span></span>](cimagedisplay-getdisplayformat.md)       | <span data-ttu-id="5d7c7-139">Ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-139">Retrieves a video format that describes the current display mode.</span></span>                      |
| [<span data-ttu-id="5d7c7-140">**Ispalettisiert**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-140">**IsPalettised**</span></span>](cimagedisplay-ispalettised.md)               | <span data-ttu-id="5d7c7-141">Gibt an, ob das aktuelle Anzeige Format palettisiert ist.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-141">Retermines whether the current display format is palettized.</span></span>                           |
| [<span data-ttu-id="5d7c7-142">**Erfrischendes Display Type**</span><span class="sxs-lookup"><span data-stu-id="5d7c7-142">**RefreshDisplayType**</span></span>](cimagedisplay-refreshdisplaytype.md)   | <span data-ttu-id="5d7c7-143">Aktualisiert das Videoformat des Objekts entsprechend der angegebenen Anzeige.</span><span class="sxs-lookup"><span data-stu-id="5d7c7-143">Updates the object's video format to match the specified display</span></span>                       |



 

## <a name="requirements"></a><span data-ttu-id="5d7c7-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d7c7-144">Requirements</span></span>



| <span data-ttu-id="5d7c7-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d7c7-145">Requirement</span></span> | <span data-ttu-id="5d7c7-146">Wert</span><span class="sxs-lookup"><span data-stu-id="5d7c7-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7c7-147">Header</span><span class="sxs-lookup"><span data-stu-id="5d7c7-147">Header</span></span><br/>  | <dl> <span data-ttu-id="5d7c7-148"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d7c7-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d7c7-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d7c7-149">Library</span></span><br/> | <dl> <span data-ttu-id="5d7c7-150">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5d7c7-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




