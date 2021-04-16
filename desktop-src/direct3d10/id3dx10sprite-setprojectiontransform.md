---
description: Legen Sie die Projektions Matrix für alle Sprites fest.
ms.assetid: cb4c5546-1a31-40d9-a943-af4fbddcee01
title: 'ID3DX10Sprite:: setprojectiontransform-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c49fb570f87c8c86313e1f4adcf1560fee909433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531088"
---
# <a name="id3dx10spritesetprojectiontransform-method"></a><span data-ttu-id="09d9c-103">ID3DX10Sprite:: setprojectiontransform-Methode</span><span class="sxs-lookup"><span data-stu-id="09d9c-103">ID3DX10Sprite::SetProjectionTransform method</span></span>

<span data-ttu-id="09d9c-104">Legen Sie die Projektions Matrix für alle Sprites fest.</span><span class="sxs-lookup"><span data-stu-id="09d9c-104">Set the projection matrix for all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d9c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09d9c-105">Syntax</span></span>


```C++
HRESULT SetProjectionTransform(
  [in] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="09d9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09d9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d9c-107">*pprojectiontransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09d9c-107">*pProjectionTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d9c-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="09d9c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="09d9c-109">Die Projektions Matrix, die für alle Sprites verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09d9c-109">The projection matrix to be used on all sprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d9c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09d9c-110">Return value</span></span>

<span data-ttu-id="09d9c-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09d9c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09d9c-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="09d9c-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09d9c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09d9c-113">Requirements</span></span>



| <span data-ttu-id="09d9c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09d9c-114">Requirement</span></span> | <span data-ttu-id="09d9c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="09d9c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09d9c-116">Header</span><span class="sxs-lookup"><span data-stu-id="09d9c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="09d9c-117"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="09d9c-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="09d9c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09d9c-118">Library</span></span><br/> | <dl> <span data-ttu-id="09d9c-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09d9c-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d9c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09d9c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d9c-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="09d9c-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="09d9c-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="09d9c-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
