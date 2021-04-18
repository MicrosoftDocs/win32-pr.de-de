---
description: Fügt der Liste der im Batch verarbeiteten Sprites ein Sprite hinzu.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite::D RAW-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364391"
---
# <a name="id3dxspritedraw-method"></a><span data-ttu-id="c7851-103">ID3DXSprite::D RAW-Methode</span><span class="sxs-lookup"><span data-stu-id="c7851-103">ID3DXSprite::Draw method</span></span>

<span data-ttu-id="c7851-104">Fügt der Liste der im Batch verarbeiteten Sprites ein Sprite hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7851-104">Adds a sprite to the list of batched sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7851-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7851-105">Syntax</span></span>


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a><span data-ttu-id="c7851-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7851-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7851-107">*ptexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7851-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7851-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c7851-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c7851-109">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die Sprite-Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7851-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the sprite texture.</span></span>

</dd> <dt>

<span data-ttu-id="c7851-110">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7851-110">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7851-111">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="c7851-111">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="c7851-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die den Teil der Quell Textur angibt, der für das Sprite verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7851-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that indicates the portion of the source texture to use for the sprite.</span></span> <span data-ttu-id="c7851-113">Wenn dieser Parameter **null** ist, wird das gesamte Quell Image für das Sprite verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7851-113">If this parameter is **NULL**, then the entire source image is used for the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="c7851-114">*pcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7851-114">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7851-115">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7851-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c7851-116">Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Mitte des Sprite identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c7851-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite.</span></span> <span data-ttu-id="c7851-117">Wenn dieses Argument **null** ist, wird der Punkt (0, 0, 0) verwendet. Dies ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="c7851-117">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="c7851-118">*pposition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7851-118">*pPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7851-119">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7851-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c7851-120">Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Position des Sprite angibt.</span><span class="sxs-lookup"><span data-stu-id="c7851-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite.</span></span> <span data-ttu-id="c7851-121">Wenn dieses Argument **null** ist, wird der Punkt (0, 0, 0) verwendet. Dies ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="c7851-121">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="c7851-122">*Farbe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7851-122">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7851-123">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="c7851-123">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="c7851-124">[**D3DCOLOR**](d3dcolor.md) -Typ.</span><span class="sxs-lookup"><span data-stu-id="c7851-124">[**D3DCOLOR**](d3dcolor.md) type.</span></span> <span data-ttu-id="c7851-125">Die Farb-und Alphakanäle werden von diesem Wert moduliert.</span><span class="sxs-lookup"><span data-stu-id="c7851-125">The color and alpha channels are modulated by this value.</span></span> <span data-ttu-id="c7851-126">Der Wert 0xFFFFFFFF behält die ursprüngliche Quellfarbe und Alpha Daten bei.</span><span class="sxs-lookup"><span data-stu-id="c7851-126">A value of 0xFFFFFFFF maintains the original source color and alpha data.</span></span> <span data-ttu-id="c7851-127">Verwenden Sie das [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) -Makro, um diese Farbe zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c7851-127">Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7851-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7851-128">Return value</span></span>

<span data-ttu-id="c7851-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7851-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7851-130">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7851-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c7851-131">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="c7851-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7851-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7851-132">Remarks</span></span>

<span data-ttu-id="c7851-133">Um Sprite zu skalieren, zu drehen oder zu übersetzen, rufen Sie [**ID3DXSprite:: setTransform**](id3dxsprite--settransform.md) mit einer Matrix auf, die die Werte für Skala, Drehung und Übersetzung (SRT) enthält, bevor Sie ID3DXSprite::D RAW aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c7851-133">To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw.</span></span> <span data-ttu-id="c7851-134">Weitere Informationen zum Festlegen von SRT-Werten in einer Matrix finden Sie unter [Matrix Transformationen](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="c7851-134">For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7851-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7851-135">Requirements</span></span>



| <span data-ttu-id="c7851-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7851-136">Requirement</span></span> | <span data-ttu-id="c7851-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c7851-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7851-138">Header</span><span class="sxs-lookup"><span data-stu-id="c7851-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c7851-139"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7851-139"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c7851-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7851-140">Library</span></span><br/> | <dl> <span data-ttu-id="c7851-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7851-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7851-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7851-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7851-143">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="c7851-143">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="c7851-144">**ID3DXSprite:: GetTransform**</span><span class="sxs-lookup"><span data-stu-id="c7851-144">**ID3DXSprite::GetTransform**</span></span>](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
