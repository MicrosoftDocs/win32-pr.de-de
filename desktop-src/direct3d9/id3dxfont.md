---
description: Die ID3DXFont-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: ID3DXFont-Schnittstelle (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355839"
---
# <a name="id3dxfont-interface"></a><span data-ttu-id="1ecf4-103">ID3DXFont-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1ecf4-103">ID3DXFont interface</span></span>

<span data-ttu-id="1ecf4-104">Die ID3DXFont-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-104">The ID3DXFont interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="1ecf4-105">Member</span><span class="sxs-lookup"><span data-stu-id="1ecf4-105">Members</span></span>

<span data-ttu-id="1ecf4-106">Die **ID3DXFont** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-106">The **ID3DXFont** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1ecf4-107">**ID3DXFont** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ecf4-107">**ID3DXFont** also has these types of members:</span></span>

-   [<span data-ttu-id="1ecf4-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ecf4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1ecf4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ecf4-109">Methods</span></span>

<span data-ttu-id="1ecf4-110">Die **ID3DXFont** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-110">The **ID3DXFont** interface has these methods.</span></span>



| <span data-ttu-id="1ecf4-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1ecf4-111">Method</span></span>                                                    | <span data-ttu-id="1ecf4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ecf4-112">Description</span></span>                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ecf4-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-113">**DrawText**</span></span>](id3dxfont--drawtext.md)                   | <span data-ttu-id="1ecf4-114">Zeichnet formatierten Text.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-114">Draws formatted text.</span></span> <span data-ttu-id="1ecf4-115">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="1ecf4-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-116">**GetDC**</span></span>](id3dxfont--getdc.md)                         | <span data-ttu-id="1ecf4-117">Gibt ein Handle für einen Anzeigegeräte Kontext (DC) zurück, der über den Schriftart Satz verfügt.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-117">Returns a handle to a display device context (DC) that has the font set.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="1ecf4-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-118">**GetDesc**</span></span>](id3dxfont--getdesc.md)                     | <span data-ttu-id="1ecf4-119">Ruft eine Beschreibung des aktuellen Schriftart Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-119">Gets a description of the current font object.</span></span> <span data-ttu-id="1ecf4-120">Getdescw und getdesca sind mit dieser Methode identisch, mit dem Unterschied, dass ein Zeiger an eine [**D3DXFONT \_**](d3dxfont-desc.md) -oder **D3DXFONT- \_ DeScA** -Struktur zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-120">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span><br/> |
| [<span data-ttu-id="1ecf4-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-121">**GetDevice**</span></span>](id3dxfont--getdevice.md)                 | <span data-ttu-id="1ecf4-122">Ruft das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-122">Retrieves the Direct3D device associated with the font object.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="1ecf4-123">**Getglyphdata**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-123">**GetGlyphData**</span></span>](id3dxfont--getglyphdata.md)           | <span data-ttu-id="1ecf4-124">Gibt Informationen über die Platzierung und die Ausrichtung eines Symbols in einer Zeichen Zelle zurück.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-124">Returns information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="1ecf4-125">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-125">**GetTextMetrics**</span></span>](id3dxfont--gettextmetrics.md)       | <span data-ttu-id="1ecf4-126">Ruft Schriftart Eigenschaften ab, die in einer [**TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) -Struktur identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-126">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="1ecf4-127">Diese Methode unterstützt die ANSI-und Unicode-Compilereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-127">This method supports ANSI and Unicode compiler settings.</span></span><br/>                                                                       |
| [<span data-ttu-id="1ecf4-128">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-128">**OnLostDevice**</span></span>](id3dxfont--onlostdevice.md)           | <span data-ttu-id="1ecf4-129">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-129">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="1ecf4-130">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-130">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/>                                              |
| [<span data-ttu-id="1ecf4-131">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-131">**OnResetDevice**</span></span>](id3dxfont--onresetdevice.md)         | <span data-ttu-id="1ecf4-132">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-132">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="1ecf4-133">**Preloadcharacter**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-133">**PreloadCharacters**</span></span>](id3dxfont--preloadcharacters.md) | <span data-ttu-id="1ecf4-134">Lädt eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-134">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="1ecf4-135">**Präloadglyphen**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-135">**PreloadGlyphs**</span></span>](id3dxfont--preloadglyphs.md)         | <span data-ttu-id="1ecf4-136">Lädt eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-136">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1ecf4-137">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="1ecf4-137">**PreloadText**</span></span>](id3dxfont--preloadtext.md)             | <span data-ttu-id="1ecf4-138">Lädt formatierten Text in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-138">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="1ecf4-139">Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-139">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="1ecf4-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ecf4-140">Remarks</span></span>

<span data-ttu-id="1ecf4-141">Die **ID3DXFont** -Schnittstelle wird durch Aufrufen von [**D3DXCreateFont**](d3dxcreatefont.md) oder [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-141">The **ID3DXFont** interface is obtained by calling [**D3DXCreateFont**](d3dxcreatefont.md) or [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span></span>

<span data-ttu-id="1ecf4-142">Der LPD3DXFONT-Typ wird als Zeiger auf die **ID3DXFont** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-142">The LPD3DXFONT type is defined as a pointer to the **ID3DXFont** interface.</span></span>


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a><span data-ttu-id="1ecf4-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ecf4-143">Requirements</span></span>



| <span data-ttu-id="1ecf4-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ecf4-144">Requirement</span></span> | <span data-ttu-id="1ecf4-145">Wert</span><span class="sxs-lookup"><span data-stu-id="1ecf4-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecf4-146">Header</span><span class="sxs-lookup"><span data-stu-id="1ecf4-146">Header</span></span><br/>  | <dl> <span data-ttu-id="1ecf4-147"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ecf4-147"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1ecf4-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ecf4-148">Library</span></span><br/> | <dl> <span data-ttu-id="1ecf4-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ecf4-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ecf4-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ecf4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecf4-151">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ecf4-151">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
