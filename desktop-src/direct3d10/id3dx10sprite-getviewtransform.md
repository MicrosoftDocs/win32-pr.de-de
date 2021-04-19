---
description: Hiermit wird die Ansichts Transformation für alle Sprites angezeigt.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'ID3DX10Sprite:: GetViewTransform-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355849"
---
# <a name="id3dx10spritegetviewtransform-method"></a><span data-ttu-id="f756b-103">ID3DX10Sprite:: GetViewTransform-Methode</span><span class="sxs-lookup"><span data-stu-id="f756b-103">ID3DX10Sprite::GetViewTransform method</span></span>

<span data-ttu-id="f756b-104">Hiermit wird die Ansichts Transformation für alle Sprites angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f756b-104">Get the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="f756b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f756b-105">Syntax</span></span>


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="f756b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f756b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f756b-107">*pviewtransform* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f756b-107">*pViewTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f756b-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f756b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f756b-109">Zeiger auf eine [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) , die auf die Transformation des Sprite aus dem ursprünglichen Raum festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f756b-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f756b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f756b-110">Return value</span></span>

<span data-ttu-id="f756b-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f756b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f756b-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f756b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f756b-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="f756b-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f756b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f756b-114">Requirements</span></span>



| <span data-ttu-id="f756b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f756b-115">Requirement</span></span> | <span data-ttu-id="f756b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f756b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f756b-117">Header</span><span class="sxs-lookup"><span data-stu-id="f756b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f756b-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f756b-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f756b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f756b-119">Library</span></span><br/> | <dl> <span data-ttu-id="f756b-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f756b-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f756b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f756b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f756b-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="f756b-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="f756b-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f756b-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
