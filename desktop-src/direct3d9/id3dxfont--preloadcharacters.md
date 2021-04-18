---
description: Lädt eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: ID3DXFont::P reloadcharacters-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371948"
---
# <a name="id3dxfontpreloadcharacters-method"></a><span data-ttu-id="43ee5-103">ID3DXFont::P reloadcharacters-Methode</span><span class="sxs-lookup"><span data-stu-id="43ee5-103">ID3DXFont::PreloadCharacters method</span></span>

<span data-ttu-id="43ee5-104">Lädt eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="43ee5-104">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ee5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43ee5-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="43ee5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43ee5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ee5-107">*Zuerst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43ee5-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ee5-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43ee5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43ee5-109">ID des ersten Zeichens, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="43ee5-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="43ee5-110">*Letzter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43ee5-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ee5-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43ee5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43ee5-112">ID des letzten Zeichens, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="43ee5-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ee5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43ee5-113">Return value</span></span>

<span data-ttu-id="43ee5-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43ee5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43ee5-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43ee5-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="43ee5-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="43ee5-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ee5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43ee5-117">Remarks</span></span>

<span data-ttu-id="43ee5-118">Diese Methode generiert Texturen mit Symbolen, die die Eingabezeichen darstellen.</span><span class="sxs-lookup"><span data-stu-id="43ee5-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="43ee5-119">Die Symbole werden als eine Reihe von Dreiecken gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="43ee5-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="43ee5-120">Zeichen werden nicht auf dem Gerät gerendert. [**DrawText**](id3dxfont--drawtext.md) muss dennoch aufgerufen werden, um die Zeichen zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="43ee5-120">Characters will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the characters.</span></span> <span data-ttu-id="43ee5-121">Durch das vorab Laden von Zeichen in den Videospeicher verwendet **DrawText** aber erheblich weniger CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="43ee5-121">However, by pre-loading characters into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="43ee5-122">Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [**getcharakteriplacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)in Glyphen.</span><span class="sxs-lookup"><span data-stu-id="43ee5-122">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="43ee5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43ee5-123">Requirements</span></span>



| <span data-ttu-id="43ee5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43ee5-124">Requirement</span></span> | <span data-ttu-id="43ee5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="43ee5-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43ee5-126">Header</span><span class="sxs-lookup"><span data-stu-id="43ee5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="43ee5-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="43ee5-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="43ee5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43ee5-128">Library</span></span><br/> | <dl> <span data-ttu-id="43ee5-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43ee5-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43ee5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43ee5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ee5-131">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="43ee5-131">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
