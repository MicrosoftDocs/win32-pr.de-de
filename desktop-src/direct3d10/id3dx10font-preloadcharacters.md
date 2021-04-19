---
description: Laden Sie eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: ID3DX10Font::P reloadcharacters-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361868"
---
# <a name="id3dx10fontpreloadcharacters-method"></a><span data-ttu-id="408fc-103">ID3DX10Font::P reloadcharacters-Methode</span><span class="sxs-lookup"><span data-stu-id="408fc-103">ID3DX10Font::PreloadCharacters method</span></span>

<span data-ttu-id="408fc-104">Laden Sie eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="408fc-104">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="408fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="408fc-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="408fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="408fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408fc-107">*Zuerst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="408fc-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408fc-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="408fc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="408fc-109">ID des ersten Zeichens, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="408fc-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="408fc-110">*Letzter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="408fc-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408fc-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="408fc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="408fc-112">ID des letzten Zeichens, das in den Videospeicher geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="408fc-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="408fc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="408fc-113">Return value</span></span>

<span data-ttu-id="408fc-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="408fc-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="408fc-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="408fc-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="408fc-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="408fc-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="408fc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="408fc-117">Remarks</span></span>

<span data-ttu-id="408fc-118">Diese Methode generiert Texturen mit Symbolen, die die Eingabezeichen darstellen.</span><span class="sxs-lookup"><span data-stu-id="408fc-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="408fc-119">Die Symbole werden als eine Reihe von Dreiecken gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="408fc-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="408fc-120">Zeichen werden nicht auf dem Gerät gerendert. ID3DX10Font::D rawtext muss nach wie vor aufgerufen werden, um die Zeichen zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="408fc-120">Characters will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the characters.</span></span> <span data-ttu-id="408fc-121">Durch das vorab Laden von Zeichen in den Videospeicher verwendet ID3DX10Font::D rawtext erheblich weniger CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="408fc-121">However, by pre-loading characters into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="408fc-122">Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [getcharakteriplacement](/previous-versions//ms534004(v=vs.85))in Glyphen.</span><span class="sxs-lookup"><span data-stu-id="408fc-122">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="408fc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="408fc-123">Requirements</span></span>



| <span data-ttu-id="408fc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="408fc-124">Requirement</span></span> | <span data-ttu-id="408fc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="408fc-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="408fc-126">Header</span><span class="sxs-lookup"><span data-stu-id="408fc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="408fc-127"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="408fc-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="408fc-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="408fc-128">Library</span></span><br/> | <dl> <span data-ttu-id="408fc-129"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="408fc-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="408fc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="408fc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="408fc-131">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="408fc-131">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="408fc-132">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="408fc-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
