---
description: Verwendet eine vom Benutzer bereitgestellte Funktion, um die einzelnen texttaten der MIP-Ebene einer angegebenen cubetextur auszufüllen.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: D3DXFillCubeTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9fda70aa42d6982c40eb1ec926b6823e7ac7d997
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351950"
---
# <a name="d3dxfillcubetexture-function"></a><span data-ttu-id="0b213-103">D3DXFillCubeTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="0b213-103">D3DXFillCubeTexture function</span></span>

<span data-ttu-id="0b213-104">Verwendet eine vom Benutzer bereitgestellte Funktion, um die einzelnen texttaten der MIP-Ebene einer angegebenen cubetextur auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="0b213-104">Uses a user-provided function to fill each texel of each mip level of a given cube texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b213-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b213-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a><span data-ttu-id="0b213-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b213-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b213-107">*ptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b213-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b213-108">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="0b213-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="0b213-109">Zeiger auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die die gefüllte Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b213-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="0b213-110">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b213-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b213-111">Typ: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="0b213-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="0b213-112">Ein Zeiger auf eine vom Benutzer bereitgestellte Auswertungsfunktion, die verwendet wird, um den Wert der einzelnen Texttypen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0b213-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="0b213-113">Die-Funktion folgt dem Prototyp von [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="0b213-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b213-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b213-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b213-115">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b213-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b213-116">Zeiger auf einen beliebigen Block von benutzerdefinierten Daten.</span><span class="sxs-lookup"><span data-stu-id="0b213-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="0b213-117">Dieser Zeiger wird an die Funktion übergeben, die in *pfunction* bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0b213-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b213-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b213-118">Return value</span></span>

<span data-ttu-id="0b213-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b213-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b213-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b213-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b213-121">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="0b213-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b213-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b213-122">Remarks</span></span>

<span data-ttu-id="0b213-123">Im folgenden Beispiel wird eine Funktion namens colorcubefill erstellt, die auf D3DXFillCubeTexture basiert.</span><span class="sxs-lookup"><span data-stu-id="0b213-123">Here is an example that creates a function called ColorCubeFill, which relies on D3DXFillCubeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0b213-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b213-124">Requirements</span></span>



| <span data-ttu-id="0b213-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b213-125">Requirement</span></span> | <span data-ttu-id="0b213-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0b213-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b213-127">Header</span><span class="sxs-lookup"><span data-stu-id="0b213-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0b213-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b213-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0b213-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b213-129">Library</span></span><br/> | <dl> <span data-ttu-id="0b213-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b213-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0b213-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b213-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b213-132">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0b213-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
