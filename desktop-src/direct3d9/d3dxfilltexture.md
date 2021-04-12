---
description: Verwendet eine vom Benutzer bereitgestellte Funktion, um die einzelnen texttwerte der MIP-Ebene einer angegebenen Textur auszufüllen.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: D3DXFillTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354866"
---
# <a name="d3dxfilltexture-function"></a><span data-ttu-id="c4491-103">D3DXFillTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4491-103">D3DXFillTexture function</span></span>

<span data-ttu-id="c4491-104">Verwendet eine vom Benutzer bereitgestellte Funktion, um die einzelnen texttwerte der MIP-Ebene einer angegebenen Textur auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="c4491-104">Uses a user-provided function to fill each texel of each mip level of a given texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4491-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4491-105">Syntax</span></span>


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a><span data-ttu-id="c4491-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4491-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4491-107">*ptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4491-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4491-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c4491-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c4491-109">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die gefüllte Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4491-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="c4491-110">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4491-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4491-111">Typ: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span><span class="sxs-lookup"><span data-stu-id="c4491-111">Type: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span></span>

<span data-ttu-id="c4491-112">Ein Zeiger auf eine vom Benutzer bereitgestellte Auswertungsfunktion, die verwendet wird, um den Wert der einzelnen Texttypen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c4491-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="c4491-113">Die-Funktion folgt dem Prototyp von [LPD3DXFILL2D](lpd3dxfill2d.md).</span><span class="sxs-lookup"><span data-stu-id="c4491-113">The function follows the prototype of [LPD3DXFILL2D](lpd3dxfill2d.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4491-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4491-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4491-115">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4491-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4491-116">Zeiger auf einen beliebigen Block von benutzerdefinierten Daten.</span><span class="sxs-lookup"><span data-stu-id="c4491-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="c4491-117">Dieser Zeiger wird an die Funktion übergeben, die in *pfunction* bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4491-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4491-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4491-118">Return value</span></span>

<span data-ttu-id="c4491-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4491-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4491-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4491-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c4491-121">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="c4491-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4491-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4491-122">Remarks</span></span>

<span data-ttu-id="c4491-123">Im folgenden Beispiel wird eine Funktion namens ColorFill erstellt, die auf D3DXFillTexture basiert.</span><span class="sxs-lookup"><span data-stu-id="c4491-123">Here is an example that creates a function called ColorFill, which relies on D3DXFillTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c4491-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4491-124">Requirements</span></span>



| <span data-ttu-id="c4491-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4491-125">Requirement</span></span> | <span data-ttu-id="c4491-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c4491-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4491-127">Header</span><span class="sxs-lookup"><span data-stu-id="c4491-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c4491-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4491-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c4491-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4491-129">Library</span></span><br/> | <dl> <span data-ttu-id="c4491-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4491-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c4491-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4491-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4491-132">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c4491-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
