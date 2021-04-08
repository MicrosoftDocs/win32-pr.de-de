---
title: Portieren von Farb aufrufen
description: In der folgenden Tabelle sind die Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- IRIS GL portieren, Farbe
- Portieren von IRIS GL, Color
- Portieren auf OpenGL von IRIS GL, Color
- OpenGL-Portierung von IRIS GL, Color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708465"
---
# <a name="porting-color-calls"></a><span data-ttu-id="5ebf4-107">Portieren von Farb aufrufen</span><span class="sxs-lookup"><span data-stu-id="5ebf4-107">Porting Color Calls</span></span>

<span data-ttu-id="5ebf4-108">In der folgenden Tabelle sind die Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-108">The following table lists IRIS GL color functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="5ebf4-109">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ebf4-109">IRIS GL function</span></span>                  | <span data-ttu-id="5ebf4-110">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ebf4-110">OpenGL function</span></span>                                                                                                                               | <span data-ttu-id="5ebf4-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5ebf4-111">Meaning</span></span>                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ebf4-112">**c**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-112">**c**</span></span>                             | [<span data-ttu-id="5ebf4-113">glcolor</span><span class="sxs-lookup"><span data-stu-id="5ebf4-113">glColor</span></span>](glcolor-functions.md)                                                                                                              | <span data-ttu-id="5ebf4-114">Legt RGB-Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-114">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="5ebf4-115">**color**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-115">**color**</span></span>                         | [<span data-ttu-id="5ebf4-116">glindex</span><span class="sxs-lookup"><span data-stu-id="5ebf4-116">glIndex</span></span>](glindex-functions.md)                                                                                                              | <span data-ttu-id="5ebf4-117">Legt den Farbindex fest.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-117">Sets the color index.</span></span>                                |
| <span data-ttu-id="5ebf4-118">**GetColor**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-118">**getcolor**</span></span>                      | <span data-ttu-id="5ebf4-119">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ Aktueller Index von GL \_ )</span><span class="sxs-lookup"><span data-stu-id="5ebf4-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_CURRENT\_INDEX )</span></span>                                               | <span data-ttu-id="5ebf4-120">Gibt den aktuellen Farbindex zurück.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-120">Returns the current color index.</span></span>                     |
| <span data-ttu-id="5ebf4-121">**getmcolor**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-121">**getmcolor**</span></span>                     |                                                                                                                                               | <span data-ttu-id="5ebf4-122">Ruft eine Kopie der RGB-Werte für einen Farb Zuordnungs Eintrag ab.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-122">Gets a copy of the RGB values for a color map entry.</span></span> |
| <span data-ttu-id="5ebf4-123">**grgbcolor**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-123">**gRGBcolor**</span></span>                     | <span data-ttu-id="5ebf4-124">**glget**(aktuelle GL- \_ \_ Farbe)</span><span class="sxs-lookup"><span data-stu-id="5ebf4-124">**glGet**( GL\_CURRENT\_COLOR )</span></span>                                                                                                               | <span data-ttu-id="5ebf4-125">Ruft die aktuellen RGB-Farbwerte ab.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-125">Gets the current RGB color values.</span></span>                   |
| <span data-ttu-id="5ebf4-126">**mapcolor**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-126">**mapcolor**</span></span>                      |                                                                                                                                               |                                                      |
| <span data-ttu-id="5ebf4-127">**RGBColor**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-127">**RGBcolor**</span></span>                      | <span data-ttu-id="5ebf4-128">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-128">**glColor**</span></span>                                                                                                                                   | <span data-ttu-id="5ebf4-129">Legt RGB-Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-129">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="5ebf4-130">**Schreibzugriff**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-130">**writemask**</span></span>                     | [<span data-ttu-id="5ebf4-131">**glindexmask**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-131">**glIndexMask**</span></span>](glindexmask.md)                                                                                                            | <span data-ttu-id="5ebf4-132">Legt die Farb Maske für den Farb Index Modus fest.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-132">Sets the color-index mode color mask.</span></span>                |
| <span data-ttu-id="5ebf4-133">**wmpackrgbschreitefrage**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-133">**wmpackRGBwritemask**</span></span><br/> | [<span data-ttu-id="5ebf4-134">**glcolormask**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-134">**glColorMask**</span></span>](glcolormask.md)                                                                                                            | <span data-ttu-id="5ebf4-135">Legt die RGB-farbmodusmaske fest.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-135">Sets the RGB color mode mask.</span></span>                        |
| <span data-ttu-id="5ebf4-136">**getschreitefrage**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-136">**getwritemask**</span></span>                  | <span data-ttu-id="5ebf4-137">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ - \_ farbschreibfrage)**glget**(GL- \_ Index \_ schreibfrage)</span><span class="sxs-lookup"><span data-stu-id="5ebf4-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_COLOR\_WRITEMASK )**glGet**( GL\_INDEX\_WRITEMASK )</span></span><br/> | <span data-ttu-id="5ebf4-138">Ruft die Farb Maske ab.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-138">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="5ebf4-139">**grgbmask**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-139">**gRGBmask**</span></span>                      | <span data-ttu-id="5ebf4-140">**glget**(GL- \_ Farb \_ schreibfrage)</span><span class="sxs-lookup"><span data-stu-id="5ebf4-140">**glGet**( GL\_COLOR\_WRITEMASK )</span></span>                                                                                                             | <span data-ttu-id="5ebf4-141">Ruft die Farb Maske ab.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-141">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="5ebf4-142">**zschreitemask**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-142">**zwritemask**</span></span>                    | [<span data-ttu-id="5ebf4-143">**gldepthmask**</span><span class="sxs-lookup"><span data-stu-id="5ebf4-143">**glDepthMask**</span></span>](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> <span data-ttu-id="5ebf4-144">Seien Sie vorsichtig, wenn Sie **zschreitemask** durch " [**gldepthmask**](gldepthmask.md)" ersetzen. **gldepthmask** nimmt ein boolesches Argument an, während **zwrite temask** ein Bitfeld annimmt.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-144">Be careful when replacing **zwritemask** with [**glDepthMask**](gldepthmask.md); **glDepthMask** takes a Boolean argument, whereas **zwritemask** takes a bit field.</span></span>

 

<span data-ttu-id="5ebf4-145">Wenn Sie mehrere Farb Zuordnungen verwenden möchten, müssen Sie die entsprechenden Windows Color Map-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-145">If you want to use multiple color maps, you need to use the appropriate Windows color map functions.</span></span> <span data-ttu-id="5ebf4-146">Daher verfügen **multimap**, **onemap**, **getcmmode**, **setmap** und **getMap** über keine OpenGL-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="5ebf4-146">Therefore, **multimap**, **onemap**, **getcmmode**, **setmap**, and **getmap** have no OpenGL equivalents.</span></span>

 

 





