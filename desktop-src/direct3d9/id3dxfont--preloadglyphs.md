---
description: Lädt eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: ID3DXFont::P reloadglyphs-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050932"
---
# <a name="id3dxfontpreloadglyphs-method"></a><span data-ttu-id="f39a7-103">ID3DXFont::P reloadglyphs-Methode</span><span class="sxs-lookup"><span data-stu-id="f39a7-103">ID3DXFont::PreloadGlyphs method</span></span>

<span data-ttu-id="f39a7-104">Lädt eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="f39a7-104">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f39a7-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="f39a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f39a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f39a7-107">*Zuerst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f39a7-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f39a7-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f39a7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f39a7-109">ID des ersten Symbols, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f39a7-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="f39a7-110">*Letzter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f39a7-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f39a7-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f39a7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f39a7-112">ID des letzten Symbols, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f39a7-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f39a7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f39a7-113">Return value</span></span>

<span data-ttu-id="f39a7-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f39a7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f39a7-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f39a7-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f39a7-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="f39a7-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f39a7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f39a7-117">Remarks</span></span>

<span data-ttu-id="f39a7-118">Diese Methode generiert Texturen, die die Eingabe Symbole enthalten.</span><span class="sxs-lookup"><span data-stu-id="f39a7-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="f39a7-119">Die Symbole werden als eine Reihe von Dreiecken gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f39a7-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="f39a7-120">Symbole werden nicht auf dem Gerät gerendert. [**DrawText**](id3dxfont--drawtext.md) muss dennoch aufgerufen werden, um die Symbole zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="f39a7-120">Glyphs will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the glyphs.</span></span> <span data-ttu-id="f39a7-121">Durch das vorab Laden von Symbolen in den Videospeicher verwendet **DrawText** aber erheblich weniger CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="f39a7-121">However, by pre-loading glyphs into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="f39a7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f39a7-122">Requirements</span></span>



| <span data-ttu-id="f39a7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f39a7-123">Requirement</span></span> | <span data-ttu-id="f39a7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f39a7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f39a7-125">Header</span><span class="sxs-lookup"><span data-stu-id="f39a7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f39a7-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f39a7-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f39a7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f39a7-127">Library</span></span><br/> | <dl> <span data-ttu-id="f39a7-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f39a7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f39a7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f39a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39a7-130">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="f39a7-130">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
