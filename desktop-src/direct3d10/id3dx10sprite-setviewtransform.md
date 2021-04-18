---
description: Legen Sie die Ansichts Transformation fest, die für alle Sprites gilt.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'ID3DX10Sprite:: SetViewTransform-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365356"
---
# <a name="id3dx10spritesetviewtransform-method"></a><span data-ttu-id="dc03c-103">ID3DX10Sprite:: SetViewTransform-Methode</span><span class="sxs-lookup"><span data-stu-id="dc03c-103">ID3DX10Sprite::SetViewTransform method</span></span>

<span data-ttu-id="dc03c-104">Legen Sie die Ansichts Transformation fest, die für alle Sprites gilt.</span><span class="sxs-lookup"><span data-stu-id="dc03c-104">Set the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc03c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc03c-105">Syntax</span></span>


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="dc03c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc03c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc03c-107">*pviewtransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc03c-107">*pViewTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc03c-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc03c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dc03c-109">Zeiger auf eine D3DXMATRIX, die eine Transformation des Sprite aus dem ursprünglichen Raum enthält.</span><span class="sxs-lookup"><span data-stu-id="dc03c-109">Pointer to a D3DXMATRIX that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="dc03c-110">Verwenden Sie diese Transformation, um Sprite zu skalieren, zu drehen oder zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="dc03c-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc03c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc03c-111">Return value</span></span>

<span data-ttu-id="dc03c-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc03c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc03c-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dc03c-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dc03c-114">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="dc03c-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc03c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc03c-115">Requirements</span></span>



| <span data-ttu-id="dc03c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc03c-116">Requirement</span></span> | <span data-ttu-id="dc03c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dc03c-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc03c-118">Header</span><span class="sxs-lookup"><span data-stu-id="dc03c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dc03c-119"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc03c-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc03c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc03c-120">Library</span></span><br/> | <dl> <span data-ttu-id="dc03c-121"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc03c-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc03c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc03c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc03c-123">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="dc03c-123">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="dc03c-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dc03c-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
