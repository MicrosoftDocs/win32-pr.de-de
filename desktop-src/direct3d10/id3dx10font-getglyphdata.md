---
description: Gibt Informationen über die Platzierung und Ausrichtung eines Symbols in einer Zeichen Zelle zurück.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font:: getglyphdata-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365118"
---
# <a name="id3dx10fontgetglyphdata-method"></a><span data-ttu-id="476dd-103">ID3DX10Font:: getglyphdata-Methode</span><span class="sxs-lookup"><span data-stu-id="476dd-103">ID3DX10Font::GetGlyphData method</span></span>

<span data-ttu-id="476dd-104">Gibt Informationen über die Platzierung und Ausrichtung eines Symbols in einer Zeichen Zelle zurück.</span><span class="sxs-lookup"><span data-stu-id="476dd-104">Return information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="476dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="476dd-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="476dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="476dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="476dd-107">*Glyphe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="476dd-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476dd-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="476dd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="476dd-109">Der Glyphe-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="476dd-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="476dd-110">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="476dd-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="476dd-111">Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="476dd-111">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="476dd-112">Adresse eines Zeigers auf ein ID3D10Texture-Objekt, das das Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="476dd-112">Address of a pointer to a ID3D10Texture object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="476dd-113">*pblackbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="476dd-113">*pBlackBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476dd-114">Typ: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="476dd-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="476dd-115">Zeiger auf das kleinste Rechteck Objekt, das das Symbol vollständig einschließt.</span><span class="sxs-lookup"><span data-stu-id="476dd-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span> <span data-ttu-id="476dd-116">Siehe [Rect](/previous-versions//ms536136(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="476dd-116">See [RECT](/previous-versions//ms536136(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="476dd-117">*pcellinc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="476dd-117">*pCellInc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476dd-118">Typ: **Punkt \***</span><span class="sxs-lookup"><span data-stu-id="476dd-118">Type: **POINT\***</span></span>

<span data-ttu-id="476dd-119">Ein Zeiger auf den zweidimensionalen Vektor, der den Ursprung der aktuellen Zeichen Zelle mit dem Ursprung der nächsten Zeichen Zelle verbindet.</span><span class="sxs-lookup"><span data-stu-id="476dd-119">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="476dd-120">Siehe [Punkt](/previous-versions//ms536119(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="476dd-120">See [POINT](/previous-versions//ms536119(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="476dd-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="476dd-121">Return value</span></span>

<span data-ttu-id="476dd-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="476dd-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="476dd-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="476dd-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="476dd-124">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="476dd-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="476dd-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="476dd-125">Requirements</span></span>



| <span data-ttu-id="476dd-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="476dd-126">Requirement</span></span> | <span data-ttu-id="476dd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="476dd-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="476dd-128">Header</span><span class="sxs-lookup"><span data-stu-id="476dd-128">Header</span></span><br/>  | <dl> <span data-ttu-id="476dd-129"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="476dd-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="476dd-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="476dd-130">Library</span></span><br/> | <dl> <span data-ttu-id="476dd-131"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="476dd-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="476dd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="476dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="476dd-133">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="476dd-133">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="476dd-134">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="476dd-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
