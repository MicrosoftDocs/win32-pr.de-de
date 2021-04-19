---
title: IDWriteTextFormat1-Schnittstelle
description: Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen. | IDWriteTextFormat1-Schnittstelle
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- IDWriteTextFormat1 Interface Direct Write
- IDWriteTextFormat1 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373437"
---
# <a name="idwritetextformat1-interface"></a><span data-ttu-id="9a903-106">IDWriteTextFormat1-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9a903-106">IDWriteTextFormat1 interface</span></span>

<span data-ttu-id="9a903-107">Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen.</span><span class="sxs-lookup"><span data-stu-id="9a903-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span> <span data-ttu-id="9a903-108">Diese Schnittstelle verfügt über dieselben Methoden wie [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und bietet Ihnen die Möglichkeit, eine explizite Ausrichtung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="9a903-108">This interface has all the same methods as [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and adds the ability for you to apply an explicit orientation.</span></span>

## <a name="members"></a><span data-ttu-id="9a903-109">Member</span><span class="sxs-lookup"><span data-stu-id="9a903-109">Members</span></span>

<span data-ttu-id="9a903-110">Die **IDWriteTextFormat1** -Schnittstelle erbt von [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="9a903-110">The **IDWriteTextFormat1** interface inherits from [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span> <span data-ttu-id="9a903-111">**IDWriteTextFormat1** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9a903-111">**IDWriteTextFormat1** also has these types of members:</span></span>

-   [<span data-ttu-id="9a903-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="9a903-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9a903-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="9a903-113">Methods</span></span>

<span data-ttu-id="9a903-114">Die **IDWriteTextFormat1** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9a903-114">The **IDWriteTextFormat1** interface has these methods.</span></span>



| <span data-ttu-id="9a903-115">Methode</span><span class="sxs-lookup"><span data-stu-id="9a903-115">Method</span></span>                                                                                | <span data-ttu-id="9a903-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a903-116">Description</span></span>                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a903-117">**Getfontfallback**</span><span class="sxs-lookup"><span data-stu-id="9a903-117">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | <span data-ttu-id="9a903-118">Ruft den aktuellen Fallback ab.</span><span class="sxs-lookup"><span data-stu-id="9a903-118">Gets the current fallback.</span></span> <span data-ttu-id="9a903-119">Wenn seit dem Erstellen des Layouts nichts festgelegt wurde, wird es auf nullptr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9a903-119">If none was ever set since creating the layout, it will be nullptr.</span></span><br/>               |
| [<span data-ttu-id="9a903-120">**Getlastlinewrapping**</span><span class="sxs-lookup"><span data-stu-id="9a903-120">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | <span data-ttu-id="9a903-121">Ruft den Wrapping Modus der letzten Zeile ab.</span><span class="sxs-lookup"><span data-stu-id="9a903-121">Gets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="9a903-122">**Getopticalalignment**</span><span class="sxs-lookup"><span data-stu-id="9a903-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | <span data-ttu-id="9a903-123">Ruft die optische Rand Ausrichtung für das Textformat ab.</span><span class="sxs-lookup"><span data-stu-id="9a903-123">Gets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="9a903-124">**Getverticalglyphorientation**</span><span class="sxs-lookup"><span data-stu-id="9a903-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | <span data-ttu-id="9a903-125">Hiermit wird die bevorzugte Ausrichtung von Symbolen bei Verwendung einer vertikalen Leserichtung erhalten.</span><span class="sxs-lookup"><span data-stu-id="9a903-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/>                             |
| [<span data-ttu-id="9a903-126">**Setfontfallback**</span><span class="sxs-lookup"><span data-stu-id="9a903-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | <span data-ttu-id="9a903-127">Wendet den benutzerdefinierten Schriftart Fall Back auf das Layout an.</span><span class="sxs-lookup"><span data-stu-id="9a903-127">Applies the custom font fallback onto the layout.</span></span> <span data-ttu-id="9a903-128">Wenn kein Wert festgelegt ist, wird die standardmäßige System Fall Back Liste verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a903-128">If none is set, it uses the default system fallback list.</span></span> <br/> |
| [<span data-ttu-id="9a903-129">**Setlastlinewrapping**</span><span class="sxs-lookup"><span data-stu-id="9a903-129">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | <span data-ttu-id="9a903-130">Legt den Wrapping Modus der letzten Zeile fest.</span><span class="sxs-lookup"><span data-stu-id="9a903-130">Sets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="9a903-131">**Setopticalalignment**</span><span class="sxs-lookup"><span data-stu-id="9a903-131">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | <span data-ttu-id="9a903-132">Legt die optische Rand Ausrichtung für das Textformat fest.</span><span class="sxs-lookup"><span data-stu-id="9a903-132">Sets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="9a903-133">**Setverticalglyphorientation**</span><span class="sxs-lookup"><span data-stu-id="9a903-133">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | <span data-ttu-id="9a903-134">Legt die Ausrichtung eines Text Formats fest.</span><span class="sxs-lookup"><span data-stu-id="9a903-134">Sets the orientation of a text format.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="9a903-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a903-135">Requirements</span></span>



| <span data-ttu-id="9a903-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a903-136">Requirement</span></span> | <span data-ttu-id="9a903-137">Wert</span><span class="sxs-lookup"><span data-stu-id="9a903-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a903-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a903-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9a903-139">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9a903-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="9a903-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a903-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9a903-141">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9a903-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="9a903-142">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="9a903-142">Minimum supported phone</span></span><br/>  | <span data-ttu-id="9a903-143">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="9a903-143">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="9a903-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a903-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a903-145"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a903-145"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9a903-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9a903-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a903-147"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a903-147"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a903-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a903-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a903-149">**Idschreitetextformat**</span><span class="sxs-lookup"><span data-stu-id="9a903-149">**IDWriteTextFormat**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

