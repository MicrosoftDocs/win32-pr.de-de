---
title: IDWriteTextLayout2-Schnittstelle
description: Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde. | IDWriteTextLayout2-Schnittstelle
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- IDWriteTextLayout2 Interface Direct Write
- IDWriteTextLayout2 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353279"
---
# <a name="idwritetextlayout2-interface"></a><span data-ttu-id="6ff43-106">IDWriteTextLayout2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6ff43-106">IDWriteTextLayout2 interface</span></span>

<span data-ttu-id="6ff43-107">Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ff43-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="6ff43-108">Member</span><span class="sxs-lookup"><span data-stu-id="6ff43-108">Members</span></span>

<span data-ttu-id="6ff43-109">Die **IDWriteTextLayout2** -Schnittstelle erbt von [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span><span class="sxs-lookup"><span data-stu-id="6ff43-109">The **IDWriteTextLayout2** interface inherits from [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span></span> <span data-ttu-id="6ff43-110">**IDWriteTextLayout2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6ff43-110">**IDWriteTextLayout2** also has these types of members:</span></span>

-   [<span data-ttu-id="6ff43-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ff43-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ff43-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ff43-112">Methods</span></span>

<span data-ttu-id="6ff43-113">Die **IDWriteTextLayout2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6ff43-113">The **IDWriteTextLayout2** interface has these methods.</span></span>



| <span data-ttu-id="6ff43-114">Methode</span><span class="sxs-lookup"><span data-stu-id="6ff43-114">Method</span></span>                                                                                | <span data-ttu-id="6ff43-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ff43-115">Description</span></span>                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ff43-116">**Getfontfallback**</span><span class="sxs-lookup"><span data-stu-id="6ff43-116">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | <span data-ttu-id="6ff43-117">Das aktuelle Schriftart-Fall Back-Objekt wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ff43-117">Get the current font fallback object.</span></span> <br/>                                           |
| [<span data-ttu-id="6ff43-118">**Getlastlinewrapping**</span><span class="sxs-lookup"><span data-stu-id="6ff43-118">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | <span data-ttu-id="6ff43-119">Gibt an, ob das letzte Wort in der letzten Zeile umschließt ist.</span><span class="sxs-lookup"><span data-stu-id="6ff43-119">Get whether or not the last word on the last line is wrapped.</span></span><br/>                    |
| [<span data-ttu-id="6ff43-120">**Getmetrics**</span><span class="sxs-lookup"><span data-stu-id="6ff43-120">**GetMetrics**</span></span>](idwritetextlayout2-getmetrics.md)                                   | <span data-ttu-id="6ff43-121">Ruft allgemeine Metriken für die formatierte Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="6ff43-121">Retrieves overall metrics for the formatted string.</span></span> <br/>                             |
| [<span data-ttu-id="6ff43-122">**Getopticalalignment**</span><span class="sxs-lookup"><span data-stu-id="6ff43-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | <span data-ttu-id="6ff43-123">Gibt an, wie die Symbole am Rand ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6ff43-123">Get how the glyphs align to the edges the margin.</span></span> <br/>                               |
| [<span data-ttu-id="6ff43-124">**Getverticalglyphorientation**</span><span class="sxs-lookup"><span data-stu-id="6ff43-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | <span data-ttu-id="6ff43-125">Hiermit wird die bevorzugte Ausrichtung von Symbolen bei Verwendung einer vertikalen Leserichtung erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ff43-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |
| [<span data-ttu-id="6ff43-126">**Setfontfallback**</span><span class="sxs-lookup"><span data-stu-id="6ff43-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | <span data-ttu-id="6ff43-127">Anwenden eines benutzerdefinierten Schriftart Fallbacks auf das Layout.</span><span class="sxs-lookup"><span data-stu-id="6ff43-127">Apply a custom font fallback onto layout.</span></span><br/>                                        |
| [<span data-ttu-id="6ff43-128">**Setlastlinewrapping**</span><span class="sxs-lookup"><span data-stu-id="6ff43-128">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | <span data-ttu-id="6ff43-129">Legen Sie fest, ob das letzte Wort in der letzten Zeile umschließt ist.</span><span class="sxs-lookup"><span data-stu-id="6ff43-129">Set whether or not the last word on the last line is wrapped.</span></span> <br/>                   |
| [<span data-ttu-id="6ff43-130">**Setopticalalignment**</span><span class="sxs-lookup"><span data-stu-id="6ff43-130">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | <span data-ttu-id="6ff43-131">Legen Sie fest, wie die Symbole an den Rändern am Rand ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6ff43-131">Set how the glyphs align to the edges the margin.</span></span><br/>                                |
| [<span data-ttu-id="6ff43-132">**Setverticalglyphorientation**</span><span class="sxs-lookup"><span data-stu-id="6ff43-132">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | <span data-ttu-id="6ff43-133">Legen Sie die bevorzugte Ausrichtung der Symbole fest, wenn Sie eine vertikale Leserichtung verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ff43-133">Set the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ff43-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ff43-134">Requirements</span></span>



| <span data-ttu-id="6ff43-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ff43-135">Requirement</span></span> | <span data-ttu-id="6ff43-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6ff43-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff43-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ff43-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff43-138">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6ff43-138">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="6ff43-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ff43-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff43-140">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6ff43-140">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6ff43-141">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="6ff43-141">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6ff43-142">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="6ff43-142">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="6ff43-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ff43-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ff43-144"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ff43-144"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6ff43-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6ff43-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ff43-146"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ff43-146"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ff43-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ff43-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff43-148">**IDWriteTextLayout1**</span><span class="sxs-lookup"><span data-stu-id="6ff43-148">**IDWriteTextLayout1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

