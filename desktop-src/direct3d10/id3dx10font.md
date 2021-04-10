---
description: Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: ID3DX10Font-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219534"
---
# <a name="id3dx10font-interface"></a><span data-ttu-id="a8973-103">ID3DX10Font-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a8973-103">ID3DX10Font interface</span></span>

<span data-ttu-id="a8973-104">Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="a8973-104">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="a8973-105">Member</span><span class="sxs-lookup"><span data-stu-id="a8973-105">Members</span></span>

<span data-ttu-id="a8973-106">Die **ID3DX10Font** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a8973-106">The **ID3DX10Font** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8973-107">**ID3DX10Font** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a8973-107">**ID3DX10Font** also has these types of members:</span></span>

-   [<span data-ttu-id="a8973-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="a8973-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8973-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a8973-109">Methods</span></span>

<span data-ttu-id="a8973-110">Die **ID3DX10Font** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a8973-110">The **ID3DX10Font** interface has these methods.</span></span>



| <span data-ttu-id="a8973-111">Methode</span><span class="sxs-lookup"><span data-stu-id="a8973-111">Method</span></span>                                                     | <span data-ttu-id="a8973-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8973-112">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8973-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="a8973-113">**DrawText**</span></span>](id3dx10font-drawtext.md)                   | <span data-ttu-id="a8973-114">Formatierten Text zeichnen.</span><span class="sxs-lookup"><span data-stu-id="a8973-114">Draw formatted text.</span></span> <span data-ttu-id="a8973-115">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="a8973-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                        |
| [<span data-ttu-id="a8973-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="a8973-116">**GetDC**</span></span>](id3dx10font-getdc.md)                         | <span data-ttu-id="a8973-117">Gibt ein Handle für einen Anzeigegeräte Kontext (DC) zurück, für den die Schriftart festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8973-117">Return a handle to a display device context (DC) that has the font set onto it.</span></span><br/>                                                            |
| [<span data-ttu-id="a8973-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="a8973-118">**GetDesc**</span></span>](id3dx10font-getdesc.md)                     | <span data-ttu-id="a8973-119">Eine Beschreibung des aktuellen Schriftart Objekts erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8973-119">Get a description of the current font object.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a8973-120">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="a8973-120">**GetDevice**</span></span>](id3dx10font-getdevice.md)                 | <span data-ttu-id="a8973-121">Rufen Sie das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a8973-121">Retrieve the Direct3D device associated with the font object.</span></span><br/>                                                                              |
| [<span data-ttu-id="a8973-122">**Getglyphdata**</span><span class="sxs-lookup"><span data-stu-id="a8973-122">**GetGlyphData**</span></span>](id3dx10font-getglyphdata.md)           | <span data-ttu-id="a8973-123">Gibt Informationen über die Platzierung und Ausrichtung eines Symbols in einer Zeichen Zelle zurück.</span><span class="sxs-lookup"><span data-stu-id="a8973-123">Return information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                     |
| [<span data-ttu-id="a8973-124">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="a8973-124">**GetTextMetrics**</span></span>](id3dx10font-gettextmetrics.md)       | <span data-ttu-id="a8973-125">Rufen Sie Schriftart Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="a8973-125">Retrieve font characteristics.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="a8973-126">**Preloadcharacter**</span><span class="sxs-lookup"><span data-stu-id="a8973-126">**PreloadCharacters**</span></span>](id3dx10font-preloadcharacters.md) | <span data-ttu-id="a8973-127">Laden Sie eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a8973-127">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                        |
| [<span data-ttu-id="a8973-128">**Präloadglyphen**</span><span class="sxs-lookup"><span data-stu-id="a8973-128">**PreloadGlyphs**</span></span>](id3dx10font-preloadglyphs.md)         | <span data-ttu-id="a8973-129">Laden Sie eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a8973-129">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                            |
| [<span data-ttu-id="a8973-130">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="a8973-130">**PreloadText**</span></span>](id3dx10font-preloadtext.md)             | <span data-ttu-id="a8973-131">Laden Sie formatierten Text in den Videospeicher, um die Effizienz beim Rendern auf das Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a8973-131">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="a8973-132">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="a8973-132">This method supports ANSI and Unicode strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8973-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8973-133">Remarks</span></span>

<span data-ttu-id="a8973-134">Die ID3DX10Font-Schnittstelle wird durch Aufrufen von [**D3DX10CreateFont**](d3dx10createfont.md) oder [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a8973-134">The ID3DX10Font interface is obtained by calling [**D3DX10CreateFont**](d3dx10createfont.md) or [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span></span>

<span data-ttu-id="a8973-135">Der LPD3DX10FONT-Typ wird als Zeiger auf die ID3DX10Font-Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="a8973-135">The LPD3DX10FONT type is defined as a pointer to the ID3DX10Font interface.</span></span>


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a><span data-ttu-id="a8973-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8973-136">Requirements</span></span>



| <span data-ttu-id="a8973-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8973-137">Requirement</span></span> | <span data-ttu-id="a8973-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a8973-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8973-139">Header</span><span class="sxs-lookup"><span data-stu-id="a8973-139">Header</span></span><br/>  | <dl> <span data-ttu-id="a8973-140"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8973-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8973-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8973-141">Library</span></span><br/> | <dl> <span data-ttu-id="a8973-142"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8973-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8973-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8973-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8973-144">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a8973-144">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
