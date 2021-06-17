---
title: Attribute mit mehreren Werten (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über Attribute mit mehreren Werten im Windows Media Format 11 SDK. Einige Medienelementattribute können mehrere Werte haben.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute,mehrere Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262692"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="af71c-108">Attribute mit mehreren Werten (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="af71c-108">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="af71c-109">Einigen vordefinierten Attributen können mehrere Werte zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="af71c-109">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="af71c-110">Beispielsweise ist **Interpret** ein Attribut, das mehrere Werte haben kann.</span><span class="sxs-lookup"><span data-stu-id="af71c-110">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="af71c-111">Sie können [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) mehrmals aufrufen, um so viele **Interpretenwerte** wie erforderlich hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="af71c-111">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="af71c-112">Wenn Sie mehrere Aufrufe von **AddAttribute** für Attribute ausführen, die nicht mehrere Werte unterstützen, gibt die Methode möglicherweise einen Fehlercode zurück oder ignoriert einfach Ihre Anforderung.</span><span class="sxs-lookup"><span data-stu-id="af71c-112">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="af71c-113">In der folgenden Tabelle sind die Attribute aufgeführt, die mehrere Werte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="af71c-113">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="af71c-114">Einige Attribute können nur in ASF-Dateien mehrere Werte enthalten, während andere in ASF- und MP3-Dateien mehrere Werte enthalten können.</span><span class="sxs-lookup"><span data-stu-id="af71c-114">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="af71c-115">attribute</span><span class="sxs-lookup"><span data-stu-id="af71c-115">Attribute</span></span>                                                 | <span data-ttu-id="af71c-116">Unterstützung für mehrere Werte</span><span class="sxs-lookup"><span data-stu-id="af71c-116">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="af71c-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="af71c-117">**Author**</span></span>](author.md)                                  | <span data-ttu-id="af71c-118">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-118">ASF, MP3</span></span>                    |
| [<span data-ttu-id="af71c-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="af71c-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="af71c-120">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-120">ASF</span></span>                         |
| [<span data-ttu-id="af71c-121">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="af71c-121">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="af71c-122">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-122">ASF</span></span>                         |
| [<span data-ttu-id="af71c-123">**WM/Category**</span><span class="sxs-lookup"><span data-stu-id="af71c-123">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="af71c-124">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-124">ASF</span></span>                         |
| [<span data-ttu-id="af71c-125">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="af71c-125">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="af71c-126">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-126">ASF, MP3</span></span>                    |
| [<span data-ttu-id="af71c-127">**WM/2016**</span><span class="sxs-lookup"><span data-stu-id="af71c-127">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="af71c-128">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-128">ASF</span></span>                         |
| [<span data-ttu-id="af71c-129">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="af71c-129">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="af71c-130">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-130">ASF</span></span>                         |
| [<span data-ttu-id="af71c-131">**WM/Genre**</span><span class="sxs-lookup"><span data-stu-id="af71c-131">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="af71c-132">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-132">ASF</span></span>                         |
| [<span data-ttu-id="af71c-133">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="af71c-133">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="af71c-134">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-134">ASF</span></span>                         |
| [<span data-ttu-id="af71c-135">**WM/Sprache**</span><span class="sxs-lookup"><span data-stu-id="af71c-135">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="af71c-136">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-136">ASF, MP3</span></span>                    |
| [<span data-ttu-id="af71c-137">**WM/Synchronisierung \_**</span><span class="sxs-lookup"><span data-stu-id="af71c-137">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="af71c-138">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-138">ASF, MP3</span></span>                    |
| [<span data-ttu-id="af71c-139">**WM/Stimmung**</span><span class="sxs-lookup"><span data-stu-id="af71c-139">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="af71c-140">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-140">ASF, MP3</span></span>                    |
| [<span data-ttu-id="af71c-141">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="af71c-141">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="af71c-142">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-142">ASF, MP3</span></span>                    |
| [<span data-ttu-id="af71c-143">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="af71c-143">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="af71c-144">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-144">ASF</span></span>                         |
| [<span data-ttu-id="af71c-145">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="af71c-145">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="af71c-146">ASF</span><span class="sxs-lookup"><span data-stu-id="af71c-146">ASF</span></span>                         |
| [<span data-ttu-id="af71c-147">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="af71c-147">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="af71c-148">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-148">ASF, MP3</span></span>                    |
| [<span data-ttu-id="af71c-149">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="af71c-149">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="af71c-150">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="af71c-150">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="af71c-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af71c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af71c-152">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="af71c-152">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




