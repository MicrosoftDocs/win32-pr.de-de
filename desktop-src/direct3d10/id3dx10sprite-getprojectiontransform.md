---
description: Holen Sie sich die Sprite-Projektions Matrix, die auf alle Sprites angewendet wird.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'ID3DX10Sprite:: getprojectiontransform-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762381"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a><span data-ttu-id="1d151-103">ID3DX10Sprite:: getprojectiontransform-Methode</span><span class="sxs-lookup"><span data-stu-id="1d151-103">ID3DX10Sprite::GetProjectionTransform method</span></span>

<span data-ttu-id="1d151-104">Holen Sie sich die Sprite-Projektions Matrix, die auf alle Sprites angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d151-104">Get the sprite projection matrix that is applied to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d151-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d151-105">Syntax</span></span>


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="1d151-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d151-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d151-107">*pprojectiontransform* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d151-107">*pProjectionTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d151-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d151-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1d151-109">Zeiger auf ein [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) -Wert, der auf die Projektions Matrix des Sprite festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1d151-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the sprite's projection matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d151-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d151-110">Return value</span></span>

<span data-ttu-id="1d151-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d151-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d151-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="1d151-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d151-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d151-113">Requirements</span></span>



| <span data-ttu-id="1d151-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d151-114">Requirement</span></span> | <span data-ttu-id="1d151-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1d151-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d151-116">Header</span><span class="sxs-lookup"><span data-stu-id="1d151-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1d151-117"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d151-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d151-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d151-118">Library</span></span><br/> | <dl> <span data-ttu-id="1d151-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d151-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d151-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d151-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d151-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="1d151-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="1d151-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1d151-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
