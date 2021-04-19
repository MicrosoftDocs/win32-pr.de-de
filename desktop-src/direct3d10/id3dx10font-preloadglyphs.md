---
description: Laden Sie eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: ID3DX10Font::P reloadglyphs-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355192"
---
# <a name="id3dx10fontpreloadglyphs-method"></a><span data-ttu-id="948ff-103">ID3DX10Font::P reloadglyphs-Methode</span><span class="sxs-lookup"><span data-stu-id="948ff-103">ID3DX10Font::PreloadGlyphs method</span></span>

<span data-ttu-id="948ff-104">Laden Sie eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="948ff-104">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="948ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="948ff-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="948ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="948ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948ff-107">*Zuerst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="948ff-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948ff-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="948ff-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="948ff-109">ID des ersten Symbols, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="948ff-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="948ff-110">*Letzter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="948ff-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948ff-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="948ff-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="948ff-112">ID des letzten Symbols, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="948ff-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948ff-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="948ff-113">Return value</span></span>

<span data-ttu-id="948ff-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="948ff-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="948ff-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="948ff-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="948ff-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="948ff-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="948ff-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="948ff-117">Remarks</span></span>

<span data-ttu-id="948ff-118">Diese Methode generiert Texturen, die die Eingabe Symbole enthalten.</span><span class="sxs-lookup"><span data-stu-id="948ff-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="948ff-119">Die Symbole werden als eine Reihe von Dreiecken gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="948ff-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="948ff-120">Symbole werden nicht auf dem Gerät gerendert. ID3DX10Font::D rawtext muss nach wie vor aufgerufen werden, um die Symbole zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="948ff-120">Glyphs will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the glyphs.</span></span> <span data-ttu-id="948ff-121">Durch das vorab Laden von Symbolen in den Videospeicher verwendet ID3DX10Font::D rawtext erheblich weniger CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="948ff-121">However, by pre-loading glyphs into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="948ff-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="948ff-122">Requirements</span></span>



| <span data-ttu-id="948ff-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="948ff-123">Requirement</span></span> | <span data-ttu-id="948ff-124">Wert</span><span class="sxs-lookup"><span data-stu-id="948ff-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="948ff-125">Header</span><span class="sxs-lookup"><span data-stu-id="948ff-125">Header</span></span><br/>  | <dl> <span data-ttu-id="948ff-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="948ff-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="948ff-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="948ff-127">Library</span></span><br/> | <dl> <span data-ttu-id="948ff-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="948ff-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="948ff-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="948ff-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948ff-130">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="948ff-130">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="948ff-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="948ff-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
