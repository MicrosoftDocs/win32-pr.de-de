---
description: Gibt Informationen über die Platzierung und die Ausrichtung eines Symbols in einer Zeichen Zelle zurück.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'ID3DXFont:: getglyphdata-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355182"
---
# <a name="id3dxfontgetglyphdata-method"></a><span data-ttu-id="569b3-103">ID3DXFont:: getglyphdata-Methode</span><span class="sxs-lookup"><span data-stu-id="569b3-103">ID3DXFont::GetGlyphData method</span></span>

<span data-ttu-id="569b3-104">Gibt Informationen über die Platzierung und die Ausrichtung eines Symbols in einer Zeichen Zelle zurück.</span><span class="sxs-lookup"><span data-stu-id="569b3-104">Returns information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="569b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="569b3-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="569b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="569b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="569b3-107">*Glyphe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="569b3-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="569b3-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="569b3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="569b3-109">Der Glyphe-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="569b3-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="569b3-110">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="569b3-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="569b3-111">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="569b3-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="569b3-112">Adresse eines Zeigers auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt, das das Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="569b3-112">Address of a pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="569b3-113">*pblackbox* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="569b3-113">*pBlackBox* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="569b3-114">Typ: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="569b3-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="569b3-115">Zeiger auf das kleinste Rechteck Objekt, das das Symbol vollständig einschließt.</span><span class="sxs-lookup"><span data-stu-id="569b3-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="569b3-116">*pcellinc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="569b3-116">*pCellInc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="569b3-117">Typ: **[ **Punkt**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="569b3-117">Type: **[**POINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="569b3-118">Ein Zeiger auf den zweidimensionalen Vektor, der den Ursprung der aktuellen Zeichen Zelle mit dem Ursprung der nächsten Zeichen Zelle verbindet.</span><span class="sxs-lookup"><span data-stu-id="569b3-118">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="569b3-119">Siehe [**Punkt**](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="569b3-119">See [**POINT**](../winprog/windows-data-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="569b3-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="569b3-120">Return value</span></span>

<span data-ttu-id="569b3-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="569b3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="569b3-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="569b3-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="569b3-123">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="569b3-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="569b3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="569b3-124">Requirements</span></span>



| <span data-ttu-id="569b3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="569b3-125">Requirement</span></span> | <span data-ttu-id="569b3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="569b3-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="569b3-127">Header</span><span class="sxs-lookup"><span data-stu-id="569b3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="569b3-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="569b3-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="569b3-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="569b3-129">Library</span></span><br/> | <dl> <span data-ttu-id="569b3-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="569b3-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="569b3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="569b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="569b3-132">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="569b3-132">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
