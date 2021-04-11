---
description: Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes texsebene jeder MIP-Ebene einer bestimmten volumetextur auszufüllen.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: D3DXFillVolumeTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354857"
---
# <a name="d3dxfillvolumetexture-function"></a><span data-ttu-id="0e41d-103">D3DXFillVolumeTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e41d-103">D3DXFillVolumeTexture function</span></span>

<span data-ttu-id="0e41d-104">Verwendet eine vom Benutzer bereitgestellte Funktion, um jedes texsebene jeder MIP-Ebene einer bestimmten volumetextur auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="0e41d-104">Uses a user-provided function to fill each texel of each mip level of a given volume texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e41d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e41d-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a><span data-ttu-id="0e41d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e41d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e41d-107">*ptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0e41d-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e41d-108">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="0e41d-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="0e41d-109">Zeiger auf eine [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Schnittstelle, die die gefüllte Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e41d-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="0e41d-110">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e41d-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e41d-111">Typ: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="0e41d-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="0e41d-112">Ein Zeiger auf eine vom Benutzer bereitgestellte Auswertungsfunktion, die verwendet wird, um den Wert der einzelnen Texttypen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0e41d-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="0e41d-113">Die-Funktion folgt dem Prototyp von [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="0e41d-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e41d-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e41d-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e41d-115">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e41d-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e41d-116">Zeiger auf einen beliebigen Block von benutzerdefinierten Daten.</span><span class="sxs-lookup"><span data-stu-id="0e41d-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="0e41d-117">Dieser Zeiger wird an die Funktion übergeben, die in *pfunction* bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0e41d-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e41d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e41d-118">Return value</span></span>

<span data-ttu-id="0e41d-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e41d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e41d-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e41d-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0e41d-121">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="0e41d-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e41d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e41d-122">Remarks</span></span>

<span data-ttu-id="0e41d-123">Wenn das Volume nicht dynamisch ist (weil die Verwendung bei der Erstellung auf 0 festgelegt ist) und sich im Videospeicher befindet (der auf D3DPOOL default festgelegte Speicherpool \_ ), schlägt **D3DXFillVolumeTexture** fehl, da das Volume nicht gesperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e41d-123">If the volume is non-dynamic (because usage is set to 0 when it is created), and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXFillVolumeTexture** will fail because the volume cannot be locked.</span></span>

<span data-ttu-id="0e41d-124">In diesem Beispiel wird eine Funktion namens colorvolumefill erstellt, die auf D3DXFillVolumeTexture basiert.</span><span class="sxs-lookup"><span data-stu-id="0e41d-124">This example creates a function called ColorVolumeFill, which relies on D3DXFillVolumeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0e41d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e41d-125">Requirements</span></span>



| <span data-ttu-id="0e41d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e41d-126">Requirement</span></span> | <span data-ttu-id="0e41d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0e41d-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e41d-128">Header</span><span class="sxs-lookup"><span data-stu-id="0e41d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0e41d-129"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e41d-129"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0e41d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e41d-130">Library</span></span><br/> | <dl> <span data-ttu-id="0e41d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e41d-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0e41d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e41d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e41d-133">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0e41d-133">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
