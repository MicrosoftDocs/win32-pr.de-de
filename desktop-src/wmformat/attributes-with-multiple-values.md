---
title: Attribute mit mehreren Werten (Windows Media Format 11 SDK)
description: Attribute mit mehreren Werten
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, mehrere Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039952"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="b5b97-107">Attribute mit mehreren Werten (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="b5b97-107">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="b5b97-108">Einigen vordefinierten Attributen können mehrere Werte zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b5b97-108">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="b5b97-109">Beispielsweise ist " **Artist** " ein Attribut, das mehrere Werte aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="b5b97-109">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="b5b97-110">Sie können [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) mehrmals aufzurufen, um beliebig viele **Künstler** Werte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b5b97-110">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="b5b97-111">Wenn Sie mehrere Aufrufe von **AddAttribute** für Attribute durchführen, die mehrere Werte nicht unterstützen, gibt die Methode möglicherweise einen Fehlercode zurück, oder ignorieren Sie Ihre Anforderung einfach.</span><span class="sxs-lookup"><span data-stu-id="b5b97-111">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="b5b97-112">In der folgenden Tabelle werden die Attribute aufgelistet, die mehrere Werte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b5b97-112">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="b5b97-113">Einige Attribute können mehrere Werte nur in ASF-Dateien aufweisen, während andere mehrere Werte in den Dateien "ASF" und "MP3" aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="b5b97-113">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="b5b97-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="b5b97-114">Attribute</span></span>                                                 | <span data-ttu-id="b5b97-115">Unterstützung für mehrere Werte</span><span class="sxs-lookup"><span data-stu-id="b5b97-115">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="b5b97-116">**Autor**</span><span class="sxs-lookup"><span data-stu-id="b5b97-116">**Author**</span></span>](author.md)                                  | <span data-ttu-id="b5b97-117">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-117">ASF, MP3</span></span>                    |
| [<span data-ttu-id="b5b97-118">**WM/albumartist**</span><span class="sxs-lookup"><span data-stu-id="b5b97-118">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="b5b97-119">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-119">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-120">**WM/albumcoverurl**</span><span class="sxs-lookup"><span data-stu-id="b5b97-120">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="b5b97-121">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-121">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-122">**WM/Kategorie**</span><span class="sxs-lookup"><span data-stu-id="b5b97-122">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="b5b97-123">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-123">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-124">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="b5b97-124">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="b5b97-125">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-125">ASF, MP3</span></span>                    |
| [<span data-ttu-id="b5b97-126">**WM/Dirigent**</span><span class="sxs-lookup"><span data-stu-id="b5b97-126">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="b5b97-127">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-127">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-128">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="b5b97-128">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="b5b97-129">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-129">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-130">**WM/Genre**</span><span class="sxs-lookup"><span data-stu-id="b5b97-130">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="b5b97-131">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-131">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-132">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="b5b97-132">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="b5b97-133">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-133">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-134">**WM/Sprache**</span><span class="sxs-lookup"><span data-stu-id="b5b97-134">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="b5b97-135">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-135">ASF, MP3</span></span>                    |
| [<span data-ttu-id="b5b97-136">**Synchronisierte WM/Liedtexte \_**</span><span class="sxs-lookup"><span data-stu-id="b5b97-136">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="b5b97-137">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-137">ASF, MP3</span></span>                    |
| [<span data-ttu-id="b5b97-138">**WM/Stimmung**</span><span class="sxs-lookup"><span data-stu-id="b5b97-138">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="b5b97-139">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-139">ASF, MP3</span></span>                    |
| [<span data-ttu-id="b5b97-140">**WM/Bild**</span><span class="sxs-lookup"><span data-stu-id="b5b97-140">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="b5b97-141">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-141">ASF, MP3</span></span>                    |
| [<span data-ttu-id="b5b97-142">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="b5b97-142">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="b5b97-143">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-143">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-144">**WM/promotionurl**</span><span class="sxs-lookup"><span data-stu-id="b5b97-144">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="b5b97-145">ASF</span><span class="sxs-lookup"><span data-stu-id="b5b97-145">ASF</span></span>                         |
| [<span data-ttu-id="b5b97-146">**WM/userweburl**</span><span class="sxs-lookup"><span data-stu-id="b5b97-146">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="b5b97-147">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-147">ASF, MP3</span></span>                    |
| [<span data-ttu-id="b5b97-148">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="b5b97-148">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="b5b97-149">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="b5b97-149">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="b5b97-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5b97-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5b97-151">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b5b97-151">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




